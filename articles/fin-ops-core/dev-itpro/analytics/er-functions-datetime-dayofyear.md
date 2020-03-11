---
title: Функция ER DAYOFYEAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYOFYEAR.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070675"
---
# <span data-ttu-id="20161-103"><a name="DAYOFYEAR">Функция ER DAYOFYEAR</a></span><span class="sxs-lookup"><span data-stu-id="20161-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20161-104">Функция `DAYOFYEAR` возвращает *целочисленное* значение числа дней между 1 января и указанной датой.</span><span class="sxs-lookup"><span data-stu-id="20161-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="20161-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20161-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="20161-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="20161-106">Arguments</span></span>

<span data-ttu-id="20161-107">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="20161-107">`date`: *Date*</span></span>

<span data-ttu-id="20161-108">Значение даты, представляющее дату для использования для расчета количества дней.</span><span class="sxs-lookup"><span data-stu-id="20161-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="20161-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="20161-109">Return values</span></span>

<span data-ttu-id="20161-110">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="20161-110">*Integer*</span></span>

<span data-ttu-id="20161-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="20161-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="20161-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20161-112">Example 1</span></span>

<span data-ttu-id="20161-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` возвращает **61**.</span><span class="sxs-lookup"><span data-stu-id="20161-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="20161-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="20161-114">Example 2</span></span>

<span data-ttu-id="20161-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` возвращает **1**.</span><span class="sxs-lookup"><span data-stu-id="20161-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20161-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20161-116">Additional resources</span></span>

[<span data-ttu-id="20161-117">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="20161-117">Date and time functions</span></span>](er-functions-category-datetime.md)
