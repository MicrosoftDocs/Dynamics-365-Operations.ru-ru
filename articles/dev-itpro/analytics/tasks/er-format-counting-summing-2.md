--- 
title: "Настройка вычислений для подсчета и суммирования для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7b9035d8e7baf3c7ecb063b104b9a567be60840
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="configure-computations-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="8bab9-103">Настройка вычислений для подсчета и суммирования для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="8bab9-103">Configure computations to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8bab9-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8bab9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="8bab9-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="8bab9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8bab9-106">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 1. Создание формата)".</span><span class="sxs-lookup"><span data-stu-id="8bab9-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="8bab9-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="8bab9-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="8bab9-108">Создание конфигурации формата для добавления сведений об инвентаризации и суммировании</span><span class="sxs-lookup"><span data-stu-id="8bab9-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="8bab9-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="8bab9-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8bab9-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="8bab9-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8bab9-111">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="8bab9-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="8bab9-112">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="8bab9-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="8bab9-113">Допустим, требуется настроить формат, предоставленный Microsoft, добавив строки со сводными сведениями в конец отчета Интрастат.</span><span class="sxs-lookup"><span data-stu-id="8bab9-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="8bab9-114">Это следует сделать, создав наш собственный экземпляр на основе конфигурации Интрастат из экземпляра Microsoft для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="8bab9-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="8bab9-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="8bab9-116">В поле "Создать" введите "Производное от имени: Интрастат (DE), Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8bab9-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="8bab9-117">В поле "Имя" введите "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="8bab9-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="8bab9-118">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="8bab9-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="8bab9-119">Настройте этот отчет, чтобы выполнять инвентаризацию и суммирование на основе выходных сведений</span><span class="sxs-lookup"><span data-stu-id="8bab9-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="8bab9-120">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="8bab9-120">Click Designer.</span></span>
2. <span data-ttu-id="8bab9-121">Выберите "Да" в поле "Сбор сведений о результате".</span><span class="sxs-lookup"><span data-stu-id="8bab9-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="8bab9-122">Этот флаг активируется во время выполнения процесса сбора выходных сведения для создания файла Интрастат.</span><span class="sxs-lookup"><span data-stu-id="8bab9-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="8bab9-123">Необходимо выполнять инвентаризацию для различных направлений Интрастат, поэтому следует добавить специальное перечисление модели в список источников данных конфигурации этого формата.</span><span class="sxs-lookup"><span data-stu-id="8bab9-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="8bab9-124">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="8bab9-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="8bab9-125">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="8bab9-126">В дереве выберите "Модель данных\Перечисление".</span><span class="sxs-lookup"><span data-stu-id="8bab9-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="8bab9-127">В поле "Имя" введите "Направление".</span><span class="sxs-lookup"><span data-stu-id="8bab9-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="8bab9-128">В поле "Перечисление модели" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8bab9-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="8bab9-129">Выберите значение "Направление".</span><span class="sxs-lookup"><span data-stu-id="8bab9-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="8bab9-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8bab9-130">Click OK.</span></span>
9. <span data-ttu-id="8bab9-131">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="8bab9-132">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="8bab9-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="8bab9-133">В поле "Имя" введите "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="8bab9-134">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="8bab9-134">Click Edit formula.</span></span>
13. <span data-ttu-id="8bab9-135">В поле "Формула" введите "блок".</span><span class="sxs-lookup"><span data-stu-id="8bab9-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="8bab9-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-136">Click Save.</span></span>
15. <span data-ttu-id="8bab9-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-137">Close the page.</span></span>
16. <span data-ttu-id="8bab9-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8bab9-138">Click OK.</span></span>
17. <span data-ttu-id="8bab9-139">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="8bab9-140">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="8bab9-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="8bab9-141">В поле "Имя" введите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="8bab9-142">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="8bab9-142">Click Edit formula.</span></span>
21. <span data-ttu-id="8bab9-143">В поле "Формула" введите "запись".</span><span class="sxs-lookup"><span data-stu-id="8bab9-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="8bab9-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-144">Click Save.</span></span>
23. <span data-ttu-id="8bab9-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-145">Close the page.</span></span>
24. <span data-ttu-id="8bab9-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8bab9-146">Click OK.</span></span>
25. <span data-ttu-id="8bab9-147">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="8bab9-148">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="8bab9-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="8bab9-149">В поле "Имя" введите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="8bab9-150">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="8bab9-150">Click Edit formula.</span></span>
29. <span data-ttu-id="8bab9-151">В поле "Формула" введите "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="8bab9-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="8bab9-152">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-152">Click Save.</span></span>
31. <span data-ttu-id="8bab9-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-153">Close the page.</span></span>
32. <span data-ttu-id="8bab9-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8bab9-154">Click OK.</span></span>
33. <span data-ttu-id="8bab9-155">В дереве выберите "Интрастат\Данные".</span><span class="sxs-lookup"><span data-stu-id="8bab9-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="8bab9-156">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="8bab9-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="8bab9-157">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-157">Click Add data source.</span></span>
    * <span data-ttu-id="8bab9-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="8bab9-158">$BlockName</span></span>  
