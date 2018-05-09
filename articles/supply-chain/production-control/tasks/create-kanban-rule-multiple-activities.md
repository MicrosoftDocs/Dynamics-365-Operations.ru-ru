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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 37b9224e1c2af3340a0412e90a35f0e2c4cbffaf
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="af7be-103">Создание правила канбана для нескольких мероприятий</span><span class="sxs-lookup"><span data-stu-id="af7be-103">Create a kanban rule for multiple activities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af7be-104">В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="af7be-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="af7be-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="af7be-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="af7be-106">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="af7be-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="af7be-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="af7be-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="af7be-108">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="af7be-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="af7be-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="af7be-109">Click New.</span></span>
3. <span data-ttu-id="af7be-110">В поле "Стратегия пополнения" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="af7be-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="af7be-111">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="af7be-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="af7be-112">Выберите SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="af7be-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="af7be-113">Установите флажок "Несколько мероприятий".</span><span class="sxs-lookup"><span data-stu-id="af7be-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="af7be-114">Цель — включить несколько мероприятий в правило канбана.</span><span class="sxs-lookup"><span data-stu-id="af7be-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="af7be-115">Вы выбираете путь в производственном потоке при выборе последнего мероприятия плана.</span><span class="sxs-lookup"><span data-stu-id="af7be-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="af7be-116">В поле "Последнее мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="af7be-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="af7be-117">Выберите SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="af7be-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="af7be-118">После выбора значения страница откроется автоматически.</span><span class="sxs-lookup"><span data-stu-id="af7be-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="af7be-119">Выберите поток канбана SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="af7be-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="af7be-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="af7be-120">Click OK.</span></span>  
7. <span data-ttu-id="af7be-121">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="af7be-121">Expand the Details section.</span></span>
8. <span data-ttu-id="af7be-122">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="af7be-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="af7be-123">Выберите номенклатуру L0006.</span><span class="sxs-lookup"><span data-stu-id="af7be-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="af7be-124">Создание канбана и просмотр заданий</span><span class="sxs-lookup"><span data-stu-id="af7be-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="af7be-125">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="af7be-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="af7be-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="af7be-126">Click Add.</span></span>
3. <span data-ttu-id="af7be-127">В поле "Число новых канбанов" введите "1".</span><span class="sxs-lookup"><span data-stu-id="af7be-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="af7be-128">В результате будет создан один канбан.</span><span class="sxs-lookup"><span data-stu-id="af7be-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="af7be-129">Установите количество продукта равным 3.</span><span class="sxs-lookup"><span data-stu-id="af7be-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="af7be-130">Канбан будет обрабатывать 3 продукта.</span><span class="sxs-lookup"><span data-stu-id="af7be-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="af7be-131">В поле "Дата/время срока выполнения" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="af7be-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="af7be-132">Можно ввести значение "Сегодня".</span><span class="sxs-lookup"><span data-stu-id="af7be-132">You can enter Today.</span></span>  
6. <span data-ttu-id="af7be-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="af7be-133">Click Create.</span></span>
7. <span data-ttu-id="af7be-134">Нажмите кнопку Состав.</span><span class="sxs-lookup"><span data-stu-id="af7be-134">Click Details.</span></span>
    * <span data-ttu-id="af7be-135">Обратите внимание, что канбан имеет два задания процесса из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="af7be-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="af7be-136">Первое задание — это SpeakerAssemblyAndPolish, второе — SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="af7be-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="af7be-137">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="af7be-137">This is the last step!</span></span>  


