---
title: Расширенный синтаксис фильтрации и запросов
description: В этой теме описываются параметры фильтрации и запросов для диалога "Расширенный фильтр/сортировка" и оператора "matches" на панели фильтров или в фильтрах заголовков столбцов сетки.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdb55a9552759e5f2b670a4eeb4e5d6572ebfb77
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744107"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="11dd1-103">Расширенный синтаксис фильтрации и запросов</span><span class="sxs-lookup"><span data-stu-id="11dd1-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11dd1-104">В этой теме описываются параметры фильтрации и запросов, доступные при использовании диалогового окна «Расширенный фильтр/сортировка» или оператора **matches** на панели фильтров или в фильтрах заголовков столбцов сетки.</span><span class="sxs-lookup"><span data-stu-id="11dd1-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="11dd1-105">Синтаксис расширенного запроса</span><span class="sxs-lookup"><span data-stu-id="11dd1-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="11dd1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11dd1-106">Syntax</span></span></th>
<th><span data-ttu-id="11dd1-107">Описание символов</span><span class="sxs-lookup"><span data-stu-id="11dd1-107">Character description</span></span></th>
<th><span data-ttu-id="11dd1-108">описание</span><span class="sxs-lookup"><span data-stu-id="11dd1-108">Description</span></span></th>
<th><span data-ttu-id="11dd1-109">Пример</span><span class="sxs-lookup"><span data-stu-id="11dd1-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="11dd1-110"><em>значение</em></span><span class="sxs-lookup"><span data-stu-id="11dd1-110"><em>value</em></span></span></td>
<td><span data-ttu-id="11dd1-111">Равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="11dd1-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-112">Введите значение, которое требуется найти:</span><span class="sxs-lookup"><span data-stu-id="11dd1-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="11dd1-113">При вводе <strong>Виктор</strong> будет осуществлен поиск всех значений &quot;Виктор&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-114">!<em>значение</em> (восклицательный знак)</span><span class="sxs-lookup"><span data-stu-id="11dd1-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="11dd1-115">Не равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="11dd1-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-116">Введите восклицательный знак, затем значение, которое требуется исключить из поиска.</span><span class="sxs-lookup"><span data-stu-id="11dd1-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="11dd1-117">При вводе <strong>!Виктор</strong> будет осуществлен поиск всех значений, кроме &quot;Виктор&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-118"><em>начальное-значение</em>..<em>конечное-значение</em> (две точки)</span><span class="sxs-lookup"><span data-stu-id="11dd1-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="11dd1-119">Между двумя значениями, разделенными двумя точками</span><span class="sxs-lookup"><span data-stu-id="11dd1-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="11dd1-120">Введите начальное значение, затем две точки, затем конечное значение.</span><span class="sxs-lookup"><span data-stu-id="11dd1-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="11dd1-121">Если ввести <strong>1..10</strong>, будут найдены все значения от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="11dd1-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="11dd1-122">Однако, если ввести текстовое выражение <strong>A..C</strong> , то будут найдены все значения, начинающиеся на &quot;A&quot; и &quot;B&quot;, а также значения, строго равные &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="11dd1-123">Например, этот запрос не найдет &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="11dd1-124">Чтобы найти все значения, начинающиеся на буквы от &quot;A<em>&quot; до &quot;C</em>&quot;, следует ввести <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-125">..<em>значение</em> (две точки)</span><span class="sxs-lookup"><span data-stu-id="11dd1-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="11dd1-126">Меньше или равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="11dd1-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-127">Введите две точки, а затем необходимое значение.</span><span class="sxs-lookup"><span data-stu-id="11dd1-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="11dd1-128">Если ввести <strong>..1000</strong>, то будут найдены все значения, меньшие или равные 1000, например &quot;100&quot;, &quot;999,95&quot; и &quot;1 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-129"><em>значение</em>..</span><span class="sxs-lookup"><span data-stu-id="11dd1-129"><em>value</em>..</span></span> <span data-ttu-id="11dd1-130">(две точки)</span><span class="sxs-lookup"><span data-stu-id="11dd1-130">(double period)</span></span></td>
<td><span data-ttu-id="11dd1-131">Больше или равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="11dd1-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-132">Введите значение, затем две точки.</span><span class="sxs-lookup"><span data-stu-id="11dd1-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="11dd1-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="11dd1-133"><strong>1000..</strong></span></span> <span data-ttu-id="11dd1-134">будут найдены все значения, большие или равные 1000, например &quot;1 000&quot;, &quot;1 000,01&quot; и &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-135">&gt;<em>значение</em> (знак "больше чем")</span><span class="sxs-lookup"><span data-stu-id="11dd1-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="11dd1-136">Больше, чем введенное значение</span><span class="sxs-lookup"><span data-stu-id="11dd1-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-137">Введите знак "больше чем" (<strong>&gt;</strong>), а затем значение.</span><span class="sxs-lookup"><span data-stu-id="11dd1-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="11dd1-138">Если ввести <strong>&gt;1000</strong>, то будут найдены все значения, большие 1000, например &quot;1000,01&quot;, &quot;20 000&quot; и &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-139">&lt;<em>значение</em> (знак "меньше чем")</span><span class="sxs-lookup"><span data-stu-id="11dd1-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="11dd1-140">Меньше, чем введенное значение</span><span class="sxs-lookup"><span data-stu-id="11dd1-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-141">Введите знак "меньше чем" (<strong>&lt;</strong>), а затем значение.</span><span class="sxs-lookup"><span data-stu-id="11dd1-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="11dd1-142">Если ввести <strong>&lt;1000</strong>, то будут найдены все значения, меньшие 1000, например &quot;999,99&quot;, &quot;1&quot; и &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-143"><em>значение</em>\* (звездочка)</span><span class="sxs-lookup"><span data-stu-id="11dd1-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="11dd1-144">Начинается с введенного значения</span><span class="sxs-lookup"><span data-stu-id="11dd1-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-145">Введите начальное значение для поиска, а затем звездочку (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="11dd1-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="11dd1-146">Если ввести <strong>С\*</strong>, то будут найдены все записи, начинающиеся на &quot;С&quot;, например &quot;Стокгольм&quot;, &quot;Сидней&quot; и &quot;Сан-Франциско&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-147">\*<em>значение</em> (звездочка)</span><span class="sxs-lookup"><span data-stu-id="11dd1-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="11dd1-148">Заканчивается на введенное значение</span><span class="sxs-lookup"><span data-stu-id="11dd1-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-149">Введите звездочку, а потом конечное значение для поиска.</span><span class="sxs-lookup"><span data-stu-id="11dd1-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="11dd1-150">Если ввести <strong>\*восток</strong>, то будут найдены все записи, заканчивающиеся на &quot;восток&quot;, например &quot;северо-восток&quot; или &quot;юго-восток&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-151">*<em>значение</em>* (звездочка)</span><span class="sxs-lookup"><span data-stu-id="11dd1-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="11dd1-152">Содержит введенное значение</span><span class="sxs-lookup"><span data-stu-id="11dd1-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="11dd1-153">Введите звездочку, затем значение, а затем снова звездочку.</span><span class="sxs-lookup"><span data-stu-id="11dd1-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="11dd1-154">Если ввести <strong>*во*</strong>, то будут найдены все записи, содержащие &quot;во&quot;, например &quot;северо-восток&quot; или &quot;юго-восток&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-155">?</span><span class="sxs-lookup"><span data-stu-id="11dd1-155">?</span></span> <span data-ttu-id="11dd1-156">(вопросительный знак)</span><span class="sxs-lookup"><span data-stu-id="11dd1-156">(question mark)</span></span></td>
<td><span data-ttu-id="11dd1-157">Содержится один или более неизвестных символов</span><span class="sxs-lookup"><span data-stu-id="11dd1-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="11dd1-158">Введите вопросительный знак вместо неизвестного символа в значении.</span><span class="sxs-lookup"><span data-stu-id="11dd1-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="11dd1-159">Если ввести <strong>В?ктор</strong>, то будут найдены &quot;Виктор&quot; и &quot;Вектор&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-160"><em>значение</em>,<em>значение</em> (запятая)</span><span class="sxs-lookup"><span data-stu-id="11dd1-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="11dd1-161">Поиск записей, совпадающих с введенными через запятую значениями</span><span class="sxs-lookup"><span data-stu-id="11dd1-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="11dd1-162">Введите все критерии поиска, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="11dd1-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="11dd1-163">Если ввести <strong>A, D, F, G</strong>, то будут найдены &quot;A&quot;, &quot;D&quot;, &quot;F&quot; и &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="11dd1-164">Если ввести <strong>10, 20, 30, 100</strong>, то будут найдены &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="11dd1-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-165">"" (две двойные кавычки)</span><span class="sxs-lookup"><span data-stu-id="11dd1-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="11dd1-166">Соответствие пустому значению</span><span class="sxs-lookup"><span data-stu-id="11dd1-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="11dd1-167">Введите две последовательные двойные кавычки для фильтрации пустых значений в этом поле.</span><span class="sxs-lookup"><span data-stu-id="11dd1-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="11dd1-168">Две последовательные двойные кавычки (<strong>""</strong>) ищут строки без значения для текущего столбца.</span><span class="sxs-lookup"><span data-stu-id="11dd1-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-169">(<span class="code">Запрос Finance and Operations</span>) (запрос Finance and Operations между скобками)</span><span class="sxs-lookup"><span data-stu-id="11dd1-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="11dd1-170">Поиск согласно введенному запросу</span><span class="sxs-lookup"><span data-stu-id="11dd1-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="11dd1-171">Введите запрос в виде SQL-инструкции в скобках, используя язык запросов Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11dd1-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="11dd1-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="11dd1-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="11dd1-173">как пример синтаксиса для условия фильтра по полю из корневого источника данных, а также по полю из другого источника данных (для страницы "Все клиенты")</span><span class="sxs-lookup"><span data-stu-id="11dd1-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-174">Н</span><span class="sxs-lookup"><span data-stu-id="11dd1-174">T</span></span></td>
<td><span data-ttu-id="11dd1-175">Сегодняшняя дата</span><span class="sxs-lookup"><span data-stu-id="11dd1-175">Today's date</span></span></td>
<td><span data-ttu-id="11dd1-176">Введите <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="11dd1-177"><strong>T</strong> соответствует сегодняшней дате.</span><span class="sxs-lookup"><span data-stu-id="11dd1-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-178">(имяМетода(параметры)) (метод <strong>SysQueryRangeUtil</strong> в скобках)</span><span class="sxs-lookup"><span data-stu-id="11dd1-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="11dd1-179">Сопоставление значения или диапазона значений, указанных в параметрах метода <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="11dd1-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="11dd1-180">Введите метод <strong>SysQueryRangeUtil</strong> с параметрами, которые задают значение или диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="11dd1-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="11dd1-181">Перейдите в раздел <strong>Расчеты с клиентами</strong> &gt; <strong>Накладные</strong> &gt; <strong>Открытые накладные клиента</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-182">Нажмите Ctrl+Shift+F3, чтобы открыть страницу <strong>Запрос</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="11dd1-183">На вкладке <strong>Диапазон</strong> нажмите кнопку <strong>Добавить</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-184">В поле <strong>Таблица</strong> выберите <strong>Открытые проводки по клиентам</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-185">В поле <strong>Поле</strong> выберите <strong>Срок выполнения</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-186">В поле <strong>Критерии</strong> введите <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-187">Нажмите кнопку <strong>OК</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="11dd1-188">Страница списка обновляется, и на ней отображаются накладные, соответствующие введенному условию.</span><span class="sxs-lookup"><span data-stu-id="11dd1-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="11dd1-189">В данном примере отображаются накладные, которые подлежали оплате в течение последних двух лет.</span><span class="sxs-lookup"><span data-stu-id="11dd1-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="11dd1-190">В таблице в следующем разделе приведены дополнительные сведения о методах даты <strong>SysQueryRangeUtil</strong> и несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="11dd1-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="11dd1-191">Расширенные запросы даты, которые используют методы SysQueryRangeUtil</span><span class="sxs-lookup"><span data-stu-id="11dd1-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="11dd1-192">Метод</span><span class="sxs-lookup"><span data-stu-id="11dd1-192">Method</span></span></th>
<th><span data-ttu-id="11dd1-193">Описание</span><span class="sxs-lookup"><span data-stu-id="11dd1-193">Description</span></span></th>
<th><span data-ttu-id="11dd1-194">Пример</span><span class="sxs-lookup"><span data-stu-id="11dd1-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="11dd1-195">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="11dd1-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="11dd1-196">Поиск даты по отношению к дате сессии.</span><span class="sxs-lookup"><span data-stu-id="11dd1-196">Find a date relative to the session date.</span></span> <span data-ttu-id="11dd1-197">Положительные значения показывают будущие даты, отрицательные значения показывают прошлые даты.</span><span class="sxs-lookup"><span data-stu-id="11dd1-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-198"><strong>Завтра</strong> — введите <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-199"><strong>Сегодня</strong> — введите <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-200"><strong>Вчера</strong> — введите <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="11dd1-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="11dd1-202">Поиск диапазона дат по отношению к дате сессии.</span><span class="sxs-lookup"><span data-stu-id="11dd1-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="11dd1-203">Положительные значения показывают будущие даты, отрицательные значения показывают прошлые даты.</span><span class="sxs-lookup"><span data-stu-id="11dd1-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-204"><strong>Последние 30 дней</strong> — введите <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-205"><strong>Предыдущие 30 дней и будущие 30 дней</strong> — введите <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="11dd1-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="11dd1-207">Поиск всех дат после указанной относительной даты.</span><span class="sxs-lookup"><span data-stu-id="11dd1-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-208"><strong>Больше чем 30 дней от сегодняшнего дня</strong> — введите <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="11dd1-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="11dd1-210">Поиск всех записей даты/времени после текущего момента времени.</span><span class="sxs-lookup"><span data-stu-id="11dd1-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-211"><strong>Все будущие даты/моменты времени</strong> — введите <strong>(GreaterThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="11dd1-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="11dd1-213">Поиск всех дат до указанной относительной даты.</span><span class="sxs-lookup"><span data-stu-id="11dd1-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-214"><strong>Меньше чем семь дней от сегодняшнего числа</strong> — введите <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="11dd1-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="11dd1-216">Поиск всех записей даты/времени до текущего момента времени.</span><span class="sxs-lookup"><span data-stu-id="11dd1-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-217"><strong>Все прошедшие даты/моменты времени</strong> — введите <strong>(LessThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="11dd1-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="11dd1-219">Поиск диапазона дат на основе месяца по отношению к текущему месяцу.</span><span class="sxs-lookup"><span data-stu-id="11dd1-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-220"><strong>Предыдущие два месяца</strong> — введите <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-221"><strong>Следующие три месяца</strong> — введите <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="11dd1-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="11dd1-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="11dd1-223">Поиск диапазона дат на основе числа лет по отношению к текущему году.</span><span class="sxs-lookup"><span data-stu-id="11dd1-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="11dd1-224"><strong>Следующий год</strong> — введите <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="11dd1-225"><strong>Предыдущий год</strong> — введите <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11dd1-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]