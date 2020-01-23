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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916553"
---
# <span data-ttu-id="219ac-103"><a name="INT64VALUE">Функция ER INT64VALUE</a></span><span class="sxs-lookup"><span data-stu-id="219ac-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="219ac-104">Функция `INT64VALUE` возвращает значение *Int64*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="219ac-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="219ac-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="219ac-105">Syntax 1</span></span>

```
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="219ac-106">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="219ac-106">Syntax 2</span></span>

```
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="219ac-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="219ac-107">Arguments</span></span>

<span data-ttu-id="219ac-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="219ac-108">`text`: *String*</span></span>

<span data-ttu-id="219ac-109">Текстовое значение, которое должно быть преобразовано в число *Int64*.</span><span class="sxs-lookup"><span data-stu-id="219ac-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="219ac-110">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="219ac-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="219ac-111">Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int64*.</span><span class="sxs-lookup"><span data-stu-id="219ac-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="219ac-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="219ac-112">Return values</span></span>

<span data-ttu-id="219ac-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="219ac-113">*Int64*</span></span>

<span data-ttu-id="219ac-114">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="219ac-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="219ac-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="219ac-115">Usage notes</span></span>

<span data-ttu-id="219ac-116">Все десятичные знаки усекаются.</span><span class="sxs-lookup"><span data-stu-id="219ac-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="219ac-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="219ac-117">Example 1</span></span>

<span data-ttu-id="219ac-118">`INT64VALUE ("22565422744")` возвращает значение *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="219ac-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="219ac-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="219ac-119">Example 2</span></span>

<span data-ttu-id="219ac-120">`INT64VALUE ( VALUE("22565422744.77"))` возвращает значение *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="219ac-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="219ac-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="219ac-121">Additional resources</span></span>

[<span data-ttu-id="219ac-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="219ac-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
