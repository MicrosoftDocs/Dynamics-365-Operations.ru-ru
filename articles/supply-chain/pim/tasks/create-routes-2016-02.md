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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844569"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="ffb61-103">Создание маршрутов (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="ffb61-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffb61-104">Эта задача рассматривает создание маршрутов производства для готовой продукции и полуфабриката.</span><span class="sxs-lookup"><span data-stu-id="ffb61-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="ffb61-105">Это пятая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="ffb61-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="ffb61-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ffb61-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="ffb61-107">Создание маршрута для полуфабриката</span><span class="sxs-lookup"><span data-stu-id="ffb61-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="ffb61-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="ffb61-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ffb61-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ffb61-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ffb61-110">Выберите код номенклатуры BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ffb61-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="ffb61-111">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="ffb61-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="ffb61-112">Щелкните "Маршрут".</span><span class="sxs-lookup"><span data-stu-id="ffb61-112">Click Route.</span></span>
5. <span data-ttu-id="ffb61-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ffb61-113">Click New.</span></span>
6. <span data-ttu-id="ffb61-114">Щелкните "Маршрут и версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="ffb61-114">Click Route and route version.</span></span>
7. <span data-ttu-id="ffb61-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ffb61-116">Например, введите "МАРШРУТ 2".</span><span class="sxs-lookup"><span data-stu-id="ffb61-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="ffb61-117">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-118">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="ffb61-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ffb61-119">Click OK.</span></span>
10. <span data-ttu-id="ffb61-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ffb61-120">Click New.</span></span>
11. <span data-ttu-id="ffb61-121">В поле "Операция" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-122">В этом примере выберите "Сборка".</span><span class="sxs-lookup"><span data-stu-id="ffb61-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="ffb61-123">В поле "Время выполнения" введите число.</span><span class="sxs-lookup"><span data-stu-id="ffb61-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ffb61-124">Например, введите "1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-124">For example, type 1.</span></span> <span data-ttu-id="ffb61-125">Время выполнения часто является частью цены, рассчитанной для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ffb61-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="ffb61-126">В поле "Маршрутная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-127">В этом примере выберите "Стандарт".</span><span class="sxs-lookup"><span data-stu-id="ffb61-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="ffb61-128">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="ffb61-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="ffb61-129">В поле "Категория настройки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-130">В этом примере выберите "Сборка".</span><span class="sxs-lookup"><span data-stu-id="ffb61-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="ffb61-131">Перейдите на вкладку "Время".</span><span class="sxs-lookup"><span data-stu-id="ffb61-131">Click the Times tab.</span></span>
17. <span data-ttu-id="ffb61-132">В поле "Время настройки" введите число.</span><span class="sxs-lookup"><span data-stu-id="ffb61-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="ffb61-133">В этом примере введите "1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-133">For this example, type 1.</span></span> <span data-ttu-id="ffb61-134">Время настройки часто является частью цены, рассчитанной для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ffb61-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="ffb61-135">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="ffb61-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="ffb61-136">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="ffb61-136">Click Approve.</span></span>
20. <span data-ttu-id="ffb61-137">Выберите значение "Да" в поле "Также утвердить маршрут?". .</span><span class="sxs-lookup"><span data-stu-id="ffb61-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="ffb61-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ffb61-138">Click OK.</span></span>
22. <span data-ttu-id="ffb61-139">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="ffb61-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="ffb61-140">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="ffb61-140">Click Activate.</span></span>
24. <span data-ttu-id="ffb61-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ffb61-141">Close the page.</span></span>
25. <span data-ttu-id="ffb61-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ffb61-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="ffb61-143">Создание маршрута для готовой продукции</span><span class="sxs-lookup"><span data-stu-id="ffb61-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="ffb61-144">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ffb61-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ffb61-145">Выберите код номенклатуры BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ffb61-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="ffb61-146">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="ffb61-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="ffb61-147">Щелкните "Маршрут".</span><span class="sxs-lookup"><span data-stu-id="ffb61-147">Click Route.</span></span>
4. <span data-ttu-id="ffb61-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ffb61-148">Click New.</span></span>
5. <span data-ttu-id="ffb61-149">Щелкните "Маршрут и версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="ffb61-149">Click Route and route version.</span></span>
6. <span data-ttu-id="ffb61-150">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ffb61-151">В этом примере введите "МАРШРУТ 1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="ffb61-152">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-153">В этом примере введите или выберите "Сайт 1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="ffb61-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ffb61-154">Click OK.</span></span>
9. <span data-ttu-id="ffb61-155">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ffb61-155">Click New.</span></span>
10. <span data-ttu-id="ffb61-156">В поле "Операция" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-157">В этом примере выберите "Упаковка".</span><span class="sxs-lookup"><span data-stu-id="ffb61-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="ffb61-158">В поле "Время выполнения" введите число.</span><span class="sxs-lookup"><span data-stu-id="ffb61-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ffb61-159">В этом примере введите "1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="ffb61-160">В поле "Маршрутная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-161">В этом примере выберите "Стандарт".</span><span class="sxs-lookup"><span data-stu-id="ffb61-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="ffb61-162">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="ffb61-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="ffb61-163">В поле "Категория настройки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ffb61-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="ffb61-164">В этом примере выберите "Упаковка".</span><span class="sxs-lookup"><span data-stu-id="ffb61-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="ffb61-165">Перейдите на вкладку "Время".</span><span class="sxs-lookup"><span data-stu-id="ffb61-165">Click the Times tab.</span></span>
16. <span data-ttu-id="ffb61-166">В поле "Время настройки" введите число.</span><span class="sxs-lookup"><span data-stu-id="ffb61-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="ffb61-167">В этом примере введите "1".</span><span class="sxs-lookup"><span data-stu-id="ffb61-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="ffb61-168">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="ffb61-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="ffb61-169">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="ffb61-169">Click Approve.</span></span>
19. <span data-ttu-id="ffb61-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ffb61-170">Click OK.</span></span>
20. <span data-ttu-id="ffb61-171">В области действий щелкните "Версия маршрута".</span><span class="sxs-lookup"><span data-stu-id="ffb61-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="ffb61-172">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="ffb61-172">Click Activate.</span></span>
22. <span data-ttu-id="ffb61-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ffb61-173">Close the page.</span></span>
23. <span data-ttu-id="ffb61-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ffb61-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="ffb61-175">Включение автоматического потребления времени настройки</span><span class="sxs-lookup"><span data-stu-id="ffb61-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="ffb61-176">Перейдите в раздел "Управление производством" > "Настройка" > "Маршруты" > "Маршрутные группы".</span><span class="sxs-lookup"><span data-stu-id="ffb61-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="ffb61-177">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ffb61-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ffb61-178">Выберите "Стандарт" в списке.</span><span class="sxs-lookup"><span data-stu-id="ffb61-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="ffb61-179">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="ffb61-179">Click Edit.</span></span>
4. <span data-ttu-id="ffb61-180">Выберите значение "Да" в поле "Время настройки".</span><span class="sxs-lookup"><span data-stu-id="ffb61-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="ffb61-181">Время настройки часто является частью цены, рассчитанной для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ffb61-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="ffb61-182">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ffb61-182">Click Save.</span></span>
6. <span data-ttu-id="ffb61-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ffb61-183">Close the page.</span></span>

