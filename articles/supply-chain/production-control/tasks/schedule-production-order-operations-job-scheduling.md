---
title: Планирование производственного заказа с помощью планирования операций и заданий
description: Эта процедура рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4932cfa472c34a16249b226aa4a07b8e5f528053
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838495"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="00f87-103">Планирование производственного заказа с помощью планирования операций и заданий</span><span class="sxs-lookup"><span data-stu-id="00f87-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00f87-104">Эта процедура рассматривает планирование производственного заказа с помощью планирования операций и планирования заданий.</span><span class="sxs-lookup"><span data-stu-id="00f87-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="00f87-105">Задания не создаются при планировании операций и создаются при планировании заданий.</span><span class="sxs-lookup"><span data-stu-id="00f87-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="00f87-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="00f87-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="00f87-107">Эта процедура предназначена для менеджера по производству, планировщика производства или начальника производственного участка, работающего в среде дискретного производства.</span><span class="sxs-lookup"><span data-stu-id="00f87-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="00f87-108">Создание производственного заказа</span><span class="sxs-lookup"><span data-stu-id="00f87-108">Create a production order</span></span>
1. <span data-ttu-id="00f87-109">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="00f87-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="00f87-110">Щелкните "Новый производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="00f87-110">Click New production order.</span></span>
3. <span data-ttu-id="00f87-111">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="00f87-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="00f87-112">Выберите код номенклатуры D0001.</span><span class="sxs-lookup"><span data-stu-id="00f87-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="00f87-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="00f87-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="00f87-114">Планирование операций для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="00f87-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="00f87-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="00f87-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="00f87-116">Выберите производственный заказ, который вы только что создали.</span><span class="sxs-lookup"><span data-stu-id="00f87-116">Select the production order that you have just created.</span></span> <span data-ttu-id="00f87-117">Он должен находиться вверху списка.</span><span class="sxs-lookup"><span data-stu-id="00f87-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="00f87-118">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="00f87-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="00f87-119">Щелкните "Планирование операций".</span><span class="sxs-lookup"><span data-stu-id="00f87-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="00f87-120">В поле "Направление планирования" выберите "Вперед от даты планирования".</span><span class="sxs-lookup"><span data-stu-id="00f87-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="00f87-121">В поле "Дата планирования" введите дату.</span><span class="sxs-lookup"><span data-stu-id="00f87-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="00f87-122">Выберите дату в будущем, например сегодня плюс одна неделя.</span><span class="sxs-lookup"><span data-stu-id="00f87-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="00f87-123">При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.</span><span class="sxs-lookup"><span data-stu-id="00f87-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="00f87-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="00f87-124">Click OK.</span></span>
7. <span data-ttu-id="00f87-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="00f87-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="00f87-126">Обратите внимание, что статус изменяется на "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="00f87-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="00f87-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="00f87-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="00f87-128">Щелкните "Все задания".</span><span class="sxs-lookup"><span data-stu-id="00f87-128">Click All jobs.</span></span>
    * <span data-ttu-id="00f87-129">Обратите внимание, что задания не создаются при планировании операций.</span><span class="sxs-lookup"><span data-stu-id="00f87-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="00f87-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00f87-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="00f87-131">Планирование заданий для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="00f87-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="00f87-132">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="00f87-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="00f87-133">Щелкните "Планирование заданий".</span><span class="sxs-lookup"><span data-stu-id="00f87-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="00f87-134">В поле "Направление планирования" выберите "Вперед от даты планирования".</span><span class="sxs-lookup"><span data-stu-id="00f87-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="00f87-135">В поле "Дата планирования" введите дату.</span><span class="sxs-lookup"><span data-stu-id="00f87-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="00f87-136">Выберите дату в будущем, например сегодня плюс одна неделя.</span><span class="sxs-lookup"><span data-stu-id="00f87-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="00f87-137">При выбранном направлении планирования для производственного заказа будет выполнено планирование вперед с этой даты.</span><span class="sxs-lookup"><span data-stu-id="00f87-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="00f87-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="00f87-138">Click OK.</span></span>
6. <span data-ttu-id="00f87-139">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="00f87-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="00f87-140">Щелкните "Все задания".</span><span class="sxs-lookup"><span data-stu-id="00f87-140">Click All jobs.</span></span>
    * <span data-ttu-id="00f87-141">Обратите внимание, что на основе активного маршрута создано 5 заданий с помощью планирования заданий.</span><span class="sxs-lookup"><span data-stu-id="00f87-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

