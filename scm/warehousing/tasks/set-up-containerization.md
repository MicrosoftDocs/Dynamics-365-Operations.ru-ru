--- 
title: "Настройка контейнеризации"
description: "В этой процедуре описывается, как автоматизировать контейнеризацию загрузок в модуле \"Управление складом\"."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="3ef88-103">Настройка контейнеризации</span><span class="sxs-lookup"><span data-stu-id="3ef88-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ef88-104">В этой процедуре описывается, как автоматизировать контейнеризацию загрузок в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="3ef88-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="3ef88-105">Автоматизированная контейнеризация создает контейнеры и работу комплектации для отгрузок при обработке волны, и строки работы можно разделить на количества, помещающиеся в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="3ef88-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="3ef88-106">Это помогает работникам склада комплектовать номенклатуры непосредственно в выбранный контейнер.</span><span class="sxs-lookup"><span data-stu-id="3ef88-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="3ef88-107">По сравнению с процессом упаковки вручную задачи, такие как создание контейнеров, назначение номенклатур и закрытие контейнеров, автоматизированы системой.</span><span class="sxs-lookup"><span data-stu-id="3ef88-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="3ef88-108">В данной процедуре используется демонстрационная компания USMF, и она выполняется менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="3ef88-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="3ef88-109">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="3ef88-109">Set up a wave template</span></span>
1. <span data-ttu-id="3ef88-110">Перейдите в раздел "Управление складом" > "Настройка" > "Волны" > "Шаблоны волны".</span><span class="sxs-lookup"><span data-stu-id="3ef88-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="3ef88-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-111">Click New.</span></span>
3. <span data-ttu-id="3ef88-112">В поле "Шаблон волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="3ef88-113">В поле "Описание шаблона волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="3ef88-114">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="3ef88-115">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="3ef88-116">Разверните раздел "Методы".</span><span class="sxs-lookup"><span data-stu-id="3ef88-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="3ef88-117">В области "Выбранные методы" перечислены методы для выбранного типа шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="3ef88-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="3ef88-118">Шаблон волны должен включать метод контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="3ef88-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="3ef88-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3ef88-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="3ef88-120">В поле "Код шага волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="3ef88-121">Введите код шага волны для добавленного метода, который может быть любым кодом.</span><span class="sxs-lookup"><span data-stu-id="3ef88-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="3ef88-122">Можно добавить метод несколько раз и назначить различные коды шага волны.</span><span class="sxs-lookup"><span data-stu-id="3ef88-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="3ef88-123">Для этого выберите "Сделать повторяемым для этого метода" на странице "Методы обработки волн".</span><span class="sxs-lookup"><span data-stu-id="3ef88-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="3ef88-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3ef88-124">Click Save.</span></span>
11. <span data-ttu-id="3ef88-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3ef88-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="3ef88-126">Настройка типа контейнера</span><span class="sxs-lookup"><span data-stu-id="3ef88-126">Set up a container type</span></span>
1. <span data-ttu-id="3ef88-127">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Типы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="3ef88-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="3ef88-128">Контейнеры можно определить на странице "Типы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="3ef88-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="3ef88-129">Можно настроить физические аналитики контейнеров, включая вес тары, максимальный вес, максимальный объем, длину, ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="3ef88-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="3ef88-130">В этом примере мы имеем три разных размера коробок.</span><span class="sxs-lookup"><span data-stu-id="3ef88-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="3ef88-131">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-131">Click New.</span></span>
3. <span data-ttu-id="3ef88-132">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="3ef88-133">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="3ef88-134">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="3ef88-135">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="3ef88-136">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="3ef88-137">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="3ef88-138">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="3ef88-139">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3ef88-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3ef88-140">Click Save.</span></span>
12. <span data-ttu-id="3ef88-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-141">Click New.</span></span>
13. <span data-ttu-id="3ef88-142">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="3ef88-143">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="3ef88-144">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="3ef88-145">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="3ef88-146">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="3ef88-147">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="3ef88-148">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="3ef88-149">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="3ef88-150">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3ef88-150">Click Save.</span></span>
22. <span data-ttu-id="3ef88-151">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-151">Click New.</span></span>
23. <span data-ttu-id="3ef88-152">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="3ef88-153">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="3ef88-154">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="3ef88-155">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="3ef88-156">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="3ef88-157">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="3ef88-158">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="3ef88-159">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="3ef88-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="3ef88-160">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3ef88-160">Click Save.</span></span>
32. <span data-ttu-id="3ef88-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3ef88-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="3ef88-162">Настройка группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="3ef88-162">Set up a container group</span></span>
1. <span data-ttu-id="3ef88-163">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Группы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="3ef88-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="3ef88-164">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-164">Click New.</span></span>
    * <span data-ttu-id="3ef88-165">Можно настроить логические группы типов контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3ef88-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="3ef88-166">Для каждой группы можно определить последовательность, в которой будут упаковываться контейнеры, и процент заполнения контейнеров. Для определения того, поместится ли номенклатура в контейнер, используются аналитики размеров номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3ef88-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="3ef88-167">Используется контейнер, размеры которого наиболее подходят к аналитикам размера номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3ef88-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="3ef88-168">При наличии нескольких типов контейнеров в группе рекомендуется упорядочивать последовательность по размеру, чтобы самый большой контейнер был в последовательности первым, а самый маленький — последним.</span><span class="sxs-lookup"><span data-stu-id="3ef88-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="3ef88-169">В поле "Код группы контейнеров" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="3ef88-170">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3ef88-171">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="3ef88-171">Click New.</span></span>
