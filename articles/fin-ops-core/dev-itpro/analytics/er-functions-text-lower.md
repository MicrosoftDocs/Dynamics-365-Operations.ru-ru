---
title: Функция ER LOWER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LOWER.
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746299"
---
# <a name="lower-er-function"></a><span data-ttu-id="53289-103">Функция ER LOWER</span><span class="sxs-lookup"><span data-stu-id="53289-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53289-104">Функция `LOWER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="53289-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="53289-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53289-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="53289-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="53289-106">Arguments</span></span>

<span data-ttu-id="53289-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="53289-107">`text`: *String*</span></span>

<span data-ttu-id="53289-108">*Строковое* значение, задающее текст.</span><span class="sxs-lookup"><span data-stu-id="53289-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="53289-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="53289-109">Return values</span></span>

<span data-ttu-id="53289-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="53289-110">*String*</span></span>

<span data-ttu-id="53289-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="53289-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="53289-112">Пример</span><span class="sxs-lookup"><span data-stu-id="53289-112">Example</span></span>

<span data-ttu-id="53289-113">`LOWER ("Sample")` возвращает **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="53289-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53289-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="53289-114">Additional resources</span></span>

[<span data-ttu-id="53289-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="53289-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]