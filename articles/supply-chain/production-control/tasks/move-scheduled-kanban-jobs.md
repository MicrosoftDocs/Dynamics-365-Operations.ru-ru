--- 
title: "Перемещение запланированных заданий канбана"
description: "В этой процедуре описывается перемещение запланированных заданий обработки канбана в другой период."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="da8d9-103">Перемещение запланированных заданий канбана</span><span class="sxs-lookup"><span data-stu-id="da8d9-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da8d9-104">В этой процедуре описывается перемещение запланированных заданий обработки канбана в другой период.</span><span class="sxs-lookup"><span data-stu-id="da8d9-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="da8d9-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="da8d9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="da8d9-106">Эта процедура предназначена для начальника цеха или планировщика производства, работающего с канбанами.</span><span class="sxs-lookup"><span data-stu-id="da8d9-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="da8d9-107">Выбор запланированных заданий канбана</span><span class="sxs-lookup"><span data-stu-id="da8d9-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="da8d9-108">Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="da8d9-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="da8d9-109">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="da8d9-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="da8d9-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="da8d9-110">áçêìõý !</span></span>
3. <span data-ttu-id="da8d9-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="da8d9-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="da8d9-112">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="da8d9-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="da8d9-113">Нажмите кнопку "Выбрать".</span><span class="sxs-lookup"><span data-stu-id="da8d9-113">Klik på Select.</span></span>
5. <span data-ttu-id="da8d9-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="da8d9-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="da8d9-115">В результате будет отфильтрован список заданий для отображения только запланированных заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="da8d9-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="da8d9-116">Перемещение заданий канбана в другой период</span><span class="sxs-lookup"><span data-stu-id="da8d9-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="da8d9-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="da8d9-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="da8d9-118">Выберите задание со статусом "Запланировано", например задание, запланированное на 20 декабря 2012 г., в поле "Запланированный период".</span><span class="sxs-lookup"><span data-stu-id="da8d9-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="da8d9-119">Затем переместите задание в предыдущий период.</span><span class="sxs-lookup"><span data-stu-id="da8d9-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="da8d9-120">Щелкните "Предыдущий период".</span><span class="sxs-lookup"><span data-stu-id="da8d9-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="da8d9-121">Щелкните "Конец".</span><span class="sxs-lookup"><span data-stu-id="da8d9-121">Klik på End.</span></span>
    * <span data-ttu-id="da8d9-122">В результате задание переместится в конец списка заданий как последнее задание в предыдущем периоде.</span><span class="sxs-lookup"><span data-stu-id="da8d9-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="da8d9-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="da8d9-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="da8d9-124">Выберите задание со статусом "Запланировано", например задание, запланированное на 18 декабря 2012 г., в поле "Запланированный период".</span><span class="sxs-lookup"><span data-stu-id="da8d9-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="da8d9-125">Затем переместите задание в следующий период.</span><span class="sxs-lookup"><span data-stu-id="da8d9-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="da8d9-126">Щелкните "Следующий период".</span><span class="sxs-lookup"><span data-stu-id="da8d9-126">Klik på Next period.</span></span>
6. <span data-ttu-id="da8d9-127">Щелкните "Начало".</span><span class="sxs-lookup"><span data-stu-id="da8d9-127">Klik på Start.</span></span>
    * <span data-ttu-id="da8d9-128">В результате задание переместится в начало списка заданий как первое задание в предыдущем периоде.</span><span class="sxs-lookup"><span data-stu-id="da8d9-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="da8d9-129">Задача: перемещение задания в пределах периода</span><span class="sxs-lookup"><span data-stu-id="da8d9-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="da8d9-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="da8d9-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="da8d9-131">Выберите задание со статусом "Запланировано", например второе задание, запланированное на 19 декабря 2012 г., в поле "Запланированный период".</span><span class="sxs-lookup"><span data-stu-id="da8d9-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="da8d9-132">Затем переместите задание в запланированном периоде.</span><span class="sxs-lookup"><span data-stu-id="da8d9-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="da8d9-133">Щелкните "Вперед".</span><span class="sxs-lookup"><span data-stu-id="da8d9-133">Klik på Forward.</span></span>
    * <span data-ttu-id="da8d9-134">Обратите внимание, что задание переместится на одну строку вниз в списке.</span><span class="sxs-lookup"><span data-stu-id="da8d9-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="da8d9-135">Щелкните "Назад".</span><span class="sxs-lookup"><span data-stu-id="da8d9-135">Klik på Backward.</span></span>
    * <span data-ttu-id="da8d9-136">Обратите внимание, что задание переместится на одну строку вверх в списке.</span><span class="sxs-lookup"><span data-stu-id="da8d9-136">Notice that the job is moved one line up on the list.</span></span>  


