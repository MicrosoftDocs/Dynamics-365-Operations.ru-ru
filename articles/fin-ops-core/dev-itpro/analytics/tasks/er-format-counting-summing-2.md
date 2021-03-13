---
title: Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)
description: В этой теме описывается, как настроить формат электронный отчетности для выполнения инвентаризации и суммирования на основе данных уже созданного текстового вывода. (Часть 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6215fe1f32bcb4833bd009b7c33e09edbba17817
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093005"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="3b657-104">Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 2. Настройка вычислений)</span><span class="sxs-lookup"><span data-stu-id="3b657-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b657-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3b657-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="3b657-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="3b657-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="3b657-107">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 1. Создание формата)".</span><span class="sxs-lookup"><span data-stu-id="3b657-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="3b657-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="3b657-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="3b657-109">Создание конфигурации формата для добавления сведений об инвентаризации и суммировании</span><span class="sxs-lookup"><span data-stu-id="3b657-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="3b657-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="3b657-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3b657-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="3b657-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3b657-112">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="3b657-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="3b657-113">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="3b657-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="3b657-114">Допустим, требуется настроить формат, предоставленный Microsoft, добавив строки со сводными сведениями в конец отчета Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3b657-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="3b657-115">Это следует сделать, создав наш собственный экземпляр на основе конфигурации Интрастат из экземпляра Microsoft для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="3b657-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="3b657-116">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b657-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="3b657-117">В поле "Создать" введите "Производное от имени: Интрастат (DE), Microsoft".</span><span class="sxs-lookup"><span data-stu-id="3b657-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="3b657-118">В поле "Имя" введите "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="3b657-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="3b657-119">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="3b657-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="3b657-120">Настройте этот отчет, чтобы выполнять инвентаризацию и суммирование на основе выходных сведений</span><span class="sxs-lookup"><span data-stu-id="3b657-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="3b657-121">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="3b657-121">Click Designer.</span></span>
2. <span data-ttu-id="3b657-122">Выберите "Да" в поле "Сбор сведений о результате".</span><span class="sxs-lookup"><span data-stu-id="3b657-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="3b657-123">Этот флаг активируется во время выполнения процесса сбора выходных сведения для создания файла Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3b657-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="3b657-124">Необходимо выполнять инвентаризацию для различных направлений Интрастат, поэтому следует добавить специальное перечисление модели в список источников данных конфигурации этого формата.</span><span class="sxs-lookup"><span data-stu-id="3b657-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="3b657-125">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3b657-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="3b657-126">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b657-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="3b657-127">В дереве выберите "Модель данных\Перечисление".</span><span class="sxs-lookup"><span data-stu-id="3b657-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="3b657-128">В поле "Имя" введите "Направление".</span><span class="sxs-lookup"><span data-stu-id="3b657-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="3b657-129">В поле "Перечисление модели" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3b657-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="3b657-130">Выберите значение "Направление".</span><span class="sxs-lookup"><span data-stu-id="3b657-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="3b657-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3b657-131">Click OK.</span></span>
9. <span data-ttu-id="3b657-132">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b657-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="3b657-133">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="3b657-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="3b657-134">В поле "Имя" введите "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="3b657-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="3b657-135">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="3b657-135">Click Edit formula.</span></span>
13. <span data-ttu-id="3b657-136">В поле "Формула" введите "блок".</span><span class="sxs-lookup"><span data-stu-id="3b657-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="3b657-137">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-137">Click Save.</span></span>
15. <span data-ttu-id="3b657-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-138">Close the page.</span></span>
16. <span data-ttu-id="3b657-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3b657-139">Click OK.</span></span>
17. <span data-ttu-id="3b657-140">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b657-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="3b657-141">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="3b657-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="3b657-142">В поле "Имя" введите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="3b657-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="3b657-143">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="3b657-143">Click Edit formula.</span></span>
21. <span data-ttu-id="3b657-144">В поле "Формула" введите "запись".</span><span class="sxs-lookup"><span data-stu-id="3b657-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="3b657-145">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-145">Click Save.</span></span>
23. <span data-ttu-id="3b657-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-146">Close the page.</span></span>
24. <span data-ttu-id="3b657-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3b657-147">Click OK.</span></span>
25. <span data-ttu-id="3b657-148">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b657-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="3b657-149">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="3b657-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="3b657-150">В поле "Имя" введите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="3b657-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="3b657-151">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="3b657-151">Click Edit formula.</span></span>
29. <span data-ttu-id="3b657-152">В поле "Формула" введите "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="3b657-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="3b657-153">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-153">Click Save.</span></span>
31. <span data-ttu-id="3b657-154">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-154">Close the page.</span></span>
32. <span data-ttu-id="3b657-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3b657-155">Click OK.</span></span>
33. <span data-ttu-id="3b657-156">В дереве выберите "Интрастат\Данные".</span><span class="sxs-lookup"><span data-stu-id="3b657-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="3b657-157">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="3b657-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="3b657-158">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-158">Click Add data source.</span></span>
    * <span data-ttu-id="3b657-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="3b657-159">$BlockName</span></span>  
