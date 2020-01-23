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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915909"
---
# <span data-ttu-id="be332-103"><a name="POWER">Функция ER POWER</a></span><span class="sxs-lookup"><span data-stu-id="be332-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be332-104">Функция `POWER` возвращает *вещественное* значение, которое представляет собой результат увеличения указанного положительного числа до указанной степени.</span><span class="sxs-lookup"><span data-stu-id="be332-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="be332-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be332-105">Syntax</span></span>

```
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="be332-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="be332-106">Arguments</span></span>

<span data-ttu-id="be332-107">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="be332-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="be332-108">Числовое значение, которое должно быть возведено в указанную степень.</span><span class="sxs-lookup"><span data-stu-id="be332-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="be332-109">`power`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="be332-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="be332-110">Числовое значение, представляющее определенную степень.</span><span class="sxs-lookup"><span data-stu-id="be332-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="be332-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="be332-111">Return values</span></span>

<span data-ttu-id="be332-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="be332-112">*Real*</span></span>

<span data-ttu-id="be332-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="be332-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="be332-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be332-114">Example 1</span></span>

<span data-ttu-id="be332-115">`POWER (10, 2)` возвращает **100**.</span><span class="sxs-lookup"><span data-stu-id="be332-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="be332-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="be332-116">Example 2</span></span>

<span data-ttu-id="be332-117">`POWER (4, 0.5)` возвращает **2**.</span><span class="sxs-lookup"><span data-stu-id="be332-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be332-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be332-118">Additional resources</span></span>

[<span data-ttu-id="be332-119">Математические функции</span><span class="sxs-lookup"><span data-stu-id="be332-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
