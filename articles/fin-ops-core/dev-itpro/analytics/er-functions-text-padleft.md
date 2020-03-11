---
title: Функция ER PADLEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности PADLEFT.
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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040971"
---
# <span data-ttu-id="476e6-103"><a name="PADLEFT">Функция ER PADLEFT</a></span><span class="sxs-lookup"><span data-stu-id="476e6-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="476e6-104">Функция `PADLEFT` возвращает *строковое* значение указанной длины, в котором в начало указанной строки добавлены указанные символы.</span><span class="sxs-lookup"><span data-stu-id="476e6-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="476e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="476e6-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="476e6-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="476e6-106">Arguments</span></span>

<span data-ttu-id="476e6-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="476e6-107">`text`: *String*</span></span>

<span data-ttu-id="476e6-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="476e6-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="476e6-109">`length`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="476e6-109">`length`: *Integer*</span></span>

<span data-ttu-id="476e6-110">*Целочисленное* значение, представляющее окончательное число символов в строке с отступами.</span><span class="sxs-lookup"><span data-stu-id="476e6-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="476e6-111">`padding chars`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="476e6-111">`padding chars`: *String*</span></span>

<span data-ttu-id="476e6-112">Символы для использования для отступа.</span><span class="sxs-lookup"><span data-stu-id="476e6-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="476e6-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="476e6-113">Return values</span></span>

<span data-ttu-id="476e6-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="476e6-114">*String*</span></span>

<span data-ttu-id="476e6-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="476e6-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="476e6-116">Пример</span><span class="sxs-lookup"><span data-stu-id="476e6-116">Example</span></span>

<span data-ttu-id="476e6-117">`PADLEFT ("1234", 10, "`&nbsp;`")` возвращает текстовую строку **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="476e6-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="476e6-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="476e6-118">Additional resources</span></span>

[<span data-ttu-id="476e6-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="476e6-119">Text functions</span></span>](er-functions-category-text.md)
