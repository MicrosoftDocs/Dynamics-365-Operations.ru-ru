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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9b937e7fae3e90d1a87196fab653dfac8e94179
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682397"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="666e1-103">Функция ER DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="666e1-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="666e1-104">Функция `DAYOFYEAR` возвращает *целочисленное* значение числа дней между 1 января и указанной датой.</span><span class="sxs-lookup"><span data-stu-id="666e1-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="666e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="666e1-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="666e1-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="666e1-106">Arguments</span></span>

<span data-ttu-id="666e1-107">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="666e1-107">`date`: *Date*</span></span>

<span data-ttu-id="666e1-108">Значение даты, представляющее дату для использования для расчета количества дней.</span><span class="sxs-lookup"><span data-stu-id="666e1-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="666e1-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="666e1-109">Return values</span></span>

<span data-ttu-id="666e1-110">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="666e1-110">*Integer*</span></span>

<span data-ttu-id="666e1-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="666e1-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="666e1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="666e1-112">Example 1</span></span>

<span data-ttu-id="666e1-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` возвращает **61**.</span><span class="sxs-lookup"><span data-stu-id="666e1-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="666e1-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="666e1-114">Example 2</span></span>

<span data-ttu-id="666e1-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` возвращает **1**.</span><span class="sxs-lookup"><span data-stu-id="666e1-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="666e1-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="666e1-116">Additional resources</span></span>

[<span data-ttu-id="666e1-117">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="666e1-117">Date and time functions</span></span>](er-functions-category-datetime.md)