36. <span data-ttu-id="3b657-160">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="3b657-160">Click Save.</span></span>
37. <span data-ttu-id="3b657-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-161">Close the page.</span></span>
38. <span data-ttu-id="3b657-162">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="3b657-163">В поле "Формула" введите "IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")".</span><span class="sxs-lookup"><span data-stu-id="3b657-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="3b657-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="3b657-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="3b657-165">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-165">Click Save.</span></span>
41. <span data-ttu-id="3b657-166">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-166">Close the page.</span></span>
    * <span data-ttu-id="3b657-167">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3b657-167">Count the lines of this sequence.</span></span> <span data-ttu-id="3b657-168">Результаты будут использоваться с именем "блок" отдельно для различных направлений.</span><span class="sxs-lookup"><span data-stu-id="3b657-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="3b657-169">Значение "Импорт" будет использоваться для всех проводок поступлений Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3b657-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="3b657-170">Значение "Экспорт" будет использоваться для всех проводок отправок Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3b657-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="3b657-171">Можно считать это виртуальной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="3b657-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="3b657-172">Для каждой проводки имеется строка, в которой первый столбец "блок" заполнен значениями "Импорт" и "Экспорт" соответственно.</span><span class="sxs-lookup"><span data-stu-id="3b657-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="3b657-173">В дереве разверните узел "Интрастат\Данные: последовательность".</span><span class="sxs-lookup"><span data-stu-id="3b657-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="3b657-174">В дереве выберите узел "Интрастат\Данные: последовательность\Поступления?".</span><span class="sxs-lookup"><span data-stu-id="3b657-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="3b657-175">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="3b657-176">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3b657-176">Count the lines of this sequence.</span></span> <span data-ttu-id="3b657-177">Результаты будут запомнены с использованием имени "запись".</span><span class="sxs-lookup"><span data-stu-id="3b657-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="3b657-178">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="3b657-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="3b657-179">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-179">Click Add data source.</span></span>
47. <span data-ttu-id="3b657-180">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="3b657-180">Click Save.</span></span>
48. <span data-ttu-id="3b657-181">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-181">Close the page.</span></span>
49. <span data-ttu-id="3b657-182">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="3b657-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="3b657-183">В поле "Формула" введите "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="3b657-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="3b657-184">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-184">Click Save.</span></span>
52. <span data-ttu-id="3b657-185">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-185">Close the page.</span></span>
    * <span data-ttu-id="3b657-186">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3b657-186">Count the lines of this sequence.</span></span> <span data-ttu-id="3b657-187">Результаты будут использоваться с именем "запись" отдельно для кодов товара.</span><span class="sxs-lookup"><span data-stu-id="3b657-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="3b657-188">Можно считать это виртуальной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="3b657-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="3b657-189">Для каждой проводки имеется строка, в которой столбец "блок" заполняется значениями "Импорт" и "Экспорт" соответственно, а второй блок "запись" заполняется значением кода товара.</span><span class="sxs-lookup"><span data-stu-id="3b657-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="3b657-190">В дереве выберите узел "Интрастат\Данные: последовательность\Отправки?".</span><span class="sxs-lookup"><span data-stu-id="3b657-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="3b657-191">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="3b657-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="3b657-192">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="3b657-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="3b657-193">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-193">Click Add data source.</span></span>
