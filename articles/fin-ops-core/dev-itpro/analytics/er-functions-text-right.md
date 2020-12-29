---
title: Функция ER RIGHT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности RIGHT.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682950"
---
# <a name="right-er-function"></a><span data-ttu-id="59296-103">Функция ER RIGHT</span><span class="sxs-lookup"><span data-stu-id="59296-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59296-104">Функция `RIGHT` возвращает *строковое* значение, которое представляет указанное число символов от конца указанной строки.</span><span class="sxs-lookup"><span data-stu-id="59296-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="59296-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59296-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="59296-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="59296-106">Arguments</span></span>

<span data-ttu-id="59296-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="59296-107">`text`: *String*</span></span>

<span data-ttu-id="59296-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="59296-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="59296-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="59296-109">`number`: *Integer*</span></span>

<span data-ttu-id="59296-110">Количество символов, которые должны быть возвращены с конца исходного текста.</span><span class="sxs-lookup"><span data-stu-id="59296-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="59296-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59296-111">Return values</span></span>

<span data-ttu-id="59296-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="59296-112">*String*</span></span>

<span data-ttu-id="59296-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="59296-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="59296-114">Пример</span><span class="sxs-lookup"><span data-stu-id="59296-114">Example</span></span>

<span data-ttu-id="59296-115">`RIGHT ("Sample", 3)` возвращает **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="59296-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59296-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59296-116">Additional resources</span></span>

[<span data-ttu-id="59296-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="59296-117">Text functions</span></span>](er-functions-category-text.md)
