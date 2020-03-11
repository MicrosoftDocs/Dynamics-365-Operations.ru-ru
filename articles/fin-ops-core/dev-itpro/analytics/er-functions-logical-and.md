---
title: Функция ER AND
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности AND
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041831"
---
# <span data-ttu-id="bad0d-103"><a name="AND">Функция ER AND</a></span><span class="sxs-lookup"><span data-stu-id="bad0d-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bad0d-104">Функция `AND` возвращает *логическое* значение **TRUE**, если все указанные условия — true.</span><span class="sxs-lookup"><span data-stu-id="bad0d-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="bad0d-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bad0d-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad0d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bad0d-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="bad0d-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="bad0d-107">Arguments</span></span>

<span data-ttu-id="bad0d-108">`condition 1`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="bad0d-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="bad0d-109">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="bad0d-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="bad0d-110">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="bad0d-110">This argument is required.</span></span>

<span data-ttu-id="bad0d-111">`condition N`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="bad0d-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="bad0d-112">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="bad0d-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="bad0d-113">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="bad0d-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="bad0d-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bad0d-114">Return values</span></span>

<span data-ttu-id="bad0d-115">*Логический*</span><span class="sxs-lookup"><span data-stu-id="bad0d-115">*Boolean*</span></span>

<span data-ttu-id="bad0d-116">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="bad0d-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bad0d-117">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="bad0d-117">Usage notes</span></span>

<span data-ttu-id="bad0d-118">В аргументах логических функций можно использовать ссылки на источники данных, числовые и текстовые значения, логические значения, операторы сравнения и другие функции электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="bad0d-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="bad0d-119">Тем не менее, все аргументы должны быть оценены как *логическое* значение **TRUE** или **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bad0d-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="bad0d-120">Пример</span><span class="sxs-lookup"><span data-stu-id="bad0d-120">Example</span></span>

<span data-ttu-id="bad0d-121">`AND (1=1, "a"="a")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="bad0d-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="bad0d-122">`AND (1=2, "a"="a")` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bad0d-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bad0d-123">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bad0d-123">Additional resources</span></span>

[<span data-ttu-id="bad0d-124">Логические функции</span><span class="sxs-lookup"><span data-stu-id="bad0d-124">Logical functions</span></span>](er-functions-category-logical.md)
