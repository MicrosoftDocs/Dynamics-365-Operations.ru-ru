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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f6f3326c9ca5cdcb3cef52f243d6d3da34251ce
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915932"
---
# <span data-ttu-id="88aac-103"><a name="ISVALIDCHARACTERISO7064">Функция ER ISVALIDCHARACTERISO7064</a></span><span class="sxs-lookup"><span data-stu-id="88aac-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88aac-104">Функция `ISVALIDCHARACTERISO7064` возвращает *логическое* значение **TRUE**, если указанная строка представляет допустимый международный номер банковского счета (IBAN).</span><span class="sxs-lookup"><span data-stu-id="88aac-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="88aac-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="88aac-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="88aac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88aac-106">Syntax</span></span>

```
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="88aac-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="88aac-107">Arguments</span></span>

<span data-ttu-id="88aac-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="88aac-108">`text`: *String*</span></span>

<span data-ttu-id="88aac-109">Текстовое значение, представляющее IBAN.</span><span class="sxs-lookup"><span data-stu-id="88aac-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="88aac-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="88aac-110">Return values</span></span>

<span data-ttu-id="88aac-111">*Строка*</span><span class="sxs-lookup"><span data-stu-id="88aac-111">*String*</span></span>

<span data-ttu-id="88aac-112">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="88aac-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="88aac-113">Пример</span><span class="sxs-lookup"><span data-stu-id="88aac-113">Example</span></span>

<span data-ttu-id="88aac-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="88aac-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="88aac-115">`ISVALIDCHARACTERISO7064 ("AT61")` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="88aac-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88aac-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="88aac-116">Additional resources</span></span>

[<span data-ttu-id="88aac-117">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="88aac-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
