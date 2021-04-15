---
title: Функция ER NUMBERVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMBERVALUE.
author: NickSelin
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755356"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="434c9-103">Функция ER NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="434c9-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="434c9-104">Функция `NUMBERVALUE` возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="434c9-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="434c9-105">При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.</span><span class="sxs-lookup"><span data-stu-id="434c9-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="434c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="434c9-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="434c9-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="434c9-107">Arguments</span></span>

<span data-ttu-id="434c9-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="434c9-108">`text`: *String*</span></span>

<span data-ttu-id="434c9-109">Текстовое значение, которое должно быть преобразовано в *вещественное* число.</span><span class="sxs-lookup"><span data-stu-id="434c9-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="434c9-110">`decimal separator`: Строка</span><span class="sxs-lookup"><span data-stu-id="434c9-110">`decimal separator`: String</span></span>

<span data-ttu-id="434c9-111">Десятичный разделитель.</span><span class="sxs-lookup"><span data-stu-id="434c9-111">A decimal separator.</span></span> <span data-ttu-id="434c9-112">Он используется для разделения целых и дробных частей десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="434c9-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="434c9-113">`digit grouping separator`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="434c9-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="434c9-114">Разделитель групп цифр.</span><span class="sxs-lookup"><span data-stu-id="434c9-114">A digit grouping separator.</span></span> <span data-ttu-id="434c9-115">Он используется в качестве разделителя тысяч.</span><span class="sxs-lookup"><span data-stu-id="434c9-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="434c9-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="434c9-116">Return values</span></span>

<span data-ttu-id="434c9-117">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="434c9-117">*Real*</span></span>

<span data-ttu-id="434c9-118">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="434c9-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="434c9-119">Пример</span><span class="sxs-lookup"><span data-stu-id="434c9-119">Example</span></span>

<span data-ttu-id="434c9-120">`NUMBERVALUE( "1 234,56", ",", " ")` возвращает **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="434c9-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="434c9-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="434c9-121">Additional resources</span></span>

[<span data-ttu-id="434c9-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="434c9-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]