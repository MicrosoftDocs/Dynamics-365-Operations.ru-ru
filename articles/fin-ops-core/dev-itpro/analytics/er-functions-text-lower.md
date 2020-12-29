---
title: Функция ER LOWER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LOWER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680322"
---
# <a name="lower-er-function"></a><span data-ttu-id="59db1-103">Функция ER LOWER</span><span class="sxs-lookup"><span data-stu-id="59db1-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59db1-104">Функция `LOWER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="59db1-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="59db1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59db1-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="59db1-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="59db1-106">Arguments</span></span>

<span data-ttu-id="59db1-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="59db1-107">`text`: *String*</span></span>

<span data-ttu-id="59db1-108">*Строковое* значение, задающее текст.</span><span class="sxs-lookup"><span data-stu-id="59db1-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="59db1-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59db1-109">Return values</span></span>

<span data-ttu-id="59db1-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="59db1-110">*String*</span></span>

<span data-ttu-id="59db1-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="59db1-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="59db1-112">Пример</span><span class="sxs-lookup"><span data-stu-id="59db1-112">Example</span></span>

<span data-ttu-id="59db1-113">`LOWER ("Sample")` возвращает **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="59db1-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59db1-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59db1-114">Additional resources</span></span>

[<span data-ttu-id="59db1-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="59db1-115">Text functions</span></span>](er-functions-category-text.md)
