--- 
title: "Настройка контейнеризации"
description: "В этой процедуре описывается, как автоматизировать контейнеризацию загрузок в модуле \"Управление складом\"."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4e7a2fde65c8dba8b16c5a87eae0ec2bbebc3388
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="73ae6-103">Настройка контейнеризации</span><span class="sxs-lookup"><span data-stu-id="73ae6-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73ae6-104">В этой процедуре описывается, как автоматизировать контейнеризацию загрузок в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="73ae6-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="73ae6-105">Автоматизированная контейнеризация создает контейнеры и работу комплектации для отгрузок при обработке волны, и строки работы можно разделить на количества, помещающиеся в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="73ae6-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="73ae6-106">Это помогает работникам склада комплектовать номенклатуры непосредственно в выбранный контейнер.</span><span class="sxs-lookup"><span data-stu-id="73ae6-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="73ae6-107">По сравнению с процессом упаковки вручную задачи, такие как создание контейнеров, назначение номенклатур и закрытие контейнеров, автоматизированы системой.</span><span class="sxs-lookup"><span data-stu-id="73ae6-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="73ae6-108">В данной процедуре используется демонстрационная компания USMF, и она выполняется менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="73ae6-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="73ae6-109">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="73ae6-109">Set up a wave template</span></span>
1. <span data-ttu-id="73ae6-110">Перейдите в раздел "Управление складом" > "Настройка" > "Волны" > "Шаблоны волны".</span><span class="sxs-lookup"><span data-stu-id="73ae6-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="73ae6-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-111">Click New.</span></span>
3. <span data-ttu-id="73ae6-112">В поле "Шаблон волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="73ae6-113">В поле "Описание шаблона волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="73ae6-114">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="73ae6-115">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="73ae6-116">Разверните раздел "Методы".</span><span class="sxs-lookup"><span data-stu-id="73ae6-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="73ae6-117">В области "Выбранные методы" перечислены методы для выбранного типа шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="73ae6-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="73ae6-118">Шаблон волны должен включать метод контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="73ae6-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="73ae6-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="73ae6-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="73ae6-120">В поле "Код шага волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="73ae6-121">Введите код шага волны для добавленного метода, который может быть любым кодом.</span><span class="sxs-lookup"><span data-stu-id="73ae6-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="73ae6-122">Можно добавить метод несколько раз и назначить различные коды шага волны.</span><span class="sxs-lookup"><span data-stu-id="73ae6-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="73ae6-123">Для этого выберите "Сделать повторяемым для этого метода" на странице "Методы обработки волн".</span><span class="sxs-lookup"><span data-stu-id="73ae6-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="73ae6-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="73ae6-124">Click Save.</span></span>
11. <span data-ttu-id="73ae6-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="73ae6-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="73ae6-126">Настройка типа контейнера</span><span class="sxs-lookup"><span data-stu-id="73ae6-126">Set up a container type</span></span>
1. <span data-ttu-id="73ae6-127">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Типы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="73ae6-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="73ae6-128">Контейнеры можно определить на странице "Типы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="73ae6-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="73ae6-129">Можно настроить физические аналитики контейнеров, включая вес тары, максимальный вес, максимальный объем, длину, ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="73ae6-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="73ae6-130">В этом примере мы имеем три разных размера коробок.</span><span class="sxs-lookup"><span data-stu-id="73ae6-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="73ae6-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-131">Click New.</span></span>
3. <span data-ttu-id="73ae6-132">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="73ae6-133">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="73ae6-134">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="73ae6-135">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="73ae6-136">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="73ae6-137">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="73ae6-138">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="73ae6-139">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="73ae6-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="73ae6-140">Click Save.</span></span>
12. <span data-ttu-id="73ae6-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-141">Click New.</span></span>
13. <span data-ttu-id="73ae6-142">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="73ae6-143">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="73ae6-144">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="73ae6-145">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="73ae6-146">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="73ae6-147">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="73ae6-148">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="73ae6-149">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="73ae6-150">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="73ae6-150">Click Save.</span></span>
22. <span data-ttu-id="73ae6-151">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-151">Click New.</span></span>
23. <span data-ttu-id="73ae6-152">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="73ae6-153">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="73ae6-154">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="73ae6-155">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="73ae6-156">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="73ae6-157">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="73ae6-158">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="73ae6-159">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="73ae6-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="73ae6-160">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="73ae6-160">Click Save.</span></span>
32. <span data-ttu-id="73ae6-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="73ae6-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="73ae6-162">Настройка группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="73ae6-162">Set up a container group</span></span>
1. <span data-ttu-id="73ae6-163">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Группы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="73ae6-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="73ae6-164">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-164">Click New.</span></span>
    * <span data-ttu-id="73ae6-165">Можно настроить логические группы типов контейнеров.</span><span class="sxs-lookup"><span data-stu-id="73ae6-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="73ae6-166">Для каждой группы можно указать последовательность, в которой упаковываются контейнеры, и процент заполнения каждого контейнера.</span><span class="sxs-lookup"><span data-stu-id="73ae6-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="73ae6-167">Аналитики размера номенклатуры используются для определения того, поместится ли она в контейнер.</span><span class="sxs-lookup"><span data-stu-id="73ae6-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="73ae6-168">Используется контейнер, размеры которого наиболее подходят к аналитикам размера номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="73ae6-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="73ae6-169">При наличии нескольких типов контейнеров в группе рекомендуется упорядочивать последовательность по размеру, чтобы самый большой контейнер был в последовательности первым, а самый маленький — последним.</span><span class="sxs-lookup"><span data-stu-id="73ae6-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="73ae6-170">В поле "Код группы контейнеров" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="73ae6-171">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="73ae6-172">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="73ae6-172">Click New.</span></span>
