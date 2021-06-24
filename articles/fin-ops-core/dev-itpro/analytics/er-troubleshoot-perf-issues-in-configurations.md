---
title: Устранение проблем с производительностью в конфигурациях электронной отчетности
description: В этой теме объясняется, как найти и исправить проблемы с производительностью в конфигурациях электронной отчетности (ER).
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216873"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="91f48-103">Устранение проблем с производительностью в конфигурациях электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="91f48-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="91f48-104">В этой теме объясняется, как найти и решить проблемы с производительностью в [конфигурациях](general-electronic-reporting.md#Configuration) [электронной отчетности](general-electronic-reporting.md) (ER).</span><span class="sxs-lookup"><span data-stu-id="91f48-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="91f48-105">Как правило, исследование производительности состоит из нескольких этапов.</span><span class="sxs-lookup"><span data-stu-id="91f48-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="91f48-106">[Соберите](#collecting-data) данные.</span><span class="sxs-lookup"><span data-stu-id="91f48-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="91f48-107">Проанализируйте собранные данные.</span><span class="sxs-lookup"><span data-stu-id="91f48-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="91f48-108">На основе результатов анализа используйте конфигурации электронной отчетности для [внесения изменений](#making-changes) или для принятия решения о сборе дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="91f48-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="91f48-109">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="91f48-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="91f48-110">Анализ времени выполнения</span><span class="sxs-lookup"><span data-stu-id="91f48-110">Analyze execution time</span></span>

<span data-ttu-id="91f48-111">Время выполнения может зависеть от непредсказуемых факторов, таких как другие задачи, выполняемые в той же среде, и кэширование, в котором используются данные при их первом вызове.</span><span class="sxs-lookup"><span data-stu-id="91f48-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="91f48-112">Поэтому следует повторить выполнение и измерение несколько раз.</span><span class="sxs-lookup"><span data-stu-id="91f48-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="91f48-113">Иногда проблемы с производительностью не вызваны конфигурацией формата электронной отчетности, который используется для отчетности.</span><span class="sxs-lookup"><span data-stu-id="91f48-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="91f48-114">Вместо этого они вызваны кодом X++, который используется для открытия этой конфигурации формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="91f48-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="91f48-115">В [центре действий](#infolog-time) или в [журнале событий](#event-log-time) посмотрите на время выполнения отчета.</span><span class="sxs-lookup"><span data-stu-id="91f48-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="91f48-116">Сравните время выполнения отчета с общим временем выполнения в сценарии.</span><span class="sxs-lookup"><span data-stu-id="91f48-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="91f48-117">Если время выполнения отчета намного меньше общего времени выполнения, рассмотрим объем данных, которые обрабатывает отчет:</span><span class="sxs-lookup"><span data-stu-id="91f48-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="91f48-118">Если отчет обрабатывает небольшой объем данных, проблема может быть связана со временем загрузки конфигурации.</span><span class="sxs-lookup"><span data-stu-id="91f48-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="91f48-119">Если отчет обрабатывает большой объем данных, проблема может быть связана с предварительной обработкой X++.</span><span class="sxs-lookup"><span data-stu-id="91f48-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="91f48-120">Для анализа этого случая используйте [синтаксический анализатор трассировки](#analyze-trace-parser-trace).</span><span class="sxs-lookup"><span data-stu-id="91f48-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="91f48-121">В других случаях смотрите следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="91f48-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="91f48-122">Запустите несколько тестов, которые включают различные объемы данных, чтобы определить, как время выполнения зависит от объема данных.</span><span class="sxs-lookup"><span data-stu-id="91f48-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="91f48-123">Анализ трассировок синтаксического анализатора трассировки</span><span class="sxs-lookup"><span data-stu-id="91f48-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="91f48-124">Подготовьте небольшой пример или соберите несколько трассировок во время случайных частей генерации отчета.</span><span class="sxs-lookup"><span data-stu-id="91f48-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="91f48-125">Затем, в [синтаксическом анализаторе трассировки](#trace-parser) сделайте стандартный анализ «снизу вверх» и ответьте на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="91f48-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="91f48-126">Какие методы потребляют больше всего времени?</span><span class="sxs-lookup"><span data-stu-id="91f48-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="91f48-127">Какую часть общего времени используют эти методы?</span><span class="sxs-lookup"><span data-stu-id="91f48-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="91f48-128">Ответьте на те же вопросы для запросов.</span><span class="sxs-lookup"><span data-stu-id="91f48-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="91f48-129">Если вы видите, что методы имеют префикс "ER", перейти к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="91f48-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="91f48-130">Если вы видите, что методы или запросы возникли в наборе приложений, рассмотрите общие способы оптимизации (например, создайте индексы).</span><span class="sxs-lookup"><span data-stu-id="91f48-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="91f48-131">Проанализируйте количество вызовов.</span><span class="sxs-lookup"><span data-stu-id="91f48-131">Analyze the number of calls.</span></span> <span data-ttu-id="91f48-132">Если число значительно выше ожидаемого, рассмотрите кэширование соответствующих узлов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="91f48-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="91f48-133">Анализ вызовов базы данных</span><span class="sxs-lookup"><span data-stu-id="91f48-133">Analyze database calls</span></span>

<span data-ttu-id="91f48-134">Подготовь пример, который имеет небольшой объем данных, так что вы можете собрать [трассировку электронной отчетности](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="91f48-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="91f48-135">Затем откройте трассировку в конструкторе сопоставления модели электронной отчетности и посмотрите на нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="91f48-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="91f48-136">Ответьте на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="91f48-136">Answer the following questions:</span></span>

- <span data-ttu-id="91f48-137">Есть ли дублирование запросов?</span><span class="sxs-lookup"><span data-stu-id="91f48-137">Is there any query duplication?</span></span> <span data-ttu-id="91f48-138">Если есть, рассмотрите одно из следующих исправлений:</span><span class="sxs-lookup"><span data-stu-id="91f48-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="91f48-139">[Используйте кэширование](#use-caching), если вы считаете, что внутри одной родительской записи есть несколько вызовов.</span><span class="sxs-lookup"><span data-stu-id="91f48-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="91f48-140">[Используйте кэшированное, параметризированное вычисляемое поле](#cached-parameterized), если вы считаете, что внутри разных записей есть вызовы к одной и той же записи.</span><span class="sxs-lookup"><span data-stu-id="91f48-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="91f48-141">[Используйте источник данных **JOIN**](#use-join-datasource), если вам нужно считать значительное количество различных записей из базы данных.</span><span class="sxs-lookup"><span data-stu-id="91f48-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="91f48-142">Соответствует ли количество запросов и полученных записей общему объему данных?</span><span class="sxs-lookup"><span data-stu-id="91f48-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="91f48-143">Например, если документ содержит 10 строк, показывает ли статистика, что в отчет извлекает ровно 10 строк или 1000 строк?</span><span class="sxs-lookup"><span data-stu-id="91f48-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="91f48-144">Если у вас есть значительное количество извлеченных записей, рассмотрите одно из следующих исправлений:</span><span class="sxs-lookup"><span data-stu-id="91f48-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="91f48-145">[Используйте функцию **FILTER** вместо функции **WHERE**](#filter) для обработки данных на стороне сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="91f48-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="91f48-146">Используйте кэширование, чтобы избежать извлечения одних и тех же данных.</span><span class="sxs-lookup"><span data-stu-id="91f48-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="91f48-147">[Используйте функции собранных данных](#collected-data), чтобы избежать извлечения одних и тех же данных для суммирования.</span><span class="sxs-lookup"><span data-stu-id="91f48-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="91f48-148">Анализ трассировок PerfView</span><span class="sxs-lookup"><span data-stu-id="91f48-148">Analyze PerfView traces</span></span>

<span data-ttu-id="91f48-149">[PerfView](#perfview) является инструментом для опытных разработчиков.</span><span class="sxs-lookup"><span data-stu-id="91f48-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="91f48-150">Подробнее о следующих шагах см. в разделе [Основы исследования общего времени](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="91f48-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="91f48-151">Соберите трассировку с помощью времени потока.</span><span class="sxs-lookup"><span data-stu-id="91f48-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="91f48-152">Включите только стеки, которые используют **runUnattended**, чтобы фильтровать только поток, который имеет выполнение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="91f48-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="91f48-153">(Добавьте **runUnattended** в поле ввода **IncPats**.)</span><span class="sxs-lookup"><span data-stu-id="91f48-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="91f48-154">Сложите все время процессора, время сети и заблокированное время.</span><span class="sxs-lookup"><span data-stu-id="91f48-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="91f48-155">Загрузите [предустановки электронной отчетности для PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="91f48-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="91f48-156">Выберите **Электронная отчетность** \> **Другая предустановка**.</span><span class="sxs-lookup"><span data-stu-id="91f48-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="91f48-157">Посмотрите на имена:</span><span class="sxs-lookup"><span data-stu-id="91f48-157">Look at the names:</span></span>

    - <span data-ttu-id="91f48-158">Вы, вероятно, увидите код платформы, который потребляет больше всего времени.</span><span class="sxs-lookup"><span data-stu-id="91f48-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="91f48-159">Вы можете дважды нажать (или дважды щелкнуть) и перейти вверх через **вызывающих**.</span><span class="sxs-lookup"><span data-stu-id="91f48-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="91f48-160">Если вы нашли классы с префиксом "ERExpression", и если они являются функциями, связанными с формулами, вы можете угадать имя функции на основе имени класса и посмотреть в репозитории электронной отчетности для просмотра атрибутов.</span><span class="sxs-lookup"><span data-stu-id="91f48-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="91f48-161">Исправления</span><span class="sxs-lookup"><span data-stu-id="91f48-161">Fixes</span></span>

- <span data-ttu-id="91f48-162">Если вы видите, что большая часть времени процессора потребляется запросами, постарайтесь уменьшить количество запросов:</span><span class="sxs-lookup"><span data-stu-id="91f48-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="91f48-163">[Просмотрите трассировку электронной отчетности](#analyze-database-calls) на предмет дублирования запросов.</span><span class="sxs-lookup"><span data-stu-id="91f48-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="91f48-164">Посмотрите, сколько записей извлечено, и оцените, сколько данных теоретически должно быть извлечено.</span><span class="sxs-lookup"><span data-stu-id="91f48-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="91f48-165">Если вы видите, что большая часть времени процессора потребляется функциями, которые используются, попробуйте найти место в конфигурации, которое потребляет больше всего ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91f48-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="91f48-166">Если вы видите, что большая часть времени процессора потребляется функциями сбора данных, подумайте о замене их на команды *SQL группировать по* на стороне сопоставления модели.</span><span class="sxs-lookup"><span data-stu-id="91f48-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="91f48-167">Сбор данных</span><span class="sxs-lookup"><span data-stu-id="91f48-167">Collecting data</span></span>

<span data-ttu-id="91f48-168">В зависимости от среды существует несколько способов сбора доступных данных:</span><span class="sxs-lookup"><span data-stu-id="91f48-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="91f48-169">Получите общее время работы:</span><span class="sxs-lookup"><span data-stu-id="91f48-169">Get the total running time:</span></span>

    - <span data-ttu-id="91f48-170">Из центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="91f48-170">From the Action center</span></span>
    - <span data-ttu-id="91f48-171">Из журнала событий</span><span class="sxs-lookup"><span data-stu-id="91f48-171">From the event log</span></span>

- <span data-ttu-id="91f48-172">Профилирование исполнения:</span><span class="sxs-lookup"><span data-stu-id="91f48-172">Profile the execution:</span></span>

    - <span data-ttu-id="91f48-173">С помощью инструментов электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="91f48-173">By using ER tools</span></span>
    - <span data-ttu-id="91f48-174">С помощью синтаксического анализатора трассировки</span><span class="sxs-lookup"><span data-stu-id="91f48-174">By using Trace parser</span></span>
    - <span data-ttu-id="91f48-175">С помощью PerfView</span><span class="sxs-lookup"><span data-stu-id="91f48-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="91f48-176">Сбор данных в производственной среде</span><span class="sxs-lookup"><span data-stu-id="91f48-176">Collecting data in a production environment</span></span>

<span data-ttu-id="91f48-177">Иногда проблемы могут воспроизводиться только в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="91f48-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="91f48-178">Данные можно собирать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="91f48-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="91f48-179">С помощью трассировок [синтаксического анализатора трассировки](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="91f48-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="91f48-180">С помощью трассировок [выполнения электронной отчетности](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="91f48-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="91f48-181">С помощью общего времени выполнения</span><span class="sxs-lookup"><span data-stu-id="91f48-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="91f48-182">Сбор данных в среде разработки</span><span class="sxs-lookup"><span data-stu-id="91f48-182">Collecting data in a development environment</span></span>

<span data-ttu-id="91f48-183">В дополнение к инструментам, которые могут быть использованы в производственной среде, есть несколько инструментов, которые можно использовать в среде разработки:</span><span class="sxs-lookup"><span data-stu-id="91f48-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="91f48-184">Журнал событий (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="91f48-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="91f48-185">Этот журнал может дать вам общее время выполнения.</span><span class="sxs-lookup"><span data-stu-id="91f48-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="91f48-186">Общие инструменты .NET, такие как PerfView.</span><span class="sxs-lookup"><span data-stu-id="91f48-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="91f48-187">Кроме того, среда разработки дает больше гибкости для экспериментов.</span><span class="sxs-lookup"><span data-stu-id="91f48-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="91f48-188">Например, можно отключить части отчетов, чтобы увидеть, как это влияет на время выполнения.</span><span class="sxs-lookup"><span data-stu-id="91f48-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="91f48-189">Сервис</span><span class="sxs-lookup"><span data-stu-id="91f48-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="91f48-190">Время выполнения в центре уведомлений</span><span class="sxs-lookup"><span data-stu-id="91f48-190">Execution time in the Action center</span></span>

<span data-ttu-id="91f48-191">Электронная отчетность может показать время выполнения конфигурации в центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="91f48-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="91f48-192">Этот параметр применяется только к конкретному пользователю и конкретной компании и только к интерактивным сеансам.</span><span class="sxs-lookup"><span data-stu-id="91f48-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="91f48-193">Чтобы сделать эту функцию доступной, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="91f48-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="91f48-194">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="91f48-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="91f48-195">На странице **Конфигурации** в области действий на вкладке **Конфигурации** в группе **Дополнительные параметры** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="91f48-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="91f48-196">В диалоговом окне **Параметры пользователя** установите для параметра **Показать время создания файла** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="91f48-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="91f48-197">Время выполнения в журнале событий</span><span class="sxs-lookup"><span data-stu-id="91f48-197">Execution time in the event log</span></span>

1. <span data-ttu-id="91f48-198">Откройте средство просмотра событий Windows.</span><span class="sxs-lookup"><span data-stu-id="91f48-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="91f48-199">В пункте **Журналы приложений и служб** откройте **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="91f48-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="91f48-200">Найдите события **FormatMapingRun**, в которых **EventID=2**, поскольку эти события содержат информацию о прошедшем времени.</span><span class="sxs-lookup"><span data-stu-id="91f48-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="91f48-201">Трассировки синтаксического анализатора трассировки</span><span class="sxs-lookup"><span data-stu-id="91f48-201">Trace parser traces</span></span> 

<span data-ttu-id="91f48-202">Поскольку электронная отчетность реализована на X++, для анализа производительности можно использовать обычные инструменты X++.</span><span class="sxs-lookup"><span data-stu-id="91f48-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="91f48-203">Дополнительные сведения см. в разделе [Получение трассировок с помощью синтаксического анализатора трассировки](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="91f48-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="91f48-204">При этом подходе есть несколько ограничений.</span><span class="sxs-lookup"><span data-stu-id="91f48-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="91f48-205">Поскольку часть электронной отчетности реализована на C#, будут доступны не все данные.</span><span class="sxs-lookup"><span data-stu-id="91f48-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="91f48-206">Однако можно просмотреть сведения об использовании данных.</span><span class="sxs-lookup"><span data-stu-id="91f48-206">However, you can view the data usage details.</span></span> <span data-ttu-id="91f48-207">Кроме того, выполнения длинных отчетов могут превысить ограничения для хранения трассировки.</span><span class="sxs-lookup"><span data-stu-id="91f48-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="91f48-208">Трассировки электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="91f48-208">ER traces</span></span>

<span data-ttu-id="91f48-209">Электронная отчетность может собирать свои собственные трассировки, и она содержит средства визуализации и анализа для этих трассировок.</span><span class="sxs-lookup"><span data-stu-id="91f48-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="91f48-210">Дополнительные сведения см. в разделе [Трассировка выполнения форматов электронной отчетности для устранения неполадок, связанных с производительностью](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="91f48-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="91f48-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="91f48-211">PerfView</span></span>

<span data-ttu-id="91f48-212">Поскольку X++ и электронная отчетность реализованы на платформе .NET, можно использовать общие инструменты .NET.</span><span class="sxs-lookup"><span data-stu-id="91f48-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="91f48-213">Например, можно использовать бесплатное средство [PerfView](https://github.com/Microsoft/perfview).</span><span class="sxs-lookup"><span data-stu-id="91f48-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="91f48-214">Кроме того, можно собирать данные из командной строки.</span><span class="sxs-lookup"><span data-stu-id="91f48-214">You can also collect data from the command line.</span></span> <span data-ttu-id="91f48-215">Например, следующий сценарий Windows PowerShell собирает время выполнения до тех пор, пока любое выполнение формата на компьютере не будет остановлено.</span><span class="sxs-lookup"><span data-stu-id="91f48-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="91f48-216">При этом подходе есть несколько ограничений.</span><span class="sxs-lookup"><span data-stu-id="91f48-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="91f48-217">Вы должны иметь административный доступ к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="91f48-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="91f48-218">Кроме того, вы должны быть опытным разработчиком, так как здесь требуется интенсивное обучение.</span><span class="sxs-lookup"><span data-stu-id="91f48-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="91f48-219">Внесение изменений</span><span class="sxs-lookup"><span data-stu-id="91f48-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="91f48-220">Использование кэширования</span><span class="sxs-lookup"><span data-stu-id="91f48-220">Use caching</span></span>

<span data-ttu-id="91f48-221">Хотя кэширование позволяет сократить время, необходимое для повторной выборки данных, кэш занимает память.</span><span class="sxs-lookup"><span data-stu-id="91f48-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="91f48-222">Кэширование используется в случаях, когда объем загружаемых данных не слишком велик.</span><span class="sxs-lookup"><span data-stu-id="91f48-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="91f48-223">Дополнительные сведения и пример, показывающий порядок использования кэширования, см. в разделе [Улучшение сопоставления модели на основе сведений, содержащихся в трассировке выполнения](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="91f48-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="91f48-224">Использование кэшированного параметризованного вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="91f48-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="91f48-225">Иногда значения следует искать многократно.</span><span class="sxs-lookup"><span data-stu-id="91f48-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="91f48-226">Примерами являются наименования счетов и номера счетов.</span><span class="sxs-lookup"><span data-stu-id="91f48-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="91f48-227">Чтобы помочь экономить время, можно создать вычисляемое поле, имеющее параметры на верхнем уровне, а затем добавить поле в кэш.</span><span class="sxs-lookup"><span data-stu-id="91f48-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="91f48-228">Этот подход рекомендуется использовать только в том случае, если размер кэшированных данных мал.</span><span class="sxs-lookup"><span data-stu-id="91f48-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="91f48-229">Дополнительные сведения см. в разделе [Повышение производительности решений электронной отчетности путем добавления параметризованных источников ВЫЧИСЛЯЕМОЕ ПОЛЕ](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="91f48-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="91f48-230">Использование источника данных JOIN</span><span class="sxs-lookup"><span data-stu-id="91f48-230">Use a JOIN data source</span></span>

<span data-ttu-id="91f48-231">Источник данных **JOIN** позволяет выбирать несколько подключенных записей в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="91f48-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="91f48-232">Отдельный запрос не требуется использовать для получения каждой связанной записи.</span><span class="sxs-lookup"><span data-stu-id="91f48-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="91f48-233">Например, если имеется 1000 строк, и при этом извлекаются данные номенклатур для каждой строки по отношению, у вас будет 1001 запрос (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="91f48-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="91f48-234">При использовании источника данных **JOIN** для получения тех же данных будет использоваться только один запрос.</span><span class="sxs-lookup"><span data-stu-id="91f48-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="91f48-235">Дополнительные сведения см. в разделе [Использование источников данных JOIN в сопоставлениях моделей электронной отчетности для извлечения данных из нескольких таблиц приложений](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="91f48-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="91f48-236">Использование функции FILTER вместо функции WHERE</span><span class="sxs-lookup"><span data-stu-id="91f48-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="91f48-237">Функция **[FILTER](er-functions-list-filter.md)** выполняет условия на SQL Server, в то время как функция **WHERE** выбирает все данные из списка, по одной записи за раз, и применяет условие для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="91f48-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="91f48-238">Например, необходимо выделить одну запись из 1000 записей.</span><span class="sxs-lookup"><span data-stu-id="91f48-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="91f48-239">При использовании **WHERE** будут извлечены все из 1000 записей.</span><span class="sxs-lookup"><span data-stu-id="91f48-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="91f48-240">Однако если используется функция **FILTER**, будет извлечена только одна запись.</span><span class="sxs-lookup"><span data-stu-id="91f48-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="91f48-241">Функция **FILTER** также может использовать индексы на стороне базы данных.</span><span class="sxs-lookup"><span data-stu-id="91f48-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="91f48-242">Использование функций собранных данных или источника данных накопленных данных</span><span class="sxs-lookup"><span data-stu-id="91f48-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="91f48-243">Если в конфигурации имеется компонент *группировать по*, который суммирует ранее извлеченные данные по отчетам, этот компонент будет снова извлекать все данные.</span><span class="sxs-lookup"><span data-stu-id="91f48-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="91f48-244">Используя функции собранных данных, можно позволить электронной отчетности накапливать данные во время первой выборки.</span><span class="sxs-lookup"><span data-stu-id="91f48-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="91f48-245">Дополнительные сведения см. в разделе [Электронная отчетность — настройка формата для инвентаризации и суммирования](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="91f48-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="91f48-246">Переопределение частей конфигурации в X++</span><span class="sxs-lookup"><span data-stu-id="91f48-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="91f48-247">Электронная отчетность поддерживает вызовы методов таблиц и классов, в том числе и расширений.</span><span class="sxs-lookup"><span data-stu-id="91f48-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="91f48-248">Рекомендуется переписать части сопоставления модели в X++, чтобы повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="91f48-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="91f48-249">Электронная отчетность может получать данные из следующих источников:</span><span class="sxs-lookup"><span data-stu-id="91f48-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="91f48-250">Классы (источники данных **объект** и **класс**)</span><span class="sxs-lookup"><span data-stu-id="91f48-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="91f48-251">Таблицы (источники данных **таблица** и **записи таблицы**)</span><span class="sxs-lookup"><span data-stu-id="91f48-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="91f48-252">[API-интерфейс электронной отчетности](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) также предоставляет способ отправки предварительно рассчитанных данных из вызывающего кода.</span><span class="sxs-lookup"><span data-stu-id="91f48-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="91f48-253">В набор приложений входят многочисленные примеры такого подхода.</span><span class="sxs-lookup"><span data-stu-id="91f48-253">The application suite contains numerous examples of this approach.</span></span>
