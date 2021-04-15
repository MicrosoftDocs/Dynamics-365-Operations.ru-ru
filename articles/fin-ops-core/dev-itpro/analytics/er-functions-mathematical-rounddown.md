---
title: Функция ER ROUNDDOWN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDDOWN.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744471"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="abf04-103">Функция ER ROUNDDOWN</span><span class="sxs-lookup"><span data-stu-id="abf04-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abf04-104">Функция `ROUNDDOWN` возвращает указанное число в виде *вещественного* значения после его округления вниз до указанного числа десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="abf04-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf04-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abf04-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="abf04-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="abf04-106">Arguments</span></span>

<span data-ttu-id="abf04-107">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="abf04-107">`number`: *Real*</span></span>

<span data-ttu-id="abf04-108">Числовое значение, которое должно быть округлено вниз.</span><span class="sxs-lookup"><span data-stu-id="abf04-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="abf04-109">`decimals`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="abf04-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="abf04-110">Числовое значение, представляющее количество десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="abf04-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="abf04-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="abf04-111">Return values</span></span>

<span data-ttu-id="abf04-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="abf04-112">*Real*</span></span>

<span data-ttu-id="abf04-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="abf04-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="abf04-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="abf04-114">Usage notes</span></span>

<span data-ttu-id="abf04-115">Эта функция поступает как [ROUND](er-functions-mathematical-round.md), но она всегда округляет указанное число вниз (в направлении нуля).</span><span class="sxs-lookup"><span data-stu-id="abf04-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="abf04-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="abf04-116">Example 1</span></span>

<span data-ttu-id="abf04-117">`ROUNDDOWN (1200.767, 2)` округляет вниз до двух десятичных знаков и возвращает **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="abf04-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="abf04-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="abf04-118">Example 2</span></span>

<span data-ttu-id="abf04-119">`ROUNDDOWN (1700.767, -3)` округляет вниз до ближайшего числа, кратного тысяче, и возвращает **1000**.</span><span class="sxs-lookup"><span data-stu-id="abf04-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abf04-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="abf04-120">Additional resources</span></span>

[<span data-ttu-id="abf04-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="abf04-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]