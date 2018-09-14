--- 
title: "Создание правила фиксированного канбана для производства"
description: "Эта процедура описывает настройку, необходимую для создания фиксированного производственного правила канбана для включения действий преобразования, в производственной ячейке, в экономичной среде."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9e0f58d1e265fb001474eb572b9bc325cf08790c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="a5d45-103">Создание правила фиксированного канбана для производства</span><span class="sxs-lookup"><span data-stu-id="a5d45-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5d45-104">Эта процедура описывает настройку, необходимую для создания фиксированного производственного правила канбана для включения действий преобразования, в производственной ячейке, в экономичной среде.</span><span class="sxs-lookup"><span data-stu-id="a5d45-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="a5d45-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a5d45-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a5d45-106">Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта.</span><span class="sxs-lookup"><span data-stu-id="a5d45-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="a5d45-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="a5d45-107">Create new kanban rule</span></span>
1. <span data-ttu-id="a5d45-108">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="a5d45-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="a5d45-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a5d45-109">Click New.</span></span>
    * <span data-ttu-id="a5d45-110">Обратите внимание, что типом по умолчанию является производство, а стратегией пополнения — "фиксировано".</span><span class="sxs-lookup"><span data-stu-id="a5d45-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="a5d45-111">Нет необходимости изменять эти параметры.</span><span class="sxs-lookup"><span data-stu-id="a5d45-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="a5d45-112">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a5d45-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="a5d45-113">Это действие, которое будет выполняться для канбанов, созданных на основе этого правила канбана.</span><span class="sxs-lookup"><span data-stu-id="a5d45-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="a5d45-114">Выберите "SpeakerTestAndPackaging".</span><span class="sxs-lookup"><span data-stu-id="a5d45-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="a5d45-115">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="a5d45-115">Expand the Details section.</span></span>
5. <span data-ttu-id="a5d45-116">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a5d45-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="a5d45-117">Выберите L0050.</span><span class="sxs-lookup"><span data-stu-id="a5d45-117">Select L0050.</span></span>  
6. <span data-ttu-id="a5d45-118">В поле "Единица измерения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a5d45-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="a5d45-119">Выберите минуты.</span><span class="sxs-lookup"><span data-stu-id="a5d45-119">Select minutes.</span></span>  
7. <span data-ttu-id="a5d45-120">В поле "Время упреждения" введите число.</span><span class="sxs-lookup"><span data-stu-id="a5d45-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="a5d45-121">Введите 5.</span><span class="sxs-lookup"><span data-stu-id="a5d45-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="a5d45-122">Указание количества</span><span class="sxs-lookup"><span data-stu-id="a5d45-122">Set quantities</span></span>
1. <span data-ttu-id="a5d45-123">Развернуть раздел "Количества".</span><span class="sxs-lookup"><span data-stu-id="a5d45-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="a5d45-124">Установите количество по умолчанию равным 10.</span><span class="sxs-lookup"><span data-stu-id="a5d45-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="a5d45-125">Это количество, которое будет передано для каждого канбана.</span><span class="sxs-lookup"><span data-stu-id="a5d45-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="a5d45-126">Установите флажок "Отклонение по количеству продукта".</span><span class="sxs-lookup"><span data-stu-id="a5d45-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="a5d45-127">При этом, выбранные канбаны можно выполнить с расхождением от количества по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5d45-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="a5d45-128">Чтобы разрешить выполнение канбанов с количеством от 8 до 12, установите оба отклонения как 2.</span><span class="sxs-lookup"><span data-stu-id="a5d45-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="a5d45-129">Задайте расхождение ниже "2".</span><span class="sxs-lookup"><span data-stu-id="a5d45-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="a5d45-130">Это позволит выполнить вниз до 10 – 2 = 8</span><span class="sxs-lookup"><span data-stu-id="a5d45-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="a5d45-131">Задайте расхождение выше "2".</span><span class="sxs-lookup"><span data-stu-id="a5d45-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="a5d45-132">Это позволит выполнить вверх до 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="a5d45-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="a5d45-133">В поле "Фиксированное количество канбанов" введите число.</span><span class="sxs-lookup"><span data-stu-id="a5d45-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="a5d45-134">Это сумма канбанов, которые должны быть активными.</span><span class="sxs-lookup"><span data-stu-id="a5d45-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="a5d45-135">В этом случае 5 канбанов обрабатывают 10 каждый.</span><span class="sxs-lookup"><span data-stu-id="a5d45-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="a5d45-136">В поле "Минимальная граница оповещения" введите "2".</span><span class="sxs-lookup"><span data-stu-id="a5d45-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="a5d45-137">Используется для того, чтобы отслеживать минимальную сумму полных канбанов, которые должны находиться в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="a5d45-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="a5d45-138">Например, это используется при обзоре количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a5d45-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="a5d45-139">В поле "Максимальная граница оповещения" введите "4".</span><span class="sxs-lookup"><span data-stu-id="a5d45-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="a5d45-140">Используется для того, чтобы отслеживать максимальную сумму полных канбанов, которые должны находиться в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="a5d45-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="a5d45-141">Например, это используется при обзоре количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a5d45-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="a5d45-142">В поле "Автоматическое планирование количества" введите "1".</span><span class="sxs-lookup"><span data-stu-id="a5d45-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="a5d45-143">Если задать 1, это означает, что каждый канбан будет автоматически запланирован.</span><span class="sxs-lookup"><span data-stu-id="a5d45-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="a5d45-144">Если ввести 3, канбаны не будут запланированы, пока 3 пустых канбана готовы для планирования.</span><span class="sxs-lookup"><span data-stu-id="a5d45-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="a5d45-145">Это полезно для группировки работ и упрощения настройки.</span><span class="sxs-lookup"><span data-stu-id="a5d45-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="a5d45-146">Создание канбанов</span><span class="sxs-lookup"><span data-stu-id="a5d45-146">Create Kanbans</span></span>
1. <span data-ttu-id="a5d45-147">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="a5d45-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="a5d45-148">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a5d45-148">Click Save.</span></span>
    * <span data-ttu-id="a5d45-149">Правило канбана должно быть сохранено, прежде чем канбаны можно создать.</span><span class="sxs-lookup"><span data-stu-id="a5d45-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="a5d45-150">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a5d45-150">Click Add.</span></span>
    * <span data-ttu-id="a5d45-151">Обратите внимание, что нет активных канбанов, поэтому для количества новых канбанов предлагается 5.</span><span class="sxs-lookup"><span data-stu-id="a5d45-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="a5d45-152">Это равно значению в поле "Фиксированное количество канбанов".</span><span class="sxs-lookup"><span data-stu-id="a5d45-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="a5d45-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a5d45-153">Click Create.</span></span>
    * <span data-ttu-id="a5d45-154">Это создаст 5 канбанов.</span><span class="sxs-lookup"><span data-stu-id="a5d45-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="a5d45-155">Обратите внимание, что 5 канбанов, по 10 каждый, были созданы для этого производственного правила канбана.</span><span class="sxs-lookup"><span data-stu-id="a5d45-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="a5d45-156">Это последний этап в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="a5d45-156">This is the last step in this procedure.</span></span>  


