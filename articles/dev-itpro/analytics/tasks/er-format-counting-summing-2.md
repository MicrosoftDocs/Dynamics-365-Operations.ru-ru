--- 
title: "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a><span data-ttu-id="3a764-103">Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)</span><span class="sxs-lookup"><span data-stu-id="3a764-103">ER Configure format to do counting and summing (Part 2: Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a764-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3a764-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="3a764-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="3a764-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3a764-106">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 1. Создание формата)".</span><span class="sxs-lookup"><span data-stu-id="3a764-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="3a764-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="3a764-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="3a764-108">Создание конфигурации формата для добавления сведений об инвентаризации и суммировании</span><span class="sxs-lookup"><span data-stu-id="3a764-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="3a764-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="3a764-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3a764-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="3a764-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3a764-111">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="3a764-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="3a764-112">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="3a764-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="3a764-113">Допустим, требуется настроить формат, предоставленный Microsoft, добавив строки со сводными сведениями в конец отчета Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3a764-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="3a764-114">Это следует сделать, создав наш собственный экземпляр на основе конфигурации Интрастат из экземпляра Microsoft для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="3a764-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="3a764-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a764-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="3a764-116">В поле "Создать" введите "Производное от имени: Интрастат (DE), Microsoft".</span><span class="sxs-lookup"><span data-stu-id="3a764-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="3a764-117">В поле "Имя" введите "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="3a764-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="3a764-118">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="3a764-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="3a764-119">Настройте этот отчет, чтобы выполнять инвентаризацию и суммирование на основе выходных сведений</span><span class="sxs-lookup"><span data-stu-id="3a764-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="3a764-120">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="3a764-120">Click Designer.</span></span>
2. <span data-ttu-id="3a764-121">Выберите "Да" в поле "Сбор сведений о результате".</span><span class="sxs-lookup"><span data-stu-id="3a764-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="3a764-122">Этот флаг активируется во время выполнения процесса сбора выходных сведения для создания файла Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3a764-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="3a764-123">Необходимо выполнять инвентаризацию для различных направлений Интрастат, поэтому следует добавить специальное перечисление модели в список источников данных конфигурации этого формата.</span><span class="sxs-lookup"><span data-stu-id="3a764-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="3a764-124">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3a764-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="3a764-125">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a764-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="3a764-126">В дереве выберите "Модель данных\Перечисление".</span><span class="sxs-lookup"><span data-stu-id="3a764-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="3a764-127">В поле "Имя" введите "Направление".</span><span class="sxs-lookup"><span data-stu-id="3a764-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="3a764-128">В поле "Перечисление модели" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3a764-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="3a764-129">Выберите значение "Направление".</span><span class="sxs-lookup"><span data-stu-id="3a764-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="3a764-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3a764-130">Click OK.</span></span>
9. <span data-ttu-id="3a764-131">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a764-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="3a764-132">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="3a764-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="3a764-133">В поле "Имя" введите "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="3a764-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="3a764-134">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="3a764-134">Click Edit formula.</span></span>
13. <span data-ttu-id="3a764-135">В поле "Формула" введите "блок".</span><span class="sxs-lookup"><span data-stu-id="3a764-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="3a764-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-136">Click Save.</span></span>
15. <span data-ttu-id="3a764-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-137">Close the page.</span></span>
16. <span data-ttu-id="3a764-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3a764-138">Click OK.</span></span>
17. <span data-ttu-id="3a764-139">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a764-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="3a764-140">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="3a764-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="3a764-141">В поле "Имя" введите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="3a764-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="3a764-142">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="3a764-142">Click Edit formula.</span></span>
21. <span data-ttu-id="3a764-143">В поле "Формула" введите "запись".</span><span class="sxs-lookup"><span data-stu-id="3a764-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="3a764-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-144">Click Save.</span></span>
23. <span data-ttu-id="3a764-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-145">Close the page.</span></span>
24. <span data-ttu-id="3a764-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3a764-146">Click OK.</span></span>
25. <span data-ttu-id="3a764-147">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a764-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="3a764-148">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="3a764-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="3a764-149">В поле "Имя" введите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="3a764-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="3a764-150">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="3a764-150">Click Edit formula.</span></span>
29. <span data-ttu-id="3a764-151">В поле "Формула" введите "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="3a764-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="3a764-152">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-152">Click Save.</span></span>
31. <span data-ttu-id="3a764-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-153">Close the page.</span></span>
32. <span data-ttu-id="3a764-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3a764-154">Click OK.</span></span>
33. <span data-ttu-id="3a764-155">В дереве выберите "Интрастат\Данные".</span><span class="sxs-lookup"><span data-stu-id="3a764-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="3a764-156">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="3a764-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="3a764-157">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-157">Click Add data source.</span></span>
    * <span data-ttu-id="3a764-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="3a764-158">$BlockName</span></span>  
