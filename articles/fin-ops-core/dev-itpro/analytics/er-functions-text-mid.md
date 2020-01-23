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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915610"
---
# <span data-ttu-id="b7b7f-103"><a name="MID">Функция ER MID</a></span><span class="sxs-lookup"><span data-stu-id="b7b7f-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7b7f-104">Функция `MID` возвращает *строковое* значение, которое представляет указанное число символов из указанной строки, начиная с указанного положения.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7b7f-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="b7b7f-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b7b7f-106">Arguments</span></span>

<span data-ttu-id="b7b7f-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b7b7f-107">`text`: *String*</span></span>

<span data-ttu-id="b7b7f-108">Строковое *значение*, которое определяет текст, из которого возвращаются символы.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="b7b7f-109">`starting position`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="b7b7f-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="b7b7f-110">*Целочисленное* значение, определяющее положение первого символа, который должен быть возвращен из указанного текста.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="b7b7f-111">`number of characters`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="b7b7f-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="b7b7f-112">*Целочисленное* значение, определяющее число символов, которые должны быть возвращены, начиная с указанного места.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7b7f-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b7b7f-113">Return values</span></span>

<span data-ttu-id="b7b7f-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="b7b7f-114">*String*</span></span>

<span data-ttu-id="b7b7f-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b7b7f-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="b7b7f-116">Usage notes</span></span>

<span data-ttu-id="b7b7f-117">Если значение аргумента `starting position` меньше 0 (ноль), символы, которые возвращаются, учитываются из первой позиции в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="b7b7f-118">Если значение аргумента `starting position` превышает длину указанной строки, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="b7b7f-119">Пример</span><span class="sxs-lookup"><span data-stu-id="b7b7f-119">Example</span></span>

<span data-ttu-id="b7b7f-120">`MID ("Sample", 2, 3)` возвращает **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="b7b7f-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7b7f-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7b7f-121">Additional resources</span></span>

[<span data-ttu-id="b7b7f-122">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="b7b7f-122">Text functions</span></span>](er-functions-category-text.md)
