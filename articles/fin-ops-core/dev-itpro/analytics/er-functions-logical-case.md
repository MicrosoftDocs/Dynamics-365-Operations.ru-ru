---
title: Функция ER CASE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CASE.
author: NickSelin
ms.date: 12/17/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44815160957922f508fccd72174be2c4145a8d89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745457"
---
# <a name="case-er-function"></a><span data-ttu-id="b1834-103">Функция ER CASE</span><span class="sxs-lookup"><span data-stu-id="b1834-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1834-104">Функция `CASE` оценивает значение указанного выражения по сравнению с указанными альтернативными вариантами и возвращает результат первого варианта, равного значению указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="b1834-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="b1834-105">В противном случае возвращает дополнительный результат по умолчанию, если результат по умолчанию указан в качестве последнего аргумента вызванной функции, которой не предшествует вариант.</span><span class="sxs-lookup"><span data-stu-id="b1834-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="b1834-106">Возвращаемое значение может быть значением любого из поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="b1834-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1834-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1834-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="b1834-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b1834-108">Arguments</span></span>

<span data-ttu-id="b1834-109">`expression`: *Примитивный тип данных* (логический, числовой или текстовый)</span><span class="sxs-lookup"><span data-stu-id="b1834-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="b1834-110">Допустимое выражение, возвращающее значение примитивного типа данных.</span><span class="sxs-lookup"><span data-stu-id="b1834-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="b1834-111">`option 1`: *Примитивный тип данных* (логический, числовой или текстовый)</span><span class="sxs-lookup"><span data-stu-id="b1834-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="b1834-112">Допустимое выражение, возвращающее значение того же примитивного типа данных, что и аргумент `expression` вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="b1834-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="b1834-113">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="b1834-113">This argument is required.</span></span>

<span data-ttu-id="b1834-114">`result 1`: *Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="b1834-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="b1834-115">Возвращаемый результат, соответствующий предыдущему параметру.</span><span class="sxs-lookup"><span data-stu-id="b1834-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="b1834-116">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="b1834-116">This argument is required.</span></span>

<span data-ttu-id="b1834-117">`option N`: *Примитивный тип данных* (логический, числовой или текстовый)</span><span class="sxs-lookup"><span data-stu-id="b1834-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="b1834-118">Допустимое выражение, возвращающее значение того же примитивного типа данных, что и аргумент `expression` вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="b1834-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="b1834-119">Это необязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b1834-119">This argument is optional.</span></span>

<span data-ttu-id="b1834-120">`result N`: *Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="b1834-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="b1834-121">Возвращаемый результат, соответствующий предыдущему параметру.</span><span class="sxs-lookup"><span data-stu-id="b1834-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="b1834-122">Это необязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b1834-122">This argument is optional.</span></span>

<span data-ttu-id="b1834-123">`default result`: *Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="b1834-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="b1834-124">Результат, который должен быть возвращен, если нет совпадения.</span><span class="sxs-lookup"><span data-stu-id="b1834-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="b1834-125">Это необязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b1834-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1834-126">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b1834-126">Return values</span></span>

<span data-ttu-id="b1834-127">*Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="b1834-127">*Any of the supported data types*</span></span>

<span data-ttu-id="b1834-128">Полученное значение любого из поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="b1834-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1834-129">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="b1834-129">Usage notes</span></span>

<span data-ttu-id="b1834-130">Исключение выдается во время выполнения, если нет совпадения и не задан дополнительный результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1834-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="b1834-131">Все результаты должны быть указаны с помощью одного и того же типа данных.</span><span class="sxs-lookup"><span data-stu-id="b1834-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="b1834-132">Исключение выдается во время разработки, если типы данных настроенных результатов не совпадают.</span><span class="sxs-lookup"><span data-stu-id="b1834-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="b1834-133">Если значение первого результата и значение *n*-го результата являются значениями типа данных *Контейнер (запись)* или *Список записей*, то в результате есть только поля, которые существуют в обоих значениях.</span><span class="sxs-lookup"><span data-stu-id="b1834-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="b1834-134">Пример</span><span class="sxs-lookup"><span data-stu-id="b1834-134">Example</span></span>

<span data-ttu-id="b1834-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` возвращает строку **"WINTER"**, если текущая дата сеанса приложения приходится на период с октября по декабрь.</span><span class="sxs-lookup"><span data-stu-id="b1834-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="b1834-136">В противном случае она возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="b1834-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1834-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1834-137">Additional resources</span></span>

[<span data-ttu-id="b1834-138">Логические функции</span><span class="sxs-lookup"><span data-stu-id="b1834-138">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]