--- 
title: "Использование конфигурации сопоставления модели для агрегированных расчетов на уровне базы данных (ER)"
description: "В этой процедуре предоставляются сведения о создании новой конфигурации сопоставления модели электронной отчетности (ER) и использовании встроенных функций ER для эффективного агрегирования расчетов."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1dfb0d62f87f4bfdf4916fe2348bee5019841e93
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="d07be-103">Использование конфигурации сопоставления модели для агрегированных расчетов на уровне базы данных (ER)</span><span class="sxs-lookup"><span data-stu-id="d07be-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d07be-104">В этой процедуре предоставляются сведения о создании новой конфигурации сопоставления модели электронной отчетности (ER) и использовании встроенных функций ER для эффективного агрегирования расчетов.</span><span class="sxs-lookup"><span data-stu-id="d07be-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="d07be-105">В этой процедуре вам предстоит создать конфигурацию для компании-образца Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d07be-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="d07be-106">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="d07be-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="d07be-107">Эти шаги можно выполнить с использованием любого набора данных.</span><span class="sxs-lookup"><span data-stu-id="d07be-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="d07be-108">Для выполнения этих шагов сначала необходимо выполнить шаги процедуры "Электронная отчетность повышает эффективность агрегированных расчетов путем их выполнения на уровне базы данных (Часть 1. Подготовка конфигураций)".</span><span class="sxs-lookup"><span data-stu-id="d07be-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="d07be-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="d07be-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d07be-110">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="d07be-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="d07be-111">В дереве выберите "Модель Интрастат\Сопоставление образца Интрастат".</span><span class="sxs-lookup"><span data-stu-id="d07be-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="d07be-112">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d07be-112">Click Designer.</span></span>
5. <span data-ttu-id="d07be-113">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d07be-113">Click Designer.</span></span>
6. <span data-ttu-id="d07be-114">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="d07be-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="d07be-115">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="d07be-115">Click Add root.</span></span>
    * <span data-ttu-id="d07be-116">Добавьте новый источник данных, представляющий записи, которые требуется сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="d07be-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="d07be-117">В поле "Имя" введите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="d07be-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="d07be-118">Транзакции</span><span class="sxs-lookup"><span data-stu-id="d07be-118">Transactions</span></span>  
9. <span data-ttu-id="d07be-119">В поле "Таблица" введите "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="d07be-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="d07be-120">Интрастат</span><span class="sxs-lookup"><span data-stu-id="d07be-120">Intrastat</span></span>  
10. <span data-ttu-id="d07be-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d07be-121">Click OK.</span></span>
11. <span data-ttu-id="d07be-122">В дереве выберите "Функции\Группировка по".</span><span class="sxs-lookup"><span data-stu-id="d07be-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="d07be-123">Этот тип источника данных используется для ввода нового источника данных во время выполнения для группировки записей и вычисления требуемых агрегирований.</span><span class="sxs-lookup"><span data-stu-id="d07be-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="d07be-124">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="d07be-124">Click Add root.</span></span>
13. <span data-ttu-id="d07be-125">В поле "Имя" введите TransactionsGroups.</span><span class="sxs-lookup"><span data-stu-id="d07be-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="d07be-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="d07be-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="d07be-127">Щелкните "Изменить группу по".</span><span class="sxs-lookup"><span data-stu-id="d07be-127">Click Edit group by.</span></span>
15. <span data-ttu-id="d07be-128">В дереве выберите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="d07be-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="d07be-129">Выберите добавленный источник данных типа "Список записей", представляющий записи, которые требуется сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="d07be-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="d07be-130">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="d07be-130">Click Add field to.</span></span>
17. <span data-ttu-id="d07be-131">Щелкните "Элементы для группировки".</span><span class="sxs-lookup"><span data-stu-id="d07be-131">Click What to group.</span></span>
18. <span data-ttu-id="d07be-132">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="d07be-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="d07be-133">В дереве выберите "Проводки\Направление".</span><span class="sxs-lookup"><span data-stu-id="d07be-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="d07be-134">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="d07be-134">Click Add field to.</span></span>
21. <span data-ttu-id="d07be-135">Щелкните "Сгруппированные поля".</span><span class="sxs-lookup"><span data-stu-id="d07be-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="d07be-136">Выберите поле, чтобы указать уровень группировки.</span><span class="sxs-lookup"><span data-stu-id="d07be-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="d07be-137">На основе этого выбора источник данных будет возвращать во время выполнения столько групп проводок, сколько имеется кодов направлений, которые будут отвечать условиям в таблице Интрастат.</span><span class="sxs-lookup"><span data-stu-id="d07be-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="d07be-138">В дереве выберите "Проводки\Сумма накладной(сумма MST)".</span><span class="sxs-lookup"><span data-stu-id="d07be-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="d07be-139">Выберите поле для указания источника расчета агрегирования.</span><span class="sxs-lookup"><span data-stu-id="d07be-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="d07be-140">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="d07be-140">Click Add field to.</span></span>
24. <span data-ttu-id="d07be-141">Щелкните "Поля агрегирования".</span><span class="sxs-lookup"><span data-stu-id="d07be-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="d07be-142">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d07be-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="d07be-143">В поле "Метод" выберите "Сумма".</span><span class="sxs-lookup"><span data-stu-id="d07be-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="d07be-144">Выберите тип агрегирования.</span><span class="sxs-lookup"><span data-stu-id="d07be-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="d07be-145">В поле "Имя" введите SumOfAmountMST.</span><span class="sxs-lookup"><span data-stu-id="d07be-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="d07be-146">Укажите имя этого агрегирования в настроенном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="d07be-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="d07be-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d07be-147">Click Save.</span></span>
    * <span data-ttu-id="d07be-148">Обратите внимание, что поле "Место выполнения" указывает, что эта группировка будет выполняться во время выполнения в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d07be-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="d07be-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d07be-149">Close the page.</span></span>
