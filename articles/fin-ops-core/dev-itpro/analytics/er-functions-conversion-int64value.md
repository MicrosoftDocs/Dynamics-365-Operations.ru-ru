---
title: Функция ER INT64VALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INT64VALUE.
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
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744847"
---
# <a name="int64value-er-function"></a><span data-ttu-id="675e9-103">Функция ER INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="675e9-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="675e9-104">Функция `INT64VALUE` возвращает значение *Int64*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="675e9-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="675e9-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="675e9-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="675e9-106">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="675e9-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="675e9-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="675e9-107">Arguments</span></span>

<span data-ttu-id="675e9-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="675e9-108">`text`: *String*</span></span>

<span data-ttu-id="675e9-109">Текстовое значение, которое должно быть преобразовано в число *Int64*.</span><span class="sxs-lookup"><span data-stu-id="675e9-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="675e9-110">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="675e9-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="675e9-111">Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int64*.</span><span class="sxs-lookup"><span data-stu-id="675e9-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="675e9-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="675e9-112">Return values</span></span>

<span data-ttu-id="675e9-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="675e9-113">*Int64*</span></span>

<span data-ttu-id="675e9-114">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="675e9-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="675e9-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="675e9-115">Usage notes</span></span>

<span data-ttu-id="675e9-116">Все десятичные знаки усекаются.</span><span class="sxs-lookup"><span data-stu-id="675e9-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="675e9-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="675e9-117">Example 1</span></span>

<span data-ttu-id="675e9-118">`INT64VALUE ("22565422744")` возвращает значение *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="675e9-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="675e9-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="675e9-119">Example 2</span></span>

<span data-ttu-id="675e9-120">`INT64VALUE ( VALUE("22565422744.77"))` возвращает значение *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="675e9-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="675e9-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="675e9-121">Additional resources</span></span>

[<span data-ttu-id="675e9-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="675e9-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
