--- 
title: "Удаление задания канбана из плана"
description: "В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на \"Не запланировано\"."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: ab49ce6669982e6822e1972422acfce43deb5a21
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="df63a-103">Удаление задания канбана из плана</span><span class="sxs-lookup"><span data-stu-id="df63a-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df63a-104">В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="df63a-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="df63a-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="df63a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="df63a-106">Эта процедура предназначена для начальника цеха или планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="df63a-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="df63a-107">Поиск запланированного задания канбана</span><span class="sxs-lookup"><span data-stu-id="df63a-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="df63a-108">Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="df63a-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="df63a-109">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="df63a-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="df63a-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="df63a-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="df63a-111">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="df63a-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="df63a-112">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="df63a-112">Click Select.</span></span>
5. <span data-ttu-id="df63a-113">В поле "Показать статус задания" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="df63a-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="df63a-114">Удаление запланированного задания канбана из плана</span><span class="sxs-lookup"><span data-stu-id="df63a-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="df63a-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="df63a-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="df63a-116">Выберите задание со статусом "Запланировано", например задание, запланированное на 19 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="df63a-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="df63a-117">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="df63a-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="df63a-118">Щелкните "Вернуть статус задания".</span><span class="sxs-lookup"><span data-stu-id="df63a-118">Click Revert job status.</span></span>
4. <span data-ttu-id="df63a-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="df63a-119">Click OK.</span></span>
    * <span data-ttu-id="df63a-120">В результате текущий статус задания будет изменен с "Запланировано" на "Не запланировано" и задание будет удалено с панели процессов.</span><span class="sxs-lookup"><span data-stu-id="df63a-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   


