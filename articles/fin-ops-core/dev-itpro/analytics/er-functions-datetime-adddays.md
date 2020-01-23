---
title: Функция ER ADDDAYS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916461"
---
# <span data-ttu-id="e071d-103"><a name="ADDDAYS">Функция ER ADDDAYS</a></span><span class="sxs-lookup"><span data-stu-id="e071d-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e071d-104">Функция `ADDDAYS` вычисляет значение *DateTime*, которое является указанным числом дней до или после указанной даты начала.</span><span class="sxs-lookup"><span data-stu-id="e071d-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e071d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e071d-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="e071d-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e071d-106">Arguments</span></span>

<span data-ttu-id="e071d-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="e071d-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="e071d-108">Значение даты/времени, представляющее дату начала.</span><span class="sxs-lookup"><span data-stu-id="e071d-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="e071d-109">`days`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="e071d-109">`days`: *Integer*</span></span>

<span data-ttu-id="e071d-110">Количество дней до или после `datetime`.</span><span class="sxs-lookup"><span data-stu-id="e071d-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="e071d-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e071d-111">Return values</span></span>

<span data-ttu-id="e071d-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="e071d-112">*DateTime*</span></span>

<span data-ttu-id="e071d-113">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="e071d-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e071d-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="e071d-114">Usage notes</span></span>

<span data-ttu-id="e071d-115">Положительное значение для `days` дает будущую дату.</span><span class="sxs-lookup"><span data-stu-id="e071d-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="e071d-116">Отрицательное значение дает прошлую дату.</span><span class="sxs-lookup"><span data-stu-id="e071d-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="e071d-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e071d-117">Example 1</span></span>

<span data-ttu-id="e071d-118">`ADDDAYS (NOW(), 7)` возвращает дату и время на семь дней в будущем.</span><span class="sxs-lookup"><span data-stu-id="e071d-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="e071d-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e071d-119">Example 2</span></span>

<span data-ttu-id="e071d-120">`ADDDAYS (NOW(), -3)` возвращает дату и время на три дня в прошлом.</span><span class="sxs-lookup"><span data-stu-id="e071d-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e071d-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e071d-121">Additional resources</span></span>

[<span data-ttu-id="e071d-122">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="e071d-122">Date and time functions</span></span>](er-functions-category-datetime.md)
