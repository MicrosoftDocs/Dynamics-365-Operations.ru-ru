---
title: "Расширенная фильтрация и синтаксис запросов"
description: "Эта статья описывает параметры фильтрации и запросов, которые доступны при использовании оператора &quot;matches&quot; в диалоговом окне расширенной фильтрации/сортировки."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>Расширенная фильтрация и синтаксис запросов

Эта статья описывает параметры фильтрации и запросов, которые доступны при использовании оператора "matches" в диалоговом окне расширенной фильтрации/сортировки.

<a name="advanced-query-syntax"></a>Синтаксис расширенный запрос
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
<th>Синтаксис</th>
<th>Описание символов</th>
<th>описание</th>
<th>Пример</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>значение</em></td>
<td>Равно введенному значению</td>
<td>Введите значение, которое требуется найти:</td>
<td><strong>Виктор</strong>, то будут найдены &quot;Виктор&quot;.</td>
</tr>
<tr class="even">
<td>! <em>значение</em> (восклицательный знак)</td>
<td>Не равно введенному значению</td>
<td>Введите восклицательный знак, затем значение, которое требуется исключить из поиска.</td>
<td><strong>! Виктор</strong>, то будут найдены все значения, кроме &quot;Виктор&quot;.</td>
</tr>
<tr class="odd">
<td><em>начальное-значение</em>..<em>конечное-значение</em> (две точки)</td>
<td>Между двумя значениями, разделенными двумя точками</td>
<td>Введите начальное значение, затем две точки, затем конечное значение.</td>
<td><strong>1..10</strong>, то будут найдены все значения от 1 до 10. Однако в поля строки <strong>A.. C</strong>, то будут найдены все значения, начинающиеся с &quot;A&quot; и &quot;B&quot;и значения, которые точно равны &quot;C&quot;. Например, этот запрос не будет найден &quot;Ca&quot;. Чтобы найти все значения из &quot;A*&quot; через &quot;C*&quot;, тип <strong>A.. D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>значение</em> (две точки)</td>
<td>Меньше или равно введенному значению</td>
<td>Введите две точки, а затем необходимое значение.</td>
<td><strong>.. 1000</strong> будут найдены все значения, которое меньше или равно 1000, таких как &quot;100&quot;, &quot;999.95&quot;, и &quot;1000&quot;.</td>
</tr>
<tr class="odd">
<td><em>значение</em>.. (две точки)</td>
<td>Больше или равно введенному значению</td>
<td>Введите значение, затем две точки.</td>
<td><strong>1000..</strong> будут найдены все значения, которое больше или равно 1000, таких как &quot;1000&quot;, &quot;1000,01&quot;, и &quot;1 000 000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>значение</em> (знак больше)</td>
<td>Больше, чем введенное значение</td>
<td>Введите знак больше (<strong>&gt;</strong>), а затем значение.</td>
<td><strong>&gt;1000</strong> будут найдены все значения, большие 1000, таких как &quot;1000,01&quot;, &quot;20 000&quot;, и &quot;1 000 000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>значение</em> (знак меньше)</td>
<td>Меньше, чем введенное значение</td>
<td>Введите «меньше» (<strong>&lt;</strong>), а затем значение.</td>
<td><strong>&lt;1000</strong> будут найдены все значения, меньшие 1000, таких как &quot;999,99&quot;, &quot;1&quot;, и &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>значение</em>* (звездочка)</td>
<td>Начинается с введенного значения</td>
<td>Введите начальное значение, а затем звездочку (<strong>*</strong>).</td>
<td><strong>S *</strong> находит какого-либо строка, которая начинается с &quot;S&quot;, таких как &quot;Стокгольм&quot;, &quot;Сидней&quot;, и &quot;Сан-Франциско&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>Заканчивается на введенное значение</td>
<td>Введите звездочку, а потом конечное значение для поиска.</td>
<td><strong>* Восток</strong> какого-либо строка, которая находит заканчивается &quot;Восток&quot;, таких как &quot;северо-восток&quot; и &quot;юго-восток&quot;.</td>
</tr>
<tr class="even">
<td>*<em>значение</em>* (звездочка)</td>
<td>Содержит введенное значение</td>
<td>Введите звездочку, затем значение, а затем снова звездочку.</td>
<td><strong>*о-в*</strong> находит какого-либо строка, которая содержит &quot;ой&quot;, таких как &quot;северо-восток&quot; и &quot;юго-восток&quot;.</td>
</tr>
<tr class="odd">
<td>? (вопросительный знак)</td>
<td>Содержится один или более неизвестных символов</td>
<td>Введите вопросительный знак вместо неизвестного символа в значении.</td>
<td><strong>Если? ктор</strong>, то будут найдены &quot;Виктор&quot; и &quot;вектор&quot;.</td>
</tr>
<tr class="even">
<td><em>значение</em>,<em>значение</em> (запятая)</td>
<td>Поиск записей, совпадающих с введенными через запятую значениями</td>
<td>Введите все критерии поиска, разделяя их запятыми.</td>
<td><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;. <strong>10, 20, 30, 100</strong> найдены &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">Оператор SQL</span>) (оператор SQL в скобках)</td>
<td>Поиск согласно введенному запросу</td>
<td>В скобках введите запрос в виде SQL-выражения.</td>
<td><strong><span class="code">(источник данных. FieldName! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>В</td>
<td>Сегодняшняя дата</td>
<td>Введите <strong>T</strong>.</td>
<td><strong>T</strong> соответствует сегодняшней дате.</td>
</tr>
<tr class="odd">
<td>(имяМетода(параметры)) (метод <strong>SysQueryRangeUtil</strong> в скобках)</td>
<td>Сопоставление значения или диапазона значений, указанных в параметрах метода <strong>SysQueryRangeUtil</strong></td>
<td>Введите метод <strong>SysQueryRangeUtil</strong> с параметрами, которые задают значение или диапазон значений.</td>
<td><ol>
<li>Щелкните <strong>Расчеты с клиентами</strong>&gt;<strong>накладные</strong>&gt;<strong>открытые накладные клиента</strong>.</li>
<li>Нажмите Ctrl+Shift+F3, чтобы открыть страницу <strong>Запрос</strong>.</li>
<li>На вкладке <strong>Диапазон</strong> нажмите кнопку <strong>Добавить</strong>.</li>
<li>В поле <strong>Таблица</strong> выберите <strong>Открытые проводки по клиентам</strong>.</li>
<li>В поле <strong>Поле</strong> выберите <strong>Срок выполнения</strong>.</li>
<li>В поле <strong>Критерии</strong> введите <strong>(yearRange(-2,0))</strong>.</li>
<li>Нажмите кнопку <strong>OК</strong>. Страница списка обновляется, и на ней отображаются накладные, соответствующие введенному условию. В данном примере отображаются накладные, которые подлежали оплате в течение последних двух лет.</li>
</ol>
В таблице в следующем разделе приведены дополнительные сведения о методах даты <strong> SysQueryRangeUtil</strong> и несколько примеров.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Расширенные запросы даты, которые используют методы SysQueryRangeUtil
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Метод</th>
<th>Описание</th>
<th>Пример</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Day (_relativeDays=0)</td>
<td>Поиск даты по отношению к дате сессии. Положительные значения показывают будущие даты, отрицательные значения показывают прошлые даты.</td>
<td><ul>
<li><strong>Завтра</strong> — введите <strong>(Day(1))</strong>.</li>
<li><strong>Сегодня</strong> — введите <strong>(Day(0))</strong>.</li>
<li><strong>Вчера</strong> — введите <strong>(Day(-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Поиск диапазона дат по отношению к дате сессии. Положительные значения показывают будущие даты, отрицательные значения показывают прошлые даты.</td>
<td><ul>
<li><strong>Последние 30 дней</strong> — введите <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Предыдущие 30 дней и будущие 30 дней</strong> — введите <strong>(DayRange(-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Поиск всех дат после указанной относительной даты.</td>
<td><ul>
<li><strong>Больше чем 30 дней от сегодняшнего дня</strong> — введите <strong>(GreaterThanDate(30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Поиск всех записей даты/времени после текущего момента времени.</td>
<td><ul>
<li><strong>Все будущие даты/моменты времени</strong> — введите <strong>(GreaterThanUtcNow ())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Поиск всех дат до указанной относительной даты.</td>
<td><ul>
<li><strong>Меньше чем семь дней от сегодняшнего числа</strong> — введите <strong>(LessThanDate(7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Поиск всех записей даты/времени до текущего момента времени.</td>
<td><ul>
<li><strong>Все прошедшие даты/моменты времени</strong> — введите <strong>(LessThanUtcNow ())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Поиск диапазона дат на основе месяца по отношению к текущему месяцу.</td>
<td><ul>
<li><strong>Предыдущие два месяца</strong> — введите <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Следующие три месяца</strong> — введите <strong>(MonthRange(0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Поиск диапазона дат на основе числа лет по отношению к текущему году.</td>
<td><ul>
<li><strong>Следующий год</strong> — введите <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Предыдущий год</strong> — введите <strong>(YearRange(-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>




