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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744631"
---
# <a name="or-er-function"></a><span data-ttu-id="69ebc-103">Функция ER OR</span><span class="sxs-lookup"><span data-stu-id="69ebc-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69ebc-104">Функция `OR` возвращает *логическое* значение **FALSE**, если все указанные условия — false.</span><span class="sxs-lookup"><span data-stu-id="69ebc-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="69ebc-105">Если какое-либо указанное условие — true, эта функция возвращает *логическое* значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="69ebc-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ebc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69ebc-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="69ebc-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="69ebc-107">Arguments</span></span>

<span data-ttu-id="69ebc-108">`condition 1`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="69ebc-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="69ebc-109">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="69ebc-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="69ebc-110">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="69ebc-110">This argument is required.</span></span>

<span data-ttu-id="69ebc-111">`condition N`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="69ebc-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="69ebc-112">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="69ebc-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="69ebc-113">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="69ebc-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="69ebc-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="69ebc-114">Return values</span></span>

<span data-ttu-id="69ebc-115">*Логический*</span><span class="sxs-lookup"><span data-stu-id="69ebc-115">*Boolean*</span></span>

<span data-ttu-id="69ebc-116">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="69ebc-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="69ebc-117">Пример</span><span class="sxs-lookup"><span data-stu-id="69ebc-117">Example</span></span>

<span data-ttu-id="69ebc-118">`OR (1=2, "a"="a")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="69ebc-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69ebc-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69ebc-119">Additional resources</span></span>

[<span data-ttu-id="69ebc-120">Логические функции</span><span class="sxs-lookup"><span data-stu-id="69ebc-120">Logical functions</span></span>](er-functions-category-logical.md)
