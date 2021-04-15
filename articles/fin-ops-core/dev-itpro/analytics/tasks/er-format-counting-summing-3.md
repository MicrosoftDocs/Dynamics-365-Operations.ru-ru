---
title: Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)
description: В этой теме описывается, как настроить формат электронный отчетности для выполнения инвентаризации и суммирования на основе данных уже созданного текстового вывода. (Часть 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749005"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="da792-104">Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)</span><span class="sxs-lookup"><span data-stu-id="da792-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da792-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="da792-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="da792-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="da792-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="da792-107">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)".</span><span class="sxs-lookup"><span data-stu-id="da792-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="da792-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="da792-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="da792-109">Настройка этого отчета для использования сведений об инвентаризации и суммировании</span><span class="sxs-lookup"><span data-stu-id="da792-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="da792-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="da792-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="da792-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="da792-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="da792-112">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="da792-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="da792-113">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="da792-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="da792-114">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="da792-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="da792-115">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="da792-115">Click Designer.</span></span>
7. <span data-ttu-id="da792-116">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="da792-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="da792-117">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="da792-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="da792-118">Добавьте новый источник данных для получения списка запомненных блоков.</span><span class="sxs-lookup"><span data-stu-id="da792-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="da792-119">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="da792-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="da792-120">В поле "Имя" введите "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="da792-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="da792-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="da792-121">$BlocksList</span></span>  
11. <span data-ttu-id="da792-122">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="da792-122">Click Edit formula.</span></span>
12. <span data-ttu-id="da792-123">В дереве выберите "Функции сбора данных\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="da792-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="da792-124">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="da792-124">Click Add function.</span></span>
14. <span data-ttu-id="da792-125">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="da792-125">Click Add data source.</span></span>
15. <span data-ttu-id="da792-126">В поле "Формула" введите "COLLECTEDLIST('$BlockName', ".</span><span class="sxs-lookup"><span data-stu-id="da792-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="da792-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="da792-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="da792-128">В поле "Формула" введите "COLLECTEDLIST('$BlockName', "\*")".</span><span class="sxs-lookup"><span data-stu-id="da792-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="da792-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="da792-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="da792-130">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="da792-130">Click Save.</span></span>
    * <span data-ttu-id="da792-131">Шаблон "\*" означает, что все блоки будут включены в список для этой записи.</span><span class="sxs-lookup"><span data-stu-id="da792-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="da792-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="da792-132">Close the page.</span></span>
19. <span data-ttu-id="da792-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="da792-133">Click OK.</span></span>
20. <span data-ttu-id="da792-134">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="da792-134">Click the Format tab.</span></span>
21. <span data-ttu-id="da792-135">В дереве выберите "Интрастат\Данные".</span><span class="sxs-lookup"><span data-stu-id="da792-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="da792-136">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="da792-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="da792-137">В дереве выберите "Текст\Последовательность".</span><span class="sxs-lookup"><span data-stu-id="da792-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="da792-138">В поле "Имя" введите "Итого по блокам".</span><span class="sxs-lookup"><span data-stu-id="da792-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="da792-139">Итого по блокам</span><span class="sxs-lookup"><span data-stu-id="da792-139">Totals by blocks</span></span>  
25. <span data-ttu-id="da792-140">В поле "Специальные знаки", выберите "Создать строку — Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="da792-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="da792-141">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="da792-141">Click OK.</span></span>
27. <span data-ttu-id="da792-142">В дереве выберите узел "Интрастат\Данные\Итого по блокам".</span><span class="sxs-lookup"><span data-stu-id="da792-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="da792-143">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="da792-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="da792-144">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="da792-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="da792-145">В поле "Имя" введите "Код блока".</span><span class="sxs-lookup"><span data-stu-id="da792-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="da792-146">Код блока</span><span class="sxs-lookup"><span data-stu-id="da792-146">Block code</span></span>  
31. <span data-ttu-id="da792-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="da792-147">Click OK.</span></span>
32. <span data-ttu-id="da792-148">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="da792-148">Click Add String.</span></span>
33. <span data-ttu-id="da792-149">В поле "Имя" введите "Инвентаризация строк".</span><span class="sxs-lookup"><span data-stu-id="da792-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="da792-150">Инвентаризация строк</span><span class="sxs-lookup"><span data-stu-id="da792-150">Lines counting</span></span>  
34. <span data-ttu-id="da792-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="da792-151">Click OK.</span></span>
35. <span data-ttu-id="da792-152">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="da792-152">Click Add String.</span></span>
36. <span data-ttu-id="da792-153">В поле "Имя" введите "Итоговая сумма".</span><span class="sxs-lookup"><span data-stu-id="da792-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="da792-154">Итоговая сумма</span><span class="sxs-lookup"><span data-stu-id="da792-154">Total amount</span></span>  
37. <span data-ttu-id="da792-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="da792-155">Click OK.</span></span>
38. <span data-ttu-id="da792-156">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="da792-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="da792-157">В дереве выберите "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="da792-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="da792-158">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="da792-158">Click Bind.</span></span>
    * <span data-ttu-id="da792-159">Создайте сводную строка для каждого запомненного блока.</span><span class="sxs-lookup"><span data-stu-id="da792-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="da792-160">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="da792-160">Click the Format tab.</span></span>
42. <span data-ttu-id="da792-161">В дереве выберите узел "Интрастат\Данные\Итого по блокам\Код блока".</span><span class="sxs-lookup"><span data-stu-id="da792-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="da792-162">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="da792-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="da792-163">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="da792-163">Click Edit formula.</span></span>
45. <span data-ttu-id="da792-164">В поле "Формула" введите «"Код блока: " & ».</span><span class="sxs-lookup"><span data-stu-id="da792-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="da792-165">"Код блока: " &</span><span class="sxs-lookup"><span data-stu-id="da792-165">"Block id: " &</span></span>  
46. <span data-ttu-id="da792-166">В дереве разверните узел "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="da792-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="da792-167">В дереве выберите "$BlocksList\Значение".</span><span class="sxs-lookup"><span data-stu-id="da792-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="da792-168">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="da792-168">Click Add data source.</span></span>
49. <span data-ttu-id="da792-169">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="da792-169">Click Save.</span></span>
50. <span data-ttu-id="da792-170">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="da792-170">Close the page.</span></span>
51. <span data-ttu-id="da792-171">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="da792-171">Click the Format tab.</span></span>
52. <span data-ttu-id="da792-172">В дереве выберите узел "Интрастат\Данные\Итого по блокам\Инвентаризация строк".</span><span class="sxs-lookup"><span data-stu-id="da792-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="da792-173">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="da792-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="da792-174">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="da792-174">Click Edit formula.</span></span>
    * <span data-ttu-id="da792-175">Создайте выходные данные для числа строк для каждого блока, представленного в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="da792-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="da792-176">В поле "Формула", введите «"Число строк в этом блоке: " & ».</span><span class="sxs-lookup"><span data-stu-id="da792-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="da792-177">"Число строк в этом блоке: " &</span><span class="sxs-lookup"><span data-stu-id="da792-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="da792-178">В поле "Формула", введите «"Число строк в этом блоке: " & TEXT(».</span><span class="sxs-lookup"><span data-stu-id="da792-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="da792-179">"Число строк в этом блоке: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="da792-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="da792-180">В дереве выберите "Функции сбора данных\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="da792-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="da792-181">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="da792-181">Click Add function.</span></span>
59. <span data-ttu-id="da792-182">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="da792-182">Click Add data source.</span></span>
60. <span data-ttu-id="da792-183">В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', ».</span><span class="sxs-lookup"><span data-stu-id="da792-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="da792-184">"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="da792-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="da792-185">В дереве разверните узел "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="da792-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="da792-186">В дереве выберите "$BlocksList\Значение".</span><span class="sxs-lookup"><span data-stu-id="da792-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="da792-187">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="da792-187">Click Add data source.</span></span>
64. <span data-ttu-id="da792-188">В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ».</span><span class="sxs-lookup"><span data-stu-id="da792-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="da792-189">"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="da792-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="da792-190">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="da792-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="da792-191">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="da792-191">Click Add data source.</span></span>
67. <span data-ttu-id="da792-192">В поле "Формула" введите «"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))».</span><span class="sxs-lookup"><span data-stu-id="da792-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="da792-193">"Число строк в этом блоке: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="da792-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="da792-194">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="da792-194">Click Save.</span></span>
69. <span data-ttu-id="da792-195">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="da792-195">Close the page.</span></span>
70. <span data-ttu-id="da792-196">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="da792-196">Click the Format tab.</span></span>
71. <span data-ttu-id="da792-197">В дереве выберите узел "Интрастат\Данные\Итого по блокам\Итоговая сумма".</span><span class="sxs-lookup"><span data-stu-id="da792-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="da792-198">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="da792-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="da792-199">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="da792-199">Click Edit formula.</span></span>
    * <span data-ttu-id="da792-200">Создайте выходные данные, которые будут итоговой суммой по выставленным накладным для каждого блока, представленного в этом отчете.</span><span class="sxs-lookup"><span data-stu-id="da792-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="da792-201">В поле "Формула" введите «"Итого по выставленным накладным: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))».</span><span class="sxs-lookup"><span data-stu-id="da792-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="da792-202">"Итого по выставленным накладным: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="da792-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="da792-203">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="da792-203">Click Save.</span></span>
76. <span data-ttu-id="da792-204">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="da792-204">Close the page.</span></span>
77. <span data-ttu-id="da792-205">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="da792-205">Click Save.</span></span>
78. <span data-ttu-id="da792-206">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="da792-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]