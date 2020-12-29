---
title: Функция ER UPPER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности UPPER.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688349"
---
# <a name="upper-er-function"></a><span data-ttu-id="65aae-103">Функция ER UPPER</span><span class="sxs-lookup"><span data-stu-id="65aae-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65aae-104">Функция `UPPER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="65aae-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="65aae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65aae-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="65aae-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="65aae-106">Arguments</span></span>

<span data-ttu-id="65aae-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="65aae-107">`text`: *String*</span></span>

<span data-ttu-id="65aae-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="65aae-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="65aae-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="65aae-109">Return values</span></span>

<span data-ttu-id="65aae-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="65aae-110">*String*</span></span>

<span data-ttu-id="65aae-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="65aae-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="65aae-112">Пример</span><span class="sxs-lookup"><span data-stu-id="65aae-112">Example</span></span>

<span data-ttu-id="65aae-113">`UPPER ("Sample")` возвращает **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="65aae-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65aae-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="65aae-114">Additional resources</span></span>

[<span data-ttu-id="65aae-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="65aae-115">Text functions</span></span>](er-functions-category-text.md)
