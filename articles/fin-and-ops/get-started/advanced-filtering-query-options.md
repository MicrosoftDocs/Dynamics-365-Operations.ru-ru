---
title: "Расширенная фильтрация и синтаксис запросов"
description: "Эта статья описывает параметры фильтрации и запросов, которые доступны при использовании оператора \"matches\" в диалоговом окне расширенной фильтрации/сортировки."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fa9c962ffce161365d1a030cf9995cce3ff19934
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="fc8d4-103">Расширенная фильтрация и синтаксис запросов</span><span class="sxs-lookup"><span data-stu-id="fc8d4-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc8d4-104">Эта статья описывает параметры фильтрации и запросов, которые доступны при использовании оператора "matches" в диалоговом окне расширенной фильтрации/сортировки.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-104">This article describes the filtering and query options that are available when you use the "matches" operator in the Advanced filter/sort dialog.</span></span>

<a name="advanced-query-syntax"></a><span data-ttu-id="fc8d4-105">Синтаксис расширенного запроса</span><span class="sxs-lookup"><span data-stu-id="fc8d4-105">Advanced query syntax</span></span>
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc8d4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc8d4-106">Syntax</span></span></th>
<th><span data-ttu-id="fc8d4-107">Описание символов</span><span class="sxs-lookup"><span data-stu-id="fc8d4-107">Character description</span></span></th>
<th><span data-ttu-id="fc8d4-108">описание</span><span class="sxs-lookup"><span data-stu-id="fc8d4-108">Description</span></span></th>
<th><span data-ttu-id="fc8d4-109">Пример</span><span class="sxs-lookup"><span data-stu-id="fc8d4-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc8d4-110"><em>значение</em></span><span class="sxs-lookup"><span data-stu-id="fc8d4-110"><em>value</em></span></span></td>
<td><span data-ttu-id="fc8d4-111">Равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="fc8d4-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-112">Введите значение, которое требуется найти:</span><span class="sxs-lookup"><span data-stu-id="fc8d4-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="fc8d4-113">При вводе <strong>Виктор</strong> будет осуществлен поиск всех значений &quot;Виктор&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-114">!<em>значение</em> (восклицательный знак)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="fc8d4-115">Не равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="fc8d4-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-116">Введите восклицательный знак, затем значение, которое требуется исключить из поиска.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="fc8d4-117">При вводе <strong>!Виктор</strong> будет осуществлен поиск всех значений, кроме &quot;Виктор&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-118"><em>начальное-значение</em>..<em>конечное-значение</em> (две точки)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="fc8d4-119">Между двумя значениями, разделенными двумя точками</span><span class="sxs-lookup"><span data-stu-id="fc8d4-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="fc8d4-120">Введите начальное значение, затем две точки, затем конечное значение.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="fc8d4-121">Если ввести <strong>1..10</strong>, будут найдены все значения от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="fc8d4-122">Однако, если ввести текстовое выражение <strong>A..C</strong> , то будут найдены все значения, начинающиеся на &quot;A&quot; и &quot;B&quot;, а также значения, строго равные &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="fc8d4-123">Например, этот запрос не найдет &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-123">For example, this query won&#39;t find &quot;Ca&quot;.</span></span> <span data-ttu-id="fc8d4-124">Чтобы найти все значения, начинающиеся на буквы от &quot;A<em>&quot; до &quot;C</em>&quot;, следует ввести <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-125">..<em>значение</em> (две точки)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="fc8d4-126">Меньше или равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="fc8d4-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-127">Введите две точки, а затем необходимое значение.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="fc8d4-128">Если ввести <strong>..1000</strong>, то будут найдены все значения, меньшие или равные 1000, например &quot;100&quot;, &quot;999,95&quot; и &quot;1 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-129"><em>значение</em>..</span><span class="sxs-lookup"><span data-stu-id="fc8d4-129"><em>value</em>..</span></span> <span data-ttu-id="fc8d4-130">(две точки)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-130">(double period)</span></span></td>
<td><span data-ttu-id="fc8d4-131">Больше или равно введенному значению</span><span class="sxs-lookup"><span data-stu-id="fc8d4-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-132">Введите значение, затем две точки.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="fc8d4-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="fc8d4-133"><strong>1000..</strong></span></span> <span data-ttu-id="fc8d4-134">будут найдены все значения, большие или равные 1000, например &quot;1 000&quot;, &quot;1 000,01&quot; и &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-135">&gt;<em>значение</em> (знак "больше чем")</span><span class="sxs-lookup"><span data-stu-id="fc8d4-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="fc8d4-136">Больше, чем введенное значение</span><span class="sxs-lookup"><span data-stu-id="fc8d4-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-137">Введите знак "больше чем" (<strong>&gt;</strong>), а затем значение.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="fc8d4-138">Если ввести <strong>&gt;1000</strong>, то будут найдены все значения, большие 1000, например &quot;1000,01&quot;, &quot;20 000&quot; и &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-139">&lt;<em>значение</em> (знак "меньше чем")</span><span class="sxs-lookup"><span data-stu-id="fc8d4-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="fc8d4-140">Меньше, чем введенное значение</span><span class="sxs-lookup"><span data-stu-id="fc8d4-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-141">Введите знак "меньше чем" (<strong>&lt;</strong>), а затем значение.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="fc8d4-142">Если ввести <strong>&lt;1000</strong>, то будут найдены все значения, меньшие 1000, например &quot;999,99&quot;, &quot;1&quot; и &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-143"><em>значение</em>\* (звездочка)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="fc8d4-144">Начинается с введенного значения</span><span class="sxs-lookup"><span data-stu-id="fc8d4-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-145">Введите начальное значение для поиска, а затем звездочку (<strong><em></strong>).</span><span class="sxs-lookup"><span data-stu-id="fc8d4-145">Type the starting value and then an asterisk (<strong><em></strong>).</span></span></td>
<td><span data-ttu-id="fc8d4-146">Если ввести <strong>С</em></strong>, то будут найдены все записи, начинающиеся с &quot;С&quot;, например &quot;Стокгольм&quot;, &quot;Сидней&quot; и &quot;Сан-Франциско&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-146"><strong>S</em></strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-147"><em><em>значение</em> (звездочка)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-147"><em><em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="fc8d4-148">Заканчивается на введенное значение</span><span class="sxs-lookup"><span data-stu-id="fc8d4-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-149">Введите звездочку, а потом конечное значение для поиска.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="fc8d4-150">Если ввести <strong></em>восток</strong>, то будут найдены все записи, заканчивающиеся на &quot;восток&quot;, например &quot;северо-восток&quot; или &quot;юго-восток&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-150"><strong></em>east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-151"><em><em>значение</em></em> (звездочка)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-151"><em><em>value</em></em> (asterisk)</span></span></td>
<td><span data-ttu-id="fc8d4-152">Содержит введенное значение</span><span class="sxs-lookup"><span data-stu-id="fc8d4-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="fc8d4-153">Введите звездочку, затем значение, а затем снова звездочку.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="fc8d4-154">Если ввести <strong><em>во</em></strong>, то будут найдены все записи, содержащие &quot;во&quot;, например &quot;северо-восток&quot; или &quot;юго-восток&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-154"><strong><em>th</em></strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-155">?</span><span class="sxs-lookup"><span data-stu-id="fc8d4-155">?</span></span> <span data-ttu-id="fc8d4-156">(вопросительный знак)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-156">(question mark)</span></span></td>
<td><span data-ttu-id="fc8d4-157">Содержится один или более неизвестных символов</span><span class="sxs-lookup"><span data-stu-id="fc8d4-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="fc8d4-158">Введите вопросительный знак вместо неизвестного символа в значении.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="fc8d4-159">Если ввести <strong>В?ктор</strong>, то будут найдены &quot;Виктор&quot; и &quot;Вектор&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-160"><em>значение</em>,<em>значение</em> (запятая)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="fc8d4-161">Поиск записей, совпадающих с введенными через запятую значениями</span><span class="sxs-lookup"><span data-stu-id="fc8d4-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="fc8d4-162">Введите все критерии поиска, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="fc8d4-163">Если ввести <strong>A, D, F, G</strong>, то будут найдены &quot;A&quot;, &quot;D&quot;, &quot;F&quot; и &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="fc8d4-164">Если ввести <strong>10, 20, 30, 100</strong>, то будут найдены &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-165">(<span class="code">Оператор SQL</span>) (оператор SQL в скобках)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="fc8d4-166">Поиск согласно введенному запросу</span><span class="sxs-lookup"><span data-stu-id="fc8d4-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="fc8d4-167">В скобках введите запрос в виде SQL-выражения.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="fc8d4-168"><strong><span class="code">(источник данных.Имя поля != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="fc8d4-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-169">T</span><span class="sxs-lookup"><span data-stu-id="fc8d4-169">T</span></span></td>
<td><span data-ttu-id="fc8d4-170">Сегодняшняя дата</span><span class="sxs-lookup"><span data-stu-id="fc8d4-170">Today&#39;s date</span></span></td>
<td><span data-ttu-id="fc8d4-171">Введите <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="fc8d4-172"><strong>T</strong> соответствует сегодняшней дате.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-172"><strong>T</strong> matches today&#39;s date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-173">(имяМетода(параметры)) (метод <strong>SysQueryRangeUtil</strong> в скобках)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="fc8d4-174">Сопоставление значения или диапазона значений, указанных в параметрах метода <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="fc8d4-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="fc8d4-175">Введите метод <strong>SysQueryRangeUtil</strong> с параметрами, которые задают значение или диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="fc8d4-176">Перейдите в раздел <strong>Расчеты с клиентами</strong> &gt; <strong>Накладные</strong> &gt; <strong>Открытые накладные клиента</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-177">Нажмите Ctrl+Shift+F3, чтобы открыть страницу <strong>Запрос</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="fc8d4-178">На вкладке <strong>Диапазон</strong> нажмите кнопку <strong>Добавить</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-179">В поле <strong>Таблица</strong> выберите <strong>Открытые проводки по клиентам</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-180">В поле <strong>Поле</strong> выберите <strong>Срок выполнения</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-181">В поле <strong>Критерии</strong> введите <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-182">Нажмите кнопку <strong>OК</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="fc8d4-183">Страница списка обновляется, и на ней отображаются накладные, соответствующие введенному условию.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="fc8d4-184">В данном примере отображаются накладные, которые подлежали оплате в течение последних двух лет.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="fc8d4-185">В таблице в следующем разделе приведены дополнительные сведения о методах даты <strong>SysQueryRangeUtil</strong> и несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="fc8d4-186">Расширенные запросы даты, которые используют методы SysQueryRangeUtil</span><span class="sxs-lookup"><span data-stu-id="fc8d4-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc8d4-187">Метод</span><span class="sxs-lookup"><span data-stu-id="fc8d4-187">Method</span></span></th>
<th><span data-ttu-id="fc8d4-188">Описание</span><span class="sxs-lookup"><span data-stu-id="fc8d4-188">Description</span></span></th>
<th><span data-ttu-id="fc8d4-189">Пример</span><span class="sxs-lookup"><span data-stu-id="fc8d4-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc8d4-190">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="fc8d4-191">Поиск даты по отношению к дате сессии.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-191">Find a date relative to the session date.</span></span> <span data-ttu-id="fc8d4-192">Положительные значения показывают будущие даты, отрицательные значения показывают прошлые даты.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-193"><strong>Завтра</strong> — введите <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-194"><strong>Сегодня</strong> — введите <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-195"><strong>Вчера</strong> — введите <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="fc8d4-197">Поиск диапазона дат по отношению к дате сессии.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="fc8d4-198">Положительные значения показывают будущие даты, отрицательные значения показывают прошлые даты.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-199"><strong>Последние 30 дней</strong> — введите <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-200"><strong>Предыдущие 30 дней и будущие 30 дней</strong> — введите <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="fc8d4-202">Поиск всех дат после указанной относительной даты.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-203"><strong>Больше чем 30 дней от сегодняшнего дня</strong> — введите <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="fc8d4-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="fc8d4-205">Поиск всех записей даты/времени после текущего момента времени.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-206"><strong>Все будущие даты/моменты времени</strong> — введите <strong>(GreaterThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="fc8d4-208">Поиск всех дат до указанной относительной даты.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-209"><strong>Меньше чем семь дней от сегодняшнего числа</strong> — введите <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="fc8d4-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="fc8d4-211">Поиск всех записей даты/времени до текущего момента времени.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-212"><strong>Все прошедшие даты/моменты времени</strong> — введите <strong>(LessThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc8d4-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="fc8d4-214">Поиск диапазона дат на основе месяца по отношению к текущему месяцу.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-215"><strong>Предыдущие два месяца</strong> — введите <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-216"><strong>Следующие три месяца</strong> — введите <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc8d4-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="fc8d4-218">Поиск диапазона дат на основе числа лет по отношению к текущему году.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="fc8d4-219"><strong>Следующий год</strong> — введите <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="fc8d4-220"><strong>Предыдущий год</strong> — введите <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






