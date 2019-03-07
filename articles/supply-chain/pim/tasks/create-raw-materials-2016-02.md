---
title: Создание сырья (февраль 2016 г.)
description: Эта задача рассматривает создание компонентов готовой продукции и полуфабрикатов.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "351064"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="b6b0b-103">Создание сырья (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="b6b0b-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6b0b-104">Эта задача рассматривает создание компонентов готовой продукции и полуфабрикатов.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="b6b0b-105">Это третья задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="b6b0b-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="b6b0b-107">Создание первого материала</span><span class="sxs-lookup"><span data-stu-id="b6b0b-107">Create the first material</span></span>
1. <span data-ttu-id="b6b0b-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b6b0b-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-109">Click New.</span></span>
3. <span data-ttu-id="b6b0b-110">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="b6b0b-111">В этом примере введите "ITEM_A".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="b6b0b-112">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-113">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-113">Select STD.</span></span> <span data-ttu-id="b6b0b-114">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="b6b0b-115">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-116">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-116">For example, select Audio.</span></span> <span data-ttu-id="b6b0b-117">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="b6b0b-118">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-119">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-119">Select SiteWH.</span></span> <span data-ttu-id="b6b0b-120">Только сайт и склад будут использоваться для демонстрации.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="b6b0b-121">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-122">Аналитики отслеживания не будут использоваться для данного примера.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="b6b0b-123">Выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-123">Select None.</span></span>  
8. <span data-ttu-id="b6b0b-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-124">Click OK.</span></span>
9. <span data-ttu-id="b6b0b-125">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="b6b0b-126">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-126">Click Default order settings.</span></span>
11. <span data-ttu-id="b6b0b-127">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-128">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="b6b0b-129">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-130">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="b6b0b-131">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-132">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="b6b0b-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-133">Close the page.</span></span>
15. <span data-ttu-id="b6b0b-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-134">Close the page.</span></span>
16. <span data-ttu-id="b6b0b-135">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6b0b-136">Щелкните ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="b6b0b-137">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="b6b0b-138">В поле "Группа затрат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="b6b0b-139">В этом примере введите "M2".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="b6b0b-140">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="b6b0b-141">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-141">Click Item price.</span></span>
21. <span data-ttu-id="b6b0b-142">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-142">Click New.</span></span>
22. <span data-ttu-id="b6b0b-143">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-144">В этом примере выберите 10 — тип цены стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="b6b0b-145">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-146">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="b6b0b-147">В поле "Цена" введите число.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b6b0b-148">В этом примере введите "10".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="b6b0b-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-149">Click Save.</span></span>
26. <span data-ttu-id="b6b0b-150">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="b6b0b-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-151">Close the page.</span></span>
28. <span data-ttu-id="b6b0b-152">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="b6b0b-153">Создание второго материала</span><span class="sxs-lookup"><span data-stu-id="b6b0b-153">Create the second material</span></span>
1. <span data-ttu-id="b6b0b-154">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-154">Click New.</span></span>
2. <span data-ttu-id="b6b0b-155">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="b6b0b-156">В этом примере введите "ITEM_B".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="b6b0b-157">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-158">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-158">Select STD.</span></span> <span data-ttu-id="b6b0b-159">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="b6b0b-160">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-161">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-161">For example, select Audio.</span></span> <span data-ttu-id="b6b0b-162">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="b6b0b-163">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-164">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-164">Select SiteWH.</span></span> <span data-ttu-id="b6b0b-165">Только сайт и склад будут использоваться в этом примере.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="b6b0b-166">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-167">Аналитики отслеживания не будут использоваться для данного примера.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="b6b0b-168">Выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-168">Select None.</span></span>  
7. <span data-ttu-id="b6b0b-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-169">Click OK.</span></span>
8. <span data-ttu-id="b6b0b-170">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="b6b0b-171">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-171">Click Default order settings.</span></span>
10. <span data-ttu-id="b6b0b-172">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-173">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="b6b0b-174">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-175">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="b6b0b-176">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-177">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="b6b0b-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-178">Close the page.</span></span>
14. <span data-ttu-id="b6b0b-179">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-179">Close the page.</span></span>
15. <span data-ttu-id="b6b0b-180">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6b0b-181">Щелкните ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="b6b0b-182">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="b6b0b-183">В поле "Группа затрат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="b6b0b-184">В этом примере введите "M2".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="b6b0b-185">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="b6b0b-186">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-186">Click Item price.</span></span>
20. <span data-ttu-id="b6b0b-187">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-187">Click New.</span></span>
21. <span data-ttu-id="b6b0b-188">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-189">В этом примере выберите "10".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-189">For this example, select 10.</span></span> <span data-ttu-id="b6b0b-190">Это тип цены стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="b6b0b-191">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-192">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="b6b0b-193">В поле "Цена" введите число.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b6b0b-194">В целя демонстрации введите 10.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="b6b0b-195">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-195">Click Save.</span></span>
25. <span data-ttu-id="b6b0b-196">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="b6b0b-197">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-197">Close the page.</span></span>
27. <span data-ttu-id="b6b0b-198">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="b6b0b-199">Создание третьего материала</span><span class="sxs-lookup"><span data-stu-id="b6b0b-199">Create the third material</span></span>
1. <span data-ttu-id="b6b0b-200">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-200">Click New.</span></span>
2. <span data-ttu-id="b6b0b-201">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="b6b0b-202">В целя демонстрации введите ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="b6b0b-203">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-204">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-204">Select STD.</span></span> <span data-ttu-id="b6b0b-205">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="b6b0b-206">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-207">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-207">For example, select Audio.</span></span> <span data-ttu-id="b6b0b-208">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="b6b0b-209">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-210">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-210">Select SiteWH.</span></span> <span data-ttu-id="b6b0b-211">Только сайт и склад будут использоваться для демонстрации.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="b6b0b-212">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-213">Аналитики отслеживания не будут использоваться для данного примера.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="b6b0b-214">Выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-214">Select None.</span></span>  
7. <span data-ttu-id="b6b0b-215">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-215">Click OK.</span></span>
8. <span data-ttu-id="b6b0b-216">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="b6b0b-217">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-217">Click Default order settings.</span></span>
10. <span data-ttu-id="b6b0b-218">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-219">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="b6b0b-220">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-221">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="b6b0b-222">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-223">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="b6b0b-224">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-224">Close the page.</span></span>
14. <span data-ttu-id="b6b0b-225">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-225">Close the page.</span></span>
15. <span data-ttu-id="b6b0b-226">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6b0b-227">Щелкните ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="b6b0b-228">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="b6b0b-229">В поле "Группа затрат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="b6b0b-230">В этом примере введите "M1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="b6b0b-231">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="b6b0b-232">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-232">Click Item price.</span></span>
20. <span data-ttu-id="b6b0b-233">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-233">Click New.</span></span>
21. <span data-ttu-id="b6b0b-234">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-235">В этом примере выберите "10".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-235">For this example, select 10.</span></span> <span data-ttu-id="b6b0b-236">Это тип цены стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="b6b0b-237">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b6b0b-238">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="b6b0b-239">В поле "Цена" введите число.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b6b0b-240">В этом примере введите "10".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="b6b0b-241">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-241">Click Save.</span></span>
25. <span data-ttu-id="b6b0b-242">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="b6b0b-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="b6b0b-243">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-243">Close the page.</span></span>
27. <span data-ttu-id="b6b0b-244">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b6b0b-244">Close the page.</span></span>

