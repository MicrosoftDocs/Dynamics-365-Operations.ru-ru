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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845904"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="341f5-103">Настройка стандартной стоимости труда и расходов</span><span class="sxs-lookup"><span data-stu-id="341f5-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="341f5-104">В этой процедуре показано, как настроить стандартные затраты на труд и расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="341f5-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="341f5-105">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="341f5-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="341f5-106">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Себестоимость (час)".</span><span class="sxs-lookup"><span data-stu-id="341f5-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="341f5-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="341f5-107">Click New.</span></span>
3. <span data-ttu-id="341f5-108">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="341f5-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="341f5-109">В поле "Себестоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="341f5-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="341f5-110">Можно настроить стандартную себестоимость категории проекта или настроить себестоимость по коду работника, номеру проекта, категории, дате или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="341f5-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="341f5-111">Применяемая себестоимость будет себестоимостью при самом высоком уровне детализации.</span><span class="sxs-lookup"><span data-stu-id="341f5-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="341f5-112">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="341f5-112">Click Save.</span></span>
6. <span data-ttu-id="341f5-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="341f5-113">Close the page.</span></span>
7. <span data-ttu-id="341f5-114">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Цена продажи (время)".</span><span class="sxs-lookup"><span data-stu-id="341f5-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="341f5-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="341f5-115">Click New.</span></span>
9. <span data-ttu-id="341f5-116">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="341f5-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="341f5-117">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="341f5-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="341f5-118">В поле "Ценообразование" введите число.</span><span class="sxs-lookup"><span data-stu-id="341f5-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="341f5-119">Можно настроить стандартную цену продажи для почасовых проводок или категории проектов.</span><span class="sxs-lookup"><span data-stu-id="341f5-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="341f5-120">Можно также настроить цены продажи по коду работника, номеру проекта, категории, дате проводки или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="341f5-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="341f5-121">Фактическая цена продажи, которая применяется, когда работник вводит проводку в журнале регистрации времени, является ценой продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="341f5-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="341f5-122">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="341f5-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="341f5-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="341f5-123">Click Save.</span></span>
13. <span data-ttu-id="341f5-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="341f5-124">Close the page.</span></span>
14. <span data-ttu-id="341f5-125">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Себестоимость (расход)".</span><span class="sxs-lookup"><span data-stu-id="341f5-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="341f5-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="341f5-126">Click New.</span></span>
16. <span data-ttu-id="341f5-127">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="341f5-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="341f5-128">В поле "Себестоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="341f5-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="341f5-129">Можно заполнить несколько полей, но это минимум, необходимый для сохранения записи.</span><span class="sxs-lookup"><span data-stu-id="341f5-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="341f5-130">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="341f5-130">Click Save.</span></span>
19. <span data-ttu-id="341f5-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="341f5-131">Close the page.</span></span>
20. <span data-ttu-id="341f5-132">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Цена продажи (расход)".</span><span class="sxs-lookup"><span data-stu-id="341f5-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="341f5-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="341f5-133">Click New.</span></span>
22. <span data-ttu-id="341f5-134">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="341f5-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="341f5-135">В поле "Допустимо для" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="341f5-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="341f5-136">В поле "Ценообразование" введите число.</span><span class="sxs-lookup"><span data-stu-id="341f5-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="341f5-137">Фактической ценой продажи, которая используется, когда работник заносит проводки в журнал затрат, является цена продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="341f5-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="341f5-138">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="341f5-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="341f5-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="341f5-139">Click Save.</span></span>

