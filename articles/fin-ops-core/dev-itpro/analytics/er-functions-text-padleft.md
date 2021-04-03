---
title: Функция ER PADLEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности PADLEFT.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562693"
---
# <a name="padleft-er-function"></a><span data-ttu-id="4e1ce-103">Функция ER PADLEFT</span><span class="sxs-lookup"><span data-stu-id="4e1ce-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e1ce-104">Функция `PADLEFT` возвращает *строковое* значение указанной длины, в котором в начало указанной строки добавлены указанные символы.</span><span class="sxs-lookup"><span data-stu-id="4e1ce-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e1ce-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="4e1ce-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="4e1ce-106">Arguments</span></span>

<span data-ttu-id="4e1ce-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4e1ce-107">`text`: *String*</span></span>

<span data-ttu-id="4e1ce-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="4e1ce-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="4e1ce-109">`length`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="4e1ce-109">`length`: *Integer*</span></span>

<span data-ttu-id="4e1ce-110">*Целочисленное* значение, представляющее окончательное число символов в строке с отступами.</span><span class="sxs-lookup"><span data-stu-id="4e1ce-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="4e1ce-111">`padding chars`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4e1ce-111">`padding chars`: *String*</span></span>

<span data-ttu-id="4e1ce-112">Символы для использования для отступа.</span><span class="sxs-lookup"><span data-stu-id="4e1ce-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e1ce-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4e1ce-113">Return values</span></span>

<span data-ttu-id="4e1ce-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="4e1ce-114">*String*</span></span>

<span data-ttu-id="4e1ce-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="4e1ce-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4e1ce-116">Пример</span><span class="sxs-lookup"><span data-stu-id="4e1ce-116">Example</span></span>

<span data-ttu-id="4e1ce-117">`PADLEFT ("1234", 10, "`&nbsp;`")` возвращает текстовую строку **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="4e1ce-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e1ce-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e1ce-118">Additional resources</span></span>

[<span data-ttu-id="4e1ce-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="4e1ce-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]