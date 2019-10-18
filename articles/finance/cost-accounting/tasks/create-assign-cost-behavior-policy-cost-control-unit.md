---
title: Создание и назначение политик поведения затрат единицам управления затратами
description: Поведение затрат представляет собой отнесение затрат к постоянным или переменным.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187828"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="2cd38-103">Создание и назначение политик поведения затрат единицам управления затратами</span><span class="sxs-lookup"><span data-stu-id="2cd38-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cd38-104">Поведение затрат представляет собой отнесение затрат к постоянным или переменным.</span><span class="sxs-lookup"><span data-stu-id="2cd38-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="2cd38-105">Для вступления политики в силу политика и соответствующие правила должны быть назначены единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="2cd38-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="2cd38-106">Эта процедура используется для создания политики и ее назначения единице управления затратами.</span><span class="sxs-lookup"><span data-stu-id="2cd38-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="2cd38-107">Создание иерархии поведения затрат</span><span class="sxs-lookup"><span data-stu-id="2cd38-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="2cd38-108">Перейдите в раздел "Учет затрат" > "Аналитики" > "Иерархии аналитик".</span><span class="sxs-lookup"><span data-stu-id="2cd38-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="2cd38-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-109">Click New.</span></span>
3. <span data-ttu-id="2cd38-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-110">Click Create.</span></span>
4. <span data-ttu-id="2cd38-111">В поле "Имя иерархии аналитик" введите "Иерархия поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="2cd38-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="2cd38-112">В поле "Аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-113">Выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="2cd38-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="2cd38-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2cd38-114">Click Save.</span></span>
7. <span data-ttu-id="2cd38-115">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="2cd38-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="2cd38-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-116">Click New.</span></span>
9. <span data-ttu-id="2cd38-117">В поле "Имя узла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="2cd38-118">Введите "Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="2cd38-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="2cd38-119">В дереве выберите "Иерархия поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="2cd38-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="2cd38-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-120">Click New.</span></span>
12. <span data-ttu-id="2cd38-121">В поле "Имя узла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="2cd38-122">Введите "Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="2cd38-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="2cd38-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2cd38-123">Click Save.</span></span>
14. <span data-ttu-id="2cd38-124">В дереве выберите "Иерархия поведения затрат\Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="2cd38-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="2cd38-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-125">Click New.</span></span>
16. <span data-ttu-id="2cd38-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2cd38-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="2cd38-127">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-128">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="2cd38-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="2cd38-129">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-130">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="2cd38-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="2cd38-131">В дереве выберите "Иерархия поведения затрат\Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="2cd38-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="2cd38-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-132">Click New.</span></span>
21. <span data-ttu-id="2cd38-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2cd38-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="2cd38-134">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-135">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="2cd38-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="2cd38-136">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-137">Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="2cd38-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="2cd38-138">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2cd38-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="2cd38-139">Создание политики и правил</span><span class="sxs-lookup"><span data-stu-id="2cd38-139">Create the policy and rules</span></span>
1. <span data-ttu-id="2cd38-140">Перейдите в раздел "Учет затрат" > "Политики" > "Политики поведения затрат".</span><span class="sxs-lookup"><span data-stu-id="2cd38-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="2cd38-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-141">Click New.</span></span>
3. <span data-ttu-id="2cd38-142">В поле "Имя политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="2cd38-143">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-144">Выберите только что созданную иерархию политик.</span><span class="sxs-lookup"><span data-stu-id="2cd38-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="2cd38-145">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-146">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="2cd38-146">Select Organization.</span></span>  
6. <span data-ttu-id="2cd38-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2cd38-147">Click Save.</span></span>
7. <span data-ttu-id="2cd38-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-148">Click New.</span></span>
8. <span data-ttu-id="2cd38-149">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2cd38-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="2cd38-150">В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-151">Разверните иерархию, чтобы выбрать "Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="2cd38-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="2cd38-152">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2cd38-153">По умолчанию процент переменной части равен 100%.</span><span class="sxs-lookup"><span data-stu-id="2cd38-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="2cd38-154">Щелкните "Назначения политики для единицы управления затратами".</span><span class="sxs-lookup"><span data-stu-id="2cd38-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="2cd38-155">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2cd38-155">Click New.</span></span>
13. <span data-ttu-id="2cd38-156">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2cd38-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2cd38-157">В поле "Действительно с даты учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="2cd38-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="2cd38-158">Правила вступают в силу по дате, и пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.</span><span class="sxs-lookup"><span data-stu-id="2cd38-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="2cd38-159">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2cd38-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="2cd38-160">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2cd38-160">Click Save.</span></span>

