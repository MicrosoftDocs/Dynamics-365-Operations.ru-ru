---
title: Настройка стандартной стоимости труда и расходов
description: В этой процедуре показано, как настроить стандартные затраты на труд и расходы по проекту.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "339403"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="1e302-103">Настройка стандартной стоимости труда и расходов</span><span class="sxs-lookup"><span data-stu-id="1e302-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e302-104">В этой процедуре показано, как настроить стандартные затраты на труд и расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="1e302-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="1e302-105">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="1e302-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1e302-106">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Себестоимость (час)".</span><span class="sxs-lookup"><span data-stu-id="1e302-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="1e302-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1e302-107">Click New.</span></span>
3. <span data-ttu-id="1e302-108">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1e302-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="1e302-109">В поле "Себестоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="1e302-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="1e302-110">Можно настроить стандартную себестоимость категории проекта или настроить себестоимость по коду работника, номеру проекта, категории, дате или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="1e302-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="1e302-111">Применяемая себестоимость будет себестоимостью при самом высоком уровне детализации.</span><span class="sxs-lookup"><span data-stu-id="1e302-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="1e302-112">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1e302-112">Click Save.</span></span>
6. <span data-ttu-id="1e302-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e302-113">Close the page.</span></span>
7. <span data-ttu-id="1e302-114">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Цена продажи (время)".</span><span class="sxs-lookup"><span data-stu-id="1e302-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="1e302-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1e302-115">Click New.</span></span>
9. <span data-ttu-id="1e302-116">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1e302-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="1e302-117">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1e302-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="1e302-118">В поле "Ценообразование" введите число.</span><span class="sxs-lookup"><span data-stu-id="1e302-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="1e302-119">Можно настроить стандартную цену продажи для почасовых проводок или категории проектов.</span><span class="sxs-lookup"><span data-stu-id="1e302-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="1e302-120">Можно также настроить цены продажи по коду работника, номеру проекта, категории, дате проводки или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="1e302-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="1e302-121">Фактическая цена продажи, которая применяется, когда работник вводит проводку в журнале регистрации времени, является ценой продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="1e302-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="1e302-122">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="1e302-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="1e302-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1e302-123">Click Save.</span></span>
13. <span data-ttu-id="1e302-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e302-124">Close the page.</span></span>
14. <span data-ttu-id="1e302-125">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Себестоимость (расход)".</span><span class="sxs-lookup"><span data-stu-id="1e302-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="1e302-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1e302-126">Click New.</span></span>
16. <span data-ttu-id="1e302-127">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1e302-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="1e302-128">В поле "Себестоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="1e302-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="1e302-129">Можно заполнить несколько полей, но это минимум, необходимый для сохранения записи.</span><span class="sxs-lookup"><span data-stu-id="1e302-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="1e302-130">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1e302-130">Click Save.</span></span>
19. <span data-ttu-id="1e302-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e302-131">Close the page.</span></span>
20. <span data-ttu-id="1e302-132">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Цена продажи (расход)".</span><span class="sxs-lookup"><span data-stu-id="1e302-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="1e302-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1e302-133">Click New.</span></span>
22. <span data-ttu-id="1e302-134">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1e302-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="1e302-135">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1e302-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="1e302-136">В поле "Ценообразование" введите число.</span><span class="sxs-lookup"><span data-stu-id="1e302-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="1e302-137">Фактической ценой продажи, которая используется, когда работник заносит проводки в журнал затрат, является цена продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="1e302-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="1e302-138">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="1e302-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="1e302-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1e302-139">Click Save.</span></span>

