---
title: Функция ER INTVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INTVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743647"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="827a3-103">Функция ER INTVALUE</span><span class="sxs-lookup"><span data-stu-id="827a3-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="827a3-104">Функция `INTVALUE` возвращает значение *Int*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="827a3-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="827a3-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="827a3-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="827a3-106">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="827a3-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="827a3-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="827a3-107">Arguments</span></span>

<span data-ttu-id="827a3-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="827a3-108">`text`: *String*</span></span>

<span data-ttu-id="827a3-109">Текстовое значение, которое должно быть преобразовано в число *Int*.</span><span class="sxs-lookup"><span data-stu-id="827a3-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="827a3-110">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="827a3-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="827a3-111">Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int*.</span><span class="sxs-lookup"><span data-stu-id="827a3-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="827a3-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="827a3-112">Return values</span></span>

<span data-ttu-id="827a3-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="827a3-113">*Int*</span></span>

<span data-ttu-id="827a3-114">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="827a3-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="827a3-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="827a3-115">Usage notes</span></span>

<span data-ttu-id="827a3-116">Все десятичные знаки усекаются.</span><span class="sxs-lookup"><span data-stu-id="827a3-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="827a3-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="827a3-117">Example 1</span></span>

<span data-ttu-id="827a3-118">`INTVALUE ("100.77")` возвращает значение *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="827a3-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="827a3-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="827a3-119">Example 2</span></span>

<span data-ttu-id="827a3-120">`INTVALUE (-100.77)` возвращает значение *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="827a3-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="827a3-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="827a3-121">Additional resources</span></span>

[<span data-ttu-id="827a3-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="827a3-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
