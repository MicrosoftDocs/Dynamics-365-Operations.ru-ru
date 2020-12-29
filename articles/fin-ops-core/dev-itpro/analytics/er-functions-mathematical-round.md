---
title: Функция ER ROUND
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUND.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683264"
---
# <a name="round-er-function"></a><span data-ttu-id="d3679-103">Функция ER ROUND</span><span class="sxs-lookup"><span data-stu-id="d3679-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3679-104">Функция `ROUND` возвращает указанное число в виде *вещественного* значения после его округления до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="d3679-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3679-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3679-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="d3679-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="d3679-106">Arguments</span></span>

<span data-ttu-id="d3679-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="d3679-107">`number`: *Real*</span></span>

<span data-ttu-id="d3679-108">Числовое значение, которое должно быть округлено.</span><span class="sxs-lookup"><span data-stu-id="d3679-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="d3679-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="d3679-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="d3679-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="d3679-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3679-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d3679-111">Return values</span></span>

<span data-ttu-id="d3679-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="d3679-112">*Real*</span></span>

<span data-ttu-id="d3679-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="d3679-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d3679-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="d3679-114">Usage notes</span></span>

<span data-ttu-id="d3679-115">Если значение аргумента `decimals` больше 0 (нуля), указанное число округляется до этого числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="d3679-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="d3679-116">Если значение аргумента `decimals` равно **0** (ноль), указанное число округляется до ближайшего четного целого.</span><span class="sxs-lookup"><span data-stu-id="d3679-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="d3679-117">Если значение аргумента `decimals` меньше 0 (нуля), указанное число округляется слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="d3679-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="d3679-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3679-118">Example 1</span></span>

<span data-ttu-id="d3679-119">`ROUND (1200.767, 2)` округляет до двух десятичных знаков и возвращает **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="d3679-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d3679-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d3679-120">Example 2</span></span>

<span data-ttu-id="d3679-121">`ROUND (1200.767, -3)` округляет до ближайшего числа, кратного тысяче, и возвращает **1000**.</span><span class="sxs-lookup"><span data-stu-id="d3679-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="d3679-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d3679-122">Example 3</span></span>

<span data-ttu-id="d3679-123">`ROUND (1200.5, 0)` округляет до ближайшего четного целого числа и возвращает **1200**, а `ROUND (1201.5, 0)` делает то же самое и возвращает **1202**.</span><span class="sxs-lookup"><span data-stu-id="d3679-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3679-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d3679-124">Additional resources</span></span>

[<span data-ttu-id="d3679-125">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d3679-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)
