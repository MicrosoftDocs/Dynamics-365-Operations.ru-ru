---
title: Перемещение материалов с помощью заданий канбана
description: Эта процедура заключается в выполнении задания канбана изъятия для перемещения материалов.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcab5d27d1e5bb2f86910fe083168e7b97c52e2f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148818"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="4f6f6-103">Перемещение материалов с помощью заданий канбана</span><span class="sxs-lookup"><span data-stu-id="4f6f6-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f6f6-104">Эта процедура заключается в выполнении задания канбана изъятия для перемещения материалов.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="4f6f6-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4f6f6-106">Эта процедура предназначена для работника склада.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="4f6f6-107">Отображение заданий переноса</span><span class="sxs-lookup"><span data-stu-id="4f6f6-107">Display transfer jobs</span></span>
1. <span data-ttu-id="4f6f6-108">Перейдите в раздел "Управление производством" > "Канбан" > "Доска канбана для заданий переноса".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="4f6f6-109">Разверните или сверните раздел "Фильтры".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="4f6f6-110">В разделе "Фильтры" можно указать, какие задания вы хотите просматривать, отфильтровав их по полям "Производственный поток", "Наименование мероприятия", "Со склада", "Из местонахождения", "На склад", "В местонахождение".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="4f6f6-111">В поле "Со склада" введите значение "11".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="4f6f6-112">В поле "В ячейку" введите "12".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="4f6f6-113">Запустить задание переноса</span><span class="sxs-lookup"><span data-stu-id="4f6f6-113">Start a transfer job</span></span>
1. <span data-ttu-id="4f6f6-114">В списке снимите выбор с выбранной строки, если какая-либо из строк выбрана.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="4f6f6-115">В списке выберите строку 4.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="4f6f6-116">Выберите первое задание с состоянием "Не запланировано".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="4f6f6-117">Убедитесь, что это единственное выбранное задание.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="4f6f6-118">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-118">Click Start.</span></span>
    * <span data-ttu-id="4f6f6-119">Обратите внимание на значок, который показывает, что задание начато.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="4f6f6-120">Выбор второго задания переноса и изменение количества</span><span class="sxs-lookup"><span data-stu-id="4f6f6-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="4f6f6-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f6f6-122">Можно выбрать несколько заданий, но пока что выберите строку 5.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="4f6f6-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f6f6-124">Убедитесь, что задание из предыдущего шага — единственное выбранное задание.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="4f6f6-125">Снимите выбор со всех остальных заданий.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="4f6f6-126">Запомните значение в поле "Количество для задания" для справки в будущем</span><span class="sxs-lookup"><span data-stu-id="4f6f6-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="4f6f6-127">Установите количество для задания равным 30.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="4f6f6-128">Обратите внимание на предупреждение!</span><span class="sxs-lookup"><span data-stu-id="4f6f6-128">Notice the warning!</span></span> <span data-ttu-id="4f6f6-129">У вас нет разрешения на перемещение 30 единиц.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="4f6f6-130">В соответствии с настройкой правила канбана вы можете переместить только первоначальное количество.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="4f6f6-131">Используйте значение, введенное ранее в поле "Количество для задания"</span><span class="sxs-lookup"><span data-stu-id="4f6f6-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="4f6f6-132">Задайте значение в поле "Количество для задания" равным предыдущему значению.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="4f6f6-133">Запуск второго задания переноса</span><span class="sxs-lookup"><span data-stu-id="4f6f6-133">Start the second transfer job</span></span>
1. <span data-ttu-id="4f6f6-134">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-134">Click Start.</span></span>
    * <span data-ttu-id="4f6f6-135">В результате начнется перемещение задания в строке 5.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="4f6f6-136">Завершение обоих заданий переноса</span><span class="sxs-lookup"><span data-stu-id="4f6f6-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="4f6f6-137">В списке выберите строку 4.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="4f6f6-138">Теперь в строке 4 и в строке 5 выбрано два задания переноса.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="4f6f6-139">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="4f6f6-139">Click Complete.</span></span>
    * <span data-ttu-id="4f6f6-140">В результате перемещение обоих заданий будет перемещено.</span><span class="sxs-lookup"><span data-stu-id="4f6f6-140">This will complete the transfer of both jobs.</span></span>  

