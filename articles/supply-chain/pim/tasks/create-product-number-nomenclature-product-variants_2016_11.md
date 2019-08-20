---
title: Создание номенклатуры номера продукта для настроенных вариантов продукта
description: На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22aa4823fbf43b29a8fd9661645e8563c07e437d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844665"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="299ef-103">Создание номенклатуры номера продукта для настроенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="299ef-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="299ef-104">На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="299ef-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="299ef-105">Эта процедура также демонстрирует, как можно создать конфигурацию номенклатуры для компонента модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="299ef-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="299ef-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="299ef-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="299ef-107">Новая номенклатура номера продукта назначена шаблону продукта D0004.</span><span class="sxs-lookup"><span data-stu-id="299ef-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="299ef-108">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="299ef-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="299ef-109">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="299ef-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="299ef-110">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="299ef-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="299ef-111">Щелкните "Номенклатура продуктов".</span><span class="sxs-lookup"><span data-stu-id="299ef-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="299ef-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="299ef-112">Click New.</span></span>
4. <span data-ttu-id="299ef-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="299ef-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="299ef-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-115">Click Add.</span></span>
7. <span data-ttu-id="299ef-116">Щелкните "Номер шаблона продукта".</span><span class="sxs-lookup"><span data-stu-id="299ef-116">Click Product master number.</span></span>
8. <span data-ttu-id="299ef-117">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-117">Click Add.</span></span>
9. <span data-ttu-id="299ef-118">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="299ef-118">Click Text constant.</span></span>
10. <span data-ttu-id="299ef-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="299ef-120">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="299ef-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-121">Click Add.</span></span>
13. <span data-ttu-id="299ef-122">Щелкните "Конфигурация".</span><span class="sxs-lookup"><span data-stu-id="299ef-122">Click Configuration.</span></span>
14. <span data-ttu-id="299ef-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="299ef-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="299ef-124">Назначение номенклатуры номеров продуктов шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="299ef-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="299ef-125">Щелкните "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="299ef-125">Click Product masters.</span></span>
2. <span data-ttu-id="299ef-126">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="299ef-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="299ef-127">Например, отфильтруйте поле "Номер продукта" по значению "D".</span><span class="sxs-lookup"><span data-stu-id="299ef-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="299ef-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="299ef-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="299ef-129">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="299ef-129">Click Edit.</span></span>
5. <span data-ttu-id="299ef-130">Выберите "Да" в поле "Использовать номенклатуру".</span><span class="sxs-lookup"><span data-stu-id="299ef-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="299ef-131">В поле "Номенклатура номеров вариантов продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="299ef-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="299ef-132">Close the page.</span></span>
8. <span data-ttu-id="299ef-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="299ef-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="299ef-134">Создание номенклатуры для компонента модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="299ef-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="299ef-135">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="299ef-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="299ef-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="299ef-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="299ef-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="299ef-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="299ef-138">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="299ef-138">Click Edit.</span></span>
5. <span data-ttu-id="299ef-139">Выберите "Да" в поле "Использовать номенклатуру конфигурации".</span><span class="sxs-lookup"><span data-stu-id="299ef-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="299ef-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-140">Click Add.</span></span>
7. <span data-ttu-id="299ef-141">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="299ef-141">Click Attribute value.</span></span>
8. <span data-ttu-id="299ef-142">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="299ef-143">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="299ef-144">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-144">Click Add.</span></span>
11. <span data-ttu-id="299ef-145">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="299ef-145">Click Text constant.</span></span>
12. <span data-ttu-id="299ef-146">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="299ef-147">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="299ef-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-148">Click Add.</span></span>
15. <span data-ttu-id="299ef-149">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="299ef-149">Click Attribute value.</span></span>
16. <span data-ttu-id="299ef-150">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="299ef-151">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="299ef-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-152">Click Add.</span></span>
19. <span data-ttu-id="299ef-153">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="299ef-153">Click Text constant.</span></span>
20. <span data-ttu-id="299ef-154">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="299ef-155">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="299ef-156">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-156">Click Add.</span></span>
23. <span data-ttu-id="299ef-157">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="299ef-157">Click Attribute value.</span></span>
24. <span data-ttu-id="299ef-158">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="299ef-159">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="299ef-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-160">Click Add.</span></span>
27. <span data-ttu-id="299ef-161">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="299ef-161">Click Text constant.</span></span>
28. <span data-ttu-id="299ef-162">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="299ef-163">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="299ef-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-164">Click Add.</span></span>
31. <span data-ttu-id="299ef-165">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="299ef-165">Click Attribute value.</span></span>
32. <span data-ttu-id="299ef-166">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="299ef-167">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="299ef-168">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-168">Click Add.</span></span>
35. <span data-ttu-id="299ef-169">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="299ef-169">Click Text constant.</span></span>
36. <span data-ttu-id="299ef-170">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="299ef-171">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="299ef-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="299ef-172">Click Add.</span></span>
39. <span data-ttu-id="299ef-173">Щелкните "Значение номерной серии".</span><span class="sxs-lookup"><span data-stu-id="299ef-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="299ef-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="299ef-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="299ef-175">В поле "Номерная серия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="299ef-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="299ef-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="299ef-176">Close the page.</span></span>
43. <span data-ttu-id="299ef-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="299ef-177">Close the page.</span></span>
44. <span data-ttu-id="299ef-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="299ef-178">Close the page.</span></span>

