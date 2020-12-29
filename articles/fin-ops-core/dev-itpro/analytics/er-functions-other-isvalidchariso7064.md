---
title: Функция ER ISVALIDCHARACTERISO7064
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISVALIDCHARACTERISO7064
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680670"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="e47ca-103">Функция ER ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="e47ca-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e47ca-104">Функция `ISVALIDCHARACTERISO7064` возвращает *логическое* значение **TRUE**, если указанная строка представляет допустимый международный номер банковского счета (IBAN).</span><span class="sxs-lookup"><span data-stu-id="e47ca-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="e47ca-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e47ca-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e47ca-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e47ca-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="e47ca-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e47ca-107">Arguments</span></span>

<span data-ttu-id="e47ca-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="e47ca-108">`text`: *String*</span></span>

<span data-ttu-id="e47ca-109">Текстовое значение, представляющее IBAN.</span><span class="sxs-lookup"><span data-stu-id="e47ca-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="e47ca-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e47ca-110">Return values</span></span>

<span data-ttu-id="e47ca-111">*Строка*</span><span class="sxs-lookup"><span data-stu-id="e47ca-111">*String*</span></span>

<span data-ttu-id="e47ca-112">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="e47ca-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e47ca-113">Пример</span><span class="sxs-lookup"><span data-stu-id="e47ca-113">Example</span></span>

<span data-ttu-id="e47ca-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e47ca-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="e47ca-115">`ISVALIDCHARACTERISO7064 ("AT61")` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e47ca-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e47ca-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e47ca-116">Additional resources</span></span>

[<span data-ttu-id="e47ca-117">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="e47ca-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
