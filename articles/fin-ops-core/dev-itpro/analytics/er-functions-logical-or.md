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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917128"
---
# <span data-ttu-id="2eae0-103"><a name="OR">Функция ER OR</a></span><span class="sxs-lookup"><span data-stu-id="2eae0-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2eae0-104">Функция `OR` возвращает *логическое* значение **FALSE**, если все указанные условия — false.</span><span class="sxs-lookup"><span data-stu-id="2eae0-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="2eae0-105">Если какое-либо указанное условие — true, эта функция возвращает *логическое* значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eae0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eae0-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="2eae0-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2eae0-107">Arguments</span></span>

<span data-ttu-id="2eae0-108">`condition 1`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="2eae0-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="2eae0-109">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="2eae0-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="2eae0-110">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="2eae0-110">This argument is required.</span></span>

<span data-ttu-id="2eae0-111">`condition N`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="2eae0-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="2eae0-112">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="2eae0-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="2eae0-113">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2eae0-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2eae0-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2eae0-114">Return values</span></span>

<span data-ttu-id="2eae0-115">*Логический*</span><span class="sxs-lookup"><span data-stu-id="2eae0-115">*Boolean*</span></span>

<span data-ttu-id="2eae0-116">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="2eae0-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="2eae0-117">Пример</span><span class="sxs-lookup"><span data-stu-id="2eae0-117">Example</span></span>

<span data-ttu-id="2eae0-118">`OR (1=2, "a"="a")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2eae0-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2eae0-119">Additional resources</span></span>

[<span data-ttu-id="2eae0-120">Логические функции</span><span class="sxs-lookup"><span data-stu-id="2eae0-120">Logical functions</span></span>](er-functions-category-logical.md)