30. <span data-ttu-id="d07be-150">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d07be-150">Click OK.</span></span>
31. <span data-ttu-id="d07be-151">В дереве разверните "Итоги".</span><span class="sxs-lookup"><span data-stu-id="d07be-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="d07be-152">В дереве разверните "Группы проводок".</span><span class="sxs-lookup"><span data-stu-id="d07be-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="d07be-153">В дереве разверните "Группы проводок\агрегировано".</span><span class="sxs-lookup"><span data-stu-id="d07be-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="d07be-154">В дереве выберите "Группы проводок\агрегировано\Сумма MST".</span><span class="sxs-lookup"><span data-stu-id="d07be-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="d07be-155">В дереве выберите "Итоги\Общая стоимость накладной(общая стоимость накладной) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')".</span><span class="sxs-lookup"><span data-stu-id="d07be-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="d07be-156">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="d07be-156">Click Bind.</span></span>
    * <span data-ttu-id="d07be-157">На основании этого параметра этот источник данных будет рассчитывать суммарное значение поля AmountMST для каждой группы проводок.</span><span class="sxs-lookup"><span data-stu-id="d07be-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="d07be-158">Этот расчет агрегирования будет доступен как элемент TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="d07be-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="d07be-159">В дереве разверните "Группы проводок".</span><span class="sxs-lookup"><span data-stu-id="d07be-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="d07be-160">В дереве выберите "Группы проводок".</span><span class="sxs-lookup"><span data-stu-id="d07be-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="d07be-161">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d07be-161">Click Edit.</span></span>
