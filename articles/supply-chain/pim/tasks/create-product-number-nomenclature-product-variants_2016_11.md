---
title: Создание номенклатуры номера продукта для настроенных вариантов продукта
description: На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e52b7a5aff3e86e845484e1e84b4003cc4a52c95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992378"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="37378-103">Создание номенклатуры номера продукта для настроенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="37378-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37378-104">На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="37378-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="37378-105">Эта процедура также демонстрирует, как можно создать конфигурацию номенклатуры для компонента модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="37378-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="37378-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="37378-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37378-107">Новая номенклатура номера продукта назначена шаблону продукта D0004.</span><span class="sxs-lookup"><span data-stu-id="37378-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="37378-108">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="37378-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="37378-109">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="37378-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="37378-110">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="37378-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="37378-111">Щелкните "Номенклатура продуктов".</span><span class="sxs-lookup"><span data-stu-id="37378-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="37378-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="37378-112">Click New.</span></span>
4. <span data-ttu-id="37378-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="37378-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="37378-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-115">Click Add.</span></span>
7. <span data-ttu-id="37378-116">Щелкните "Номер шаблона продукта".</span><span class="sxs-lookup"><span data-stu-id="37378-116">Click Product master number.</span></span>
8. <span data-ttu-id="37378-117">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-117">Click Add.</span></span>
9. <span data-ttu-id="37378-118">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="37378-118">Click Text constant.</span></span>
10. <span data-ttu-id="37378-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="37378-120">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="37378-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-121">Click Add.</span></span>
13. <span data-ttu-id="37378-122">Щелкните "Конфигурация".</span><span class="sxs-lookup"><span data-stu-id="37378-122">Click Configuration.</span></span>
14. <span data-ttu-id="37378-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37378-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="37378-124">Назначение номенклатуры номеров продуктов шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="37378-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="37378-125">Щелкните "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="37378-125">Click Product masters.</span></span>
2. <span data-ttu-id="37378-126">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="37378-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="37378-127">Например, отфильтруйте поле "Номер продукта" по значению "D".</span><span class="sxs-lookup"><span data-stu-id="37378-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="37378-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="37378-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="37378-129">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="37378-129">Click Edit.</span></span>
5. <span data-ttu-id="37378-130">Выберите "Да" в поле "Использовать номенклатуру".</span><span class="sxs-lookup"><span data-stu-id="37378-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="37378-131">В поле "Номенклатура номеров вариантов продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="37378-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37378-132">Close the page.</span></span>
8. <span data-ttu-id="37378-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37378-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="37378-134">Создание номенклатуры для компонента модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="37378-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="37378-135">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="37378-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="37378-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="37378-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37378-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="37378-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="37378-138">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="37378-138">Click Edit.</span></span>
5. <span data-ttu-id="37378-139">Выберите "Да" в поле "Использовать номенклатуру конфигурации".</span><span class="sxs-lookup"><span data-stu-id="37378-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="37378-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-140">Click Add.</span></span>
7. <span data-ttu-id="37378-141">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="37378-141">Click Attribute value.</span></span>
8. <span data-ttu-id="37378-142">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="37378-143">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="37378-144">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-144">Click Add.</span></span>
11. <span data-ttu-id="37378-145">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="37378-145">Click Text constant.</span></span>
12. <span data-ttu-id="37378-146">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="37378-147">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="37378-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-148">Click Add.</span></span>
15. <span data-ttu-id="37378-149">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="37378-149">Click Attribute value.</span></span>
16. <span data-ttu-id="37378-150">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="37378-151">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="37378-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-152">Click Add.</span></span>
19. <span data-ttu-id="37378-153">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="37378-153">Click Text constant.</span></span>
20. <span data-ttu-id="37378-154">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="37378-155">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="37378-156">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-156">Click Add.</span></span>
23. <span data-ttu-id="37378-157">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="37378-157">Click Attribute value.</span></span>
24. <span data-ttu-id="37378-158">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="37378-159">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="37378-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-160">Click Add.</span></span>
27. <span data-ttu-id="37378-161">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="37378-161">Click Text constant.</span></span>
28. <span data-ttu-id="37378-162">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="37378-163">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="37378-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-164">Click Add.</span></span>
31. <span data-ttu-id="37378-165">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="37378-165">Click Attribute value.</span></span>
32. <span data-ttu-id="37378-166">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="37378-167">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="37378-168">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-168">Click Add.</span></span>
35. <span data-ttu-id="37378-169">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="37378-169">Click Text constant.</span></span>
36. <span data-ttu-id="37378-170">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="37378-171">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="37378-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="37378-172">Click Add.</span></span>
39. <span data-ttu-id="37378-173">Щелкните "Значение номерной серии".</span><span class="sxs-lookup"><span data-stu-id="37378-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="37378-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="37378-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="37378-175">В поле "Номерная серия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37378-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="37378-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37378-176">Close the page.</span></span>
43. <span data-ttu-id="37378-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37378-177">Close the page.</span></span>
44. <span data-ttu-id="37378-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37378-178">Close the page.</span></span>

