---
title: Функция ER REPLACE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности REPLACE.
author: NickSelin
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746213"
---
# <a name="replace-er-function"></a><span data-ttu-id="90bf0-103">Функция ER REPLACE</span><span class="sxs-lookup"><span data-stu-id="90bf0-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90bf0-104">Функция `REPLACE` возвращает указанную строку текста в качестве значения *Строка* после того, как все или ее часть была заменена другой строкой.</span><span class="sxs-lookup"><span data-stu-id="90bf0-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="90bf0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90bf0-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="90bf0-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="90bf0-106">Arguments</span></span>

<span data-ttu-id="90bf0-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="90bf0-107">`text`: *String*</span></span>

<span data-ttu-id="90bf0-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="90bf0-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="90bf0-109">`pattern`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="90bf0-109">`pattern`: *String*</span></span>

<span data-ttu-id="90bf0-110">Если аргумент `regular expression flag` — **FALSE**, этот аргумент содержит текст, который должен быть заменен.</span><span class="sxs-lookup"><span data-stu-id="90bf0-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="90bf0-111">Если аргумент `regular expression flag` — **TRUE**, этот аргумент содержит регулярное выражение, которое определяет как шаблон поиска, так и текст замены.</span><span class="sxs-lookup"><span data-stu-id="90bf0-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="90bf0-112">`replacement`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="90bf0-112">`replacement`: *String*</span></span>

<span data-ttu-id="90bf0-113">Если аргумент `regular expression flag` — **FALSE**, этот аргумент содержит текст, который используется в качестве замены.</span><span class="sxs-lookup"><span data-stu-id="90bf0-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="90bf0-114">Если аргумент `regular expression flag` — **TRUE**, этот аргумент не используется.</span><span class="sxs-lookup"><span data-stu-id="90bf0-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="90bf0-115">`regular expression flag`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="90bf0-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="90bf0-116">*Логическое* значение, которое указывает, используется ли регулярное выражение для замены.</span><span class="sxs-lookup"><span data-stu-id="90bf0-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="90bf0-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="90bf0-117">Return values</span></span>

<span data-ttu-id="90bf0-118">*Строка*</span><span class="sxs-lookup"><span data-stu-id="90bf0-118">*String*</span></span>

<span data-ttu-id="90bf0-119">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="90bf0-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="90bf0-120">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="90bf0-120">Usage notes</span></span>

<span data-ttu-id="90bf0-121">Если аргумент `regular expression flag` — **TRUE**, эта функция возвращает указанную строку после того, как она была изменена в результате использования регулярного выражения, заданного аргументом `pattern`.</span><span class="sxs-lookup"><span data-stu-id="90bf0-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="90bf0-122">Регулярное выражение используется для обнаружения символов, которые необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="90bf0-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="90bf0-123">Если аргумент `regular expression flag` имеет значение **FALSE**, эта функция возвращает указанную строку после того, как набор символов, определенных в аргументе `pattern`, был заменен символами из аргумента `replacement`.</span><span class="sxs-lookup"><span data-stu-id="90bf0-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="90bf0-124">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90bf0-124">Example 1</span></span>

<span data-ttu-id="90bf0-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` применяет регулярное выражение, которое удаляет все нечисловые символы и возвращает **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="90bf0-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="90bf0-126">Пример 2</span><span class="sxs-lookup"><span data-stu-id="90bf0-126">Example 2</span></span>

<span data-ttu-id="90bf0-127">`REPLACE ("abcdef", "cd", "GH", false)` заменяет шаблон **"cd"** строкой **"GH"** и возвращает **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="90bf0-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90bf0-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="90bf0-128">Additional resources</span></span>

[<span data-ttu-id="90bf0-129">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="90bf0-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]