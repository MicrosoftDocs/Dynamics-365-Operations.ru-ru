--- 
title: "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="a3dca-103">Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)</span><span class="sxs-lookup"><span data-stu-id="a3dca-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3dca-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a3dca-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a3dca-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="a3dca-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a3dca-106">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)".</span><span class="sxs-lookup"><span data-stu-id="a3dca-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="a3dca-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="a3dca-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="a3dca-108">Настройка этого отчета для использования сведений об инвентаризации и суммировании</span><span class="sxs-lookup"><span data-stu-id="a3dca-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="a3dca-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="a3dca-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a3dca-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="a3dca-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a3dca-111">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="a3dca-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="a3dca-112">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="a3dca-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="a3dca-113">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="a3dca-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="a3dca-114">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="a3dca-114">Click Designer.</span></span>
7. <span data-ttu-id="a3dca-115">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a3dca-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="a3dca-116">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a3dca-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="a3dca-117">Добавьте новый источник данных для получения списка запомненных блоков.</span><span class="sxs-lookup"><span data-stu-id="a3dca-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="a3dca-118">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="a3dca-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="a3dca-119">В поле "Имя" введите "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="a3dca-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="a3dca-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="a3dca-120">$BlocksList</span></span>  
11. <span data-ttu-id="a3dca-121">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="a3dca-121">Click Edit formula.</span></span>
12. <span data-ttu-id="a3dca-122">В дереве выберите "Функции сбора данных\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="a3dca-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="a3dca-123">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="a3dca-123">Click Add function.</span></span>
14. <span data-ttu-id="a3dca-124">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="a3dca-124">Click Add data source.</span></span>
15. <span data-ttu-id="a3dca-125">В поле "Формула" введите "COLLECTEDLIST('$BlockName', ".</span><span class="sxs-lookup"><span data-stu-id="a3dca-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="a3dca-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="a3dca-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="a3dca-127">В поле "Формула" введите "COLLECTEDLIST('$BlockName', "\*")".</span><span class="sxs-lookup"><span data-stu-id="a3dca-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="a3dca-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="a3dca-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="a3dca-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3dca-129">Click Save.</span></span>
    * <span data-ttu-id="a3dca-130">Шаблон "\*" означает, что все блоки будут включены в список для этой записи.</span><span class="sxs-lookup"><span data-stu-id="a3dca-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="a3dca-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a3dca-131">Close the page.</span></span>
19. <span data-ttu-id="a3dca-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a3dca-132">Click OK.</span></span>
20. <span data-ttu-id="a3dca-133">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="a3dca-133">Click the Format tab.</span></span>
21. <span data-ttu-id="a3dca-134">В дереве выберите "Интрастат\Данные".</span><span class="sxs-lookup"><span data-stu-id="a3dca-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="a3dca-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a3dca-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a3dca-136">В дереве выберите "Текст\Последовательность".</span><span class="sxs-lookup"><span data-stu-id="a3dca-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="a3dca-137">В поле "Имя" введите "Итого по блокам".</span><span class="sxs-lookup"><span data-stu-id="a3dca-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="a3dca-138">Итого по блокам</span><span class="sxs-lookup"><span data-stu-id="a3dca-138">Totals by blocks</span></span>  
25. <span data-ttu-id="a3dca-139">В поле "Специальные знаки", выберите "Создать строку — Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="a3dca-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="a3dca-140">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="a3dca-140">Click OK.</span></span>
27. <span data-ttu-id="a3dca-141">В дереве выберите узел "Интрастат\Данные\Итого по блокам".</span><span class="sxs-lookup"><span data-stu-id="a3dca-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="a3dca-142">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a3dca-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="a3dca-143">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="a3dca-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="a3dca-144">В поле "Имя" введите "Код блока".</span><span class="sxs-lookup"><span data-stu-id="a3dca-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="a3dca-145">Код блока</span><span class="sxs-lookup"><span data-stu-id="a3dca-145">Block code</span></span>  
31. <span data-ttu-id="a3dca-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a3dca-146">Click OK.</span></span>
32. <span data-ttu-id="a3dca-147">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="a3dca-147">Click Add String.</span></span>
33. <span data-ttu-id="a3dca-148">В поле "Имя" введите "Инвентаризация строк".</span><span class="sxs-lookup"><span data-stu-id="a3dca-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="a3dca-149">Инвентаризация строк</span><span class="sxs-lookup"><span data-stu-id="a3dca-149">Lines counting</span></span>  
34. <span data-ttu-id="a3dca-150">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a3dca-150">Click OK.</span></span>
35. <span data-ttu-id="a3dca-151">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="a3dca-151">Click Add String.</span></span>
36. <span data-ttu-id="a3dca-152">В поле "Имя" введите "Итоговая сумма".</span><span class="sxs-lookup"><span data-stu-id="a3dca-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="a3dca-153">Итоговая сумма</span><span class="sxs-lookup"><span data-stu-id="a3dca-153">Total amount</span></span>  
37. <span data-ttu-id="a3dca-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a3dca-154">Click OK.</span></span>
38. <span data-ttu-id="a3dca-155">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a3dca-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="a3dca-156">В дереве выберите "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="a3dca-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="a3dca-157">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="a3dca-157">Click Bind.</span></span>
    * <span data-ttu-id="a3dca-158">Создайте сводную строка для каждого запомненного блока.</span><span class="sxs-lookup"><span data-stu-id="a3dca-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="a3dca-159">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="a3dca-159">Click the Format tab.</span></span>
