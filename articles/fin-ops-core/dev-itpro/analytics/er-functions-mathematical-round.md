---
title: Функция ER ROUND
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUND.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917082"
---
# <span data-ttu-id="c6cbd-103"><a name="ROUND">Функция ER ROUND</a></span><span class="sxs-lookup"><span data-stu-id="c6cbd-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6cbd-104">Функция `ROUND` возвращает указанное число в виде *вещественного* значения после его округления до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6cbd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6cbd-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="c6cbd-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c6cbd-106">Arguments</span></span>

<span data-ttu-id="c6cbd-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="c6cbd-107">`number`: *Real*</span></span>

<span data-ttu-id="c6cbd-108">Числовое значение, которое должно быть округлено.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="c6cbd-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="c6cbd-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="c6cbd-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6cbd-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c6cbd-111">Return values</span></span>

<span data-ttu-id="c6cbd-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="c6cbd-112">*Real*</span></span>

<span data-ttu-id="c6cbd-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c6cbd-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="c6cbd-114">Usage notes</span></span>

<span data-ttu-id="c6cbd-115">Если значение аргумента `decimals` больше 0 (нуля), указанное число округляется до этого числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="c6cbd-116">Если значение аргумента `decimals` равно **0** (ноль), указанное число округляется до ближайшего целого.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="c6cbd-117">Если значение аргумента `decimals` меньше 0 (нуля), указанное число округляется слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="c6cbd-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6cbd-118">Example 1</span></span>

<span data-ttu-id="c6cbd-119">`ROUND (1200.767, 2)` округляет до двух десятичных знаков и возвращает **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c6cbd-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c6cbd-120">Example 2</span></span>

<span data-ttu-id="c6cbd-121">`ROUND (1200.767, -3)` округляет до ближайшего числа, кратного тысяче, и возвращает **1000**.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6cbd-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c6cbd-122">Additional resources</span></span>

[<span data-ttu-id="c6cbd-123">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c6cbd-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