36. <span data-ttu-id="8bab9-159">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-159">Click Save.</span></span>
37. <span data-ttu-id="8bab9-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-160">Close the page.</span></span>
38. <span data-ttu-id="8bab9-161">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="8bab9-162">В поле "Формула" введите "IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")".</span><span class="sxs-lookup"><span data-stu-id="8bab9-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="8bab9-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="8bab9-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="8bab9-164">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-164">Click Save.</span></span>
41. <span data-ttu-id="8bab9-165">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-165">Close the page.</span></span>
    * <span data-ttu-id="8bab9-166">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="8bab9-166">Count the lines of this sequence.</span></span> <span data-ttu-id="8bab9-167">Результаты будут использоваться с именем "блок" отдельно для различных направлений.</span><span class="sxs-lookup"><span data-stu-id="8bab9-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="8bab9-168">Значение "Импорт" будет использоваться для всех проводок поступлений Интрастат.</span><span class="sxs-lookup"><span data-stu-id="8bab9-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="8bab9-169">Значение "Экспорт" будет использоваться для всех проводок отправок Интрастат.</span><span class="sxs-lookup"><span data-stu-id="8bab9-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="8bab9-170">Можно считать это виртуальной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="8bab9-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="8bab9-171">Для каждой проводки имеется строка, в которой первый столбец "блок" заполнен значениями "Импорт" и "Экспорт" соответственно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="8bab9-172">В дереве разверните узел "Интрастат\Данные: последовательность".</span><span class="sxs-lookup"><span data-stu-id="8bab9-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="8bab9-173">В дереве выберите узел "Интрастат\Данные: последовательность\Поступления?".</span><span class="sxs-lookup"><span data-stu-id="8bab9-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="8bab9-174">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="8bab9-175">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="8bab9-175">Count the lines of this sequence.</span></span> <span data-ttu-id="8bab9-176">Результаты будут запомнены с использованием имени "запись".</span><span class="sxs-lookup"><span data-stu-id="8bab9-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="8bab9-177">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="8bab9-178">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-178">Click Add data source.</span></span>
47. <span data-ttu-id="8bab9-179">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-179">Click Save.</span></span>
48. <span data-ttu-id="8bab9-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-180">Close the page.</span></span>
49. <span data-ttu-id="8bab9-181">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="8bab9-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="8bab9-182">В поле "Формула" введите "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="8bab9-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="8bab9-183">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-183">Click Save.</span></span>
52. <span data-ttu-id="8bab9-184">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-184">Close the page.</span></span>
    * <span data-ttu-id="8bab9-185">Подсчитайте строки в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="8bab9-185">Count the lines of this sequence.</span></span> <span data-ttu-id="8bab9-186">Результаты будут использоваться с именем "запись" отдельно для кодов товара.</span><span class="sxs-lookup"><span data-stu-id="8bab9-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="8bab9-187">Можно считать это виртуальной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="8bab9-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="8bab9-188">Для каждой проводки имеется строка, в которой столбец "блок" заполняется значениями "Импорт" и "Экспорт" соответственно, а второй блок "запись" заполняется значением кода товара.</span><span class="sxs-lookup"><span data-stu-id="8bab9-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="8bab9-189">В дереве выберите узел "Интрастат\Данные: последовательность\Отправки?".</span><span class="sxs-lookup"><span data-stu-id="8bab9-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="8bab9-190">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных"</span><span class="sxs-lookup"><span data-stu-id="8bab9-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="8bab9-191">В дереве выберите "$RecName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="8bab9-192">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-192">Click Add data source.</span></span>
