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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e51e181de53cd185679110e99b9f89695bacdf92
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744271"
---
# <a name="len-er-function"></a><span data-ttu-id="e25f6-103">Функция ER LEN</span><span class="sxs-lookup"><span data-stu-id="e25f6-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e25f6-104">Функция `LEN` возвращает целочисленное значение, которое представляет число символов в указанной строке как *целочисленное* значение.</span><span class="sxs-lookup"><span data-stu-id="e25f6-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e25f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e25f6-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="e25f6-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e25f6-106">Arguments</span></span>

<span data-ttu-id="e25f6-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="e25f6-107">`text`: *String*</span></span>

<span data-ttu-id="e25f6-108">*Строковое* значение, задающее текст.</span><span class="sxs-lookup"><span data-stu-id="e25f6-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e25f6-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e25f6-109">Return values</span></span>

<span data-ttu-id="e25f6-110">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="e25f6-110">*Integer*</span></span>

<span data-ttu-id="e25f6-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="e25f6-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="e25f6-112">Пример</span><span class="sxs-lookup"><span data-stu-id="e25f6-112">Example</span></span>

<span data-ttu-id="e25f6-113">`LEN ("Sample")` возвращает **6**.</span><span class="sxs-lookup"><span data-stu-id="e25f6-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e25f6-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e25f6-114">Additional resources</span></span>

[<span data-ttu-id="e25f6-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="e25f6-115">Text functions</span></span>](er-functions-category-text.md)
