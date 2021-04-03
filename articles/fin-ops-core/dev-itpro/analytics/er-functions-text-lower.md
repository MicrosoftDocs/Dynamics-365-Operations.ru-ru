---
title: Функция ER LOWER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LOWER.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e507a17f5125a3cba0d2434a1aaec0f04f0cd388
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562791"
---
# <a name="lower-er-function"></a><span data-ttu-id="b3268-103">Функция ER LOWER</span><span class="sxs-lookup"><span data-stu-id="b3268-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3268-104">Функция `LOWER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="b3268-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3268-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3268-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="b3268-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b3268-106">Arguments</span></span>

<span data-ttu-id="b3268-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b3268-107">`text`: *String*</span></span>

<span data-ttu-id="b3268-108">*Строковое* значение, задающее текст.</span><span class="sxs-lookup"><span data-stu-id="b3268-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3268-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b3268-109">Return values</span></span>

<span data-ttu-id="b3268-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="b3268-110">*String*</span></span>

<span data-ttu-id="b3268-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="b3268-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b3268-112">Пример</span><span class="sxs-lookup"><span data-stu-id="b3268-112">Example</span></span>

<span data-ttu-id="b3268-113">`LOWER ("Sample")` возвращает **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="b3268-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3268-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b3268-114">Additional resources</span></span>

[<span data-ttu-id="b3268-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="b3268-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]