---
title: Функция ER POWER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности POWER.
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744583"
---
# <a name="power-er-function"></a><span data-ttu-id="43383-103">Функция ER POWER</span><span class="sxs-lookup"><span data-stu-id="43383-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43383-104">Функция `POWER` возвращает *вещественное* значение, которое представляет собой результат увеличения указанного положительного числа до указанной степени.</span><span class="sxs-lookup"><span data-stu-id="43383-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="43383-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43383-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="43383-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="43383-106">Arguments</span></span>

<span data-ttu-id="43383-107">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="43383-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="43383-108">Числовое значение, которое должно быть возведено в указанную степень.</span><span class="sxs-lookup"><span data-stu-id="43383-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="43383-109">`power`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="43383-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="43383-110">Числовое значение, представляющее определенную степень.</span><span class="sxs-lookup"><span data-stu-id="43383-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="43383-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="43383-111">Return values</span></span>

<span data-ttu-id="43383-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="43383-112">*Real*</span></span>

<span data-ttu-id="43383-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="43383-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="43383-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43383-114">Example 1</span></span>

<span data-ttu-id="43383-115">`POWER (10, 2)` возвращает **100**.</span><span class="sxs-lookup"><span data-stu-id="43383-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="43383-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43383-116">Example 2</span></span>

<span data-ttu-id="43383-117">`POWER (4, 0.5)` возвращает **2**.</span><span class="sxs-lookup"><span data-stu-id="43383-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43383-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="43383-118">Additional resources</span></span>

[<span data-ttu-id="43383-119">Математические функции</span><span class="sxs-lookup"><span data-stu-id="43383-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
