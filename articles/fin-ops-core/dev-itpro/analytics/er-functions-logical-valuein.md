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
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041707"
---
# <span data-ttu-id="9ca89-103"><a name="VALUEIN">Функция ER VALUEIN</a></span><span class="sxs-lookup"><span data-stu-id="9ca89-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ca89-104">Функция `VALUEIN` определяет, соответствует ли заданный ввод какому-либо значению указанного элемента в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="9ca89-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="9ca89-105">Она возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="9ca89-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="9ca89-106">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca89-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ca89-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="9ca89-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9ca89-108">Arguments</span></span>

<span data-ttu-id="9ca89-109">`input`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="9ca89-109">`input`: *Field*</span></span>

<span data-ttu-id="9ca89-110">Действительный путь элемента источника данных типа *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="9ca89-111">Значение этого элемента будет сопоставляться.</span><span class="sxs-lookup"><span data-stu-id="9ca89-111">The value of this item will be matched.</span></span>

<span data-ttu-id="9ca89-112">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="9ca89-112">`list`: *Record list*</span></span>

<span data-ttu-id="9ca89-113">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9ca89-114">`list item expression`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="9ca89-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="9ca89-115">Допустимое условное выражение которое либо указывает на, либо содержит одно поле указанного списка, которое должно использоваться для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9ca89-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="9ca89-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9ca89-116">Return values</span></span>

<span data-ttu-id="9ca89-117">*Логический*</span><span class="sxs-lookup"><span data-stu-id="9ca89-117">*Boolean*</span></span>

<span data-ttu-id="9ca89-118">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="9ca89-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9ca89-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="9ca89-119">Usage notes</span></span>

<span data-ttu-id="9ca89-120">Как правило, функция `VALUEIN` переводится в набор условий **OR**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="9ca89-121">В некоторых случаях она может быть переведена в выписку из базы данных SQL с помощью оператора `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="9ca89-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="9ca89-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ca89-122">Example 1</span></span>

<span data-ttu-id="9ca89-123">В своем сопоставлении модели вы определяете источник данных **Список** типа *Рассчитываемое поле*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="9ca89-124">Этот источник данных содержит выражение `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="9ca89-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="9ca89-125">Когда вызывается источник данных, если он был настроен как выражение `VALUEIN ("B", List, List.Value)`, он возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="9ca89-126">В этом случае функция `VALUEIN` переводится в следующий набор условий: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, где `("B" = "b")` равно **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="9ca89-127">Когда вызывается источник данных, если он был настроен как выражение `VALUEIN ("B", List, LEFT(List.Value, 0))`, он возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="9ca89-128">В этом случае функция `VALUEIN` переводится в следующее условие: `("B" = "")`, где не равно **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="9ca89-129">Верхний предел для числа символов в тексте таких условий составляет 32 768 знаков.</span><span class="sxs-lookup"><span data-stu-id="9ca89-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="9ca89-130">Таким образом, не следует создавать источники данных, которые могут превысить этот предел во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9ca89-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="9ca89-131">Если предел превышен, приложение перестанет работать, и будет создано исключение.</span><span class="sxs-lookup"><span data-stu-id="9ca89-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="9ca89-132">Например, такая ситуация возможна, если источник данных настроен как `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, а списки **List1** и **List2** содержат большой объем записей.</span><span class="sxs-lookup"><span data-stu-id="9ca89-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="9ca89-133">В некоторых случаях функция `VALUEIN` переводится в инструкцию базы данных с помощью оператора `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="9ca89-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="9ca89-134">Это происходит, когда функция [FILTER](er-functions-list-filter.md) используется и выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="9ca89-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="9ca89-135">Параметр **ASK FOR QUERY** отключен для источника данных функции `VALUEIN`, которая относится к списку записей.</span><span class="sxs-lookup"><span data-stu-id="9ca89-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="9ca89-136">Никакие дополнительные условия не будут применены к этому источнику данных во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9ca89-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="9ca89-137">Никакие вложенные выражения не настроены для источника данных функции `VALUEIN`, которая относится к списку записей.</span><span class="sxs-lookup"><span data-stu-id="9ca89-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="9ca89-138">Элемент списка функции `VALUEIN` ссылается на поле указанного источника данных, не выражения или метод такого источника данных.</span><span class="sxs-lookup"><span data-stu-id="9ca89-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="9ca89-139">Рекомендуется использовать этот параметр вместо функции [WHERE](er-functions-list-where.md), как описано ранее в этом примере.</span><span class="sxs-lookup"><span data-stu-id="9ca89-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="9ca89-140">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9ca89-140">Example 2</span></span>

<span data-ttu-id="9ca89-141">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="9ca89-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="9ca89-142">Источник данных **In** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="9ca89-143">Этот источник данных ссылается на таблицу Интрастат.</span><span class="sxs-lookup"><span data-stu-id="9ca89-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="9ca89-144">Источник данных **Порт** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="9ca89-145">Этот источник данных ссылается на таблицу IntrastatPort.</span><span class="sxs-lookup"><span data-stu-id="9ca89-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="9ca89-146">При вызове источника данных, который настроен как выражение `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, для возврата отфильтрованных записей таблицы Интрастат формируется следующая инструкция SQL.</span><span class="sxs-lookup"><span data-stu-id="9ca89-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="9ca89-147">Для поля **dataAreaId** последняя инструкция SQL создается с помощью оператора `IN`.</span><span class="sxs-lookup"><span data-stu-id="9ca89-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="9ca89-148">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9ca89-148">Example 3</span></span>

<span data-ttu-id="9ca89-149">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="9ca89-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="9ca89-150">Источник данных **Le** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="9ca89-151">Этот источник данных содержит выражение `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="9ca89-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="9ca89-152">Источник данных **In** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="9ca89-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="9ca89-153">Этот источник данных относится к таблице Интрастат, и для нее включен параметр **Межфирменное взаимодействие**.</span><span class="sxs-lookup"><span data-stu-id="9ca89-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="9ca89-154">При вызове источника данных, который настроен как выражение `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, конечный оператор SQL содержит следующее условие.</span><span class="sxs-lookup"><span data-stu-id="9ca89-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="9ca89-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ca89-155">Additional resources</span></span>

[<span data-ttu-id="9ca89-156">Логические функции</span><span class="sxs-lookup"><span data-stu-id="9ca89-156">Logical functions</span></span>](er-functions-category-logical.md)
