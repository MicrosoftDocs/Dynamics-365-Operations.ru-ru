--- 
title: "Создание сырья (только для версии от февраля 2016 г.)"
description: "Эта задача рассматривает создание компонентов готовой продукции и полуфабрикатов."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="01fb1-103">Создание сырья (только для версии от февраля 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="01fb1-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01fb1-104">Эта задача рассматривает создание компонентов готовой продукции и полуфабрикатов.</span><span class="sxs-lookup"><span data-stu-id="01fb1-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="01fb1-105">Это третья задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="01fb1-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="01fb1-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="01fb1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="01fb1-107">Создание первого материала</span><span class="sxs-lookup"><span data-stu-id="01fb1-107">Create the first material</span></span>
1. <span data-ttu-id="01fb1-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="01fb1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="01fb1-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01fb1-109">Click New.</span></span>
3. <span data-ttu-id="01fb1-110">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="01fb1-111">В этом примере введите "ITEM_A".</span><span class="sxs-lookup"><span data-stu-id="01fb1-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="01fb1-112">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-113">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="01fb1-113">Select STD.</span></span> <span data-ttu-id="01fb1-114">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="01fb1-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="01fb1-115">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-116">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="01fb1-116">For example, select Audio.</span></span> <span data-ttu-id="01fb1-117">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="01fb1-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="01fb1-118">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-119">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="01fb1-119">Select SiteWH.</span></span> <span data-ttu-id="01fb1-120">Только сайт и склад будут использоваться для демонстрации.</span><span class="sxs-lookup"><span data-stu-id="01fb1-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="01fb1-121">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-122">Аналитики отслеживания не будут использоваться для данного примера.</span><span class="sxs-lookup"><span data-stu-id="01fb1-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="01fb1-123">Выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="01fb1-123">Select None.</span></span>  
8. <span data-ttu-id="01fb1-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="01fb1-124">Click OK.</span></span>
9. <span data-ttu-id="01fb1-125">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="01fb1-126">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="01fb1-126">Click Default order settings.</span></span>
11. <span data-ttu-id="01fb1-127">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-128">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="01fb1-129">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-130">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="01fb1-131">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-132">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="01fb1-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-133">Close the page.</span></span>
15. <span data-ttu-id="01fb1-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-134">Close the page.</span></span>
16. <span data-ttu-id="01fb1-135">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="01fb1-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="01fb1-136">Щелкните ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="01fb1-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="01fb1-137">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="01fb1-138">В поле "Группа затрат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="01fb1-139">В этом примере введите "M2".</span><span class="sxs-lookup"><span data-stu-id="01fb1-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="01fb1-140">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="01fb1-141">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="01fb1-141">Click Item price.</span></span>
21. <span data-ttu-id="01fb1-142">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01fb1-142">Click New.</span></span>
22. <span data-ttu-id="01fb1-143">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-144">В этом примере выберите 10 — тип цены стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="01fb1-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="01fb1-145">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-146">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="01fb1-147">В поле "Цена" введите число.</span><span class="sxs-lookup"><span data-stu-id="01fb1-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="01fb1-148">В этом примере введите "10".</span><span class="sxs-lookup"><span data-stu-id="01fb1-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="01fb1-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="01fb1-149">Click Save.</span></span>
26. <span data-ttu-id="01fb1-150">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="01fb1-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="01fb1-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-151">Close the page.</span></span>
28. <span data-ttu-id="01fb1-152">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="01fb1-153">Создание второго материала</span><span class="sxs-lookup"><span data-stu-id="01fb1-153">Create the second material</span></span>
1. <span data-ttu-id="01fb1-154">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01fb1-154">Click New.</span></span>
2. <span data-ttu-id="01fb1-155">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="01fb1-156">В этом примере введите "ITEM_B".</span><span class="sxs-lookup"><span data-stu-id="01fb1-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="01fb1-157">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-158">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="01fb1-158">Select STD.</span></span> <span data-ttu-id="01fb1-159">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="01fb1-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="01fb1-160">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-161">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="01fb1-161">For example, select Audio.</span></span> <span data-ttu-id="01fb1-162">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="01fb1-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="01fb1-163">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-164">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="01fb1-164">Select SiteWH.</span></span> <span data-ttu-id="01fb1-165">Только сайт и склад будут использоваться в этом примере.</span><span class="sxs-lookup"><span data-stu-id="01fb1-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="01fb1-166">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-167">Аналитики отслеживания не будут использоваться для данного примера.</span><span class="sxs-lookup"><span data-stu-id="01fb1-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="01fb1-168">Выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="01fb1-168">Select None.</span></span>  
7. <span data-ttu-id="01fb1-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="01fb1-169">Click OK.</span></span>
8. <span data-ttu-id="01fb1-170">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="01fb1-171">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="01fb1-171">Click Default order settings.</span></span>
10. <span data-ttu-id="01fb1-172">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-173">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="01fb1-174">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-175">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="01fb1-176">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-177">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="01fb1-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-178">Close the page.</span></span>
14. <span data-ttu-id="01fb1-179">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-179">Close the page.</span></span>
15. <span data-ttu-id="01fb1-180">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="01fb1-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="01fb1-181">Щелкните ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="01fb1-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="01fb1-182">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="01fb1-183">В поле "Группа затрат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="01fb1-184">В этом примере введите "M2".</span><span class="sxs-lookup"><span data-stu-id="01fb1-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="01fb1-185">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="01fb1-186">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="01fb1-186">Click Item price.</span></span>
20. <span data-ttu-id="01fb1-187">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01fb1-187">Click New.</span></span>
21. <span data-ttu-id="01fb1-188">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-189">В этом примере выберите "10".</span><span class="sxs-lookup"><span data-stu-id="01fb1-189">For this example, select 10.</span></span> <span data-ttu-id="01fb1-190">Это тип цены стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="01fb1-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="01fb1-191">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-192">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="01fb1-193">В поле "Цена" введите число.</span><span class="sxs-lookup"><span data-stu-id="01fb1-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="01fb1-194">В целя демонстрации введите 10.</span><span class="sxs-lookup"><span data-stu-id="01fb1-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="01fb1-195">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="01fb1-195">Click Save.</span></span>
25. <span data-ttu-id="01fb1-196">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="01fb1-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="01fb1-197">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-197">Close the page.</span></span>
27. <span data-ttu-id="01fb1-198">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="01fb1-199">Создание третьего материала</span><span class="sxs-lookup"><span data-stu-id="01fb1-199">Create the third material</span></span>
1. <span data-ttu-id="01fb1-200">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01fb1-200">Click New.</span></span>
2. <span data-ttu-id="01fb1-201">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="01fb1-202">В целя демонстрации введите ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="01fb1-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="01fb1-203">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-204">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="01fb1-204">Select STD.</span></span> <span data-ttu-id="01fb1-205">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="01fb1-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="01fb1-206">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-207">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="01fb1-207">For example, select Audio.</span></span> <span data-ttu-id="01fb1-208">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="01fb1-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="01fb1-209">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-210">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="01fb1-210">Select SiteWH.</span></span> <span data-ttu-id="01fb1-211">Только сайт и склад будут использоваться для демонстрации.</span><span class="sxs-lookup"><span data-stu-id="01fb1-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="01fb1-212">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-213">Аналитики отслеживания не будут использоваться для данного примера.</span><span class="sxs-lookup"><span data-stu-id="01fb1-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="01fb1-214">Выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="01fb1-214">Select None.</span></span>  
7. <span data-ttu-id="01fb1-215">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="01fb1-215">Click OK.</span></span>
8. <span data-ttu-id="01fb1-216">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="01fb1-217">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="01fb1-217">Click Default order settings.</span></span>
10. <span data-ttu-id="01fb1-218">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-219">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="01fb1-220">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-221">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="01fb1-222">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-223">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="01fb1-224">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-224">Close the page.</span></span>
14. <span data-ttu-id="01fb1-225">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-225">Close the page.</span></span>
15. <span data-ttu-id="01fb1-226">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="01fb1-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="01fb1-227">Щелкните ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="01fb1-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="01fb1-228">Разверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="01fb1-229">В поле "Группа затрат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="01fb1-230">В этом примере введите "M1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="01fb1-231">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="01fb1-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="01fb1-232">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="01fb1-232">Click Item price.</span></span>
20. <span data-ttu-id="01fb1-233">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="01fb1-233">Click New.</span></span>
21. <span data-ttu-id="01fb1-234">В поле "Версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-235">В этом примере выберите "10".</span><span class="sxs-lookup"><span data-stu-id="01fb1-235">For this example, select 10.</span></span> <span data-ttu-id="01fb1-236">Это тип цены стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="01fb1-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="01fb1-237">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="01fb1-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="01fb1-238">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="01fb1-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="01fb1-239">В поле "Цена" введите число.</span><span class="sxs-lookup"><span data-stu-id="01fb1-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="01fb1-240">В этом примере введите "10".</span><span class="sxs-lookup"><span data-stu-id="01fb1-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="01fb1-241">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="01fb1-241">Click Save.</span></span>
25. <span data-ttu-id="01fb1-242">Щелкните "Активировать ожидающие цены".</span><span class="sxs-lookup"><span data-stu-id="01fb1-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="01fb1-243">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-243">Close the page.</span></span>
27. <span data-ttu-id="01fb1-244">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="01fb1-244">Close the page.</span></span>


