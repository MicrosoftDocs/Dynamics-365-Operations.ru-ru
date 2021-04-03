---
title: Функция ER RIGHT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности RIGHT.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570248"
---
# <a name="right-er-function"></a><span data-ttu-id="d86ca-103">Функция ER RIGHT</span><span class="sxs-lookup"><span data-stu-id="d86ca-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d86ca-104">Функция `RIGHT` возвращает *строковое* значение, которое представляет указанное число символов от конца указанной строки.</span><span class="sxs-lookup"><span data-stu-id="d86ca-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d86ca-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="d86ca-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="d86ca-106">Arguments</span></span>

<span data-ttu-id="d86ca-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="d86ca-107">`text`: *String*</span></span>

<span data-ttu-id="d86ca-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="d86ca-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="d86ca-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="d86ca-109">`number`: *Integer*</span></span>

<span data-ttu-id="d86ca-110">Количество символов, которые должны быть возвращены с конца исходного текста.</span><span class="sxs-lookup"><span data-stu-id="d86ca-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d86ca-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d86ca-111">Return values</span></span>

<span data-ttu-id="d86ca-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="d86ca-112">*String*</span></span>

<span data-ttu-id="d86ca-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="d86ca-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d86ca-114">Пример</span><span class="sxs-lookup"><span data-stu-id="d86ca-114">Example</span></span>

<span data-ttu-id="d86ca-115">`RIGHT ("Sample", 3)` возвращает **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="d86ca-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d86ca-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d86ca-116">Additional resources</span></span>

[<span data-ttu-id="d86ca-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="d86ca-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]