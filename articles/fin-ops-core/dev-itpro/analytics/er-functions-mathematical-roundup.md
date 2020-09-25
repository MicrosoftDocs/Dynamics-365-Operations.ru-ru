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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83262a11f92a924e5e49461cf414fb07ab278541
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744511"
---
# <a name="roundup-er-function"></a><span data-ttu-id="643d5-103">Функция ER ROUNDUP</span><span class="sxs-lookup"><span data-stu-id="643d5-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="643d5-104">Функция `ROUNDUP` возвращает указанное число в виде *вещественного* значения после его округления вверх до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="643d5-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="643d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="643d5-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="643d5-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="643d5-106">Arguments</span></span>

<span data-ttu-id="643d5-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="643d5-107">`number`: *Real*</span></span>

<span data-ttu-id="643d5-108">Числовое значение, которое должно быть округлено вверх.</span><span class="sxs-lookup"><span data-stu-id="643d5-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="643d5-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="643d5-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="643d5-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="643d5-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="643d5-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="643d5-111">Return values</span></span>

<span data-ttu-id="643d5-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="643d5-112">*Real*</span></span>

<span data-ttu-id="643d5-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="643d5-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="643d5-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="643d5-114">Usage notes</span></span>

<span data-ttu-id="643d5-115">Эта функция поступает как [ROUND](er-functions-mathematical-round.md), но она всегда округляет указанное число вверх (в направлении от нуля).</span><span class="sxs-lookup"><span data-stu-id="643d5-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="643d5-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="643d5-116">Example 1</span></span>

<span data-ttu-id="643d5-117">`ROUNDUP (1200.763, 2)` округляет верх до двух десятичных знаков и возвращает **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="643d5-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="643d5-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="643d5-118">Example 2</span></span>

<span data-ttu-id="643d5-119">`ROUNDUP (1200.767, -3)` округляет вверх до ближайшего числа, кратного тысяче, и возвращает **2000**.</span><span class="sxs-lookup"><span data-stu-id="643d5-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="643d5-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="643d5-120">Additional resources</span></span>

[<span data-ttu-id="643d5-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="643d5-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