57. <span data-ttu-id="3b657-194">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="3b657-194">Click Save.</span></span>
58. <span data-ttu-id="3b657-195">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-195">Close the page.</span></span>
59. <span data-ttu-id="3b657-196">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="3b657-197">В поле "Формула" введите "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="3b657-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="3b657-198">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="3b657-198">Click Save.</span></span>
62. <span data-ttu-id="3b657-199">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-199">Close the page.</span></span>
63. <span data-ttu-id="3b657-200">В дереве разверните узел "Интрастат\Данные: последовательность\Отправки: последовательность?".</span><span class="sxs-lookup"><span data-stu-id="3b657-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="3b657-201">В дереве разверните узел "Интрастат\Данные: последовательность\Отправки: последовательность?\Запись = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="3b657-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="3b657-202">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="3b657-202">Click the Format tab.</span></span>
66. <span data-ttu-id="3b657-203">В дереве выберите "Интрастат\Данные\Отправки\Запись\Сумма накладной в Евро".</span><span class="sxs-lookup"><span data-stu-id="3b657-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="3b657-204">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3b657-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="3b657-205">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="3b657-206">В дереве выберите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="3b657-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="3b657-207">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-207">Click Add data source.</span></span>
71. <span data-ttu-id="3b657-208">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-208">Click Save.</span></span>
72. <span data-ttu-id="3b657-209">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-209">Close the page.</span></span>
    * <span data-ttu-id="3b657-210">Просуммируйте значения сумм, по которым выставлены накладные, для строк в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="3b657-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="3b657-211">Результаты будут использоваться с именем "InvoicedAmountEUR" отдельно для различных направлений Интрастат и кодов товара.</span><span class="sxs-lookup"><span data-stu-id="3b657-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="3b657-212">Можно считать это виртуальным созданием таблицы Excel.</span><span class="sxs-lookup"><span data-stu-id="3b657-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="3b657-213">Для каждой проводки имеется строка, в которой первый столбец "блок" заполнен значениями "Импорт" и "Экспорт" соответственно.</span><span class="sxs-lookup"><span data-stu-id="3b657-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="3b657-214">Второй блок "запись" заполняется значением кода товара, а третий столбец "InvoicedAmountEUR" заполняется значением суммы из накладной.</span><span class="sxs-lookup"><span data-stu-id="3b657-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="3b657-215">В дереве разверните узел "Интрастат\Данные\Поступления?".</span><span class="sxs-lookup"><span data-stu-id="3b657-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="3b657-216">В дереве разверните узел "Интрастат\Данные\Поступления?\Запись = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="3b657-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="3b657-217">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="3b657-217">Click the Format tab.</span></span>
76. <span data-ttu-id="3b657-218">В дереве выберите "Интрастат\Данные\Поступления\Запись\Сумма накладной в Евро".</span><span class="sxs-lookup"><span data-stu-id="3b657-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="3b657-219">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="3b657-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="3b657-220">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="3b657-221">В дереве выберите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="3b657-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="3b657-222">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="3b657-222">Click Add data source.</span></span>
81. <span data-ttu-id="3b657-223">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-223">Click Save.</span></span>
82. <span data-ttu-id="3b657-224">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-224">Close the page.</span></span>
83. <span data-ttu-id="3b657-225">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3b657-225">Click Save.</span></span>
84. <span data-ttu-id="3b657-226">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b657-226">Close the page.</span></span>

