---
title: Функция ER TRANSLATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TRANSLATE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: f17d3439870710766906013e74452c2e76fec4ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560022"
---
# <a name="translate-er-function"></a><span data-ttu-id="af10a-103">Функция ER TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="af10a-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af10a-104">Функция `TRANSLATE` возвращает значение *Строка*, которое содержит результат замены символов указанного текста символами другого предоставленного набора.</span><span class="sxs-lookup"><span data-stu-id="af10a-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="af10a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af10a-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="af10a-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="af10a-106">Arguments</span></span>

<span data-ttu-id="af10a-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="af10a-107">`text`: *String*</span></span>

<span data-ttu-id="af10a-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="af10a-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="af10a-109">`pattern`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="af10a-109">`pattern`: *String*</span></span>

<span data-ttu-id="af10a-110">Текст, который должен быть заменен.</span><span class="sxs-lookup"><span data-stu-id="af10a-110">The text that must be replaced.</span></span>

<span data-ttu-id="af10a-111">`replacement`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="af10a-111">`replacement`: *String*</span></span>

<span data-ttu-id="af10a-112">Текст для использования в качестве замены.</span><span class="sxs-lookup"><span data-stu-id="af10a-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="af10a-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="af10a-113">Return values</span></span>

<span data-ttu-id="af10a-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="af10a-114">*String*</span></span>

<span data-ttu-id="af10a-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="af10a-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="af10a-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="af10a-116">Usage notes</span></span>

<span data-ttu-id="af10a-117">Функция `TRANSLATE` заменяет один символ за раз.</span><span class="sxs-lookup"><span data-stu-id="af10a-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="af10a-118">Функция заменяет первый символ аргумента `text` с первым символом аргумента `pattern`, затем второй символ, и действует таким образом до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="af10a-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="af10a-119">Когда символ из аргументов `text` и `pattern` совпадает, он замещается символом из аргумента `replacement`, расположенным в той же позиции, что и символ из аргумента `pattern`.</span><span class="sxs-lookup"><span data-stu-id="af10a-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="af10a-120">Если символ появляется в аргументе `pattern` несколько раз, используется сопоставление аргумента `replacement`, соответствующее первому вхождению данного символа.</span><span class="sxs-lookup"><span data-stu-id="af10a-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="af10a-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af10a-121">Example 1</span></span>

<span data-ttu-id="af10a-122">`TRANSLATE ("abcdef", "cd", "GH")` заменяет символ **"c"** указанного текста **"abcdef"** символом **"G"** аргумента `replacement`, выполняя следующие действия:</span><span class="sxs-lookup"><span data-stu-id="af10a-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="af10a-123">Символ **"c"** представлен в тексте `pattern` в первом положении.</span><span class="sxs-lookup"><span data-stu-id="af10a-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="af10a-124">Первая позиция текста `replacement` содержит символ **"G"**.</span><span class="sxs-lookup"><span data-stu-id="af10a-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="af10a-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="af10a-125">Example 2</span></span>

<span data-ttu-id="af10a-126">`TRANSLATE ("abcdef", "ccd", "GH")` возвращает **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="af10a-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="af10a-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="af10a-127">Example 3</span></span>

<span data-ttu-id="af10a-128">`TRANSLATE ("abccba", "abc", "123")` возвращает **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="af10a-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af10a-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af10a-129">Additional resources</span></span>

[<span data-ttu-id="af10a-130">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="af10a-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]