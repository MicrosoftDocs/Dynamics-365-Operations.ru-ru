---
title: Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов
description: В этой теме описывается порядок фильтрации внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701041"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="8fb9e-103">Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов</span><span class="sxs-lookup"><span data-stu-id="8fb9e-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fb9e-104">Вы можете фильтровать внутрихолдинговые заказы, чтобы исключить синхронизацию сущностей **Заказы** и **OrderLines**.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="8fb9e-105">В некоторых сценариях сведения о внутрихолдинговых заказах не являются обязательными в приложении взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="8fb9e-106">Каждая из стандартных сущностей Common Data Service расширяется со ссылками на поле **IntercompanyOrder**, а карты двойной записи изменяются для ссылки на дополнительные поля в фильтрах.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="8fb9e-107">В результате внутрихолдинговые заказы больше не синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="8fb9e-108">Этот процесс позволяет избежать ненужных данных в приложении взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="8fb9e-109">Добавьте ссылку на **IntercompanyOrder** в **Заголовки заказов на продажу CDS**.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="8fb9e-110">Оно заполняется только для внутрихолдинговых заказов.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="8fb9e-111">Поле **IntercompanyOrder** доступно в **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Сопоставить промежуточные данные с целевыми, SalesOrderHeader":::
    
2. <span data-ttu-id="8fb9e-113">После развертывания пункта **Заголовки заказов на продажу CDS** поле **IntercompanyOrder** доступно в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="8fb9e-114">Примените фильтр с `INTERCOMPANYORDER == ""` в качестве строки запроса.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Заголовки заказов на продажу, изменение запроса":::

3. <span data-ttu-id="8fb9e-116">Добавьте ссылку на **IntercompanyInventTransId** в **Строки заказа на продажу CDS**.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="8fb9e-117">Оно заполняется только для внутрихолдинговых заказов.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="8fb9e-118">Поле **InterCompanyInventTransID** доступно в **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Сопоставить промежуточные данные с целевыми, SalesOrderLine":::

4. <span data-ttu-id="8fb9e-120">После развертывания пункта **Строки заказов на продажу CDS** поле **IntercompanyInventTransId** доступно в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="8fb9e-121">Примените фильтр с `INTERCOMPANYINVENTTRANSID == ""` в качестве строки запроса.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Строки заказа на продажу, изменить запрос":::

5. <span data-ttu-id="8fb9e-123">Разверните **Заголовок накладной по продаже V2** и **Строки накладной по продаже V2** таким же образом, как разворачивали сущности Common Data Service на шагах 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="8fb9e-124">Затем добавьте запросы фильтра.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-124">Then add the filter queries.</span></span> <span data-ttu-id="8fb9e-125">Строка фильтра для сущности **Заголовок накладной по продаже V2** равна `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="8fb9e-126">Строка фильтра для сущности **Строки накладной по продаже V2** равна `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Сопоставить промежуточные данные с целевыми, Заголовки накладной по продаже":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Заголовки накладной по продаже, изменение запроса":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Строки накладной по продаже, изменение запроса":::

6. <span data-ttu-id="8fb9e-130">Сущность **Предложения с расценками** не имеет внутрихолдинговой связи.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="8fb9e-131">Если кто-то создает предложение с расценками для одного из внутрихолдинговых клиентов, можно поместить всех этих клиентов в одну группу клиентов, используя поле **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="8fb9e-132">Заголовок и строки можно развернуть, добавив поле **CustGroup**, а затем выполнить фильтрацию, чтобы не включать эту группу.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Сопоставить промежуточные данные с целевыми, Заголовок предложения с расценками по продаже":::

7. <span data-ttu-id="8fb9e-134">После того как сущность **Предложения с расценками** развернута, примените фильтр со строкой запроса `CUSTGROUP !=  "<company>"`.</span><span class="sxs-lookup"><span data-stu-id="8fb9e-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Заголовок предложения с расценками по продажам, правка запроса":::
