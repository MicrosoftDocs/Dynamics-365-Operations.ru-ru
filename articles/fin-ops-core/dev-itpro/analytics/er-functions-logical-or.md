---
title: Функция ER OR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности OR.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686986"
---
# <a name="or-er-function"></a><span data-ttu-id="5eec2-103">Функция ER OR</span><span class="sxs-lookup"><span data-stu-id="5eec2-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eec2-104">Функция `OR` возвращает *логическое* значение **FALSE**, если все указанные условия — false.</span><span class="sxs-lookup"><span data-stu-id="5eec2-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="5eec2-105">Если какое-либо указанное условие — true, эта функция возвращает *логическое* значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="5eec2-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eec2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5eec2-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="5eec2-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="5eec2-107">Arguments</span></span>

<span data-ttu-id="5eec2-108">`condition 1`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="5eec2-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="5eec2-109">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="5eec2-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="5eec2-110">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="5eec2-110">This argument is required.</span></span>

<span data-ttu-id="5eec2-111">`condition N`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="5eec2-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="5eec2-112">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="5eec2-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="5eec2-113">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="5eec2-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="5eec2-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5eec2-114">Return values</span></span>

<span data-ttu-id="5eec2-115">*Логический*</span><span class="sxs-lookup"><span data-stu-id="5eec2-115">*Boolean*</span></span>

<span data-ttu-id="5eec2-116">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="5eec2-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="5eec2-117">Пример</span><span class="sxs-lookup"><span data-stu-id="5eec2-117">Example</span></span>

<span data-ttu-id="5eec2-118">`OR (1=2, "a"="a")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="5eec2-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eec2-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5eec2-119">Additional resources</span></span>

[<span data-ttu-id="5eec2-120">Логические функции</span><span class="sxs-lookup"><span data-stu-id="5eec2-120">Logical functions</span></span>](er-functions-category-logical.md)
