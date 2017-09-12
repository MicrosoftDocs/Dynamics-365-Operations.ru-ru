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
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="f625b-103">Удаление задания канбана из плана</span><span class="sxs-lookup"><span data-stu-id="f625b-103">Remove a kanban job from the schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f625b-104">В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="f625b-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="f625b-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="f625b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f625b-106">Эта процедура предназначена для начальника цеха или планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="f625b-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="f625b-107">Поиск запланированного задания канбана</span><span class="sxs-lookup"><span data-stu-id="f625b-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="f625b-108">Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="f625b-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="f625b-109">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f625b-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f625b-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f625b-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f625b-111">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="f625b-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="f625b-112">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="f625b-112">Click Select.</span></span>
5. <span data-ttu-id="f625b-113">В поле "Показать статус задания" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="f625b-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="f625b-114">Удаление запланированного задания канбана из плана</span><span class="sxs-lookup"><span data-stu-id="f625b-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="f625b-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f625b-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f625b-116">Выберите задание со статусом "Запланировано", например задание, запланированное на 19 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="f625b-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="f625b-117">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="f625b-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="f625b-118">Щелкните "Вернуть статус задания".</span><span class="sxs-lookup"><span data-stu-id="f625b-118">Click Revert job status.</span></span>
4. <span data-ttu-id="f625b-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f625b-119">Click OK.</span></span>
    * <span data-ttu-id="f625b-120">В результате текущий статус задания будет изменен с "Запланировано" на "Не запланировано" и задание будет удалено с панели процессов.</span><span class="sxs-lookup"><span data-stu-id="f625b-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   


