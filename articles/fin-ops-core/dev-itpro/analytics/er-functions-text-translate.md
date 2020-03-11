---
title: Функция ER TRANSLATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TRANSLATE.
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040925"
---
# <span data-ttu-id="89d6a-103"><a name="TRANSLATE">Функция ER TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="89d6a-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89d6a-104">Функция `TRANSLATE` возвращает указанную строку текста в качестве значения *Строка* после того, как все или ее часть была заменена другой строкой.</span><span class="sxs-lookup"><span data-stu-id="89d6a-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d6a-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="89d6a-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="89d6a-106">Arguments</span></span>

<span data-ttu-id="89d6a-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="89d6a-107">`text`: *String*</span></span>

<span data-ttu-id="89d6a-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="89d6a-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="89d6a-109">`pattern`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="89d6a-109">`pattern`: *String*</span></span>

<span data-ttu-id="89d6a-110">Текст, который должен быть заменен.</span><span class="sxs-lookup"><span data-stu-id="89d6a-110">The text that must be replaced.</span></span>

<span data-ttu-id="89d6a-111">`replacement`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="89d6a-111">`replacement`: *String*</span></span>

<span data-ttu-id="89d6a-112">Текст для использования в качестве замены.</span><span class="sxs-lookup"><span data-stu-id="89d6a-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="89d6a-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="89d6a-113">Return values</span></span>

<span data-ttu-id="89d6a-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="89d6a-114">*String*</span></span>

<span data-ttu-id="89d6a-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="89d6a-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="89d6a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="89d6a-116">Example</span></span>

<span data-ttu-id="89d6a-117">`TRANSLATE ("abcdef", "cd", "GH")` заменяет шаблон **"cd"** строкой **"GH"** и возвращает **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="89d6a-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89d6a-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="89d6a-118">Additional resources</span></span>

[<span data-ttu-id="89d6a-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="89d6a-119">Text functions</span></span>](er-functions-category-text.md)
