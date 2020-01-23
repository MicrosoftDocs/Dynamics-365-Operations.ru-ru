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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916714"
---
# <span data-ttu-id="144a6-103"><a name="TRANSLATE">Функция ER TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="144a6-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="144a6-104">Функция `TRANSLATE` возвращает указанную строку текста в качестве значения *Строка* после того, как все или ее часть была заменена другой строкой.</span><span class="sxs-lookup"><span data-stu-id="144a6-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="144a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="144a6-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="144a6-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="144a6-106">Arguments</span></span>

<span data-ttu-id="144a6-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="144a6-107">`text`: *String*</span></span>

<span data-ttu-id="144a6-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="144a6-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="144a6-109">`pattern`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="144a6-109">`pattern`: *String*</span></span>

<span data-ttu-id="144a6-110">Текст, который должен быть заменен.</span><span class="sxs-lookup"><span data-stu-id="144a6-110">The text that must be replaced.</span></span>

<span data-ttu-id="144a6-111">`replacement`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="144a6-111">`replacement`: *String*</span></span>

<span data-ttu-id="144a6-112">Текст для использования в качестве замены.</span><span class="sxs-lookup"><span data-stu-id="144a6-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="144a6-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="144a6-113">Return values</span></span>

<span data-ttu-id="144a6-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="144a6-114">*String*</span></span>

<span data-ttu-id="144a6-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="144a6-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="144a6-116">Пример</span><span class="sxs-lookup"><span data-stu-id="144a6-116">Example</span></span>

<span data-ttu-id="144a6-117">`TRANSLATE ("abcdef", "cd", "GH")` заменяет шаблон **"cd"** строкой **"GH"** и возвращает **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="144a6-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="144a6-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="144a6-118">Additional resources</span></span>

[<span data-ttu-id="144a6-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="144a6-119">Text functions</span></span>](er-functions-category-text.md)
