---
title: Удаление задания канбана из плана
description: В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на "Не запланировано".
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "352076"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="7ff78-103">Удаление задания канбана из плана</span><span class="sxs-lookup"><span data-stu-id="7ff78-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ff78-104">В этой процедуре описывается удаление запланированного задания обработки канбана из плана путем изменения статуса задания на "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="7ff78-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="7ff78-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="7ff78-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7ff78-106">Эта процедура предназначена для начальника цеха или планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="7ff78-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="7ff78-107">Поиск запланированного задания канбана</span><span class="sxs-lookup"><span data-stu-id="7ff78-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="7ff78-108">Перейдите в раздел "Управление производством" > "Канбан" > "Планирование заданий канбана".</span><span class="sxs-lookup"><span data-stu-id="7ff78-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="7ff78-109">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7ff78-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7ff78-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7ff78-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7ff78-111">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="7ff78-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="7ff78-112">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="7ff78-112">Click Select.</span></span>
5. <span data-ttu-id="7ff78-113">В поле "Показать статус задания" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="7ff78-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="7ff78-114">Удаление запланированного задания канбана из плана</span><span class="sxs-lookup"><span data-stu-id="7ff78-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="7ff78-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7ff78-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ff78-116">Выберите задание со статусом "Запланировано", например задание, запланированное на 19 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="7ff78-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="7ff78-117">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="7ff78-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="7ff78-118">Щелкните "Вернуть статус задания".</span><span class="sxs-lookup"><span data-stu-id="7ff78-118">Click Revert job status.</span></span>
4. <span data-ttu-id="7ff78-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="7ff78-119">Click OK.</span></span>
    * <span data-ttu-id="7ff78-120">В результате текущий статус задания будет изменен с "Запланировано" на "Не запланировано" и задание будет удалено с панели процессов.</span><span class="sxs-lookup"><span data-stu-id="7ff78-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

