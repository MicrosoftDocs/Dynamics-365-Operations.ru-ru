---
title: Функция ER MID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности MID
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 6fbaf5952222d90a855956fb93713e0f9ef81305
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041040"
---
# <span data-ttu-id="18298-103"><a name="MID">Функция ER MID</a></span><span class="sxs-lookup"><span data-stu-id="18298-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18298-104">Функция `MID` возвращает *строковое* значение, которое представляет указанное число символов из указанной строки, начиная с указанного положения.</span><span class="sxs-lookup"><span data-stu-id="18298-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="18298-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18298-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="18298-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="18298-106">Arguments</span></span>

<span data-ttu-id="18298-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="18298-107">`text`: *String*</span></span>

<span data-ttu-id="18298-108">Строковое *значение*, которое определяет текст, из которого возвращаются символы.</span><span class="sxs-lookup"><span data-stu-id="18298-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="18298-109">`starting position`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="18298-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="18298-110">*Целочисленное* значение, определяющее положение первого символа, который должен быть возвращен из указанного текста.</span><span class="sxs-lookup"><span data-stu-id="18298-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="18298-111">`number of characters`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="18298-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="18298-112">*Целочисленное* значение, определяющее число символов, которые должны быть возвращены, начиная с указанного места.</span><span class="sxs-lookup"><span data-stu-id="18298-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="18298-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="18298-113">Return values</span></span>

<span data-ttu-id="18298-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="18298-114">*String*</span></span>

<span data-ttu-id="18298-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="18298-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="18298-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="18298-116">Usage notes</span></span>

<span data-ttu-id="18298-117">Если значение аргумента `starting position` меньше 0 (ноль), символы, которые возвращаются, учитываются из первой позиции в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="18298-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="18298-118">Если значение аргумента `starting position` превышает длину указанной строки, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="18298-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="18298-119">Пример</span><span class="sxs-lookup"><span data-stu-id="18298-119">Example</span></span>

<span data-ttu-id="18298-120">`MID ("Sample", 2, 3)` возвращает **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="18298-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18298-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18298-121">Additional resources</span></span>

[<span data-ttu-id="18298-122">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="18298-122">Text functions</span></span>](er-functions-category-text.md)