57. <span data-ttu-id="8bab9-193">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-193">Click Save.</span></span>
58. <span data-ttu-id="8bab9-194">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-194">Close the page.</span></span>
59. <span data-ttu-id="8bab9-195">Нажмите кнопку "Изменить" для поля "Значение ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="8bab9-196">В поле "Формула" введите "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="8bab9-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="8bab9-197">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="8bab9-197">Click Save.</span></span>
62. <span data-ttu-id="8bab9-198">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-198">Close the page.</span></span>
63. <span data-ttu-id="8bab9-199">В дереве разверните узел "Интрастат\Данные: последовательность\Отправки: последовательность?".</span><span class="sxs-lookup"><span data-stu-id="8bab9-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="8bab9-200">В дереве разверните узел "Интрастат\Данные: последовательность\Отправки: последовательность?\Запись = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="8bab9-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="8bab9-201">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="8bab9-201">Click the Format tab.</span></span>
66. <span data-ttu-id="8bab9-202">В дереве выберите "Интрастат\Данные\Отправки\Запись\Сумма накладной в Евро".</span><span class="sxs-lookup"><span data-stu-id="8bab9-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="8bab9-203">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="8bab9-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="8bab9-204">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="8bab9-205">В дереве выберите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="8bab9-206">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-206">Click Add data source.</span></span>
71. <span data-ttu-id="8bab9-207">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-207">Click Save.</span></span>
72. <span data-ttu-id="8bab9-208">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-208">Close the page.</span></span>
    * <span data-ttu-id="8bab9-209">Просуммируйте значения сумм, по которым выставлены накладные, для строк в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="8bab9-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="8bab9-210">Результаты будут использоваться с именем "InvoicedAmountEUR" отдельно для различных направлений Интрастат и кодов товара.</span><span class="sxs-lookup"><span data-stu-id="8bab9-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="8bab9-211">Можно считать это виртуальным созданием таблицы Excel.</span><span class="sxs-lookup"><span data-stu-id="8bab9-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="8bab9-212">Для каждой проводки имеется строка, в которой первый столбец "блок" заполнен значениями "Импорт" и "Экспорт" соответственно.</span><span class="sxs-lookup"><span data-stu-id="8bab9-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="8bab9-213">Второй блок "запись" заполняется значением кода товара, а третий столбец "InvoicedAmountEUR" заполняется значением суммы из накладной.</span><span class="sxs-lookup"><span data-stu-id="8bab9-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="8bab9-214">В дереве разверните узел "Интрастат\Данные\Поступления?".</span><span class="sxs-lookup"><span data-stu-id="8bab9-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="8bab9-215">В дереве разверните узел "Интрастат\Данные\Поступления?\Запись = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="8bab9-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="8bab9-216">Перейдите на вкладку "Формат".</span><span class="sxs-lookup"><span data-stu-id="8bab9-216">Click the Format tab.</span></span>
76. <span data-ttu-id="8bab9-217">В дереве выберите "Интрастат\Данные\Поступления\Запись\Сумма накладной в Евро".</span><span class="sxs-lookup"><span data-stu-id="8bab9-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="8bab9-218">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="8bab9-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="8bab9-219">Нажмите кнопку "Изменить" для поля "Имя ключа собранных данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="8bab9-220">В дереве выберите "$InvName".</span><span class="sxs-lookup"><span data-stu-id="8bab9-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="8bab9-221">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="8bab9-221">Click Add data source.</span></span>
81. <span data-ttu-id="8bab9-222">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-222">Click Save.</span></span>
82. <span data-ttu-id="8bab9-223">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-223">Close the page.</span></span>
83. <span data-ttu-id="8bab9-224">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8bab9-224">Click Save.</span></span>
84. <span data-ttu-id="8bab9-225">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8bab9-225">Close the page.</span></span>

