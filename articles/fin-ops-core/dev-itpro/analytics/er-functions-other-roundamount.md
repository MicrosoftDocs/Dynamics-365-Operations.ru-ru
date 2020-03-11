---
title: Функция ER ROUNDAMOUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDAMOUNT.
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
ms.openlocfilehash: 5903f562b5f266572f999756539fa7b9ef145023
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041339"
---
# <span data-ttu-id="e780d-103"><a name="ROUNDAMOUNT">Функция ER ROUNDAMOUNT</a></span><span class="sxs-lookup"><span data-stu-id="e780d-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e780d-104">Функция `ROUNDAMOUNT` возвращает *вещественное* значение как результат округления указанного числа до ближайшего числа, кратного другому числу в соответствии с указанным правилом округления.</span><span class="sxs-lookup"><span data-stu-id="e780d-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="e780d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e780d-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="e780d-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e780d-106">Arguments</span></span>

<span data-ttu-id="e780d-107">`number`: *Int* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="e780d-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="e780d-108">Числовое значение, которое должно быть округлено.</span><span class="sxs-lookup"><span data-stu-id="e780d-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="e780d-109">`decimals`: *Int* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="e780d-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="e780d-110">Кратное число, до которого значение параметра `number` должно быть округлено.</span><span class="sxs-lookup"><span data-stu-id="e780d-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="e780d-111">`round rule`: *Значение перечисления*</span><span class="sxs-lookup"><span data-stu-id="e780d-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="e780d-112">Значение перечисления **RoundOffType**, определяющее правило округления.</span><span class="sxs-lookup"><span data-stu-id="e780d-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="e780d-113">Это перечисление обеспечивает следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e780d-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="e780d-114">Обычный (Ordinary)</span><span class="sxs-lookup"><span data-stu-id="e780d-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="e780d-115">Вниз (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="e780d-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="e780d-116">В большую сторону (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="e780d-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="e780d-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e780d-117">Return values</span></span>

<span data-ttu-id="e780d-118">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="e780d-118">*Real*</span></span>

<span data-ttu-id="e780d-119">Полученное числовое значение является кратным значению, указанному параметром `decimals`, и ближе всего к значению, указанному параметром `number`.</span><span class="sxs-lookup"><span data-stu-id="e780d-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e780d-120">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="e780d-120">Usage notes</span></span>

<span data-ttu-id="e780d-121">Когда параметр `number` равен нулю, эта функция всегда возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e780d-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="e780d-122">Когда параметр `decimals` равен нулю, эта функция округляется до значения округления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e780d-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="e780d-123">Когда параметр `round rule` задан как **RoundOffType.Ordinary**, значение округления по умолчанию составляет **0,01**.</span><span class="sxs-lookup"><span data-stu-id="e780d-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="e780d-124">В противном случае значение округления по умолчанию составляет **1,0**.</span><span class="sxs-lookup"><span data-stu-id="e780d-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="e780d-125">Когда параметр `round rule` задан как **RoundOffType.Ordinary**, эта функция округляет до ближайшей суммы округления.</span><span class="sxs-lookup"><span data-stu-id="e780d-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="e780d-126">Когда параметр `round rule` задан как **RoundOffType.RoundDown**, эта функция округляет до нуля для ближайшей суммы округления.</span><span class="sxs-lookup"><span data-stu-id="e780d-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="e780d-127">Когда параметр `round rule` задан как **RoundOffType.RoundUp**, эта функция округляет от нуля для ближайшей суммы округления.</span><span class="sxs-lookup"><span data-stu-id="e780d-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="e780d-128">Когда параметр `round rule` задан как **RoundOffType.Ordinary**, эта функция работает как функция Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) и функция X++ [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).</span><span class="sxs-lookup"><span data-stu-id="e780d-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="e780d-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="e780d-129">Remarks</span></span>

<span data-ttu-id="e780d-130">Для округления числового значения до определенного количества десятичных знаков используйте функцию [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="e780d-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="e780d-131">Пример</span><span class="sxs-lookup"><span data-stu-id="e780d-131">Example</span></span>

<span data-ttu-id="e780d-132">Если параметр **model.RoundOff** задан как **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` возвращает 7.35.</span><span class="sxs-lookup"><span data-stu-id="e780d-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="e780d-133">Если параметр **model.RoundOff** задан как **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` возвращает 7.35.</span><span class="sxs-lookup"><span data-stu-id="e780d-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="e780d-134">Если параметр **model.RoundOff** задан как **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` возвращает 8.4.</span><span class="sxs-lookup"><span data-stu-id="e780d-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e780d-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e780d-135">Additional resources</span></span>

[<span data-ttu-id="e780d-136">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="e780d-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="e780d-137">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e780d-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