6. <span data-ttu-id="73ae6-173">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="73ae6-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="73ae6-174">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="73ae6-175">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="73ae6-175">Click New.</span></span>
9. <span data-ttu-id="73ae6-176">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="73ae6-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="73ae6-177">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="73ae6-178">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="73ae6-178">Click New.</span></span>
12. <span data-ttu-id="73ae6-179">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="73ae6-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="73ae6-180">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="73ae6-181">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="73ae6-181">Click Save.</span></span>
15. <span data-ttu-id="73ae6-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="73ae6-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="73ae6-183">Настройка шаблона сборки контейнера</span><span class="sxs-lookup"><span data-stu-id="73ae6-183">Set up a container build template</span></span>
1. <span data-ttu-id="73ae6-184">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Шаблоны создания контейнера".</span><span class="sxs-lookup"><span data-stu-id="73ae6-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="73ae6-185">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-185">Click New.</span></span>
    * <span data-ttu-id="73ae6-186">Шаблон сборки контейнера основывается на выполняемых процессах контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="73ae6-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="73ae6-187">Каждый шаблон сборки контейнера определяет один процесс контейнеризации, который будет использоваться шаблоном волны.</span><span class="sxs-lookup"><span data-stu-id="73ae6-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="73ae6-188">C помощью параметра "Изменить запрос" можно определить условия обработки выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="73ae6-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="73ae6-189">Например, можно выполнять контейнеризацию только для конкретных клиентов, продуктов или складов или можно добавить соответствующие диапазоны запроса в шаблон.</span><span class="sxs-lookup"><span data-stu-id="73ae6-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="73ae6-190">Поле "Код шага волны" определяет, как шаблон сборки контейнера связан с шагами в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="73ae6-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="73ae6-191">При выполнении волны оно определяет, какие шаблоны сборки контейнера используются для начала контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="73ae6-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="73ae6-192">Поле "Тип базового запроса" определяет, что упаковывать и на чем основывать запрос фильтра.</span><span class="sxs-lookup"><span data-stu-id="73ae6-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="73ae6-193">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="73ae6-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="73ae6-194">В поле "Код шаблона контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="73ae6-195">В поле "Код группы контейнеров" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="73ae6-196">В поле "Код шага волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="73ae6-197">Установите флажок "Разрешить разделение комплектации".</span><span class="sxs-lookup"><span data-stu-id="73ae6-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="73ae6-198">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="73ae6-198">Click Save.</span></span>
9. <span data-ttu-id="73ae6-199">Щелкните "Ограничения на смешивание контейнера".</span><span class="sxs-lookup"><span data-stu-id="73ae6-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="73ae6-200">Логика смешивания позволяет настроить правила для упаковки строк распределения в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="73ae6-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="73ae6-201">Например, если добавить поле "Код номенклатуры" при назначении номенклатур контейнерам, будет создан новый контейнер при наличии нового кода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="73ae6-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="73ae6-202">Это не позволит работникам упаковывать строки распределения для двух разных клиентов в один и тот же контейнер.</span><span class="sxs-lookup"><span data-stu-id="73ae6-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="73ae6-203">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="73ae6-203">Click New.</span></span>
11. <span data-ttu-id="73ae6-204">В поле "Таблица" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="73ae6-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="73ae6-205">В поле "Выбор поля" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="73ae6-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="73ae6-206">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="73ae6-206">Click OK.</span></span>