40. <span data-ttu-id="d07be-162">Щелкните "Изменить группу по".</span><span class="sxs-lookup"><span data-stu-id="d07be-162">Click Edit group by.</span></span>
41. <span data-ttu-id="d07be-163">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="d07be-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="d07be-164">В дереве выберите "Проводки\Сумма накладной(сумма MST)".</span><span class="sxs-lookup"><span data-stu-id="d07be-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="d07be-165">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="d07be-165">Click Add field to.</span></span>
44. <span data-ttu-id="d07be-166">Щелкните "Поля агрегирования".</span><span class="sxs-lookup"><span data-stu-id="d07be-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="d07be-167">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d07be-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="d07be-168">В поле "Метод" выберите "Макс.".</span><span class="sxs-lookup"><span data-stu-id="d07be-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="d07be-169">В поле "Имя" введите MaxOfAmountMST.</span><span class="sxs-lookup"><span data-stu-id="d07be-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="d07be-170">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d07be-170">Click Save.</span></span>
    * <span data-ttu-id="d07be-171">В настоящее время выполнение источников данных GROUPBY можно перевести на уровень базы данных SQL с некоторыми ограничениями.</span><span class="sxs-lookup"><span data-stu-id="d07be-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="d07be-172">Перевод можно выполнять либо для источников данных типа "Список записей", либо источников данных, представленных как выражение с помощью функции FILTER.</span><span class="sxs-lookup"><span data-stu-id="d07be-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="d07be-173">Это также можно сделать, только если настроено одно агрегирование для одного поля записей группировки.</span><span class="sxs-lookup"><span data-stu-id="d07be-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="d07be-174">Обратите внимание, что несмотря на то что было настроено несколько агрегирований для поля AmountMST, поле "Место выполнения" по-прежнему указывает, что эта группировка будет выполняться во время выполнения в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d07be-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="d07be-175">Это происходит потому, что только одно агрегирование привязано к элементу модели данных и будет использоваться во время выполнения для извлечения данных из этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="d07be-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="d07be-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d07be-176">Close the page.</span></span>
50. <span data-ttu-id="d07be-177">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d07be-177">Click OK.</span></span>
51. <span data-ttu-id="d07be-178">В дереве разверните "Группы проводок".</span><span class="sxs-lookup"><span data-stu-id="d07be-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="d07be-179">В дереве разверните "Группы проводок\агрегировано".</span><span class="sxs-lookup"><span data-stu-id="d07be-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="d07be-180">В дереве выберите "Группы проводок\агрегировано\Макс. сумма MST".</span><span class="sxs-lookup"><span data-stu-id="d07be-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="d07be-181">В дереве выберите "Итоги\Итоговая статистическая стоимость(итоговая статистическая стоимость) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')".</span><span class="sxs-lookup"><span data-stu-id="d07be-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="d07be-182">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="d07be-182">Click Bind.</span></span>
56. <span data-ttu-id="d07be-183">В дереве разверните "Группы проводок".</span><span class="sxs-lookup"><span data-stu-id="d07be-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="d07be-184">В дереве выберите "Группы проводок".</span><span class="sxs-lookup"><span data-stu-id="d07be-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="d07be-185">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d07be-185">Click Edit.</span></span>
59. <span data-ttu-id="d07be-186">Щелкните "Изменить группу по".</span><span class="sxs-lookup"><span data-stu-id="d07be-186">Click Edit group by.</span></span>
    * <span data-ttu-id="d07be-187">Обратите внимание, что поле "Место выполнения" указывает, что эта группировка будет выполняться во время выполнения в памяти, поскольку оба агрегирования одного и того же поля привязаны к элементам модели данных.</span><span class="sxs-lookup"><span data-stu-id="d07be-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="d07be-188">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="d07be-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="d07be-189">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="d07be-189">Click Delete.</span></span>
62. <span data-ttu-id="d07be-190">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="d07be-190">Click Yes.</span></span>
63. <span data-ttu-id="d07be-191">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="d07be-191">Click Delete.</span></span>
64. <span data-ttu-id="d07be-192">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="d07be-192">Click Yes.</span></span>
65. <span data-ttu-id="d07be-193">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="d07be-193">Click Add field to.</span></span>
66. <span data-ttu-id="d07be-194">Щелкните "Элементы для группировки".</span><span class="sxs-lookup"><span data-stu-id="d07be-194">Click What to group.</span></span>
67. <span data-ttu-id="d07be-195">В дереве разверните "Запись товара(Интрастат)".</span><span class="sxs-lookup"><span data-stu-id="d07be-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="d07be-196">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d07be-196">Click Save.</span></span>
    * <span data-ttu-id="d07be-197">Обратите внимание, что поле "Место выполнения" указывает, эта группировка будет выполняться во время выполнения в памяти, несмотря на то что не существуют определенные агрегирования и выбранный источник данных типа "Записи таблицы" ссылается на одну и ту же таблицу "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="d07be-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="d07be-198">Это происходит потому, что источник данных содержит некоторые вычисляемые поля, которые еще невозможно перевести на уровень базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d07be-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  


