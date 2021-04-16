---
title: Функция электронной отчетности CONTAINS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CONTAINS.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c1d2d761a38d0edfb9abd439e0f710b336f54927
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745433"
---
# <a name="contains-er-function"></a><span data-ttu-id="372c5-103">Функция электронной отчетности CONTAINS</span><span class="sxs-lookup"><span data-stu-id="372c5-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="372c5-104">Функция `CONTAINS` определяет, содержит ли заданный ввод заданный текст.</span><span class="sxs-lookup"><span data-stu-id="372c5-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="372c5-105">Это возвращает *логическое* значение **TRUE**, если заданный ввод содержит заданный текст.</span><span class="sxs-lookup"><span data-stu-id="372c5-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="372c5-106">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="372c5-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="372c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="372c5-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="372c5-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="372c5-108">Arguments</span></span>

<span data-ttu-id="372c5-109">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="372c5-109">`input`: *String*</span></span>

<span data-ttu-id="372c5-110">Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может содержать второй аргумент.</span><span class="sxs-lookup"><span data-stu-id="372c5-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="372c5-111">`search text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="372c5-111">`search text`: *String*</span></span>

<span data-ttu-id="372c5-112">Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может содержаться в первом аргументе.</span><span class="sxs-lookup"><span data-stu-id="372c5-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="372c5-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="372c5-113">Return values</span></span>

<span data-ttu-id="372c5-114">*Логический*</span><span class="sxs-lookup"><span data-stu-id="372c5-114">*Boolean*</span></span>

<span data-ttu-id="372c5-115">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="372c5-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="372c5-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="372c5-116">Usage notes</span></span>

<span data-ttu-id="372c5-117">Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="372c5-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="372c5-118">В противном случае исключение создается во время разработки.</span><span class="sxs-lookup"><span data-stu-id="372c5-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="372c5-119">Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="372c5-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="372c5-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="372c5-120">Example 1</span></span>

<span data-ttu-id="372c5-121">Выражение `CONTAINS ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `CONTAINS ("abc", "C")` возвращает значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="372c5-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="372c5-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="372c5-122">Example 2</span></span>

<span data-ttu-id="372c5-123">Выражение `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** содержит строку **DEU**.</span><span class="sxs-lookup"><span data-stu-id="372c5-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="372c5-124">В противном случае возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="372c5-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="372c5-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="372c5-125">Additional resources</span></span>

[<span data-ttu-id="372c5-126">Логические функции</span><span class="sxs-lookup"><span data-stu-id="372c5-126">Logical functions</span></span>](er-functions-category-logical.md)
