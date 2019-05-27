---
title: Настройка сеток компенсаций
description: Сетки компенсации используются для определения и ведения структур оплаты для фиксированных компенсационных выплат.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0caebb2dfbff12545610aa6438dccbec84db3f9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509742"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="99028-103">Настройка сеток компенсаций</span><span class="sxs-lookup"><span data-stu-id="99028-103">Set up compensation grids</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99028-104">Сетки компенсации используются для определения и ведения структур оплаты для фиксированных компенсационных выплат.</span><span class="sxs-lookup"><span data-stu-id="99028-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="99028-105">Сетки компенсации можно совместно использовать между несколькими планами или копировать при создании нового плана компенсационных выплат.</span><span class="sxs-lookup"><span data-stu-id="99028-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="99028-106">Перед созданием сетки компенсации необходимо настроить уровни и опорные точки.</span><span class="sxs-lookup"><span data-stu-id="99028-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="99028-107">В этом примере создается новый тип сетки компенсации с помощью демонстрационных данных для уровней и опорных точек.</span><span class="sxs-lookup"><span data-stu-id="99028-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="99028-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="99028-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="99028-109">Настройка информации о сетке компенсации</span><span class="sxs-lookup"><span data-stu-id="99028-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="99028-110">Перейдите в "Управление персоналом" > "Компенсация" > "Фиксированная компенсация" > "Сетки компенсации".</span><span class="sxs-lookup"><span data-stu-id="99028-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="99028-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="99028-111">Click New.</span></span>
3. <span data-ttu-id="99028-112">В поле "Сетка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="99028-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="99028-114">В поле "Тип" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="99028-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="99028-115">В поле "Установка опорной точки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="99028-116">В поле "Валюта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="99028-117">В поле "Валюта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="99028-118">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="99028-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="99028-119">Добавление уровней к структуре компенсаций</span><span class="sxs-lookup"><span data-stu-id="99028-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="99028-120">Щелкните "Структура компенсации".</span><span class="sxs-lookup"><span data-stu-id="99028-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="99028-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="99028-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="99028-122">В поле "Уровень" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="99028-123">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="99028-123">Click New.</span></span>
5. <span data-ttu-id="99028-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="99028-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="99028-125">В поле "Уровень" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="99028-126">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="99028-126">Click New.</span></span>
8. <span data-ttu-id="99028-127">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="99028-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="99028-128">В поле "Уровень" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="99028-129">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="99028-129">Click New.</span></span>
11. <span data-ttu-id="99028-130">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="99028-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="99028-131">В поле "Уровень" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="99028-132">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="99028-132">Click New.</span></span>
14. <span data-ttu-id="99028-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="99028-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="99028-134">В поле "Уровень" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="99028-135">Заполнение структуры компенсаций значениями</span><span class="sxs-lookup"><span data-stu-id="99028-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="99028-136">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="99028-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="99028-137">В этот момент значения компенсации можно вручную ввести в каждое поле в таблице или можно использовать функцию массового изменения для простого заполнения нескольких полей и выполнения основных расчетов.</span><span class="sxs-lookup"><span data-stu-id="99028-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="99028-138">Щелкните "Массовое изменение".</span><span class="sxs-lookup"><span data-stu-id="99028-138">Click Mass change.</span></span>
    * <span data-ttu-id="99028-139">Для данной сетки сначала применяется значение средней точки для первого уровня ко всем полям в таблице.</span><span class="sxs-lookup"><span data-stu-id="99028-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="99028-140">Это будет основой для матрицы компенсации.</span><span class="sxs-lookup"><span data-stu-id="99028-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="99028-141">В поле "Тип корректировки" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="99028-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="99028-142">В поле "Сумма корректировки" введите число.</span><span class="sxs-lookup"><span data-stu-id="99028-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="99028-143">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="99028-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="99028-144">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="99028-145">Теперь будет использоваться функция массового пошагового изменения сумм на каждом последующем подуровне на некоторый процент от суммы.</span><span class="sxs-lookup"><span data-stu-id="99028-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="99028-146">В этом примере каждый уровень будет иметь разброс 12,5% между средними точками.</span><span class="sxs-lookup"><span data-stu-id="99028-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="99028-147">В поле "Тип корректировки" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="99028-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="99028-148">В поле "Сумма корректировки" введите число.</span><span class="sxs-lookup"><span data-stu-id="99028-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="99028-149">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="99028-150">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="99028-151">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="99028-152">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="99028-153">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="99028-154">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="99028-155">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="99028-156">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="99028-157">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="99028-158">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="99028-159">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="99028-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="99028-160">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="99028-161">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="99028-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="99028-162">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="99028-163">Теперь используем функцию массового изменения для корректировки минимальных и максимальных опорных точек для каждого уровня.</span><span class="sxs-lookup"><span data-stu-id="99028-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="99028-164">В этом примере будет использоваться разброс 50%, чтобы минимальную опорную точку скорректировать на –20%, а максимальную — на +20%.</span><span class="sxs-lookup"><span data-stu-id="99028-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="99028-165">В поле "Сумма корректировки" введите число.</span><span class="sxs-lookup"><span data-stu-id="99028-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="99028-166">В поле "Опорная точка" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="99028-167">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="99028-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="99028-168">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="99028-169">В поле "Сумма корректировки" введите число.</span><span class="sxs-lookup"><span data-stu-id="99028-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="99028-170">В поле "Опорная точка" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="99028-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="99028-171">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="99028-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="99028-172">Щелкните "Применить к сетке".</span><span class="sxs-lookup"><span data-stu-id="99028-172">Click Apply to grid.</span></span>

