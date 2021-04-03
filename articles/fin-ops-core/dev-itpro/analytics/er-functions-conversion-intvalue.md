---
title: Функция ER INTVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INTVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 64f43ad29d59ade1e124b6800734b003f6ca07df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561478"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="2bdd1-103">Функция ER INTVALUE</span><span class="sxs-lookup"><span data-stu-id="2bdd1-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bdd1-104">Функция `INTVALUE` возвращает значение *Int*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="2bdd1-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="2bdd1-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="2bdd1-106">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="2bdd1-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="2bdd1-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2bdd1-107">Arguments</span></span>

<span data-ttu-id="2bdd1-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2bdd1-108">`text`: *String*</span></span>

<span data-ttu-id="2bdd1-109">Текстовое значение, которое должно быть преобразовано в число *Int*.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="2bdd1-110">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="2bdd1-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="2bdd1-111">Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int*.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="2bdd1-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2bdd1-112">Return values</span></span>

<span data-ttu-id="2bdd1-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="2bdd1-113">*Int*</span></span>

<span data-ttu-id="2bdd1-114">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2bdd1-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="2bdd1-115">Usage notes</span></span>

<span data-ttu-id="2bdd1-116">Все десятичные знаки усекаются.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="2bdd1-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bdd1-117">Example 1</span></span>

<span data-ttu-id="2bdd1-118">`INTVALUE ("100.77")` возвращает значение *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2bdd1-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2bdd1-119">Example 2</span></span>

<span data-ttu-id="2bdd1-120">`INTVALUE (-100.77)` возвращает значение *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="2bdd1-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2bdd1-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2bdd1-121">Additional resources</span></span>

[<span data-ttu-id="2bdd1-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="2bdd1-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]