---
title: Функция ER ROUNDUP
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDUP.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ed86e2a848248dd8f2fc99401d12e0a162bf20a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686842"
---
# <a name="roundup-er-function"></a><span data-ttu-id="f5298-103">Функция ER ROUNDUP</span><span class="sxs-lookup"><span data-stu-id="f5298-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5298-104">Функция `ROUNDUP` возвращает указанное число в виде *вещественного* значения после его округления вверх до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="f5298-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5298-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5298-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="f5298-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="f5298-106">Arguments</span></span>

<span data-ttu-id="f5298-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="f5298-107">`number`: *Real*</span></span>

<span data-ttu-id="f5298-108">Числовое значение, которое должно быть округлено вверх.</span><span class="sxs-lookup"><span data-stu-id="f5298-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="f5298-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="f5298-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="f5298-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="f5298-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5298-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f5298-111">Return values</span></span>

<span data-ttu-id="f5298-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="f5298-112">*Real*</span></span>

<span data-ttu-id="f5298-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="f5298-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f5298-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="f5298-114">Usage notes</span></span>

<span data-ttu-id="f5298-115">Эта функция поступает как [ROUND](er-functions-mathematical-round.md), но она всегда округляет указанное число вверх (в направлении от нуля).</span><span class="sxs-lookup"><span data-stu-id="f5298-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="f5298-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5298-116">Example 1</span></span>

<span data-ttu-id="f5298-117">`ROUNDUP (1200.763, 2)` округляет верх до двух десятичных знаков и возвращает **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="f5298-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f5298-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f5298-118">Example 2</span></span>

<span data-ttu-id="f5298-119">`ROUNDUP (1200.767, -3)` округляет вверх до ближайшего числа, кратного тысяче, и возвращает **2000**.</span><span class="sxs-lookup"><span data-stu-id="f5298-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5298-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f5298-120">Additional resources</span></span>

[<span data-ttu-id="f5298-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f5298-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
