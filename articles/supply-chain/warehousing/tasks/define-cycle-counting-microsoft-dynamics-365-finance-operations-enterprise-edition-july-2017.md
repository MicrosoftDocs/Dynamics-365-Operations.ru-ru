---
title: Определение цикличного подсчета
description: Подсчет циклов — это процесс склада, который можно использовать для аудита номенклатур запасов в наличии.
author: MarkusFogelberg
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 995212dd40f8665da64ca0bf8e1c878002778904
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830962"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="4b96d-103">Определение цикличного подсчета</span><span class="sxs-lookup"><span data-stu-id="4b96d-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b96d-104">Подсчет циклов — это процесс склада, который можно использовать для аудита номенклатур запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="4b96d-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="4b96d-105">В этой записи задачи показаны настройка приоритета работы подсчета по умолчанию; включение элемента меню мобильного устройства для обработки операций и комплектации, и подсчета; включение триггера порога подсчета, когда местонахождение становится пустым; включение плана цикла подсчетов для определенной номенклатуры на конкретном складе.</span><span class="sxs-lookup"><span data-stu-id="4b96d-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="4b96d-106">Обычно эти задачи выполняет менеджер склада.</span><span class="sxs-lookup"><span data-stu-id="4b96d-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="4b96d-107">Выполнить процедуру можно в компании с демонстрационными данными USMF или с вашими собственными данными.</span><span class="sxs-lookup"><span data-stu-id="4b96d-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="4b96d-108">Настройка приоритета работы подсчета</span><span class="sxs-lookup"><span data-stu-id="4b96d-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="4b96d-109">В **области перехода** выберите **Модули > Управление складом > Настройка > Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="4b96d-110">Перейдите на вкладку **Подсчет циклов**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="4b96d-111">В поле **Приоритет работы для подсчета циклов по умолчанию** введите число.</span><span class="sxs-lookup"><span data-stu-id="4b96d-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="4b96d-112">Это действие изменяет приоритет работы подсчета циклов по сравнению с другими типами работы на складе.</span><span class="sxs-lookup"><span data-stu-id="4b96d-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="4b96d-113">При вводе числа, которое меньше числа для других типов работы, приоритет работы подсчета циклов увеличится.</span><span class="sxs-lookup"><span data-stu-id="4b96d-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="4b96d-114">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-114">Click **Save**.</span></span>
5. <span data-ttu-id="4b96d-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4b96d-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="4b96d-116">Включение мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="4b96d-116">Enable the mobile device</span></span>
1. <span data-ttu-id="4b96d-117">В **области переходов** выберите **Модули >Управление складом > Настройка > Мобильное устройство > Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="4b96d-118">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-118">Click **New**.</span></span>
3. <span data-ttu-id="4b96d-119">В поле **Имя пункта меню** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="4b96d-120">В поле **Заголовок** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="4b96d-121">В поле **Режим** выберите "Работа".</span><span class="sxs-lookup"><span data-stu-id="4b96d-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="4b96d-122">Укажите для **Использовать существующую работу** вариант "Да".</span><span class="sxs-lookup"><span data-stu-id="4b96d-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="4b96d-123">При установке этого параметра в значение "Да" система выполняет поиск существующей работы, когда используется элемент меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="4b96d-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="4b96d-124">В поле **Кем управляется** выберите "Управляется системой".</span><span class="sxs-lookup"><span data-stu-id="4b96d-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="4b96d-125">При выборе варианта "Управляется системой" работнику склада будет предложено открыть работу, которая находится в заданных классах работы.</span><span class="sxs-lookup"><span data-stu-id="4b96d-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="4b96d-126">(Эти классы работы мы создадим на следующем шаге.)</span><span class="sxs-lookup"><span data-stu-id="4b96d-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="4b96d-127">Разверните экспресс-вкладку **Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="4b96d-128">Далее мы создадим два класса работы, которые будут использоваться с этим элементом меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="4b96d-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="4b96d-129">При использовании этого элемента меню будут запрашиваться эти классы, и пользователю будет показана работа с наивысшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="4b96d-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="4b96d-130">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-130">Click **New**.</span></span>
10. <span data-ttu-id="4b96d-131">В поле **Код класса работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="4b96d-132">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-132">Click **New**.</span></span>
12. <span data-ttu-id="4b96d-133">В поле **Код класса работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="4b96d-134">В области **Панель операций** щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="4b96d-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4b96d-135">Close the page.</span></span>
15. <span data-ttu-id="4b96d-136">В **области переходов** выберите **Модули >Управление складом > Настройка > Мобильное устройство > Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="4b96d-137">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4b96d-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="4b96d-138">В дереве выберите только что созданный элемент меню.</span><span class="sxs-lookup"><span data-stu-id="4b96d-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="4b96d-139">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-139">Click **Edit**.</span></span>
19. <span data-ttu-id="4b96d-140">Щелкните стрелку для добавления элемента меню в меню.</span><span class="sxs-lookup"><span data-stu-id="4b96d-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="4b96d-141">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="4b96d-142">Создание порога подсчета</span><span class="sxs-lookup"><span data-stu-id="4b96d-142">Create a counting threshold</span></span>
1. <span data-ttu-id="4b96d-143">В **области переходов** выберите **Модули > Управление складом > Настройка > Цикличный подсчет > Пороги цикличного подсчета**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="4b96d-144">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-144">Click **New**.</span></span>
3. <span data-ttu-id="4b96d-145">В поле **Код порога цикличного подсчета** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="4b96d-146">Задайте параметр **Обработать цикличный подсчет немедленно** как "Да".</span><span class="sxs-lookup"><span data-stu-id="4b96d-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="4b96d-147">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="4b96d-148">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-148">Click **Save**.</span></span>
7. <span data-ttu-id="4b96d-149">Щелкните **Выберите местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="4b96d-150">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4b96d-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4b96d-151">В поле **Критерии** выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="4b96d-152">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-152">Click **OK**.</span></span>
11. <span data-ttu-id="4b96d-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4b96d-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="4b96d-154">Создание плана подсчета циклов</span><span class="sxs-lookup"><span data-stu-id="4b96d-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="4b96d-155">В **области переходов** выберите **Модули > Управление складом > Настройка > Цикличный подсчет > Планы цикличного подсчета**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="4b96d-156">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-156">Click **New**.</span></span>
3. <span data-ttu-id="4b96d-157">В поле **Код плана цикличного подсчета** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="4b96d-158">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="4b96d-159">В поле **Максимальное количество цикличных подсчетов** введите число.</span><span class="sxs-lookup"><span data-stu-id="4b96d-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="4b96d-160">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-160">Click **Save**.</span></span>
7. <span data-ttu-id="4b96d-161">Щелкните **Выберите местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="4b96d-162">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4b96d-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4b96d-163">В поле **Критерии** выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="4b96d-164">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-164">Click **OK**.</span></span>
11. <span data-ttu-id="4b96d-165">В поле **Дней между цикличными подсчетами** введите число.</span><span class="sxs-lookup"><span data-stu-id="4b96d-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="4b96d-166">Например, в поле **Дней между цикличными подсчетами** задано значение 5, работа цикличного подсчета будет создаваться каждые пять дней.</span><span class="sxs-lookup"><span data-stu-id="4b96d-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="4b96d-167">Однако если работа подсчета циклов обрабатывается на третий день, следующая работа подсчета циклов будет создана спустя пять дней после последней обработки подсчета циклов, то есть на восьмой день.</span><span class="sxs-lookup"><span data-stu-id="4b96d-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="4b96d-168">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-168">Click **Save**.</span></span>
13. <span data-ttu-id="4b96d-169">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-169">Click **New**.</span></span>
14. <span data-ttu-id="4b96d-170">В поле **Порядковый номер** введите число.</span><span class="sxs-lookup"><span data-stu-id="4b96d-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="4b96d-171">Порядок сортировки — от наименьшего до наибольшего числа.</span><span class="sxs-lookup"><span data-stu-id="4b96d-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="4b96d-172">Значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="4b96d-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="4b96d-173">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4b96d-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="4b96d-174">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="4b96d-175">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-175">Click **Save**.</span></span>
18. <span data-ttu-id="4b96d-176">Щелкните **Определить запрос продукта**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="4b96d-177">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4b96d-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="4b96d-178">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4b96d-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="4b96d-179">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b96d-179">Click **OK**.</span></span>
22. <span data-ttu-id="4b96d-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4b96d-180">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]