36. <span data-ttu-id="3a764-159">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-159">Click Save.</span></span>
37. <span data-ttu-id="3a764-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-160">Close the page.</span></span>
38. <span data-ttu-id="3a764-161">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="3a764-162">В поле "Формула" введите "IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")".</span><span class="sxs-lookup"><span data-stu-id="3a764-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="3a764-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="3a764-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="3a764-164">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-164">Click Save.</span></span>
41. <span data-ttu-id="3a764-165">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-165">Close the page.</span></span>
    * <span data-ttu-id="3a764-166">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3a764-166">Count the lines of this sequence.</span></span> <span data-ttu-id="3a764-167">Результаты будут использоваться с именем "блок" отдельно для различных направлений.</span><span class="sxs-lookup"><span data-stu-id="3a764-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="3a764-168">Значение "Импорт" будет использоваться для всех проводок поступлений Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3a764-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="3a764-169">Значение "Экспорт" будет использоваться для всех проводок отправок Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3a764-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="3a764-170">Можно считать это виртуальной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="3a764-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="3a764-171">Для каждой проводки имеется строка, в которой первый столбец "блок" заполнен значениями "Импорт" и "Экспорт" соответственно.</span><span class="sxs-lookup"><span data-stu-id="3a764-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="3a764-172">В дереве разверните узел "Интрастат\Данные: последовательность".</span><span class="sxs-lookup"><span data-stu-id="3a764-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="3a764-173">В дереве выберите узел "Интрастат\Данные: последовательность\Поступления?".</span><span class="sxs-lookup"><span data-stu-id="3a764-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="3a764-174">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="3a764-175">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3a764-175">Count the lines of this sequence.</span></span> <span data-ttu-id="3a764-176">Результаты будут запомнены с использованием имени "запись".</span><span class="sxs-lookup"><span data-stu-id="3a764-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="3a764-177">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="3a764-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="3a764-178">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-178">Click Add data source.</span></span>
47. <span data-ttu-id="3a764-179">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-179">Click Save.</span></span>
48. <span data-ttu-id="3a764-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-180">Close the page.</span></span>
49. <span data-ttu-id="3a764-181">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="3a764-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="3a764-182">В поле "Формула" введите "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="3a764-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="3a764-183">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-183">Click Save.</span></span>
52. <span data-ttu-id="3a764-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-184">Close the page.</span></span>
    * <span data-ttu-id="3a764-185">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3a764-185">Count the lines of this sequence.</span></span> <span data-ttu-id="3a764-186">Результаты будут использоваться с именем "запись" отдельно для кодов товара.</span><span class="sxs-lookup"><span data-stu-id="3a764-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="3a764-187">Можно считать это виртуальной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="3a764-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="3a764-188">Для каждой проводки имеется строка, в которой столбец "блок" заполняется значениями "Импорт" и "Экспорт" соответственно, а второй блок "запись" заполняется значением кода товара.</span><span class="sxs-lookup"><span data-stu-id="3a764-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="3a764-189">В дереве выберите узел "Интрастат\Данные: последовательность\Отправки?".</span><span class="sxs-lookup"><span data-stu-id="3a764-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="3a764-190">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="3a764-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="3a764-191">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="3a764-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="3a764-192">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-192">Click Add data source.</span></span>
57. <span data-ttu-id="3a764-193">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-193">Click Save.</span></span>
58. <span data-ttu-id="3a764-194">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-194">Close the page.</span></span>
59. <span data-ttu-id="3a764-195">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="3a764-196">В поле "Формула" введите "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="3a764-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="3a764-197">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="3a764-197">Click Save.</span></span>
62. <span data-ttu-id="3a764-198">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-198">Close the page.</span></span>
63. <span data-ttu-id="3a764-199">В дереве разверните узел "Интрастат\Данные: последовательность\Отправки: последовательность?".</span><span class="sxs-lookup"><span data-stu-id="3a764-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="3a764-200">В дереве разверните узел "Интрастат\Данные: последовательность\Отправки: последовательность?\Запись = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="3a764-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="3a764-201">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="3a764-201">Click the Format tab.</span></span>
66. <span data-ttu-id="3a764-202">В дереве выберите "Интрастат\Данные\Отправки\Запись\Сумма накладной в Евро".</span><span class="sxs-lookup"><span data-stu-id="3a764-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="3a764-203">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3a764-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="3a764-204">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="3a764-205">В дереве выберите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="3a764-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="3a764-206">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-206">Click Add data source.</span></span>
71. <span data-ttu-id="3a764-207">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-207">Click Save.</span></span>
72. <span data-ttu-id="3a764-208">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-208">Close the page.</span></span>
    * <span data-ttu-id="3a764-209">Просуммируйте значения сумм, по которым выставлены накладные, для строк в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3a764-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="3a764-210">Результаты будут использоваться с именем "InvoicedAmountEUR" отдельно для различных направлений Интрастат и кодов товара.</span><span class="sxs-lookup"><span data-stu-id="3a764-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="3a764-211">Можно считать это виртуальным созданием таблицы Excel.</span><span class="sxs-lookup"><span data-stu-id="3a764-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="3a764-212">Для каждой проводки имеется строка, в которой первый столбец "блок" заполнен значениями "Импорт" и "Экспорт" соответственно.</span><span class="sxs-lookup"><span data-stu-id="3a764-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="3a764-213">Второй блок "запись" заполняется значением кода товара, а третий столбец "InvoicedAmountEUR" заполняется значением суммы из накладной.</span><span class="sxs-lookup"><span data-stu-id="3a764-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="3a764-214">В дереве разверните узел "Интрастат\Данные\Поступления?".</span><span class="sxs-lookup"><span data-stu-id="3a764-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="3a764-215">В дереве разверните узел "Интрастат\Данные\Поступления?\Запись = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="3a764-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="3a764-216">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="3a764-216">Click the Format tab.</span></span>
76. <span data-ttu-id="3a764-217">В дереве выберите "Интрастат\Данные\Поступления\Запись\Сумма накладной в Евро".</span><span class="sxs-lookup"><span data-stu-id="3a764-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="3a764-218">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3a764-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="3a764-219">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="3a764-220">В дереве выберите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="3a764-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="3a764-221">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3a764-221">Click Add data source.</span></span>
81. <span data-ttu-id="3a764-222">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-222">Click Save.</span></span>
82. <span data-ttu-id="3a764-223">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-223">Close the page.</span></span>
83. <span data-ttu-id="3a764-224">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3a764-224">Click Save.</span></span>
84. <span data-ttu-id="3a764-225">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a764-225">Close the page.</span></span>


