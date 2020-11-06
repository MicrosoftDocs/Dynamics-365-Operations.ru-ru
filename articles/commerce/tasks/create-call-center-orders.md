---
title: Создание заказов центра обработки вызовов
description: Эта процедура демонстрирует поиск клиента, создание нового заказа, поиск продукта и получение платежа от клиента.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dce2fdd9d91c2bd867f0455573733aefb0796fa7
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107360"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="e82f3-103">Создание заказов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="e82f3-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e82f3-104">Эта процедура демонстрирует поиск клиента, создание нового заказа, поиск продукта и получение платежа от клиента.</span><span class="sxs-lookup"><span data-stu-id="e82f3-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="e82f3-105">Эта процедура использует демонстрационные данные компании USRT и предназначена для сотрудника, занимающегося заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="e82f3-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="e82f3-106">Предварительные условия: пользователь, выполняющий эту процедуру, настроен как пользователь центра обработки вызовов, и полугодовой каталог Fabrikam опубликован и содержит по крайней мере один исходный код.</span><span class="sxs-lookup"><span data-stu-id="e82f3-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="e82f3-107">Перейдите в раздел **Retail и Commerce \> Клиенты \> Обслуживание клиентов**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="e82f3-108">Для **SearchText** введите условия поиска для поиска клиента.</span><span class="sxs-lookup"><span data-stu-id="e82f3-108">For **SearchText** , enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="e82f3-109">Для этой демонстрационной процедуры введите "Karen" и выберите **TAB**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="e82f3-110">Выберите Поиск.</span><span class="sxs-lookup"><span data-stu-id="e82f3-110">Select Search.</span></span>
    * <span data-ttu-id="e82f3-111">Поскольку в демонстрационных данных есть только один клиент с именем Karen, результат будет выбран автоматически.</span><span class="sxs-lookup"><span data-stu-id="e82f3-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="e82f3-112">Выберите **Создать заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="e82f3-113">Разверните или сверните раздел заголовка **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="e82f3-114">Выберите код источника для каталога</span><span class="sxs-lookup"><span data-stu-id="e82f3-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="e82f3-115">Если нет активных кодов источника, можно пропустить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="e82f3-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="e82f3-116">Выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-116">Select **Add line**.</span></span>
8. <span data-ttu-id="e82f3-117">Для **Код номенклатуры** введите поисковый запрос для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="e82f3-117">For **Item number** , enter the item search term.</span></span>
    * <span data-ttu-id="e82f3-118">Для этой демонстрационной процедуры введите частичный код номенклатуры "8111" и нажмите TAB. Это действие открывает окно поиска номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="e82f3-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="e82f3-119">Выберите продукта для добавления в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="e82f3-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="e82f3-120">Введите количество продаваемого продукта.</span><span class="sxs-lookup"><span data-stu-id="e82f3-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="e82f3-121">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-121">Select **Create**.</span></span>
12. <span data-ttu-id="e82f3-122">Выберите **Завершить** , чтобы зафиксировать платеж клиента.</span><span class="sxs-lookup"><span data-stu-id="e82f3-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="e82f3-123">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-123">Select **Add**.</span></span>
    * <span data-ttu-id="e82f3-124">Команда "Добавить ссылку" находится на вкладке "Платежи". Разверните вкладку "Платежи", если она свернута.</span><span class="sxs-lookup"><span data-stu-id="e82f3-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="e82f3-125">Выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="e82f3-125">Select the payment method.</span></span>
    * <span data-ttu-id="e82f3-126">Для этой процедуры выберите способ оплаты наличными.</span><span class="sxs-lookup"><span data-stu-id="e82f3-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="e82f3-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e82f3-127">Close the page.</span></span>
16. <span data-ttu-id="e82f3-128">Введите сумму.</span><span class="sxs-lookup"><span data-stu-id="e82f3-128">Enter the amount.</span></span>
    * <span data-ttu-id="e82f3-129">Для этой процедуры введите сумму, равную сальдо заказа, которую можно видеть на странице сводке заказ на продажу слева от поля суммы.</span><span class="sxs-lookup"><span data-stu-id="e82f3-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="e82f3-130">Это действие позволит вам завершить заказ как полностью оплаченный.</span><span class="sxs-lookup"><span data-stu-id="e82f3-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="e82f3-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-131">Select **OK**.</span></span>
18. <span data-ttu-id="e82f3-132">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="e82f3-132">Select **Submit**.</span></span>

