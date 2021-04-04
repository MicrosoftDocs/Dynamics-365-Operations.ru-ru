---
title: Функция ER NUMBERVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMBERVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561430"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="6d226-103">Функция ER NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="6d226-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d226-104">Функция `NUMBERVALUE` возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="6d226-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="6d226-105">При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.</span><span class="sxs-lookup"><span data-stu-id="6d226-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d226-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d226-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="6d226-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="6d226-107">Arguments</span></span>

<span data-ttu-id="6d226-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="6d226-108">`text`: *String*</span></span>

<span data-ttu-id="6d226-109">Текстовое значение, которое должно быть преобразовано в *вещественное* число.</span><span class="sxs-lookup"><span data-stu-id="6d226-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="6d226-110">`decimal separator`: Строка</span><span class="sxs-lookup"><span data-stu-id="6d226-110">`decimal separator`: String</span></span>

<span data-ttu-id="6d226-111">Десятичный разделитель.</span><span class="sxs-lookup"><span data-stu-id="6d226-111">A decimal separator.</span></span> <span data-ttu-id="6d226-112">Он используется для разделения целых и дробных частей десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="6d226-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="6d226-113">`digit grouping separator`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="6d226-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="6d226-114">Разделитель групп цифр.</span><span class="sxs-lookup"><span data-stu-id="6d226-114">A digit grouping separator.</span></span> <span data-ttu-id="6d226-115">Он используется в качестве разделителя тысяч.</span><span class="sxs-lookup"><span data-stu-id="6d226-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="6d226-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6d226-116">Return values</span></span>

<span data-ttu-id="6d226-117">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="6d226-117">*Real*</span></span>

<span data-ttu-id="6d226-118">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="6d226-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="6d226-119">Пример</span><span class="sxs-lookup"><span data-stu-id="6d226-119">Example</span></span>

<span data-ttu-id="6d226-120">`NUMBERVALUE( "1 234,56", ",", " ")` возвращает **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="6d226-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d226-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d226-121">Additional resources</span></span>

[<span data-ttu-id="6d226-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="6d226-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]