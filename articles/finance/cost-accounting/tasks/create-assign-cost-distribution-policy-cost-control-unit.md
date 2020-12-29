---
title: Создание и назначение политик отнесения затрат по единицам управления затратами
description: Правила распределения затрат используются для распределения затрат, которые были финансово подсчитаны в общем центре затрат.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66921d5eddb31ffba0946c41f634719a684e4ad1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447133"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="57887-103">Создание и назначение политик отнесения затрат по единицам управления затратами</span><span class="sxs-lookup"><span data-stu-id="57887-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57887-104">Правила распределения затрат используются для распределения затрат, которые были финансово подсчитаны в общем центре затрат.</span><span class="sxs-lookup"><span data-stu-id="57887-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="57887-105">Бухгалтер по учету затрат следит за тем, чтобы затраты были распределены по центрам затрат на основе выбранной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="57887-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="57887-106">Политика и соответствующие правила назначаются единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="57887-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="57887-107">В этом проводнике по задаче используется пример для демонстрации порядка создания политики распределения затрат и соответствующих правил.</span><span class="sxs-lookup"><span data-stu-id="57887-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="57887-108">Создание политики</span><span class="sxs-lookup"><span data-stu-id="57887-108">Create a policy</span></span>
1. <span data-ttu-id="57887-109">Перейдите в раздел "Учет затрат" > "Политики" > "Политики распределения затрат".</span><span class="sxs-lookup"><span data-stu-id="57887-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="57887-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57887-110">Click New.</span></span>
3. <span data-ttu-id="57887-111">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="57887-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="57887-113">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-114">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="57887-114">Select Organization.</span></span>  
6. <span data-ttu-id="57887-115">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-116">Выберите "CDS P/L".</span><span class="sxs-lookup"><span data-stu-id="57887-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="57887-117">В поле "Статистическая аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-118">Выберите "Статистические элементы".</span><span class="sxs-lookup"><span data-stu-id="57887-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="57887-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57887-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="57887-120">Создание правил для политики</span><span class="sxs-lookup"><span data-stu-id="57887-120">Create rules for the policy</span></span>
1. <span data-ttu-id="57887-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57887-121">Click New.</span></span>
2. <span data-ttu-id="57887-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="57887-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="57887-123">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-124">Разверните иерархию, чтобы выбрать "094".</span><span class="sxs-lookup"><span data-stu-id="57887-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="57887-125">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-126">Выберите "Другие операционные расходы", а затем выберите 605110, "Уборка".</span><span class="sxs-lookup"><span data-stu-id="57887-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="57887-127">В поле "Поведение затрат" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="57887-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="57887-128">Выберите "Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="57887-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="57887-129">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="57887-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57887-130">Click New.</span></span>
8. <span data-ttu-id="57887-131">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="57887-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="57887-132">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-133">Разверните иерархию, чтобы выбрать "094".</span><span class="sxs-lookup"><span data-stu-id="57887-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="57887-134">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="57887-135">Выберите "Другие операционные расходы", а затем выберите 605150, "Аренда".</span><span class="sxs-lookup"><span data-stu-id="57887-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="57887-136">В поле "Поведение затрат" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="57887-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="57887-137">Выберите "Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="57887-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="57887-138">В поле "База распределения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="57887-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57887-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="57887-140">Назначение правил единице управления затратами</span><span class="sxs-lookup"><span data-stu-id="57887-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="57887-141">Щелкните "Назначения политики для единицы управления затратами".</span><span class="sxs-lookup"><span data-stu-id="57887-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="57887-142">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57887-142">Click New.</span></span>
3. <span data-ttu-id="57887-143">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="57887-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="57887-144">В поле "Действительно с даты учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="57887-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="57887-145">В качестве действующего финансового года выберите 1 сентября.</span><span class="sxs-lookup"><span data-stu-id="57887-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="57887-146">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57887-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="57887-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57887-147">Click Save.</span></span>

