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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688451"
---
# <a name="adddays-er-function"></a><span data-ttu-id="75673-103">Функция ER ADDDAYS</span><span class="sxs-lookup"><span data-stu-id="75673-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75673-104">Функция `ADDDAYS` вычисляет значение *DateTime*, которое является указанным числом дней до или после указанной даты начала.</span><span class="sxs-lookup"><span data-stu-id="75673-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="75673-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75673-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="75673-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="75673-106">Arguments</span></span>

<span data-ttu-id="75673-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="75673-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="75673-108">Значение даты/времени, представляющее дату начала.</span><span class="sxs-lookup"><span data-stu-id="75673-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="75673-109">`days`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="75673-109">`days`: *Integer*</span></span>

<span data-ttu-id="75673-110">Количество дней до или после `datetime`.</span><span class="sxs-lookup"><span data-stu-id="75673-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="75673-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="75673-111">Return values</span></span>

<span data-ttu-id="75673-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="75673-112">*DateTime*</span></span>

<span data-ttu-id="75673-113">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="75673-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="75673-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="75673-114">Usage notes</span></span>

<span data-ttu-id="75673-115">Положительное значение для `days` дает будущую дату.</span><span class="sxs-lookup"><span data-stu-id="75673-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="75673-116">Отрицательное значение дает прошлую дату.</span><span class="sxs-lookup"><span data-stu-id="75673-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="75673-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75673-117">Example 1</span></span>

<span data-ttu-id="75673-118">`ADDDAYS (NOW(), 7)` возвращает дату и время на семь дней в будущем.</span><span class="sxs-lookup"><span data-stu-id="75673-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="75673-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75673-119">Example 2</span></span>

<span data-ttu-id="75673-120">`ADDDAYS (NOW(), -3)` возвращает дату и время на три дня в прошлом.</span><span class="sxs-lookup"><span data-stu-id="75673-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75673-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75673-121">Additional resources</span></span>

[<span data-ttu-id="75673-122">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="75673-122">Date and time functions</span></span>](er-functions-category-datetime.md)