6. <span data-ttu-id="3ef88-172">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="3ef88-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3ef88-173">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="3ef88-174">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="3ef88-174">Click New.</span></span>
9. <span data-ttu-id="3ef88-175">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="3ef88-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="3ef88-176">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="3ef88-177">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="3ef88-177">Click New.</span></span>
12. <span data-ttu-id="3ef88-178">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="3ef88-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3ef88-179">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="3ef88-180">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3ef88-180">Click Save.</span></span>
15. <span data-ttu-id="3ef88-181">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3ef88-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="3ef88-182">Настройка шаблона сборки контейнера</span><span class="sxs-lookup"><span data-stu-id="3ef88-182">Set up a container build template</span></span>
1. <span data-ttu-id="3ef88-183">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Шаблоны создания контейнера".</span><span class="sxs-lookup"><span data-stu-id="3ef88-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="3ef88-184">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-184">Click New.</span></span>
    * <span data-ttu-id="3ef88-185">Шаблон сборки контейнера основывается на выполняемых процессах контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="3ef88-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="3ef88-186">Каждый шаблон сборки контейнера определяет один процесс контейнеризации, который будет использоваться шаблоном волны.</span><span class="sxs-lookup"><span data-stu-id="3ef88-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="3ef88-187">C помощью параметра "Изменить запрос" можно определить условия обработки выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="3ef88-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="3ef88-188">Например, можно выполнять контейнеризацию только для конкретных клиентов, продуктов или складов или можно добавить соответствующие диапазоны запроса в шаблон.</span><span class="sxs-lookup"><span data-stu-id="3ef88-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="3ef88-189">Поле "Код шага волны" определяет, как шаблон сборки контейнера связан с шагами в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="3ef88-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="3ef88-190">При выполнении волны оно определяет, какие шаблоны сборки контейнера используются для начала контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="3ef88-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="3ef88-191">Поле "Тип базового запроса" определяет, что упаковывать и на чем основывать запрос фильтра.</span><span class="sxs-lookup"><span data-stu-id="3ef88-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="3ef88-192">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="3ef88-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3ef88-193">В поле "Код шаблона контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="3ef88-194">В поле "Код группы контейнеров" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="3ef88-195">В поле "Код шага волны" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="3ef88-196">Установите флажок "Разрешить разделение комплектации".</span><span class="sxs-lookup"><span data-stu-id="3ef88-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="3ef88-197">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3ef88-197">Click Save.</span></span>
9. <span data-ttu-id="3ef88-198">Щелкните "Ограничения на смешивание контейнера".</span><span class="sxs-lookup"><span data-stu-id="3ef88-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="3ef88-199">Логика смешивания позволяет настроить правила для упаковки строк распределения в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="3ef88-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="3ef88-200">Например, если добавить поле "Код номенклатуры" при назначении номенклатур контейнерам, будет создан новый контейнер при наличии нового кода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3ef88-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="3ef88-201">Это не позволит работникам упаковывать строки распределения для двух разных клиентов в один и тот же контейнер.</span><span class="sxs-lookup"><span data-stu-id="3ef88-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="3ef88-202">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3ef88-202">Click New.</span></span>
11. <span data-ttu-id="3ef88-203">В поле "Таблица" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="3ef88-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="3ef88-204">В поле "Выбор поля" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ef88-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="3ef88-205">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3ef88-205">Click OK.</span></span>


