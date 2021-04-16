---
title: Создание номенклатуры номера продукта для настроенных вариантов продукта
description: На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f342831d95f9988f9bb7807bac986e43cb317e0f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820017"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="b76ec-103">Создание номенклатуры номера продукта для настроенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="b76ec-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b76ec-104">На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="b76ec-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="b76ec-105">Эта процедура также демонстрирует, как можно создать конфигурацию номенклатуры для компонента модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="b76ec-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="b76ec-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b76ec-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b76ec-107">Новая номенклатура номера продукта назначена шаблону продукта D0004.</span><span class="sxs-lookup"><span data-stu-id="b76ec-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="b76ec-108">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="b76ec-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="b76ec-109">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="b76ec-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="b76ec-110">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="b76ec-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="b76ec-111">Щелкните "Номенклатура продуктов".</span><span class="sxs-lookup"><span data-stu-id="b76ec-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="b76ec-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b76ec-112">Click New.</span></span>
4. <span data-ttu-id="b76ec-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b76ec-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b76ec-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-115">Click Add.</span></span>
7. <span data-ttu-id="b76ec-116">Щелкните "Номер шаблона продукта".</span><span class="sxs-lookup"><span data-stu-id="b76ec-116">Click Product master number.</span></span>
8. <span data-ttu-id="b76ec-117">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-117">Click Add.</span></span>
9. <span data-ttu-id="b76ec-118">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="b76ec-118">Click Text constant.</span></span>
10. <span data-ttu-id="b76ec-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b76ec-120">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="b76ec-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-121">Click Add.</span></span>
13. <span data-ttu-id="b76ec-122">Щелкните "Конфигурация".</span><span class="sxs-lookup"><span data-stu-id="b76ec-122">Click Configuration.</span></span>
14. <span data-ttu-id="b76ec-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b76ec-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="b76ec-124">Назначение номенклатуры номеров продуктов шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="b76ec-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="b76ec-125">Щелкните "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="b76ec-125">Click Product masters.</span></span>
2. <span data-ttu-id="b76ec-126">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="b76ec-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b76ec-127">Например, отфильтруйте поле "Номер продукта" по значению "D".</span><span class="sxs-lookup"><span data-stu-id="b76ec-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="b76ec-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b76ec-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b76ec-129">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-129">Click Edit.</span></span>
5. <span data-ttu-id="b76ec-130">Выберите "Да" в поле "Использовать номенклатуру".</span><span class="sxs-lookup"><span data-stu-id="b76ec-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="b76ec-131">В поле "Номенклатура номеров вариантов продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="b76ec-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b76ec-132">Close the page.</span></span>
8. <span data-ttu-id="b76ec-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b76ec-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="b76ec-134">Создание номенклатуры для компонента модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="b76ec-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="b76ec-135">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="b76ec-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="b76ec-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b76ec-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b76ec-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b76ec-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b76ec-138">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-138">Click Edit.</span></span>
5. <span data-ttu-id="b76ec-139">Выберите "Да" в поле "Использовать номенклатуру конфигурации".</span><span class="sxs-lookup"><span data-stu-id="b76ec-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="b76ec-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-140">Click Add.</span></span>
7. <span data-ttu-id="b76ec-141">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="b76ec-141">Click Attribute value.</span></span>
8. <span data-ttu-id="b76ec-142">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b76ec-143">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="b76ec-144">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-144">Click Add.</span></span>
11. <span data-ttu-id="b76ec-145">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="b76ec-145">Click Text constant.</span></span>
12. <span data-ttu-id="b76ec-146">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b76ec-147">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="b76ec-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-148">Click Add.</span></span>
15. <span data-ttu-id="b76ec-149">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="b76ec-149">Click Attribute value.</span></span>
16. <span data-ttu-id="b76ec-150">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="b76ec-151">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="b76ec-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-152">Click Add.</span></span>
19. <span data-ttu-id="b76ec-153">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="b76ec-153">Click Text constant.</span></span>
20. <span data-ttu-id="b76ec-154">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="b76ec-155">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="b76ec-156">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-156">Click Add.</span></span>
23. <span data-ttu-id="b76ec-157">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="b76ec-157">Click Attribute value.</span></span>
24. <span data-ttu-id="b76ec-158">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="b76ec-159">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="b76ec-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-160">Click Add.</span></span>
27. <span data-ttu-id="b76ec-161">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="b76ec-161">Click Text constant.</span></span>
28. <span data-ttu-id="b76ec-162">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="b76ec-163">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="b76ec-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-164">Click Add.</span></span>
31. <span data-ttu-id="b76ec-165">Щелкните "Значение атрибута".</span><span class="sxs-lookup"><span data-stu-id="b76ec-165">Click Attribute value.</span></span>
32. <span data-ttu-id="b76ec-166">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="b76ec-167">В поле "Атрибут" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="b76ec-168">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-168">Click Add.</span></span>
35. <span data-ttu-id="b76ec-169">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="b76ec-169">Click Text constant.</span></span>
36. <span data-ttu-id="b76ec-170">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="b76ec-171">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="b76ec-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b76ec-172">Click Add.</span></span>
39. <span data-ttu-id="b76ec-173">Щелкните "Значение номерной серии".</span><span class="sxs-lookup"><span data-stu-id="b76ec-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="b76ec-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b76ec-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="b76ec-175">В поле "Номерная серия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b76ec-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="b76ec-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b76ec-176">Close the page.</span></span>
43. <span data-ttu-id="b76ec-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b76ec-177">Close the page.</span></span>
44. <span data-ttu-id="b76ec-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b76ec-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]