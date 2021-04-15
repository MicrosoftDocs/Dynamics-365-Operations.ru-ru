---
title: Функция ER MID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности MID
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746275"
---
# <a name="mid-er-function"></a><span data-ttu-id="f9576-103">Функция ER MID</span><span class="sxs-lookup"><span data-stu-id="f9576-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9576-104">Функция `MID` возвращает *строковое* значение, которое представляет указанное число символов из указанной строки, начиная с указанного положения.</span><span class="sxs-lookup"><span data-stu-id="f9576-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9576-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9576-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="f9576-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="f9576-106">Arguments</span></span>

<span data-ttu-id="f9576-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="f9576-107">`text`: *String*</span></span>

<span data-ttu-id="f9576-108">Строковое *значение*, которое определяет текст, из которого возвращаются символы.</span><span class="sxs-lookup"><span data-stu-id="f9576-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="f9576-109">`starting position`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="f9576-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="f9576-110">*Целочисленное* значение, определяющее положение первого символа, который должен быть возвращен из указанного текста.</span><span class="sxs-lookup"><span data-stu-id="f9576-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="f9576-111">`number of characters`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="f9576-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="f9576-112">*Целочисленное* значение, определяющее число символов, которые должны быть возвращены, начиная с указанного места.</span><span class="sxs-lookup"><span data-stu-id="f9576-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9576-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f9576-113">Return values</span></span>

<span data-ttu-id="f9576-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="f9576-114">*String*</span></span>

<span data-ttu-id="f9576-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="f9576-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f9576-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="f9576-116">Usage notes</span></span>

<span data-ttu-id="f9576-117">Если значение аргумента `starting position` меньше 0 (ноль), символы, которые возвращаются, учитываются из первой позиции в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="f9576-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="f9576-118">Если значение аргумента `starting position` превышает длину указанной строки, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f9576-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="f9576-119">Пример</span><span class="sxs-lookup"><span data-stu-id="f9576-119">Example</span></span>

<span data-ttu-id="f9576-120">`MID ("Sample", 2, 3)` возвращает **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="f9576-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9576-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f9576-121">Additional resources</span></span>

[<span data-ttu-id="f9576-122">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="f9576-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]