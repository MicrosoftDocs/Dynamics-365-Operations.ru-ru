---
title: Функция ER LEN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LEN
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 8d766b8effa9d6936de7a3def252536603330965
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680369"
---
# <a name="len-er-function"></a><span data-ttu-id="fe4ae-103">Функция ER LEN</span><span class="sxs-lookup"><span data-stu-id="fe4ae-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe4ae-104">Функция `LEN` возвращает целочисленное значение, которое представляет число символов в указанной строке как *целочисленное* значение.</span><span class="sxs-lookup"><span data-stu-id="fe4ae-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe4ae-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="fe4ae-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="fe4ae-106">Arguments</span></span>

<span data-ttu-id="fe4ae-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="fe4ae-107">`text`: *String*</span></span>

<span data-ttu-id="fe4ae-108">*Строковое* значение, задающее текст.</span><span class="sxs-lookup"><span data-stu-id="fe4ae-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe4ae-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fe4ae-109">Return values</span></span>

<span data-ttu-id="fe4ae-110">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="fe4ae-110">*Integer*</span></span>

<span data-ttu-id="fe4ae-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="fe4ae-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="fe4ae-112">Пример</span><span class="sxs-lookup"><span data-stu-id="fe4ae-112">Example</span></span>

<span data-ttu-id="fe4ae-113">`LEN ("Sample")` возвращает **6**.</span><span class="sxs-lookup"><span data-stu-id="fe4ae-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe4ae-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe4ae-114">Additional resources</span></span>

[<span data-ttu-id="fe4ae-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="fe4ae-115">Text functions</span></span>](er-functions-category-text.md)
