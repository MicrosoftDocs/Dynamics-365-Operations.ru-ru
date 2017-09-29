--- 
title: "Подготовка обработки заданий канбана при отсутствии материалов для производственной ячейки"
description: "Эта процедура заключается в подготовке задания канбана обработки, когда для производственной ячейки отсутствуют некоторые материалы, поэтому необходимо выбрать материалы со склада."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="5dbdc-103">Подготовка обработки заданий канбана при отсутствии материалов для производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="5dbdc-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dbdc-104">Эта процедура заключается в подготовке задания канбана обработки, когда для производственной ячейки отсутствуют некоторые материалы, поэтому необходимо выбрать материалы со склада.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="5dbdc-105">Процедура "Подготовка задания канбана обработки при наличии материалов" является предварительным условием для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="5dbdc-106">Эта процедура предназначена для оператора.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="5dbdc-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5dbdc-108">Перейдите в раздел "Управление производством" > "Канбан" > "Доска канбана для заданий процесса".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="5dbdc-109">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5dbdc-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5dbdc-111">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="5dbdc-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5dbdc-113">Выберите канбан 000356.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="5dbdc-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5dbdc-115">В списке отмените выбор строки 4.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-115">In the list, deselect row 4.</span></span> <span data-ttu-id="5dbdc-116">(Или выберите строку 4, если вы не выполнили задачу "Подготовка задания канбана обработки при наличии материалов").</span><span class="sxs-lookup"><span data-stu-id="5dbdc-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="5dbdc-117">Переключите развертывание раздела "Отгрузочная накладная".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="5dbdc-118">Значок "Отсутствует запись" в статусе поставки указывает, что для производственной ячейки отсутствует 48 шт. номенклатуры P0002.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="5dbdc-119">Перемещение материалов в производственную ячейку</span><span class="sxs-lookup"><span data-stu-id="5dbdc-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="5dbdc-120">Переключите развертывание раздела "Задачи перемещения".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="5dbdc-121">В экспресс-фильтре по полю "Код номенклатуры" выберите значение "P0002".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="5dbdc-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5dbdc-123">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-123">Click Start.</span></span>
    * <span data-ttu-id="5dbdc-124">Идет перемещение.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="5dbdc-125">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-125">Click Complete.</span></span>
    * <span data-ttu-id="5dbdc-126">Номенклатура P0002 теперь присутствует в листе комплектации для задания канбана.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="5dbdc-127">Это означает, что мы можем подготовить канбан со всеми необходимыми материалами.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="5dbdc-128">Щелкните "Подготовить".</span><span class="sxs-lookup"><span data-stu-id="5dbdc-128">Click Prepare.</span></span>
    * <span data-ttu-id="5dbdc-129">Обратите внимание, что значок "Статус задания" показывает, что задание теперь готово.</span><span class="sxs-lookup"><span data-stu-id="5dbdc-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


