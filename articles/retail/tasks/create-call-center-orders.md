--- 
title: "Создание заказов центра обработки вызовов"
description: "Эта процедура демонстрирует поиск клиента, создание нового заказа, поиск продукта и получение платежа от клиента."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="3b17d-103">Создание заказов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="3b17d-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3b17d-104">Эта процедура демонстрирует поиск клиента, создание нового заказа, поиск продукта и получение платежа от клиента.</span><span class="sxs-lookup"><span data-stu-id="3b17d-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="3b17d-105">Эта процедура использует демонстрационные данные компании USRT и предназначена для сотрудника, занимающегося заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="3b17d-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="3b17d-106">Предварительные условия: пользователь, выполняющий эту процедуру, настроен как пользователь центра обработки вызовов, и полугодовой каталог Fabrikam опубликован и содержит по крайней мере один исходный код.</span><span class="sxs-lookup"><span data-stu-id="3b17d-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="3b17d-107">Перейдите в раздел "Розничная торговля и коммерция" > "Клиенты" > "Обслуживание клиентов".</span><span class="sxs-lookup"><span data-stu-id="3b17d-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="3b17d-108">В поле SearchText введите условия поиска для поиска клиента.</span><span class="sxs-lookup"><span data-stu-id="3b17d-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="3b17d-109">Для этой демонстрационной процедуры введите "karen" и нажмите TAB.</span><span class="sxs-lookup"><span data-stu-id="3b17d-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="3b17d-110">Щелкните "Поиск".</span><span class="sxs-lookup"><span data-stu-id="3b17d-110">Click Search.</span></span>
    * <span data-ttu-id="3b17d-111">Поскольку в демонстрационных данных есть только один клиент с именем Karen, он будет выбран автоматически.</span><span class="sxs-lookup"><span data-stu-id="3b17d-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="3b17d-112">Щелкните "Новый заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="3b17d-112">Click New sales order.</span></span>
5. <span data-ttu-id="3b17d-113">Разверните или сверните раздел "Заголовок заказа на продажу".</span><span class="sxs-lookup"><span data-stu-id="3b17d-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="3b17d-114">Выберите код источника для каталога</span><span class="sxs-lookup"><span data-stu-id="3b17d-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="3b17d-115">Если нет активных кодов источника, можно закрыть поле "Источник" и пропустить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="3b17d-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="3b17d-116">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="3b17d-116">Click Add line.</span></span>
8. <span data-ttu-id="3b17d-117">В поле "Код номенклатуры" введите поисковый запрос для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3b17d-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="3b17d-118">Для этой демонстрационной процедуры введите частичный код номенклатуры "8111" и нажмите TAB. Появится окно поиска номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3b17d-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="3b17d-119">Выберите продукта для добавления в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3b17d-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="3b17d-120">Введите количество продаваемого продукта.</span><span class="sxs-lookup"><span data-stu-id="3b17d-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="3b17d-121">Щелкните Создать.</span><span class="sxs-lookup"><span data-stu-id="3b17d-121">Click Create.</span></span>
12. <span data-ttu-id="3b17d-122">Щелкните "Завершить", чтобы зафиксировать платеж клиента.</span><span class="sxs-lookup"><span data-stu-id="3b17d-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="3b17d-123">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="3b17d-123">Click Add.</span></span>
    * <span data-ttu-id="3b17d-124">Команда "Добавить ссылку" находится на вкладке "Платежи". Разверните вкладку "Платежи", если она свернута.</span><span class="sxs-lookup"><span data-stu-id="3b17d-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="3b17d-125">Выберите способ оплаты.</span><span class="sxs-lookup"><span data-stu-id="3b17d-125">Select the payment method.</span></span>
    * <span data-ttu-id="3b17d-126">Для этой процедуры выберите способ оплаты наличными.</span><span class="sxs-lookup"><span data-stu-id="3b17d-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="3b17d-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b17d-127">Close the page.</span></span>
16. <span data-ttu-id="3b17d-128">Введите сумму.</span><span class="sxs-lookup"><span data-stu-id="3b17d-128">Enter the amount.</span></span>
    * <span data-ttu-id="3b17d-129">Для этой процедуры введите сумму, равную сальдо заказа, которую можно видеть на странице сводке заказ на продажу слева от поля суммы.</span><span class="sxs-lookup"><span data-stu-id="3b17d-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="3b17d-130">Это позволит вам завершить заказ как полностью оплаченный.</span><span class="sxs-lookup"><span data-stu-id="3b17d-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="3b17d-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3b17d-131">Click OK.</span></span>
18. <span data-ttu-id="3b17d-132">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="3b17d-132">Click Submit.</span></span>

