---
title: Подготовка обработки заданий канбана при отсутствии материалов для производственной ячейки
description: Эта процедура заключается в подготовке задания канбана обработки, когда для производственной ячейки отсутствуют некоторые материалы, поэтому необходимо выбрать материалы со склада.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d57df6188aacc2f8a56a7ba91c4ab50a90901a7e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206918"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="2a3bb-103">Подготовка обработки заданий канбана при отсутствии материалов для производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="2a3bb-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a3bb-104">Эта процедура заключается в подготовке задания канбана обработки, когда для производственной ячейки отсутствуют некоторые материалы, поэтому необходимо выбрать материалы со склада.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="2a3bb-105">Процедура "Подготовка задания канбана обработки при наличии материалов" является предварительным условием для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="2a3bb-106">Эта процедура предназначена для оператора.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="2a3bb-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2a3bb-108">Перейдите в раздел "Управление производством" > "Канбан" > "Доска канбана для заданий процесса".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="2a3bb-109">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2a3bb-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2a3bb-111">Выберите производственную ячейку 1250.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="2a3bb-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2a3bb-113">Выберите канбан 000356.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="2a3bb-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2a3bb-115">В списке отмените выбор строки 4.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-115">In the list, deselect row 4.</span></span> <span data-ttu-id="2a3bb-116">(Или выберите строку 4, если вы не выполнили задачу "Подготовка задания канбана обработки при наличии материалов").</span><span class="sxs-lookup"><span data-stu-id="2a3bb-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="2a3bb-117">Переключите развертывание раздела "Отгрузочная накладная".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="2a3bb-118">Значок "Отсутствует запись" в статусе поставки указывает, что для производственной ячейки отсутствует 48 шт. номенклатуры P0002.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="2a3bb-119">Перемещение материалов в производственную ячейку</span><span class="sxs-lookup"><span data-stu-id="2a3bb-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="2a3bb-120">Переключите развертывание раздела "Задачи перемещения".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="2a3bb-121">В экспресс-фильтре по полю "Код номенклатуры" выберите значение "P0002".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="2a3bb-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2a3bb-123">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-123">Click Start.</span></span>
    * <span data-ttu-id="2a3bb-124">Идет перемещение.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="2a3bb-125">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-125">Click Complete.</span></span>
    * <span data-ttu-id="2a3bb-126">Номенклатура P0002 теперь присутствует в листе комплектации для задания канбана.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="2a3bb-127">Это означает, что мы можем подготовить канбан со всеми необходимыми материалами.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="2a3bb-128">Щелкните "Подготовить".</span><span class="sxs-lookup"><span data-stu-id="2a3bb-128">Click Prepare.</span></span>
    * <span data-ttu-id="2a3bb-129">Обратите внимание, что значок "Статус задания" показывает, что задание теперь готово.</span><span class="sxs-lookup"><span data-stu-id="2a3bb-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

