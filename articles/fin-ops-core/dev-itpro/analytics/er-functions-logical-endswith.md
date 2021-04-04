---
title: Функция электронной отчетности ENDSWITH
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ENDSWITH.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557547"
---
# <a name="endswith-er-function"></a><span data-ttu-id="f8364-103">Функция электронной отчетности ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="f8364-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8364-104">Функция `ENDSWITH` определяет, содержит ли заданный ввод заканчивается заданным текстом.</span><span class="sxs-lookup"><span data-stu-id="f8364-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="f8364-105">Это возвращает *логическое* значение **TRUE**, если заданный ввод заканчивается заданным текстом.</span><span class="sxs-lookup"><span data-stu-id="f8364-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="f8364-106">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f8364-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8364-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8364-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="f8364-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="f8364-108">Arguments</span></span>

<span data-ttu-id="f8364-109">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="f8364-109">`input`: *String*</span></span>

<span data-ttu-id="f8364-110">Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может заканчиваться с второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="f8364-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="f8364-111">`start text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="f8364-111">`start text`: *String*</span></span>

<span data-ttu-id="f8364-112">Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может быть в конце первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="f8364-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8364-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f8364-113">Return values</span></span>

<span data-ttu-id="f8364-114">*Логический*</span><span class="sxs-lookup"><span data-stu-id="f8364-114">*Boolean*</span></span>

<span data-ttu-id="f8364-115">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="f8364-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f8364-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="f8364-116">Usage notes</span></span>

<span data-ttu-id="f8364-117">Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="f8364-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="f8364-118">В противном случае исключение создается во время разработки.</span><span class="sxs-lookup"><span data-stu-id="f8364-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="f8364-119">Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="f8364-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="f8364-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8364-120">Example 1</span></span>

<span data-ttu-id="f8364-121">Выражение `ENDSWITH ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `ENDSWITH ("abc", "C")` возвращает значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="f8364-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f8364-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f8364-122">Example 2</span></span>

<span data-ttu-id="f8364-123">Выражение `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** заканчивается строкой **USA**.</span><span class="sxs-lookup"><span data-stu-id="f8364-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="f8364-124">В противном случае возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f8364-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8364-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8364-125">Additional resources</span></span>

[<span data-ttu-id="f8364-126">Логические функции</span><span class="sxs-lookup"><span data-stu-id="f8364-126">Logical functions</span></span>](er-functions-category-logical.md)