42. <span data-ttu-id="a3dca-160">В дереве выберите узел "Интрастат\Данные\Итого по блокам\Код блока".</span><span class="sxs-lookup"><span data-stu-id="a3dca-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="a3dca-161">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a3dca-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="a3dca-162">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="a3dca-162">Click Edit formula.</span></span>
45. <span data-ttu-id="a3dca-163">В поле "Формула" введите «"Код блока: " & ».</span><span class="sxs-lookup"><span data-stu-id="a3dca-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="a3dca-164">"Код блока: " &</span><span class="sxs-lookup"><span data-stu-id="a3dca-164">"Block id: " &</span></span>  
46. <span data-ttu-id="a3dca-165">В дереве разверните узел "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="a3dca-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="a3dca-166">В дереве выберите "$BlocksList\Значение".</span><span class="sxs-lookup"><span data-stu-id="a3dca-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="a3dca-167">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="a3dca-167">Click Add data source.</span></span>
49. <span data-ttu-id="a3dca-168">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3dca-168">Click Save.</span></span>
50. <span data-ttu-id="a3dca-169">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a3dca-169">Close the page.</span></span>
51. <span data-ttu-id="a3dca-170">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="a3dca-170">Click the Format tab.</span></span>
52. <span data-ttu-id="a3dca-171">В дереве выберите узел "Интрастат\Данные\Итого по блокам\Инвентаризация строк".</span><span class="sxs-lookup"><span data-stu-id="a3dca-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="a3dca-172">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a3dca-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="a3dca-173">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="a3dca-173">Click Edit formula.</span></span>
    * <span data-ttu-id="a3dca-174">Создайте выходные данные для числа строк для каждого блока, представленного в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="a3dca-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="a3dca-175">В поле "Формула", введите «"Число строк в этом блоке: " & ».</span><span class="sxs-lookup"><span data-stu-id="a3dca-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="a3dca-176">"Число строк в этом блоке: " &</span><span class="sxs-lookup"><span data-stu-id="a3dca-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="a3dca-177">В поле "Формула", введите «"Число строк в этом блоке: " & TEXT(».</span><span class="sxs-lookup"><span data-stu-id="a3dca-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="a3dca-178">"Число строк в этом блоке: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="a3dca-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="a3dca-179">В дереве выберите "Функции сбора данных\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="a3dca-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="a3dca-180">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="a3dca-180">Click Add function.</span></span>
59. <span data-ttu-id="a3dca-181">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="a3dca-181">Click Add data source.</span></span>
60. <span data-ttu-id="a3dca-182">В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', ».</span><span class="sxs-lookup"><span data-stu-id="a3dca-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="a3dca-183">"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="a3dca-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="a3dca-184">В дереве разверните узел "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="a3dca-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="a3dca-185">В дереве выберите "$BlocksList\Значение".</span><span class="sxs-lookup"><span data-stu-id="a3dca-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="a3dca-186">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="a3dca-186">Click Add data source.</span></span>
64. <span data-ttu-id="a3dca-187">В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ».</span><span class="sxs-lookup"><span data-stu-id="a3dca-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="a3dca-188">"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="a3dca-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="a3dca-189">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="a3dca-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="a3dca-190">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="a3dca-190">Click Add data source.</span></span>
67. <span data-ttu-id="a3dca-191">В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))».</span><span class="sxs-lookup"><span data-stu-id="a3dca-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="a3dca-192">"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="a3dca-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="a3dca-193">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3dca-193">Click Save.</span></span>
69. <span data-ttu-id="a3dca-194">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a3dca-194">Close the page.</span></span>
70. <span data-ttu-id="a3dca-195">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="a3dca-195">Click the Format tab.</span></span>
71. <span data-ttu-id="a3dca-196">В дереве выберите узел "Интрастат\Данные\Итого по блокам\Итоговая сумма".</span><span class="sxs-lookup"><span data-stu-id="a3dca-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="a3dca-197">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="a3dca-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="a3dca-198">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="a3dca-198">Click Edit formula.</span></span>
    * <span data-ttu-id="a3dca-199">Создайте выходные данные, которые будут итоговой суммой по выставленным накладным для каждого блока, представленного в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="a3dca-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="a3dca-200">В поле "Формула" введите «"Итого по выставленным накладным: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))».</span><span class="sxs-lookup"><span data-stu-id="a3dca-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="a3dca-201">"Итого по выставленным накладным: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="a3dca-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="a3dca-202">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3dca-202">Click Save.</span></span>
76. <span data-ttu-id="a3dca-203">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a3dca-203">Close the page.</span></span>
77. <span data-ttu-id="a3dca-204">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a3dca-204">Click Save.</span></span>
78. <span data-ttu-id="a3dca-205">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a3dca-205">Close the page.</span></span>


