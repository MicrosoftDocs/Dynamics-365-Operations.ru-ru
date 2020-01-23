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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916530"
---
# <span data-ttu-id="2922b-103"><a name="NUMBERVALUE">Функция ER NUMBERVALUE</a></span><span class="sxs-lookup"><span data-stu-id="2922b-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2922b-104">Функция `NUMBERVALUE` возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="2922b-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="2922b-105">При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.</span><span class="sxs-lookup"><span data-stu-id="2922b-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="2922b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2922b-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="2922b-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2922b-107">Arguments</span></span>

<span data-ttu-id="2922b-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2922b-108">`text`: *String*</span></span>

<span data-ttu-id="2922b-109">Текстовое значение, которое должно быть преобразовано в *вещественное* число.</span><span class="sxs-lookup"><span data-stu-id="2922b-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="2922b-110">`decimal separator`: Строка</span><span class="sxs-lookup"><span data-stu-id="2922b-110">`decimal separator`: String</span></span>

<span data-ttu-id="2922b-111">Десятичный разделитель.</span><span class="sxs-lookup"><span data-stu-id="2922b-111">A decimal separator.</span></span> <span data-ttu-id="2922b-112">Он используется для разделения целых и дробных частей десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="2922b-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="2922b-113">`digit grouping separator`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2922b-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="2922b-114">Разделитель групп цифр.</span><span class="sxs-lookup"><span data-stu-id="2922b-114">A digit grouping separator.</span></span> <span data-ttu-id="2922b-115">Он используется в качестве разделителя тысяч.</span><span class="sxs-lookup"><span data-stu-id="2922b-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="2922b-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2922b-116">Return values</span></span>

<span data-ttu-id="2922b-117">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="2922b-117">*Real*</span></span>

<span data-ttu-id="2922b-118">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="2922b-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="2922b-119">Пример</span><span class="sxs-lookup"><span data-stu-id="2922b-119">Example</span></span>

<span data-ttu-id="2922b-120">`NUMBERVALUE( "1 234,56", ",", " ")` возвращает **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="2922b-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2922b-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2922b-121">Additional resources</span></span>

[<span data-ttu-id="2922b-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="2922b-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
