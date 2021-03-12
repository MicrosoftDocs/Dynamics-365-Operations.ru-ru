---
title: Планирование заданий канбана
description: В этой процедуре описывается планирование заданий обработки канбана для определенной производственной ячейки.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97b88a2637e661146e8150cd6535ff32745227a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996809"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="b162e-103">Планирование заданий канбана</span><span class="sxs-lookup"><span data-stu-id="b162e-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b162e-104">В этой процедуре описывается планирование заданий обработки канбана для определенной производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="b162e-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="b162e-105">Процедура "Подготовка задания обработки канбана при отсутствии материалов" является предварительным условием для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="b162e-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="b162e-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b162e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b162e-107">Эта задача предназначена для начальника цеха и планировщика производства, работающего с канбанами.</span><span class="sxs-lookup"><span data-stu-id="b162e-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="b162e-108">Выбор заданий канбана для производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="b162e-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="b162e-109">Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="b162e-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="b162e-110">Разверните информационное поле "Мощность периода".</span><span class="sxs-lookup"><span data-stu-id="b162e-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="b162e-111">Разверните информационное поле "Канбан".</span><span class="sxs-lookup"><span data-stu-id="b162e-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="b162e-112">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b162e-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b162e-113">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b162e-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b162e-114">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="b162e-114">Select work cell 1250.</span></span> <span data-ttu-id="b162e-115">В результате представление будет отфильтровано для отображения только заданий для производственной ячейки 1250.</span><span class="sxs-lookup"><span data-stu-id="b162e-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="b162e-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b162e-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b162e-117">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="b162e-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="b162e-118">Планирование задания канбана в первом доступном периоде</span><span class="sxs-lookup"><span data-stu-id="b162e-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="b162e-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b162e-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b162e-120">Выберите первую строку в списке со статусом "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="b162e-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="b162e-121">Значок пунктирной линии в поле "Статус задания" указывает, что задание не запланировано.</span><span class="sxs-lookup"><span data-stu-id="b162e-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="b162e-122">Щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="b162e-122">Click Schedule.</span></span>
    * <span data-ttu-id="b162e-123">В результате задание канбана будет запланировано в первом доступном периоде.</span><span class="sxs-lookup"><span data-stu-id="b162e-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="b162e-124">Обратите внимание, что задание канбана перемещается в конец списка, поскольку оно было добавлено в период, начинающийся с сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="b162e-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="b162e-125">Если период, начиная с сегодняшнего дня, полностью зарезервирован, задание будет перемещено в первый доступный период.</span><span class="sxs-lookup"><span data-stu-id="b162e-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="b162e-126">Планирование двух заданий канбана на определенный день</span><span class="sxs-lookup"><span data-stu-id="b162e-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="b162e-127">В списке выберите строку 1.</span><span class="sxs-lookup"><span data-stu-id="b162e-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="b162e-128">Вы должны увидеть, что первая строка имеет статус "Не запланировано" в поле "Статус задания".</span><span class="sxs-lookup"><span data-stu-id="b162e-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="b162e-129">В списке выберите строку 2.</span><span class="sxs-lookup"><span data-stu-id="b162e-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="b162e-130">Вы должны увидеть, что вторая строка имеет статус "Не запланировано" в поле "Статус задания".</span><span class="sxs-lookup"><span data-stu-id="b162e-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="b162e-131">Теперь выбрано два первых задания.</span><span class="sxs-lookup"><span data-stu-id="b162e-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="b162e-132">Щелкните "Планировать с даты", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b162e-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="b162e-133">Установите или снимите флажок "Переопределить реакцию на нехватку мощностей".</span><span class="sxs-lookup"><span data-stu-id="b162e-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="b162e-134">Этот параметр позволяет переопределить реакцию на нехватку мощности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b162e-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="b162e-135">В поле "Реакция на нехватку мощности" выберите "Добавить к запрошенному периоду".</span><span class="sxs-lookup"><span data-stu-id="b162e-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="b162e-136">Этот параметр гарантирует, что задание будет добавлено к спрошенному периоду независимо от того, перегружена ли ячейка.</span><span class="sxs-lookup"><span data-stu-id="b162e-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="b162e-137">Щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="b162e-137">Click Schedule.</span></span>
    * <span data-ttu-id="b162e-138">Обратите внимание, что оба задания добавляются в требуемый период.</span><span class="sxs-lookup"><span data-stu-id="b162e-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="b162e-139">В разделе "Мощность периода" можно просмотреть загрузку для каждого периода.</span><span class="sxs-lookup"><span data-stu-id="b162e-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="b162e-140">В поле "Потребление" отображается запланированное потребление в этом периоде.</span><span class="sxs-lookup"><span data-stu-id="b162e-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="b162e-141">Если запланированное потребление выше доступной мощности в этом периоде, будет выбрано перегруженное потребление.</span><span class="sxs-lookup"><span data-stu-id="b162e-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

