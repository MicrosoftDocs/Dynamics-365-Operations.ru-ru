---
title: Создание структур счетов
description: В этом руководства рассказывается о создании структуры счета.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571290"
---
# <a name="create-account-structures"></a><span data-ttu-id="f301b-103">Создание структур счетов</span><span class="sxs-lookup"><span data-stu-id="f301b-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f301b-104">В этом руководства рассказывается о создании структуры счета.</span><span class="sxs-lookup"><span data-stu-id="f301b-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="f301b-105">Для выполнения шагов используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="f301b-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="f301b-106">Перейдите в раздел "Главная книга" > "План счетов" > "Структуры" > "Настройка структур счета".</span><span class="sxs-lookup"><span data-stu-id="f301b-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="f301b-107">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f301b-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="f301b-108">В поле "Структура счета" введите имя для описания назначения структуры счета.</span><span class="sxs-lookup"><span data-stu-id="f301b-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="f301b-109">В поле "Описание" введите описание для указания назначения структуры счета.</span><span class="sxs-lookup"><span data-stu-id="f301b-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="f301b-110">Щелкните Создать.</span><span class="sxs-lookup"><span data-stu-id="f301b-110">Click Create.</span></span>
6. <span data-ttu-id="f301b-111">Нажмите "Добавить сегмент".</span><span class="sxs-lookup"><span data-stu-id="f301b-111">Click Add segment.</span></span>
7. <span data-ttu-id="f301b-112">В списке "Аналитики" выберите аналитику для добавления в структуру счета.</span><span class="sxs-lookup"><span data-stu-id="f301b-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="f301b-113">Нажмите "Добавить сегмент".</span><span class="sxs-lookup"><span data-stu-id="f301b-113">Click Add segment.</span></span>
9. <span data-ttu-id="f301b-114">Нажмите "Добавить сегмент".</span><span class="sxs-lookup"><span data-stu-id="f301b-114">Click Add segment.</span></span>
10. <span data-ttu-id="f301b-115">В списке "Аналитики" выберите аналитику для добавления в структуру счета.</span><span class="sxs-lookup"><span data-stu-id="f301b-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="f301b-116">Нажмите "Добавить сегмент".</span><span class="sxs-lookup"><span data-stu-id="f301b-116">Click Add segment.</span></span>
12. <span data-ttu-id="f301b-117">Нажмите "Добавить сегмент".</span><span class="sxs-lookup"><span data-stu-id="f301b-117">Click Add segment.</span></span>
13. <span data-ttu-id="f301b-118">В списке "Аналитики" выберите аналитику для добавления в структуру счета.</span><span class="sxs-lookup"><span data-stu-id="f301b-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="f301b-119">Нажмите "Добавить сегмент".</span><span class="sxs-lookup"><span data-stu-id="f301b-119">Click Add segment.</span></span>
15. <span data-ttu-id="f301b-120">В сетке выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="f301b-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f301b-121">Например, щелкните "Счет ГК".</span><span class="sxs-lookup"><span data-stu-id="f301b-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="f301b-122">В поле "Оператор" выберите параметр, например "находится в диапазоне и включает".</span><span class="sxs-lookup"><span data-stu-id="f301b-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="f301b-123">В поле "Значение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="f301b-124">Например, 600000.</span><span class="sxs-lookup"><span data-stu-id="f301b-124">For example, 600000.</span></span>  
18. <span data-ttu-id="f301b-125">В поле введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="f301b-126">Например, 699999.</span><span class="sxs-lookup"><span data-stu-id="f301b-126">For example, 699999.</span></span>  
19. <span data-ttu-id="f301b-127">Нажмите кнопку Применить.</span><span class="sxs-lookup"><span data-stu-id="f301b-127">Click Apply.</span></span>
20. <span data-ttu-id="f301b-128">В сетке выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="f301b-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f301b-129">Например, "Отдел".</span><span class="sxs-lookup"><span data-stu-id="f301b-129">For example, Department.</span></span>  
21. <span data-ttu-id="f301b-130">В поле "Оператор" выберите параметр, например "находится в диапазоне и включает".</span><span class="sxs-lookup"><span data-stu-id="f301b-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="f301b-131">В поле "Значение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="f301b-132">Например, 022.</span><span class="sxs-lookup"><span data-stu-id="f301b-132">For example, 022.</span></span>  
23. <span data-ttu-id="f301b-133">В поле введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="f301b-134">Например, 031.</span><span class="sxs-lookup"><span data-stu-id="f301b-134">For example, 031.</span></span>  
24. <span data-ttu-id="f301b-135">Щелкните "Добавить новые критерии".</span><span class="sxs-lookup"><span data-stu-id="f301b-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="f301b-136">В поле "Оператор" выберите параметр, например "находится в диапазоне и включает".</span><span class="sxs-lookup"><span data-stu-id="f301b-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="f301b-137">В поле "Значение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="f301b-138">Например, 033.</span><span class="sxs-lookup"><span data-stu-id="f301b-138">For example, 033.</span></span>  
27. <span data-ttu-id="f301b-139">В поле введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="f301b-140">Например, 034.</span><span class="sxs-lookup"><span data-stu-id="f301b-140">For example, 034.</span></span>  
28. <span data-ttu-id="f301b-141">Нажмите кнопку Применить.</span><span class="sxs-lookup"><span data-stu-id="f301b-141">Click Apply.</span></span>
29. <span data-ttu-id="f301b-142">В сетке выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="f301b-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f301b-143">Например, "Место возникновения затрат".</span><span class="sxs-lookup"><span data-stu-id="f301b-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="f301b-144">В поле CostCenter введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="f301b-145">Например, 007..021.</span><span class="sxs-lookup"><span data-stu-id="f301b-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="f301b-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f301b-146">Click Add.</span></span>
32. <span data-ttu-id="f301b-147">В поле MainAccount введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="f301b-148">Например, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="f301b-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="f301b-149">В сетке выберите сегмент для редактирования допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="f301b-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f301b-150">Например, "Отдел".</span><span class="sxs-lookup"><span data-stu-id="f301b-150">For example, Department.</span></span>  
34. <span data-ttu-id="f301b-151">В поле "Подразделение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="f301b-152">Например, 032.</span><span class="sxs-lookup"><span data-stu-id="f301b-152">For example, 032.</span></span>  
35. <span data-ttu-id="f301b-153">В поле CostCenter введите значение.</span><span class="sxs-lookup"><span data-stu-id="f301b-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="f301b-154">Например, 086.</span><span class="sxs-lookup"><span data-stu-id="f301b-154">For example, 086.</span></span>  
36. <span data-ttu-id="f301b-155">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="f301b-155">Click Validate.</span></span>
37. <span data-ttu-id="f301b-156">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="f301b-156">Click Activate.</span></span>
38. <span data-ttu-id="f301b-157">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="f301b-157">Click Activate.</span></span>

