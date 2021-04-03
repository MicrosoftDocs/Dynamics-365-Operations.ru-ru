---
title: Выполнение заданий процессов канбана
description: Эта процедура рассматривает выполнение заданий процессов канбана.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10f8a464207fc3b1c34638a9f55df7b53a69b357
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259802"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="fa96f-103">Выполнение заданий процессов канбана</span><span class="sxs-lookup"><span data-stu-id="fa96f-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa96f-104">Эта процедура рассматривает выполнение заданий процессов канбана.</span><span class="sxs-lookup"><span data-stu-id="fa96f-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="fa96f-105">Первое задание завершено с ожидаемым количеством и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="fa96f-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="fa96f-106">Второе задание завершено с ошибками.</span><span class="sxs-lookup"><span data-stu-id="fa96f-106">The second job is completed with errors.</span></span> <span data-ttu-id="fa96f-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="fa96f-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fa96f-108">Эта процедура предназначена для оператора.</span><span class="sxs-lookup"><span data-stu-id="fa96f-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="fa96f-109">Выбор задания канбана</span><span class="sxs-lookup"><span data-stu-id="fa96f-109">Select a kanban job</span></span>
1. <span data-ttu-id="fa96f-110">Перейдите в раздел "Управление производством" > "Канбан" > "Доска канбана для заданий процесса".</span><span class="sxs-lookup"><span data-stu-id="fa96f-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="fa96f-111">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="fa96f-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fa96f-112">Щелкните строку с группой ресурсов 1250.</span><span class="sxs-lookup"><span data-stu-id="fa96f-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="fa96f-113">В результате будет отфильтрован список заданий для отображения только заданий для производственной ячейки 1250.</span><span class="sxs-lookup"><span data-stu-id="fa96f-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="fa96f-114">Пометьте строку со статусом задания "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="fa96f-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="fa96f-115">Завершение задания с ожидаемым количеством</span><span class="sxs-lookup"><span data-stu-id="fa96f-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="fa96f-116">Разверните или сверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="fa96f-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="fa96f-117">Этот раздел содержит важную информацию о номере карты, коде номенклатуры, заказанном количестве и имени мероприятия.</span><span class="sxs-lookup"><span data-stu-id="fa96f-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="fa96f-118">Разверните или сверните раздел "Производственные инструкции".</span><span class="sxs-lookup"><span data-stu-id="fa96f-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="fa96f-119">Этот раздел содержит производственные инструкции для мероприятия.</span><span class="sxs-lookup"><span data-stu-id="fa96f-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="fa96f-120">Инструкции могут быть текстом, изображениями, чертежами и другими документами.</span><span class="sxs-lookup"><span data-stu-id="fa96f-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="fa96f-121">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="fa96f-121">Click Start.</span></span>
    * <span data-ttu-id="fa96f-122">Выберите задание, которое еще не выполнено.</span><span class="sxs-lookup"><span data-stu-id="fa96f-122">Select a job that is not completed.</span></span> <span data-ttu-id="fa96f-123">Используйте значки статуса в поле "Статус задания" для просмотра статуса задания.</span><span class="sxs-lookup"><span data-stu-id="fa96f-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="fa96f-124">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="fa96f-124">Click Complete.</span></span>
    * <span data-ttu-id="fa96f-125">Задание завершено с предполагаемым качеством.</span><span class="sxs-lookup"><span data-stu-id="fa96f-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="fa96f-126">Завершение задания с ошибками</span><span class="sxs-lookup"><span data-stu-id="fa96f-126">Complete a job with errors</span></span>
1. <span data-ttu-id="fa96f-127">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="fa96f-127">Click Start.</span></span>
    * <span data-ttu-id="fa96f-128">По завершении задания будет автоматически выбрано следующее задание в списке.</span><span class="sxs-lookup"><span data-stu-id="fa96f-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="fa96f-129">Поэтому вам не нужно выбирать задание, прежде чем нажать кнопку "Начать".</span><span class="sxs-lookup"><span data-stu-id="fa96f-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="fa96f-130">В области действий щелкните "Производство".</span><span class="sxs-lookup"><span data-stu-id="fa96f-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="fa96f-131">Щелкните "Завершить (подробные сведения)".</span><span class="sxs-lookup"><span data-stu-id="fa96f-131">Click Complete (details).</span></span>
4. <span data-ttu-id="fa96f-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fa96f-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="fa96f-133">В поле "Ошибка в количестве" введите число.</span><span class="sxs-lookup"><span data-stu-id="fa96f-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="fa96f-134">В поле "Количество правильных" введите число.</span><span class="sxs-lookup"><span data-stu-id="fa96f-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="fa96f-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="fa96f-135">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]