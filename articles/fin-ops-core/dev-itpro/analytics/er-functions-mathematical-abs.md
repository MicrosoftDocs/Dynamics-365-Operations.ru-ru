---
title: Функция ER ABS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ABS.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753152"
---
# <a name="abs-er-function"></a><span data-ttu-id="35a1d-103">Функция ER ABS</span><span class="sxs-lookup"><span data-stu-id="35a1d-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35a1d-104">Функция `ABS` возвращает абсолютное значение (модуль) указанного числа в качестве *вещественного* значения.</span><span class="sxs-lookup"><span data-stu-id="35a1d-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="35a1d-105">Другими словами, возвращает число без знака.</span><span class="sxs-lookup"><span data-stu-id="35a1d-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a1d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35a1d-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="35a1d-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="35a1d-107">Arguments</span></span>

<span data-ttu-id="35a1d-108">`number`: *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="35a1d-108">`number`: *Real*</span></span>

<span data-ttu-id="35a1d-109">Числовое значение, модуль которого вам нужен.</span><span class="sxs-lookup"><span data-stu-id="35a1d-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="35a1d-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="35a1d-110">Return values</span></span>

<span data-ttu-id="35a1d-111">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="35a1d-111">*Real*</span></span>

<span data-ttu-id="35a1d-112">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="35a1d-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="35a1d-113">Пример</span><span class="sxs-lookup"><span data-stu-id="35a1d-113">Example</span></span>

<span data-ttu-id="35a1d-114">`ABS (-1)` возвращает **1**.</span><span class="sxs-lookup"><span data-stu-id="35a1d-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35a1d-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="35a1d-115">Additional resources</span></span>

[<span data-ttu-id="35a1d-116">Математические функции</span><span class="sxs-lookup"><span data-stu-id="35a1d-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]