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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744343"
---
# <a name="upper-er-function"></a><span data-ttu-id="94cf2-103">Функция ER UPPER</span><span class="sxs-lookup"><span data-stu-id="94cf2-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94cf2-104">Функция `UPPER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="94cf2-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="94cf2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94cf2-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="94cf2-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="94cf2-106">Arguments</span></span>

<span data-ttu-id="94cf2-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="94cf2-107">`text`: *String*</span></span>

<span data-ttu-id="94cf2-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="94cf2-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="94cf2-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="94cf2-109">Return values</span></span>

<span data-ttu-id="94cf2-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="94cf2-110">*String*</span></span>

<span data-ttu-id="94cf2-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="94cf2-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="94cf2-112">Пример</span><span class="sxs-lookup"><span data-stu-id="94cf2-112">Example</span></span>

<span data-ttu-id="94cf2-113">`UPPER ("Sample")` возвращает **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="94cf2-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94cf2-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="94cf2-114">Additional resources</span></span>

[<span data-ttu-id="94cf2-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="94cf2-115">Text functions</span></span>](er-functions-category-text.md)
