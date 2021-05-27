---
title: Функция электронной отчетности STARTSWITH
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности STARTSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048850"
---
# <a name="startswith-er-function"></a><span data-ttu-id="e5007-103">Функция электронной отчетности STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="e5007-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5007-104">Функция `STARTSWITH` определяет, содержит ли заданный ввод начинается заданным текстом.</span><span class="sxs-lookup"><span data-stu-id="e5007-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="e5007-105">Это возвращает *логическое* значение **TRUE**, если заданный ввод начинается заданным текстом.</span><span class="sxs-lookup"><span data-stu-id="e5007-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="e5007-106">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e5007-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5007-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5007-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="e5007-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e5007-108">Arguments</span></span>

<span data-ttu-id="e5007-109">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="e5007-109">`input`: *String*</span></span>

<span data-ttu-id="e5007-110">Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может начинаться с второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="e5007-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="e5007-111">`start text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="e5007-111">`start text`: *String*</span></span>

<span data-ttu-id="e5007-112">Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может быть в начале первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="e5007-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="e5007-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e5007-113">Return values</span></span>

<span data-ttu-id="e5007-114">*Логический*</span><span class="sxs-lookup"><span data-stu-id="e5007-114">*Boolean*</span></span>

<span data-ttu-id="e5007-115">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="e5007-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e5007-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="e5007-116">Usage notes</span></span>

<span data-ttu-id="e5007-117">Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e5007-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="e5007-118">В противном случае исключение создается во время разработки.</span><span class="sxs-lookup"><span data-stu-id="e5007-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="e5007-119">Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="e5007-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="e5007-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5007-120">Example 1</span></span>

<span data-ttu-id="e5007-121">Выражение `STARTSWITH ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `STARTSWITH ("abc", "A")` возвращает значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e5007-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e5007-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5007-122">Example 2</span></span>

<span data-ttu-id="e5007-123">Выражение `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** начинается со строки **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="e5007-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="e5007-124">В противном случае возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e5007-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5007-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e5007-125">Additional resources</span></span>

[<span data-ttu-id="e5007-126">Логические функции</span><span class="sxs-lookup"><span data-stu-id="e5007-126">Logical functions</span></span>](er-functions-category-logical.md)
