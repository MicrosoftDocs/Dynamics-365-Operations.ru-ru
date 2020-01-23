---
title: Функция ER ROUNDDOWN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDDOWN.
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
ms.openlocfilehash: ef7d81852a0bbb84fd8f37cd89555766cc47f5f8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915863"
---
# <span data-ttu-id="e9500-103"><a name="ROUNDDOWN">Функция ER ROUNDDOWN</a></span><span class="sxs-lookup"><span data-stu-id="e9500-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9500-104">Функция `ROUNDDOWN` возвращает указанное число в виде *вещественного* значения после его округления вниз до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="e9500-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9500-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9500-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="e9500-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e9500-106">Arguments</span></span>

<span data-ttu-id="e9500-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="e9500-107">`number`: *Real*</span></span>

<span data-ttu-id="e9500-108">Числовое значение, которое должно быть округлено вниз.</span><span class="sxs-lookup"><span data-stu-id="e9500-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="e9500-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="e9500-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="e9500-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="e9500-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9500-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e9500-111">Return values</span></span>

<span data-ttu-id="e9500-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="e9500-112">*Real*</span></span>

<span data-ttu-id="e9500-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="e9500-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e9500-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="e9500-114">Usage notes</span></span>

<span data-ttu-id="e9500-115">Эта функция поступает как [ROUND](er-functions-mathematical-round.md), но она всегда округляет указанное число вниз (в направлении нуля).</span><span class="sxs-lookup"><span data-stu-id="e9500-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="e9500-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9500-116">Example 1</span></span>

<span data-ttu-id="e9500-117">`ROUNDDOWN (1200.767, 2)` округляет вниз до двух десятичных знаков и возвращает **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="e9500-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="e9500-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e9500-118">Example 2</span></span>

<span data-ttu-id="e9500-119">`ROUNDDOWN (1700.767, -3)` округляет вниз до ближайшего числа, кратного тысяче, и возвращает **1000**.</span><span class="sxs-lookup"><span data-stu-id="e9500-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9500-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e9500-120">Additional resources</span></span>

[<span data-ttu-id="e9500-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e9500-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
