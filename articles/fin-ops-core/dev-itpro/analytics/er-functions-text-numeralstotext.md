---
title: Функция ER NUMERALSTOTEXT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMERALSTOTEXT.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680226"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="94cbf-103">Функция ER NUMERALSTOTEXT</span><span class="sxs-lookup"><span data-stu-id="94cbf-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94cbf-104">Функция `NUMERALSTOTEXT` возвращает указанное число в качестве *строкового* значения после того, как оно было преобразовано в текст (т.е. преобразовано в строки текста) на указанном языке.</span><span class="sxs-lookup"><span data-stu-id="94cbf-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="94cbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94cbf-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="94cbf-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="94cbf-106">Arguments</span></span>

<span data-ttu-id="94cbf-107">`number`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="94cbf-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="94cbf-108">Числовое значение, которое определяет число, которое должно быть преобразовано в текст.</span><span class="sxs-lookup"><span data-stu-id="94cbf-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="94cbf-109">`language`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="94cbf-109">`language`: *String*</span></span>

<span data-ttu-id="94cbf-110">*Строковое* значение, представляющее код языка.</span><span class="sxs-lookup"><span data-stu-id="94cbf-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="94cbf-111">`currency`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="94cbf-111">`currency`: *String*</span></span>

<span data-ttu-id="94cbf-112">*Строковое* значение, представляющее код валюты.</span><span class="sxs-lookup"><span data-stu-id="94cbf-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="94cbf-113">`print currency name flag`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="94cbf-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="94cbf-114">*Логическое* значение, указывающее, следует ли добавить название валюты в написанный текст.</span><span class="sxs-lookup"><span data-stu-id="94cbf-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="94cbf-115">`decimal points`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="94cbf-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="94cbf-116">*Целочисленное* значение, которое указывает число десятичных знаков для написанного текста.</span><span class="sxs-lookup"><span data-stu-id="94cbf-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="94cbf-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="94cbf-117">Return values</span></span>

<span data-ttu-id="94cbf-118">*Строка*</span><span class="sxs-lookup"><span data-stu-id="94cbf-118">*String*</span></span>

<span data-ttu-id="94cbf-119">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="94cbf-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="94cbf-120">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="94cbf-120">Usage notes</span></span>

<span data-ttu-id="94cbf-121">Код языка указывать необязательно.</span><span class="sxs-lookup"><span data-stu-id="94cbf-121">The language code is optional.</span></span> <span data-ttu-id="94cbf-122">Если он определен как пустая строка, вместо него используется код языка для контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="94cbf-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="94cbf-123">Код языка по умолчанию — **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="94cbf-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="94cbf-124">Код языка для выполняющегося контекста определяется в элементе **Папка** или **Файл** в выполняющемся формате электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="94cbf-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="94cbf-125">Код валюты указывать необязательно.</span><span class="sxs-lookup"><span data-stu-id="94cbf-125">The currency code is optional.</span></span> <span data-ttu-id="94cbf-126">Если он определен как пустая строка, вместо него используется валюта компании для контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="94cbf-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="94cbf-127">Аргументы `print currency name flag` и `decimal points` анализируются только для следующих кодов языка: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** и **RU**.</span><span class="sxs-lookup"><span data-stu-id="94cbf-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="94cbf-128">Кроме того, аргумент `print currency name flag` анализируется только для компаний, в которых контекст страны или региона поддерживает склонение названий валюты.</span><span class="sxs-lookup"><span data-stu-id="94cbf-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="94cbf-129">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94cbf-129">Example 1</span></span>

<span data-ttu-id="94cbf-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` возвращает **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="94cbf-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="94cbf-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94cbf-131">Example 2</span></span>

<span data-ttu-id="94cbf-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` возвращает **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="94cbf-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="94cbf-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94cbf-133">Example 3</span></span>

<span data-ttu-id="94cbf-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` возвращает **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="94cbf-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94cbf-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="94cbf-135">Additional resources</span></span>

[<span data-ttu-id="94cbf-136">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="94cbf-136">Text functions</span></span>](er-functions-category-text.md)
