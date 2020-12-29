---
title: Функция ER NUMBERVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMBERVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d3eec6dc5a472f366c9029456fe05cf1e431e1c5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685987"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="c2100-103">Функция ER NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="c2100-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2100-104">Функция `NUMBERVALUE` возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="c2100-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="c2100-105">При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.</span><span class="sxs-lookup"><span data-stu-id="c2100-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2100-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2100-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="c2100-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c2100-107">Arguments</span></span>

<span data-ttu-id="c2100-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c2100-108">`text`: *String*</span></span>

<span data-ttu-id="c2100-109">Текстовое значение, которое должно быть преобразовано в *вещественное* число.</span><span class="sxs-lookup"><span data-stu-id="c2100-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="c2100-110">`decimal separator`: Строка</span><span class="sxs-lookup"><span data-stu-id="c2100-110">`decimal separator`: String</span></span>

<span data-ttu-id="c2100-111">Десятичный разделитель.</span><span class="sxs-lookup"><span data-stu-id="c2100-111">A decimal separator.</span></span> <span data-ttu-id="c2100-112">Он используется для разделения целых и дробных частей десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="c2100-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="c2100-113">`digit grouping separator`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c2100-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="c2100-114">Разделитель групп цифр.</span><span class="sxs-lookup"><span data-stu-id="c2100-114">A digit grouping separator.</span></span> <span data-ttu-id="c2100-115">Он используется в качестве разделителя тысяч.</span><span class="sxs-lookup"><span data-stu-id="c2100-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2100-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c2100-116">Return values</span></span>

<span data-ttu-id="c2100-117">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="c2100-117">*Real*</span></span>

<span data-ttu-id="c2100-118">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="c2100-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="c2100-119">Пример</span><span class="sxs-lookup"><span data-stu-id="c2100-119">Example</span></span>

<span data-ttu-id="c2100-120">`NUMBERVALUE( "1 234,56", ",", " ")` возвращает **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="c2100-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2100-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c2100-121">Additional resources</span></span>

[<span data-ttu-id="c2100-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="c2100-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
