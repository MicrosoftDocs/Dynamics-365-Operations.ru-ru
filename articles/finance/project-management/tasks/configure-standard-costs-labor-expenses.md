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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185413"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="497a7-103">Настройка стандартной стоимости труда и расходов</span><span class="sxs-lookup"><span data-stu-id="497a7-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="497a7-104">В этой теме показано, как настроить стандартные затраты на труд и расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="497a7-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="497a7-105">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="497a7-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="497a7-106">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Себестоимость (час)**.</span><span class="sxs-lookup"><span data-stu-id="497a7-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="497a7-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="497a7-107">Select **New**.</span></span>
3. <span data-ttu-id="497a7-108">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="497a7-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="497a7-109">В поле **Себестоимость** введите число.</span><span class="sxs-lookup"><span data-stu-id="497a7-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="497a7-110">Можно настроить стандартную себестоимость категории проекта или настроить себестоимость по коду работника, номеру проекта, категории, дате или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="497a7-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="497a7-111">Применяемая себестоимость будет себестоимостью при самом высоком уровне детализации.</span><span class="sxs-lookup"><span data-stu-id="497a7-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="497a7-112">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="497a7-112">Select **Save**.</span></span>
6. <span data-ttu-id="497a7-113">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Цена продажи (время)**.</span><span class="sxs-lookup"><span data-stu-id="497a7-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="497a7-114">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="497a7-114">Select **New**.</span></span>
8. <span data-ttu-id="497a7-115">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="497a7-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="497a7-116">В поле **Допустимо для** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="497a7-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="497a7-117">В поле **Ценообразование** введите число.</span><span class="sxs-lookup"><span data-stu-id="497a7-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="497a7-118">Можно настроить стандартную цену продажи для почасовых проводок или категории проектов.</span><span class="sxs-lookup"><span data-stu-id="497a7-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="497a7-119">Можно также настроить цены продажи по коду работника, номеру проекта, категории, дате проводки или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="497a7-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="497a7-120">Фактическая цена продажи, которая применяется, когда работник вводит проводку в журнале регистрации времени, является ценой продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="497a7-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="497a7-121">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="497a7-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="497a7-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="497a7-122">Select **Save**.</span></span>
12. <span data-ttu-id="497a7-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="497a7-123">Close the page.</span></span>
13. <span data-ttu-id="497a7-124">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Себестоимость (расходы)**.</span><span class="sxs-lookup"><span data-stu-id="497a7-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="497a7-125">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="497a7-125">Select **New**.</span></span>
15. <span data-ttu-id="497a7-126">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="497a7-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="497a7-127">В поле **Себестоимость** введите число.</span><span class="sxs-lookup"><span data-stu-id="497a7-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="497a7-128">Можно заполнить несколько полей, но это минимум, необходимый для сохранения записи.</span><span class="sxs-lookup"><span data-stu-id="497a7-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="497a7-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="497a7-129">Select **Save**.</span></span>
18. <span data-ttu-id="497a7-130">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Цена продажи (расходы)**.</span><span class="sxs-lookup"><span data-stu-id="497a7-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="497a7-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="497a7-131">Select **New**.</span></span>
20. <span data-ttu-id="497a7-132">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="497a7-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="497a7-133">В поле **Допустимо для** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="497a7-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="497a7-134">В поле **Ценообразование** введите число.</span><span class="sxs-lookup"><span data-stu-id="497a7-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="497a7-135">Фактической ценой продажи, которая используется, когда работник заносит проводки в журнал затрат, является цена продажи с самым высоким уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="497a7-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="497a7-136">Например, если существует общая цена продажи и цена продажи для работника, то будет использоваться цена продажи для работника.</span><span class="sxs-lookup"><span data-stu-id="497a7-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="497a7-137">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="497a7-137">Select **Save**.</span></span>

