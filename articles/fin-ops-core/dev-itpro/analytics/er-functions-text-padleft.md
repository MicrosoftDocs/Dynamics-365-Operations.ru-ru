---
title: Функция ER PADLEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности PADLEFT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746251"
---
# <a name="padleft-er-function"></a><span data-ttu-id="4dd97-103">Функция ER PADLEFT</span><span class="sxs-lookup"><span data-stu-id="4dd97-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dd97-104">Функция `PADLEFT` возвращает *строковое* значение указанной длины, в котором в начало указанной строки добавлены указанные символы.</span><span class="sxs-lookup"><span data-stu-id="4dd97-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd97-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dd97-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="4dd97-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="4dd97-106">Arguments</span></span>

<span data-ttu-id="4dd97-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4dd97-107">`text`: *String*</span></span>

<span data-ttu-id="4dd97-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="4dd97-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="4dd97-109">`length`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="4dd97-109">`length`: *Integer*</span></span>

<span data-ttu-id="4dd97-110">*Целочисленное* значение, представляющее окончательное число символов в строке с отступами.</span><span class="sxs-lookup"><span data-stu-id="4dd97-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="4dd97-111">`padding chars`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4dd97-111">`padding chars`: *String*</span></span>

<span data-ttu-id="4dd97-112">Символы для использования для отступа.</span><span class="sxs-lookup"><span data-stu-id="4dd97-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="4dd97-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4dd97-113">Return values</span></span>

<span data-ttu-id="4dd97-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="4dd97-114">*String*</span></span>

<span data-ttu-id="4dd97-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="4dd97-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4dd97-116">Пример</span><span class="sxs-lookup"><span data-stu-id="4dd97-116">Example</span></span>

<span data-ttu-id="4dd97-117">`PADLEFT ("1234", 10, "`&nbsp;`")` возвращает текстовую строку **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="4dd97-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4dd97-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4dd97-118">Additional resources</span></span>

[<span data-ttu-id="4dd97-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="4dd97-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]