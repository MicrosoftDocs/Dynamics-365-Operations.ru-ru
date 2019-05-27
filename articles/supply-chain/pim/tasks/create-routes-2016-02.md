---
title: Создание маршрутов (февраль 2016 г.)
description: Эта задача рассматривает создание маршрутов производства для готовой продукции и полуфабриката.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567868"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="199af-103">Создание маршрутов (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="199af-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="199af-104">Эта задача рассматривает создание маршрутов производства для готовой продукции и полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="199af-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="199af-105">Это пятая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="199af-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="199af-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="199af-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="199af-107">Создание маршрута для полуфабриката</span><span class="sxs-lookup"><span data-stu-id="199af-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="199af-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="199af-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="199af-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="199af-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="199af-110">Выберите код номенклатуры BOM_2.</span><span class="sxs-lookup"><span data-stu-id="199af-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="199af-111">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="199af-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="199af-112">Щелкните "Маршрут".</span><span class="sxs-lookup"><span data-stu-id="199af-112">Click Route.</span></span>
5. <span data-ttu-id="199af-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="199af-113">Click New.</span></span>
6. <span data-ttu-id="199af-114">Щелкните "Маршрут и версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="199af-114">Click Route and route version.</span></span>
7. <span data-ttu-id="199af-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="199af-116">Например, введите "МАРШРУТ 2".</span><span class="sxs-lookup"><span data-stu-id="199af-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="199af-117">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-118">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="199af-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="199af-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="199af-119">Click OK.</span></span>
10. <span data-ttu-id="199af-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="199af-120">Click New.</span></span>
11. <span data-ttu-id="199af-121">В поле "Операция" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-122">В этом примере выберите "Сборка".</span><span class="sxs-lookup"><span data-stu-id="199af-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="199af-123">В поле "Время выполнения" введите число.</span><span class="sxs-lookup"><span data-stu-id="199af-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="199af-124">Например, введите "1".</span><span class="sxs-lookup"><span data-stu-id="199af-124">For example, type 1.</span></span> <span data-ttu-id="199af-125">Время выполнения часто является частью цены, рассчитанной для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="199af-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="199af-126">В поле "Маршрутная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-127">В этом примере выберите "Стандарт".</span><span class="sxs-lookup"><span data-stu-id="199af-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="199af-128">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="199af-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="199af-129">В поле "Категория настройки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-130">В этом примере выберите "Сборка".</span><span class="sxs-lookup"><span data-stu-id="199af-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="199af-131">Перейдите на вкладку "Время".</span><span class="sxs-lookup"><span data-stu-id="199af-131">Click the Times tab.</span></span>
17. <span data-ttu-id="199af-132">В поле "Время настройки" введите число.</span><span class="sxs-lookup"><span data-stu-id="199af-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="199af-133">В этом примере введите "1".</span><span class="sxs-lookup"><span data-stu-id="199af-133">For this example, type 1.</span></span> <span data-ttu-id="199af-134">Время настройки часто является частью цены, рассчитанной для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="199af-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="199af-135">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="199af-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="199af-136">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="199af-136">Click Approve.</span></span>
20. <span data-ttu-id="199af-137">Выберите значение "Да" в поле "Также утвердить маршрут?". .</span><span class="sxs-lookup"><span data-stu-id="199af-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="199af-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="199af-138">Click OK.</span></span>
22. <span data-ttu-id="199af-139">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="199af-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="199af-140">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="199af-140">Click Activate.</span></span>
24. <span data-ttu-id="199af-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="199af-141">Close the page.</span></span>
25. <span data-ttu-id="199af-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="199af-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="199af-143">Создание маршрута для готовой продукции</span><span class="sxs-lookup"><span data-stu-id="199af-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="199af-144">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="199af-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="199af-145">Выберите код номенклатуры BOM_1.</span><span class="sxs-lookup"><span data-stu-id="199af-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="199af-146">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="199af-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="199af-147">Щелкните "Маршрут".</span><span class="sxs-lookup"><span data-stu-id="199af-147">Click Route.</span></span>
4. <span data-ttu-id="199af-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="199af-148">Click New.</span></span>
5. <span data-ttu-id="199af-149">Щелкните "Маршрут и версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="199af-149">Click Route and route version.</span></span>
6. <span data-ttu-id="199af-150">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="199af-151">В этом примере введите "МАРШРУТ 1".</span><span class="sxs-lookup"><span data-stu-id="199af-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="199af-152">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-153">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="199af-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="199af-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="199af-154">Click OK.</span></span>
9. <span data-ttu-id="199af-155">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="199af-155">Click New.</span></span>
10. <span data-ttu-id="199af-156">В поле "Операция" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-157">В этом примере выберите "Упаковка".</span><span class="sxs-lookup"><span data-stu-id="199af-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="199af-158">В поле "Время выполнения" введите число.</span><span class="sxs-lookup"><span data-stu-id="199af-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="199af-159">В этом примере введите "1".</span><span class="sxs-lookup"><span data-stu-id="199af-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="199af-160">В поле "Маршрутная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-161">В этом примере выберите "Стандарт".</span><span class="sxs-lookup"><span data-stu-id="199af-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="199af-162">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="199af-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="199af-163">В поле "Категория настройки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="199af-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="199af-164">В этом примере выберите "Упаковка".</span><span class="sxs-lookup"><span data-stu-id="199af-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="199af-165">Перейдите на вкладку "Время".</span><span class="sxs-lookup"><span data-stu-id="199af-165">Click the Times tab.</span></span>
16. <span data-ttu-id="199af-166">В поле "Время настройки" введите число.</span><span class="sxs-lookup"><span data-stu-id="199af-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="199af-167">В этом примере введите "1".</span><span class="sxs-lookup"><span data-stu-id="199af-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="199af-168">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="199af-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="199af-169">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="199af-169">Click Approve.</span></span>
19. <span data-ttu-id="199af-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="199af-170">Click OK.</span></span>
20. <span data-ttu-id="199af-171">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="199af-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="199af-172">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="199af-172">Click Activate.</span></span>
22. <span data-ttu-id="199af-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="199af-173">Close the page.</span></span>
23. <span data-ttu-id="199af-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="199af-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="199af-175">Включение автоматического потребления времени настройки</span><span class="sxs-lookup"><span data-stu-id="199af-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="199af-176">Перейдите в раздел "Управление производством" > "Настройка" > "Маршруты" > "Маршрутные группы".</span><span class="sxs-lookup"><span data-stu-id="199af-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="199af-177">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="199af-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="199af-178">Выберите "Стандарт" в списке.</span><span class="sxs-lookup"><span data-stu-id="199af-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="199af-179">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="199af-179">Click Edit.</span></span>
4. <span data-ttu-id="199af-180">Выберите значение "Да" в поле "Время настройки".</span><span class="sxs-lookup"><span data-stu-id="199af-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="199af-181">Время настройки часто является частью цены, рассчитанной для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="199af-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="199af-182">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="199af-182">Click Save.</span></span>
6. <span data-ttu-id="199af-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="199af-183">Close the page.</span></span>

