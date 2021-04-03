---
title: Функция электронной отчетности VALUEINLARGE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности VALUEINLARGE.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1e35c695d697e0d0f42baeaf568548273f9d205b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565816"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="e8cde-103">Функция электронной отчетности VALUEINLARGE</span><span class="sxs-lookup"><span data-stu-id="e8cde-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8cde-104">Функция `VALUEINLARGE` определяет, соответствует ли заданный ввод типа *Int64* или *Integer* какому-либо значению указанного элемента в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="e8cde-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="e8cde-105">Функция возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="e8cde-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="e8cde-106">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e8cde-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="e8cde-107">Чтобы понять разницу с функцией `VALUEIN`, см. раздел [Примечание об использовании](#usage_note) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="e8cde-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cde-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8cde-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="e8cde-109">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e8cde-109">Arguments</span></span>

<span data-ttu-id="e8cde-110">`input`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="e8cde-110">`input`: *Field*</span></span>

<span data-ttu-id="e8cde-111">Действительный путь элемента источника данных типа *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="e8cde-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="e8cde-112">Значение этого элемента будет сопоставляться.</span><span class="sxs-lookup"><span data-stu-id="e8cde-112">The value of this item will be matched.</span></span>

<span data-ttu-id="e8cde-113">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="e8cde-113">`list`: *Record list*</span></span>

<span data-ttu-id="e8cde-114">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="e8cde-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e8cde-115">`list item expression`: *выражение*</span><span class="sxs-lookup"><span data-stu-id="e8cde-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="e8cde-116">Допустимое условное выражение которое либо указывает на, либо содержит одно поле указанного списка, которое должно использоваться для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="e8cde-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8cde-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e8cde-117">Return values</span></span>

<span data-ttu-id="e8cde-118">*Логический*</span><span class="sxs-lookup"><span data-stu-id="e8cde-118">*Boolean*</span></span>

<span data-ttu-id="e8cde-119">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="e8cde-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="e8cde-120"><a name="usage_note">Примечания по использованию</a></span><span class="sxs-lookup"><span data-stu-id="e8cde-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="e8cde-121">Когда указанный ввод представляет тип *Int64* или *Integer* элемента источника данных, вызов которого может быть преобразован непосредственно в инструкцию SQL, указанный список преобразовывается во временную таблицу SQL, а соответствующий запрос выполняется в базе данных путем выполнения одного запроса `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="e8cde-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="e8cde-122">В противном случае эта функция работает как функция [`VALUEIN`](er-functions-logical-valuein.md).</span><span class="sxs-lookup"><span data-stu-id="e8cde-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="e8cde-123">Когда указанный ввод представляет собой элемент источника данных, который назначен как элемент, отличный от типа *Int64* и *Integer*, в режиме разработки возникает ошибка, информирующая, что функция `VALUEINLARGE` неприменима для настроенного выражения электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e8cde-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="e8cde-124">Если при выполнении выражения функции `VALUEINLARGE` используются нескольких временных таблиц в области этого выполнения, происходит ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e8cde-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="e8cde-125">Пример</span><span class="sxs-lookup"><span data-stu-id="e8cde-125">Example</span></span>

<span data-ttu-id="e8cde-126">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="e8cde-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="e8cde-127">Источник данных **In** типа *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="e8cde-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="e8cde-128">Этот источник данных ссылается на таблицу **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="e8cde-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="e8cde-129">Для параметра **Межфирменное** задано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="e8cde-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="e8cde-130">Источник данных **InMemory** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="e8cde-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="e8cde-131">Этот источник данных содержит выражение `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="e8cde-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="e8cde-132">Источник данных **InFiltered** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="e8cde-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="e8cde-133">Этот источник данных содержит выражение `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="e8cde-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="e8cde-134">Когда источник данных **InFiltered** вызывается в контексте компании **DEMF**, в базе данных приложений создается новая временная таблица, в эту таблицу вставляется собранный в памяти список идентификационных кодов записей, и создается следующая инструкция SQL, которая возвращает отфильтрованные записи таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="e8cde-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="e8cde-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e8cde-135">Additional resources</span></span>

[<span data-ttu-id="e8cde-136">Логические функции</span><span class="sxs-lookup"><span data-stu-id="e8cde-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="e8cde-137">Функции VALUEIN</span><span class="sxs-lookup"><span data-stu-id="e8cde-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]