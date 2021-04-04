---
title: Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов
description: В этой теме объясняется, как выполнить фильтрацию внутрихолдинговых заказов, чтобы не синхронизировались сущности заказов и строк заказов.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 9a736c8e93dfa7dbcd0739b52e2da987dcefdc0e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568110"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="0b698-103">Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов</span><span class="sxs-lookup"><span data-stu-id="0b698-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b698-104">Вы можете фильтровать внутрихолдинговые заказы, чтобы таблицы **Заказы** и **OrderLines** не синхронизировались.</span><span class="sxs-lookup"><span data-stu-id="0b698-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="0b698-105">В некоторых сценариях сведения о внутрихолдинговых заказах не требуются в приложении взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="0b698-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="0b698-106">Каждая из стандартных таблиц Dataverse расширяется через ссылки на столбец **IntercompanyOrder**, а карты двойной записи изменяются, чтобы они ссылались на дополнительные столбцы в фильтрах.</span><span class="sxs-lookup"><span data-stu-id="0b698-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="0b698-107">Таким образом, внутрихолдинговые заказы больше не синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="0b698-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="0b698-108">Этот процесс помогает избежать ненужных данных в приложении взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="0b698-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="0b698-109">Расширьте таблицу **Заголовки заказов на продажу CDS**, добавив ссылку на столбец **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="0b698-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="0b698-110">Этот столбец заполняется только во внутрихолдинговых заказах.</span><span class="sxs-lookup"><span data-stu-id="0b698-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="0b698-111">Столбец **IntercompanyOrder** доступен в таблице **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="0b698-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Страница сопоставления исходных данных с целевыми для заголовков заказов на продажу CDS":::

2. <span data-ttu-id="0b698-113">После развертывания пункта **Заголовки заказов на продажу CDS** столбец **IntercompanyOrder** доступен в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="0b698-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="0b698-114">Примените фильтр, имеющий `INTERCOMPANYORDER == ""` в качестве строки запроса.</span><span class="sxs-lookup"><span data-stu-id="0b698-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Диалоговое окно изменения запроса для заголовков заказов на продажу CDS":::

3. <span data-ttu-id="0b698-116">Расширьте таблицу **Строки заказов на продажу CDS**, добавив ссылку на столбец **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="0b698-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="0b698-117">Этот столбец заполняется только во внутрихолдинговых заказах.</span><span class="sxs-lookup"><span data-stu-id="0b698-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="0b698-118">Столбец **InterCompanyInventTransId** доступен в таблице **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="0b698-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Страница сопоставления исходных данных с целевыми для строк заказов на продажу CDS":::

4. <span data-ttu-id="0b698-120">После развертывания пункта **Строки заказов на продажу CDS** столбец **IntercompanyInventTransId** доступен в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="0b698-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="0b698-121">Примените фильтр, имеющий `INTERCOMPANYINVENTTRANSID == ""` в качестве строки запроса.</span><span class="sxs-lookup"><span data-stu-id="0b698-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Диалоговое окно изменения запроса для строк заказов на продажу CDS":::

5. <span data-ttu-id="0b698-123">Повторите шаги 1 и 2, чтобы расширить таблицу **Заголовок счета на продажу V2** и добавить запрос фильтра.</span><span class="sxs-lookup"><span data-stu-id="0b698-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="0b698-124">В этом случае используйте `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` в качестве строки запроса для фильтра.</span><span class="sxs-lookup"><span data-stu-id="0b698-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Страница сопоставления исходных данных с целевыми для заголовка счета на продажу V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Диалоговое окно изменения запроса для заголовка счета на продажу V2":::

6. <span data-ttu-id="0b698-127">Повторите шаги 3 и 4, чтобы расширить таблицу **Строки счета на продажу V2** и добавить запрос фильтра.</span><span class="sxs-lookup"><span data-stu-id="0b698-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="0b698-128">В этом случае используйте `INTERCOMPANYINVENTTRANSID == ""` в качестве строки запроса для фильтра.</span><span class="sxs-lookup"><span data-stu-id="0b698-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Диалоговое окно изменения запроса для строк счета на продажу V2":::

7. <span data-ttu-id="0b698-130">Таблица **Предложения с расценками** не имеет внутрихолдинговой связи.</span><span class="sxs-lookup"><span data-stu-id="0b698-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="0b698-131">Если кто-то создает предложение с расценками для одного из внутрихолдинговых клиентов, можно использовать столбец **CustGroup**, чтобы поместить всех этих клиентов в одну группу клиентов.</span><span class="sxs-lookup"><span data-stu-id="0b698-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="0b698-132">Можно расширить заголовок и строки, добавив столбец **CustGroup**, а затем отфильтровать, чтобы группа не включалась.</span><span class="sxs-lookup"><span data-stu-id="0b698-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Страница сопоставления исходных данных с целевыми для заголовка предложения с расценками на продажу CDS":::

8. <span data-ttu-id="0b698-134">После того как сущность **Предложения с расценками** расширена, примените фильтр, имеющий `CUSTGROUP != "<company>"` в качестве строки запроса.</span><span class="sxs-lookup"><span data-stu-id="0b698-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Диалоговое окно изменения запроса для заголовка предложения с расценками на продажу CDS":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]