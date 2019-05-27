---
title: Определение цикличного подсчета
description: Подсчет циклов — это процесс склада, который можно использовать для аудита номенклатур запасов в наличии.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571704"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="4be0a-103">Определение цикличного подсчета</span><span class="sxs-lookup"><span data-stu-id="4be0a-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4be0a-104">Подсчет циклов — это процесс склада, который можно использовать для аудита номенклатур запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="4be0a-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="4be0a-105">В этой записи задачи показаны настройка приоритета работы подсчета по умолчанию; включение элемента меню мобильного устройства для обработки операций и комплектации, и подсчета; включение триггера порога подсчета, когда местонахождение становится пустым; включение плана цикла подсчетов для определенной номенклатуры на конкретном складе.</span><span class="sxs-lookup"><span data-stu-id="4be0a-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="4be0a-106">Обычно эти задачи выполняет менеджер склада.</span><span class="sxs-lookup"><span data-stu-id="4be0a-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="4be0a-107">Выполнить процедуру можно в компании с демонстрационными данными USMF или с вашими собственными данными.</span><span class="sxs-lookup"><span data-stu-id="4be0a-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="4be0a-108">Настройка приоритета работы подсчета</span><span class="sxs-lookup"><span data-stu-id="4be0a-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="4be0a-109">Перейдите в раздел "Управление складом" > "Настройка" > "Параметры управления складом".</span><span class="sxs-lookup"><span data-stu-id="4be0a-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="4be0a-110">Перейдите на вкладку "Подсчет циклов".</span><span class="sxs-lookup"><span data-stu-id="4be0a-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="4be0a-111">В поле "Приоритет работы для подсчета циклов по умолчанию" введите число.</span><span class="sxs-lookup"><span data-stu-id="4be0a-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="4be0a-112">Это действие изменяет приоритет работы подсчета циклов по сравнению с другими типами работы на складе.</span><span class="sxs-lookup"><span data-stu-id="4be0a-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="4be0a-113">При вводе числа, которое меньше числа для других типов работы, приоритет работы подсчета циклов увеличится.</span><span class="sxs-lookup"><span data-stu-id="4be0a-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="4be0a-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4be0a-114">Click Save.</span></span>
5. <span data-ttu-id="4be0a-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4be0a-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="4be0a-116">Включение мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="4be0a-116">Enable the mobile device</span></span>
1. <span data-ttu-id="4be0a-117">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Пункты меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="4be0a-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="4be0a-118">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4be0a-118">Click New.</span></span>
3. <span data-ttu-id="4be0a-119">В поле "Имя пункта меню" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="4be0a-120">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="4be0a-121">В поле "Режим" выберите "Работа".</span><span class="sxs-lookup"><span data-stu-id="4be0a-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="4be0a-122">Укажите для "Использовать существующую работу" вариант "Да".</span><span class="sxs-lookup"><span data-stu-id="4be0a-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="4be0a-123">При установке этого параметра в значение "Да" система выполняет поиск существующей работы, когда используется элемент меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="4be0a-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="4be0a-124">В поле "Кем управляется" выберите "Управляется системой".</span><span class="sxs-lookup"><span data-stu-id="4be0a-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="4be0a-125">При выборе варианта "Управляется системой" работнику склада будет предложено открыть работу, которая находится в заданных классах работы.</span><span class="sxs-lookup"><span data-stu-id="4be0a-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="4be0a-126">(Эти классы работы мы создадим на следующем шаге.)</span><span class="sxs-lookup"><span data-stu-id="4be0a-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="4be0a-127">Разверните или сверните раздел "Классы работы".</span><span class="sxs-lookup"><span data-stu-id="4be0a-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="4be0a-128">Далее мы создадим два класса работы, которые будут использоваться с этим элементом меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="4be0a-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="4be0a-129">При использовании этого элемента меню будут запрашиваться эти классы, и пользователю будет показана работа с наивысшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="4be0a-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="4be0a-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4be0a-130">Click New.</span></span>
10. <span data-ttu-id="4be0a-131">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="4be0a-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4be0a-132">Click New.</span></span>
12. <span data-ttu-id="4be0a-133">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="4be0a-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4be0a-134">Click Save.</span></span>
14. <span data-ttu-id="4be0a-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4be0a-135">Close the page.</span></span>
15. <span data-ttu-id="4be0a-136">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="4be0a-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="4be0a-137">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4be0a-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="4be0a-138">В дереве выберите только что созданный элемент меню.</span><span class="sxs-lookup"><span data-stu-id="4be0a-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="4be0a-139">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="4be0a-139">Click Edit.</span></span>
19. <span data-ttu-id="4be0a-140">Щелкните стрелку для добавления элемента меню в меню.</span><span class="sxs-lookup"><span data-stu-id="4be0a-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="4be0a-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4be0a-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="4be0a-142">Создание порога подсчета</span><span class="sxs-lookup"><span data-stu-id="4be0a-142">Create a counting threshold</span></span>
1. <span data-ttu-id="4be0a-143">Перейдите в раздел "Управление складом" > "Настройка" > "Подсчет циклов" > "Пороги подсчета циклов".</span><span class="sxs-lookup"><span data-stu-id="4be0a-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="4be0a-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4be0a-144">Click New.</span></span>
3. <span data-ttu-id="4be0a-145">В поле "Код порога подсчета циклов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="4be0a-146">Задайте параметр "Обработать подсчет циклов немедленно" как "Да".</span><span class="sxs-lookup"><span data-stu-id="4be0a-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="4be0a-147">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="4be0a-148">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="4be0a-148">Click Save.</span></span>
7. <span data-ttu-id="4be0a-149">Щелкните "Выберите местонахождения".</span><span class="sxs-lookup"><span data-stu-id="4be0a-149">Click Select locations.</span></span>
8. <span data-ttu-id="4be0a-150">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4be0a-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4be0a-151">В поле "Критерий" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="4be0a-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4be0a-152">Click OK.</span></span>
11. <span data-ttu-id="4be0a-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4be0a-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="4be0a-154">Создание плана подсчета циклов</span><span class="sxs-lookup"><span data-stu-id="4be0a-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="4be0a-155">Перейдите в раздел "Управление складом" > "Настройка" > "Подсчет циклов" > "Планы подсчета циклов".</span><span class="sxs-lookup"><span data-stu-id="4be0a-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="4be0a-156">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4be0a-156">Click New.</span></span>
3. <span data-ttu-id="4be0a-157">В поле "Код плана подсчета циклов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="4be0a-158">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4be0a-159">В поле "Максимальное количество подсчетов циклов" введите число.</span><span class="sxs-lookup"><span data-stu-id="4be0a-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="4be0a-160">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="4be0a-160">Click Save.</span></span>
7. <span data-ttu-id="4be0a-161">Щелкните "Выберите местонахождения".</span><span class="sxs-lookup"><span data-stu-id="4be0a-161">Click Select locations.</span></span>
8. <span data-ttu-id="4be0a-162">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4be0a-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4be0a-163">В поле "Критерий" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="4be0a-164">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4be0a-164">Click OK.</span></span>
11. <span data-ttu-id="4be0a-165">В поле "Дней между подсчетом циклов" введите число.</span><span class="sxs-lookup"><span data-stu-id="4be0a-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="4be0a-166">Например, в поле "Дней между подсчетом циклов" задано значение 5, работа подсчета циклов будет создаваться каждые пять дней.</span><span class="sxs-lookup"><span data-stu-id="4be0a-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="4be0a-167">Однако если работа подсчета циклов обрабатывается на третий день, следующая работа подсчета циклов будет создана спустя пять дней после последней обработки подсчета циклов, то есть на восьмой день.</span><span class="sxs-lookup"><span data-stu-id="4be0a-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="4be0a-168">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4be0a-168">Click Save.</span></span>
13. <span data-ttu-id="4be0a-169">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4be0a-169">Click New.</span></span>
14. <span data-ttu-id="4be0a-170">В поле "Порядковый номер" введите число.</span><span class="sxs-lookup"><span data-stu-id="4be0a-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="4be0a-171">Порядок сортировки — от наименьшего до наибольшего числа.</span><span class="sxs-lookup"><span data-stu-id="4be0a-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="4be0a-172">Значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="4be0a-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="4be0a-173">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4be0a-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="4be0a-174">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="4be0a-175">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="4be0a-175">Click Save.</span></span>
18. <span data-ttu-id="4be0a-176">Щелкните "Определить запрос продукта".</span><span class="sxs-lookup"><span data-stu-id="4be0a-176">Click Define product query.</span></span>
19. <span data-ttu-id="4be0a-177">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4be0a-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="4be0a-178">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4be0a-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="4be0a-179">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4be0a-179">Click OK.</span></span>
22. <span data-ttu-id="4be0a-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4be0a-180">Close the page.</span></span>

