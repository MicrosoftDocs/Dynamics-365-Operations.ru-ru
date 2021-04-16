---
title: Создание правила канбана для нескольких мероприятий
description: В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 828b01fbb3b94b1fcb9fe8a565b1191a4f4bf630
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829122"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="863b6-103">Создание правила канбана для нескольких мероприятий</span><span class="sxs-lookup"><span data-stu-id="863b6-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="863b6-104">В этой процедуре показано, как создать правило канбана, которое включает несколько мероприятий из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="863b6-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="863b6-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="863b6-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="863b6-106">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="863b6-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="863b6-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="863b6-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="863b6-108">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="863b6-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="863b6-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="863b6-109">Click New.</span></span>
3. <span data-ttu-id="863b6-110">В поле "Стратегия пополнения" выберите "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="863b6-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="863b6-111">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="863b6-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="863b6-112">Выберите SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="863b6-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="863b6-113">Установите флажок "Несколько мероприятий".</span><span class="sxs-lookup"><span data-stu-id="863b6-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="863b6-114">Цель — включить несколько мероприятий в правило канбана.</span><span class="sxs-lookup"><span data-stu-id="863b6-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="863b6-115">Вы выбираете путь в производственном потоке при выборе последнего мероприятия плана.</span><span class="sxs-lookup"><span data-stu-id="863b6-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="863b6-116">В поле "Последнее мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="863b6-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="863b6-117">Выберите SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="863b6-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="863b6-118">После выбора значения страница откроется автоматически.</span><span class="sxs-lookup"><span data-stu-id="863b6-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="863b6-119">Выберите поток канбана SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="863b6-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="863b6-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="863b6-120">Click OK.</span></span>  
7. <span data-ttu-id="863b6-121">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="863b6-121">Expand the Details section.</span></span>
8. <span data-ttu-id="863b6-122">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="863b6-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="863b6-123">Выберите номенклатуру L0006.</span><span class="sxs-lookup"><span data-stu-id="863b6-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="863b6-124">Создание канбана и просмотр заданий</span><span class="sxs-lookup"><span data-stu-id="863b6-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="863b6-125">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="863b6-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="863b6-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="863b6-126">Click Add.</span></span>
3. <span data-ttu-id="863b6-127">В поле "Число новых канбанов" введите "1".</span><span class="sxs-lookup"><span data-stu-id="863b6-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="863b6-128">В результате будет создан один канбан.</span><span class="sxs-lookup"><span data-stu-id="863b6-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="863b6-129">Установите количество продукта равным 3.</span><span class="sxs-lookup"><span data-stu-id="863b6-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="863b6-130">Канбан будет обрабатывать 3 продукта.</span><span class="sxs-lookup"><span data-stu-id="863b6-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="863b6-131">В поле "Дата/время срока выполнения" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="863b6-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="863b6-132">Можно ввести значение "Сегодня".</span><span class="sxs-lookup"><span data-stu-id="863b6-132">You can enter Today.</span></span>  
6. <span data-ttu-id="863b6-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="863b6-133">Click Create.</span></span>
7. <span data-ttu-id="863b6-134">Нажмите кнопку Состав.</span><span class="sxs-lookup"><span data-stu-id="863b6-134">Click Details.</span></span>
    * <span data-ttu-id="863b6-135">Обратите внимание, что канбан имеет два задания процесса из производственного потока.</span><span class="sxs-lookup"><span data-stu-id="863b6-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="863b6-136">Первое задание — это SpeakerAssemblyAndPolish, второе — SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="863b6-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="863b6-137">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="863b6-137">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]