--- 
title: "Создание правила канбана для нескольких мероприятий"
description: "В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.openlocfilehash: d6d0c50da3124553124b65f6ba0e1c5ed35e8613
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="4c305-103">Создание правила канбана для нескольких мероприятий</span><span class="sxs-lookup"><span data-stu-id="4c305-103">Create a kanban rule for multiple activities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c305-104">В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="4c305-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="4c305-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="4c305-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="4c305-106">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="4c305-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="4c305-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="4c305-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="4c305-108">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="4c305-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="4c305-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4c305-109">Click New.</span></span>
3. <span data-ttu-id="4c305-110">В поле "Стратегия пополнения" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="4c305-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="4c305-111">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4c305-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="4c305-112">Выберите SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="4c305-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="4c305-113">Установите флажок "Несколько мероприятий".</span><span class="sxs-lookup"><span data-stu-id="4c305-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="4c305-114">Цель — включить несколько мероприятий в правило канбана.</span><span class="sxs-lookup"><span data-stu-id="4c305-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="4c305-115">Вы выбираете путь в производственном потоке при выборе последнего мероприятия плана.</span><span class="sxs-lookup"><span data-stu-id="4c305-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="4c305-116">В поле "Последнее мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4c305-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="4c305-117">Выберите SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="4c305-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="4c305-118">После выбора значения страница откроется автоматически.</span><span class="sxs-lookup"><span data-stu-id="4c305-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="4c305-119">Выберите поток канбана SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="4c305-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="4c305-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4c305-120">Click OK.</span></span>  
7. <span data-ttu-id="4c305-121">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="4c305-121">Expand the Details section.</span></span>
8. <span data-ttu-id="4c305-122">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4c305-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="4c305-123">Выберите номенклатуру L0006.</span><span class="sxs-lookup"><span data-stu-id="4c305-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="4c305-124">Создание канбана и просмотр заданий</span><span class="sxs-lookup"><span data-stu-id="4c305-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="4c305-125">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="4c305-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="4c305-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="4c305-126">Click Add.</span></span>
3. <span data-ttu-id="4c305-127">В поле "Число новых канбанов" введите "1".</span><span class="sxs-lookup"><span data-stu-id="4c305-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="4c305-128">В результате будет создан один канбан.</span><span class="sxs-lookup"><span data-stu-id="4c305-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="4c305-129">Установите количество продукта равным 3.</span><span class="sxs-lookup"><span data-stu-id="4c305-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="4c305-130">Канбан будет обрабатывать 3 продукта.</span><span class="sxs-lookup"><span data-stu-id="4c305-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="4c305-131">В поле "Дата/время срока выполнения" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="4c305-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="4c305-132">Можно ввести значение "Сегодня".</span><span class="sxs-lookup"><span data-stu-id="4c305-132">You can enter Today.</span></span>  
6. <span data-ttu-id="4c305-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4c305-133">Click Create.</span></span>
7. <span data-ttu-id="4c305-134">Нажмите кнопку Состав.</span><span class="sxs-lookup"><span data-stu-id="4c305-134">Click Details.</span></span>
    * <span data-ttu-id="4c305-135">Обратите внимание, что канбан имеет два задания процесса из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="4c305-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="4c305-136">Первое задание — это SpeakerAssemblyAndPolish, второе — SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="4c305-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="4c305-137">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="4c305-137">This is the last step!</span></span>  


