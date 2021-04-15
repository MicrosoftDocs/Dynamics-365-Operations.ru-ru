---
title: Функция ER INT64VALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INT64VALUE.
author: NickSelin
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755404"
---
# <a name="int64value-er-function"></a><span data-ttu-id="1fce9-103">Функция ER INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="1fce9-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fce9-104">Функция `INT64VALUE` возвращает значение *Int64*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="1fce9-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1fce9-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="1fce9-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="1fce9-106">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="1fce9-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="1fce9-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="1fce9-107">Arguments</span></span>

<span data-ttu-id="1fce9-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="1fce9-108">`text`: *String*</span></span>

<span data-ttu-id="1fce9-109">Текстовое значение, которое должно быть преобразовано в число *Int64*.</span><span class="sxs-lookup"><span data-stu-id="1fce9-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="1fce9-110">`number`: *Вещественный* или *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="1fce9-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1fce9-111">Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int64*.</span><span class="sxs-lookup"><span data-stu-id="1fce9-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1fce9-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1fce9-112">Return values</span></span>

<span data-ttu-id="1fce9-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="1fce9-113">*Int64*</span></span>

<span data-ttu-id="1fce9-114">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="1fce9-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1fce9-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="1fce9-115">Usage notes</span></span>

<span data-ttu-id="1fce9-116">Все десятичные знаки усекаются.</span><span class="sxs-lookup"><span data-stu-id="1fce9-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="1fce9-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fce9-117">Example 1</span></span>

<span data-ttu-id="1fce9-118">`INT64VALUE ("22565422744")` возвращает значение *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="1fce9-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1fce9-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1fce9-119">Example 2</span></span>

<span data-ttu-id="1fce9-120">`INT64VALUE ( VALUE("22565422744.77"))` возвращает значение *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="1fce9-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fce9-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1fce9-121">Additional resources</span></span>

[<span data-ttu-id="1fce9-122">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="1fce9-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]