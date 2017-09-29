--- 
title: "Создание и назначение политик поведения затрат единицам управления затратами"
description: "Поведение затрат представляет собой отнесение затрат к постоянным или переменным."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 392cb83ceb8612a2e73cc54bb2d8d40c62a6b7b6
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="a3cb9-103">Создание и назначение политик поведения затрат единицам управления затратами</span><span class="sxs-lookup"><span data-stu-id="a3cb9-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3cb9-104">Поведение затрат представляет собой отнесение затрат к постоянным или переменным.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="a3cb9-105">Для вступления политики в силу политика и соответствующие правила должны быть назначены единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="a3cb9-106">Эта процедура используется для создания политики и ее назначения единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="a3cb9-107">Создание иерархии поведения затрат</span><span class="sxs-lookup"><span data-stu-id="a3cb9-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="a3cb9-108">Перейдите в раздел "Учет затрат" > "Аналитики" > "Иерархии аналитик".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="a3cb9-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-109">Click New.</span></span>
3. <span data-ttu-id="a3cb9-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-110">Click Create.</span></span>
4. <span data-ttu-id="a3cb9-111">В поле "Имя иерархии аналитик" введите "Иерархия поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="a3cb9-112">В поле "Аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-113">Выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="a3cb9-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-114">Click Save.</span></span>
7. <span data-ttu-id="a3cb9-115">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="a3cb9-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-116">Click New.</span></span>
9. <span data-ttu-id="a3cb9-117">В поле "Имя узла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="a3cb9-118">Введите "Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="a3cb9-119">В дереве выберите "Иерархия поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="a3cb9-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-120">Click New.</span></span>
12. <span data-ttu-id="a3cb9-121">В поле "Имя узла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="a3cb9-122">Введите "Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="a3cb9-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-123">Click Save.</span></span>
14. <span data-ttu-id="a3cb9-124">В дереве выберите "Иерархия поведения затрат\Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="a3cb9-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-125">Click New.</span></span>
16. <span data-ttu-id="a3cb9-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="a3cb9-127">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-128">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="a3cb9-129">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-130">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="a3cb9-131">В дереве выберите "Иерархия поведения затрат\Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="a3cb9-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-132">Click New.</span></span>
21. <span data-ttu-id="a3cb9-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="a3cb9-134">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-135">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="a3cb9-136">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-137">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="a3cb9-138">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="a3cb9-139">Создание политики и правил</span><span class="sxs-lookup"><span data-stu-id="a3cb9-139">Create the policy and rules</span></span>
1. <span data-ttu-id="a3cb9-140">Перейдите в раздел "Учет затрат" > "Политики" > "Политики поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="a3cb9-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-141">Click New.</span></span>
3. <span data-ttu-id="a3cb9-142">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="a3cb9-143">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-144">Выберите только что созданную иерархию политик.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="a3cb9-145">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-146">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-146">Select Organization.</span></span>  
6. <span data-ttu-id="a3cb9-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-147">Click Save.</span></span>
7. <span data-ttu-id="a3cb9-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-148">Click New.</span></span>
8. <span data-ttu-id="a3cb9-149">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a3cb9-150">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-151">Разверните иерархию, чтобы выбрать "Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="a3cb9-152">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a3cb9-153">По умолчанию процент переменной части равен 100%.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="a3cb9-154">Щелкните "Назначения политики для единицы управления затратами".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="a3cb9-155">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-155">Click New.</span></span>
13. <span data-ttu-id="a3cb9-156">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a3cb9-157">В поле "Действительно с даты учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="a3cb9-158">Правила вступают в силу по дате, и пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="a3cb9-159">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a3cb9-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="a3cb9-160">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3cb9-160">Click Save.</span></span>


