---
title: Настройка стандартной стоимости труда и расходов
description: В этой теме показано, как настроить стандартные затраты на труд и расходы по проекту.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867734"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="a01a8-103">Настройка стандартной стоимости труда и расходов</span><span class="sxs-lookup"><span data-stu-id="a01a8-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a01a8-104">В этой теме показано, как настроить стандартные затраты на труд и расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="a01a8-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="a01a8-105">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="a01a8-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a01a8-106">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Себестоимость (час)**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="a01a8-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-107">Select **New**.</span></span>
3. <span data-ttu-id="a01a8-108">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a01a8-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="a01a8-109">В поле **Себестоимость** введите число.</span><span class="sxs-lookup"><span data-stu-id="a01a8-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="a01a8-110">Можно настроить стандартную себестоимость категории проекта или настроить себестоимость по коду работника, номеру проекта, категории, дате или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="a01a8-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="a01a8-111">Применяемая себестоимость будет себестоимостью при самом высоком уровне детализации.</span><span class="sxs-lookup"><span data-stu-id="a01a8-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="a01a8-112">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-112">Select **Save**.</span></span>
6. <span data-ttu-id="a01a8-113">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Цена продажи (время)**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="a01a8-114">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-114">Select **New**.</span></span>
8. <span data-ttu-id="a01a8-115">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a01a8-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="a01a8-116">В поле **Допустимо для** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="a01a8-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="a01a8-117">В поле **Ценообразование** введите число.</span><span class="sxs-lookup"><span data-stu-id="a01a8-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="a01a8-118">Можно настроить стандартную цену продажи для почасовых проводок или категории проектов.</span><span class="sxs-lookup"><span data-stu-id="a01a8-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="a01a8-119">Можно также настроить цены продажи по коду работника, номеру проекта, категории, дате проводки или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="a01a8-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="a01a8-120">Фактическая цена продажи, которая применяется, когда работник вводит проводку в журнале регистрации времени, является ценой продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="a01a8-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="a01a8-121">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="a01a8-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="a01a8-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-122">Select **Save**.</span></span>
12. <span data-ttu-id="a01a8-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a01a8-123">Close the page.</span></span>
13. <span data-ttu-id="a01a8-124">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Себестоимость (расходы)**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="a01a8-125">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-125">Select **New**.</span></span>
15. <span data-ttu-id="a01a8-126">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a01a8-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="a01a8-127">В поле **Себестоимость** введите число.</span><span class="sxs-lookup"><span data-stu-id="a01a8-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="a01a8-128">Можно заполнить несколько полей, но это минимум, необходимый для сохранения записи.</span><span class="sxs-lookup"><span data-stu-id="a01a8-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="a01a8-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-129">Select **Save**.</span></span>
18. <span data-ttu-id="a01a8-130">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Цена продажи (расходы)**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="a01a8-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-131">Select **New**.</span></span>
20. <span data-ttu-id="a01a8-132">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a01a8-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="a01a8-133">В поле **Допустимо для** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="a01a8-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="a01a8-134">В поле **Ценообразование** введите число.</span><span class="sxs-lookup"><span data-stu-id="a01a8-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="a01a8-135">Фактической ценой продажи, которая используется, когда работник заносит проводки в журнал затрат, является цена продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="a01a8-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="a01a8-136">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="a01a8-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="a01a8-137">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a01a8-137">Select **Save**.</span></span>

