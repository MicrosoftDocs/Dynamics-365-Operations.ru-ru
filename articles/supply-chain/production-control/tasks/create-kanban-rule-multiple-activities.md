---
title: Создание правила канбана для нескольких мероприятий
description: В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b52e33c34a2fd151765833c68eab9091b22405cc
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147028"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="03a92-103">Создание правила канбана для нескольких мероприятий</span><span class="sxs-lookup"><span data-stu-id="03a92-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03a92-104">В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="03a92-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="03a92-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="03a92-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="03a92-106">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="03a92-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="03a92-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="03a92-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="03a92-108">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="03a92-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="03a92-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="03a92-109">Click New.</span></span>
3. <span data-ttu-id="03a92-110">В поле "Стратегия пополнения" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="03a92-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="03a92-111">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="03a92-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="03a92-112">Выберите SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="03a92-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="03a92-113">Установите флажок "Несколько мероприятий".</span><span class="sxs-lookup"><span data-stu-id="03a92-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="03a92-114">Цель — включить несколько мероприятий в правило канбана.</span><span class="sxs-lookup"><span data-stu-id="03a92-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="03a92-115">Вы выбираете путь в производственном потоке при выборе последнего мероприятия плана.</span><span class="sxs-lookup"><span data-stu-id="03a92-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="03a92-116">В поле "Последнее мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="03a92-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="03a92-117">Выберите SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="03a92-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="03a92-118">После выбора значения страница откроется автоматически.</span><span class="sxs-lookup"><span data-stu-id="03a92-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="03a92-119">Выберите поток канбана SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="03a92-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="03a92-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="03a92-120">Click OK.</span></span>  
7. <span data-ttu-id="03a92-121">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="03a92-121">Expand the Details section.</span></span>
8. <span data-ttu-id="03a92-122">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="03a92-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="03a92-123">Выберите номенклатуру L0006.</span><span class="sxs-lookup"><span data-stu-id="03a92-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="03a92-124">Создание канбана и просмотр заданий</span><span class="sxs-lookup"><span data-stu-id="03a92-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="03a92-125">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="03a92-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="03a92-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="03a92-126">Click Add.</span></span>
3. <span data-ttu-id="03a92-127">В поле "Число новых канбанов" введите "1".</span><span class="sxs-lookup"><span data-stu-id="03a92-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="03a92-128">В результате будет создан один канбан.</span><span class="sxs-lookup"><span data-stu-id="03a92-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="03a92-129">Установите количество продукта равным 3.</span><span class="sxs-lookup"><span data-stu-id="03a92-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="03a92-130">Канбан будет обрабатывать 3 продукта.</span><span class="sxs-lookup"><span data-stu-id="03a92-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="03a92-131">В поле "Дата/время срока выполнения" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="03a92-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="03a92-132">Можно ввести значение "Сегодня".</span><span class="sxs-lookup"><span data-stu-id="03a92-132">You can enter Today.</span></span>  
6. <span data-ttu-id="03a92-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="03a92-133">Click Create.</span></span>
7. <span data-ttu-id="03a92-134">Нажмите кнопку Состав.</span><span class="sxs-lookup"><span data-stu-id="03a92-134">Click Details.</span></span>
    * <span data-ttu-id="03a92-135">Обратите внимание, что канбан имеет два задания процесса из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="03a92-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="03a92-136">Первое задание — это SpeakerAssemblyAndPolish, второе — SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="03a92-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="03a92-137">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="03a92-137">This is the last step!</span></span>  

