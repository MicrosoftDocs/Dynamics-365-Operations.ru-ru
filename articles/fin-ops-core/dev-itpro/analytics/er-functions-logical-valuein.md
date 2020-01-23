---
title: Функция ER VALUEIN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности VALUEIN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915978"
---
# <span data-ttu-id="cfdfa-103"><a name="VALUEIN">Функция ER VALUEIN</a></span><span class="sxs-lookup"><span data-stu-id="cfdfa-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfdfa-104">Функция `VALUEIN` определяет, соответствует ли заданный ввод какому-либо значению указанного элемента в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="cfdfa-105">Она возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="cfdfa-106">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfdfa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfdfa-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="cfdfa-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="cfdfa-108">Arguments</span></span>

<span data-ttu-id="cfdfa-109">`input`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="cfdfa-109">`input`: *Field*</span></span>

<span data-ttu-id="cfdfa-110">Действительный путь элемента источника данных типа *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="cfdfa-111">Значение этого элемента будет сопоставляться.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-111">The value of this item will be matched.</span></span>

<span data-ttu-id="cfdfa-112">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="cfdfa-112">`list`: *Record list*</span></span>

<span data-ttu-id="cfdfa-113">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="cfdfa-114">`list item expression`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="cfdfa-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="cfdfa-115">Допустимое условное выражение которое либо указывает на, либо содержит одно поле указанного списка, которое должно использоваться для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="cfdfa-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cfdfa-116">Return values</span></span>

<span data-ttu-id="cfdfa-117">*Логический*</span><span class="sxs-lookup"><span data-stu-id="cfdfa-117">*Boolean*</span></span>

<span data-ttu-id="cfdfa-118">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cfdfa-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="cfdfa-119">Usage notes</span></span>

<span data-ttu-id="cfdfa-120">Как правило, функция `VALUEIN` переводится в набор условий **OR**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="cfdfa-121">В некоторых случаях она может быть переведена в выписку из базы данных SQL с помощью оператора `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="cfdfa-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfdfa-122">Example 1</span></span>

<span data-ttu-id="cfdfa-123">В своем сопоставлении модели вы определяете источник данных **Список** типа *Рассчитываемое поле*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="cfdfa-124">Этот источник данных содержит выражение `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="cfdfa-125">Когда вызывается источник данных, если он был настроен как выражение `VALUEIN ("B", List, List.Value)`, он возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="cfdfa-126">В этом случае функция `VALUEIN` переводится в следующий набор условий: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, где `("B" = "b")` равно **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="cfdfa-127">Когда вызывается источник данных, если он был настроен как выражение `VALUEIN ("B", List, LEFT(List.Value, 0))`, он возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="cfdfa-128">В этом случае функция `VALUEIN` переводится в следующее условие: `("B" = "")`, где не равно **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="cfdfa-129">Верхний предел для числа символов в тексте таких условий составляет 32 768 знаков.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="cfdfa-130">Таким образом, не следует создавать источники данных, которые могут превысить этот предел во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="cfdfa-131">Если предел превышен, приложение перестанет работать, и будет создано исключение.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="cfdfa-132">Например, такая ситуация возможна, если источник данных настроен как `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, а списки **List1** и **List2** содержат большой объем записей.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="cfdfa-133">В некоторых случаях функция `VALUEIN` переводится в инструкцию базы данных с помощью оператора `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="cfdfa-134">Это происходит, когда функция [FILTER](er-functions-list-filter.md) используется и выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="cfdfa-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="cfdfa-135">Параметр **ASK FOR QUERY** отключен для источника данных функции `VALUEIN`, которая относится к списку записей.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="cfdfa-136">Никакие дополнительные условия не будут применены к этому источнику данных во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="cfdfa-137">Никакие вложенные выражения не настроены для источника данных функции `VALUEIN`, которая относится к списку записей.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="cfdfa-138">Элемент списка функции `VALUEIN` ссылается на поле указанного источника данных, не выражения или метод такого источника данных.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="cfdfa-139">Рекомендуется использовать этот параметр вместо функции [WHERE](er-functions-list-where.md), как описано ранее в этом примере.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="cfdfa-140">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cfdfa-140">Example 2</span></span>

<span data-ttu-id="cfdfa-141">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="cfdfa-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="cfdfa-142">Источник данных **In** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="cfdfa-143">Этот источник данных ссылается на таблицу Интрастат.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="cfdfa-144">Источник данных **Порт** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="cfdfa-145">Этот источник данных ссылается на таблицу IntrastatPort.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="cfdfa-146">При вызове источника данных, который настроен как выражение `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, для возврата отфильтрованных записей таблицы Интрастат формируется следующая инструкция SQL.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="cfdfa-147">Для поля **dataAreaId** последняя инструкция SQL создается с помощью оператора `IN`.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="cfdfa-148">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cfdfa-148">Example 3</span></span>

<span data-ttu-id="cfdfa-149">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="cfdfa-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="cfdfa-150">Источник данных **Le** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="cfdfa-151">Этот источник данных содержит выражение `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="cfdfa-152">Источник данных **In** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="cfdfa-153">Этот источник данных относится к таблице Интрастат, и для нее включен параметр **Межфирменное взаимодействие**.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="cfdfa-154">При вызове источника данных, который настроен как выражение `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, конечный оператор SQL содержит следующее условие.</span><span class="sxs-lookup"><span data-stu-id="cfdfa-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="cfdfa-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cfdfa-155">Additional resources</span></span>

[<span data-ttu-id="cfdfa-156">Логические функции</span><span class="sxs-lookup"><span data-stu-id="cfdfa-156">Logical functions</span></span>](er-functions-category-logical.md)
