---
title: Перемещение запланированных заданий канбана
description: В этой процедуре описывается перемещение запланированных заданий обработки канбана в другой период.
author: ChristianRytt
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d58ee740824809f15da68db66616bb01d5dbfab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825022"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="c421a-103">Перемещение запланированных заданий канбана</span><span class="sxs-lookup"><span data-stu-id="c421a-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c421a-104">В этой процедуре описывается перемещение запланированных заданий обработки канбана в другой период.</span><span class="sxs-lookup"><span data-stu-id="c421a-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="c421a-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c421a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c421a-106">Эта процедура предназначена для начальника цеха или планировщика производства, работающего с канбанами.</span><span class="sxs-lookup"><span data-stu-id="c421a-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="c421a-107">Выберите запланированные заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="c421a-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="c421a-108">Перейдите в раздел **Управление производством > Канбан > Планирование заданий канбана**.</span><span class="sxs-lookup"><span data-stu-id="c421a-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="c421a-109">В поле **Производственная ячейка** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c421a-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="c421a-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c421a-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="c421a-111">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="c421a-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="c421a-112">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="c421a-112">Click **Select**.</span></span> 

5. <span data-ttu-id="c421a-113">В поле **Показать статус задания** выберите **Запланировано**.</span><span class="sxs-lookup"><span data-stu-id="c421a-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="c421a-114">В результате будет отфильтрован список заданий для отображения только запланированных заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="c421a-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="c421a-115">Переместите задания канбана в другой период.</span><span class="sxs-lookup"><span data-stu-id="c421a-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="c421a-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c421a-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="c421a-117">Выберите задание со статусом **Запланировано**, например задание, запланированное на 20 декабря 2012 г., в поле **Запланированный период**.</span><span class="sxs-lookup"><span data-stu-id="c421a-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="c421a-118">Затем переместите задание в предыдущий период.</span><span class="sxs-lookup"><span data-stu-id="c421a-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="c421a-119">Щелкните **Предыдущий период**.</span><span class="sxs-lookup"><span data-stu-id="c421a-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="c421a-120">Щелкните **Конец**, чтобы переместить задание в конец списка заданий как последнее задание в предыдущем периоде.</span><span class="sxs-lookup"><span data-stu-id="c421a-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="c421a-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c421a-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="c421a-122">Выберите задание со статусом **Запланировано**, например задание, запланированное на 18 декабря 2012 г., в поле **Запланированный период**.</span><span class="sxs-lookup"><span data-stu-id="c421a-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="c421a-123">Затем переместите задание в следующий период.</span><span class="sxs-lookup"><span data-stu-id="c421a-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="c421a-124">Щелкните **Следующий период**.</span><span class="sxs-lookup"><span data-stu-id="c421a-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="c421a-125">Щелкните **Начало**, чтобы переместить задание в начало списка заданий как первое задание в предыдущем периоде.</span><span class="sxs-lookup"><span data-stu-id="c421a-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="c421a-126">Переместите задание в пределах периода.</span><span class="sxs-lookup"><span data-stu-id="c421a-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="c421a-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c421a-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="c421a-128">Выберите задание со статусом "Запланировано", например второе задание, запланированное на 19 декабря 2012 г., в поле **Запланированный период**.</span><span class="sxs-lookup"><span data-stu-id="c421a-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="c421a-129">Затем переместите задание в запланированном периоде.</span><span class="sxs-lookup"><span data-stu-id="c421a-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="c421a-130">Щелкните **Вперед**.</span><span class="sxs-lookup"><span data-stu-id="c421a-130">Click **Forward**.</span></span> <span data-ttu-id="c421a-131">Обратите внимание, что задание переместится на одну строку вниз в списке.</span><span class="sxs-lookup"><span data-stu-id="c421a-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="c421a-132">Щелкните **Назад**.</span><span class="sxs-lookup"><span data-stu-id="c421a-132">Click **Backward**.</span></span> <span data-ttu-id="c421a-133">Обратите внимание, что задание переместится на одну строку вверх в списке.</span><span class="sxs-lookup"><span data-stu-id="c421a-133">Notice that the job is moved one line up on the list.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]