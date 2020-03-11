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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041615"
---
# <span data-ttu-id="43776-103"><a name="ROUND">Функция ER ROUND</a></span><span class="sxs-lookup"><span data-stu-id="43776-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43776-104">Функция `ROUND` возвращает указанное число в виде *вещественного* значения после его округления до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="43776-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="43776-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43776-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="43776-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="43776-106">Arguments</span></span>

<span data-ttu-id="43776-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="43776-107">`number`: *Real*</span></span>

<span data-ttu-id="43776-108">Числовое значение, которое должно быть округлено.</span><span class="sxs-lookup"><span data-stu-id="43776-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="43776-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="43776-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="43776-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="43776-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="43776-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="43776-111">Return values</span></span>

<span data-ttu-id="43776-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="43776-112">*Real*</span></span>

<span data-ttu-id="43776-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="43776-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="43776-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="43776-114">Usage notes</span></span>

<span data-ttu-id="43776-115">Если значение аргумента `decimals` больше 0 (нуля), указанное число округляется до этого числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="43776-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="43776-116">Если значение аргумента `decimals` равно **0** (ноль), указанное число округляется до ближайшего целого.</span><span class="sxs-lookup"><span data-stu-id="43776-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="43776-117">Если значение аргумента `decimals` меньше 0 (нуля), указанное число округляется слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="43776-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="43776-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43776-118">Example 1</span></span>

<span data-ttu-id="43776-119">`ROUND (1200.767, 2)` округляет до двух десятичных знаков и возвращает **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="43776-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="43776-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43776-120">Example 2</span></span>

<span data-ttu-id="43776-121">`ROUND (1200.767, -3)` округляет до ближайшего числа, кратного тысяче, и возвращает **1000**.</span><span class="sxs-lookup"><span data-stu-id="43776-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43776-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="43776-122">Additional resources</span></span>

[<span data-ttu-id="43776-123">Математические функции</span><span class="sxs-lookup"><span data-stu-id="43776-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
