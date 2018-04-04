---
title: "Распределение данных планирования бюджета"
description: "Эта статья описывает различные методы распределения, доступные в Microsoft Dynamics 365 for Finance and Operations, и порядок их возможного использования."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b5f262318b4defb941f1216d0bfe06961f62bad4
ms.contentlocale: ru-ru
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="a9aad-103">Распределение данных бюджетного планирования</span><span class="sxs-lookup"><span data-stu-id="a9aad-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a9aad-104">Эта статья описывает различные методы распределения, доступные в Microsoft Dynamics 365 for Finance and Operations, и порядок их возможного использования.</span><span class="sxs-lookup"><span data-stu-id="a9aad-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations and how they can be used.</span></span>  

<span data-ttu-id="a9aad-105">Вы можете распределить данные в плане бюджета несколькими способами, чтобы точно изобразить запроектированные количества.</span><span class="sxs-lookup"><span data-stu-id="a9aad-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="a9aad-106">Методы распределения</span><span class="sxs-lookup"><span data-stu-id="a9aad-106">Allocation methods</span></span>
<span data-ttu-id="a9aad-107">Три метода распределения (Распределять по нескольким периодам, Распределить по аналитикам и Использовать правила распределения ГК) могут создать строки бюджетного плана, которые основаны на строках в таком же бюджетном плане.</span><span class="sxs-lookup"><span data-stu-id="a9aad-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="a9aad-108">Три других метода (Агрегировано, Распределить, и Копировать из бюджетного плана) могут создать строки бюджетного плана в других бюджетных плана.</span><span class="sxs-lookup"><span data-stu-id="a9aad-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="a9aad-109">Для всех шести методов распределения вы определяете сценарий назначения.</span><span class="sxs-lookup"><span data-stu-id="a9aad-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="a9aad-110">Исходный и конечный сценарии могут различаться или представлять собой один и тот же сценарий.</span><span class="sxs-lookup"><span data-stu-id="a9aad-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="a9aad-111">Дополнительно, вы можете указать, добавляются ли новые строки к бюджетному плану или заменяют текущие строки в бюджетном плане.</span><span class="sxs-lookup"><span data-stu-id="a9aad-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="a9aad-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Распределять по нескольким периодам** — Категория распределения по периодам используется, чтобы распределить строки бюджетного плана из исходного сценария бюджетного плана по периодам конечного сценария.</span><span class="sxs-lookup"><span data-stu-id="a9aad-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="a9aad-113">Исходная сумма задана несколько линиям в сценарии назначения, основанном на проценте и дате, которые определены в категории распределения периода.</span><span class="sxs-lookup"><span data-stu-id="a9aad-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="a9aad-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Распределить по аналитикам** –Строки бюджетного плана распределяются из исходного сценария бюджетного планирования в одну или несколько строк конечного сценария, на основании процентов и финансовых аналитик, которые определены в выбранном условии распределения бюджета.</span><span class="sxs-lookup"><span data-stu-id="a9aad-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="a9aad-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Агрегировано** — строки бюджетного плана агрегируются из исходного сценария бюджетного плана в связанных (дочерних) бюджетных планах в конечный сценарий родительского бюджетного плана.</span><span class="sxs-lookup"><span data-stu-id="a9aad-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="a9aad-116">Этот метод включает суммы бюджета, которые подготовлены на нижнем уровне в организации и должны быть консолидированными на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="a9aad-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="a9aad-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Распределение** – Строки бюджетного плана распределяются из исходного сценария бюджетного планирования в родительском бюджетном плане в сценарии назначения в связанных (дочерних) бюджетных планах, на основании финансовых аналитик в организационных подразделениях соответствующих планов.</span><span class="sxs-lookup"><span data-stu-id="a9aad-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="a9aad-118">Этот метод включает суммы бюджета, которые подготовлены на нижнем уровне в организации и должны быть распределены для более локализованного рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="a9aad-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="a9aad-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Использовать правила распределения ГК** — Строки бюджетного плана распределяются из исходного сценария бюджетного плана в конечный сценарий бюджетного планирования согласно выбранному правилу распределения главной книги.</span><span class="sxs-lookup"><span data-stu-id="a9aad-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="a9aad-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Копировать из бюджетного плана** – Как в методе распределить распределение, строки бюджетного плана создаются в назначении на основе строк в связанном бюджетном плане.</span><span class="sxs-lookup"><span data-stu-id="a9aad-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="a9aad-121">Однако для этого метода, исходный план бюджета не должен быть родителем, но может находиться на любом более высоком уровне в иерархии плана бюджета.</span><span class="sxs-lookup"><span data-stu-id="a9aad-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="a9aad-122">Этот метод распределения полезен, если консолидированные суммы первоначально бюджетированы на гораздо более высоком уровне, и должны быть перенесены на более низкий уровень организации для подробного обзора и корректировки, прежде чем они могут получить утверждение верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="a9aad-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="a9aad-123">Использование методов распределения в плане бюджета</span><span class="sxs-lookup"><span data-stu-id="a9aad-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="a9aad-124">Чтобы выполнить распределения на странице плана бюджета, выберите строки для распределения и после этого щелкните **Распределить бюджет**.</span><span class="sxs-lookup"><span data-stu-id="a9aad-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="a9aad-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="a9aad-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="a9aad-126">Затем выберите метод распределения.</span><span class="sxs-lookup"><span data-stu-id="a9aad-126">Next, select an allocation method.</span></span> <span data-ttu-id="a9aad-127">Остальные поля после этого устанавливаются, на основе выбранного способа.</span><span class="sxs-lookup"><span data-stu-id="a9aad-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="a9aad-128">Эти поля включают источник и назначение данных плана бюджета, и вариант, который позволяет вам умножить источник на определенный Коэффициент, когда создаются суммы назначения, чтобы упростить массовую корректировку.</span><span class="sxs-lookup"><span data-stu-id="a9aad-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="a9aad-129">Вы можете также установить параметр **Присоединить к плану**.</span><span class="sxs-lookup"><span data-stu-id="a9aad-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="a9aad-130">Выберите **Нет**, чтобы заменить существующие строки плана бюджета, или выберите **Да** для того, чтобы сохранить существующие строки плана бюджета и добавить новые строки для распределенных сумм.</span><span class="sxs-lookup"><span data-stu-id="a9aad-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="a9aad-131">Автоматизация распределений во время workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="a9aad-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="a9aad-132">Одна мощная функция позволяет распределению быть выполненным автоматически как часть workflow-процесса планирования бюджета.</span><span class="sxs-lookup"><span data-stu-id="a9aad-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="a9aad-133">По мере того как план бюджета двигается через свой workflow-процесс, автоматизированные задачи могут вызывать распределение на определенной стадии планирования бюджета.</span><span class="sxs-lookup"><span data-stu-id="a9aad-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="a9aad-134">Для того, чтобы настроить автоматизированное распределение, вам сперва создать необходимо график распределения на странице **Конфигурация бюджетного планирования**.</span><span class="sxs-lookup"><span data-stu-id="a9aad-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="a9aad-135">График распределения определяет метод распределения, который будет использован, когда автоматизированное распределение выполняется, и значения различных вариантов распределения (см. описания в предыдущем разделе).</span><span class="sxs-lookup"><span data-stu-id="a9aad-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="a9aad-136">Затем, вы создаете распределение стадии на странице **Конфигурация бюджетного планирования**.</span><span class="sxs-lookup"><span data-stu-id="a9aad-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="a9aad-137">Распределение стадий назначает график распределения к workflow-процессу и стадии бюджетного планирования.</span><span class="sxs-lookup"><span data-stu-id="a9aad-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="a9aad-138">В конце концов, добавьте автоматизированную задачу для распределения стадии планирования бюджета на желаемой стадии workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a9aad-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="a9aad-139">В следующем примере, два распределения стадии планирования бюджета (отмечены красным) были вставлены в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="a9aad-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="a9aad-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="a9aad-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




