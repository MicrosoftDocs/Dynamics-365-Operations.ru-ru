---
title: Функция ER LEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LEFT
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 69b1d95ea0e82b1947b665b0724cff6c5b319633
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746347"
---
# <a name="left-er-function"></a><span data-ttu-id="467d4-103">Функция ER LEFT</span><span class="sxs-lookup"><span data-stu-id="467d4-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="467d4-104">Функция `LEFT` возвращает *строковое* значение, которое представляет указанное число символов от начала указанной строки.</span><span class="sxs-lookup"><span data-stu-id="467d4-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="467d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="467d4-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="467d4-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="467d4-106">Arguments</span></span>

<span data-ttu-id="467d4-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="467d4-107">`text`: *String*</span></span>

<span data-ttu-id="467d4-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="467d4-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="467d4-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="467d4-109">`number`: *Integer*</span></span>

<span data-ttu-id="467d4-110">Количество символов, которые должны быть возвращены с начала исходного текста.</span><span class="sxs-lookup"><span data-stu-id="467d4-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="467d4-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="467d4-111">Return values</span></span>

<span data-ttu-id="467d4-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="467d4-112">*String*</span></span>

<span data-ttu-id="467d4-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="467d4-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="467d4-114">Пример</span><span class="sxs-lookup"><span data-stu-id="467d4-114">Example</span></span>

<span data-ttu-id="467d4-115">`LEFT ("Sample", 3)` возвращает **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="467d4-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="467d4-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="467d4-116">Additional resources</span></span>

[<span data-ttu-id="467d4-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="467d4-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]