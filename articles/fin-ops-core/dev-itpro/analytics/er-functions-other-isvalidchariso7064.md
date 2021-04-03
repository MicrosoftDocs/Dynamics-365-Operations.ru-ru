---
title: Функция ER ISVALIDCHARACTERISO7064
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISVALIDCHARACTERISO7064
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563374"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="55e12-103">Функция ER ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="55e12-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55e12-104">Функция `ISVALIDCHARACTERISO7064` возвращает *логическое* значение **TRUE**, если указанная строка представляет допустимый международный номер банковского счета (IBAN).</span><span class="sxs-lookup"><span data-stu-id="55e12-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="55e12-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="55e12-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e12-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55e12-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="55e12-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="55e12-107">Arguments</span></span>

<span data-ttu-id="55e12-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="55e12-108">`text`: *String*</span></span>

<span data-ttu-id="55e12-109">Текстовое значение, представляющее IBAN.</span><span class="sxs-lookup"><span data-stu-id="55e12-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="55e12-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="55e12-110">Return values</span></span>

<span data-ttu-id="55e12-111">*Строка*</span><span class="sxs-lookup"><span data-stu-id="55e12-111">*String*</span></span>

<span data-ttu-id="55e12-112">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="55e12-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="55e12-113">Пример</span><span class="sxs-lookup"><span data-stu-id="55e12-113">Example</span></span>

<span data-ttu-id="55e12-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="55e12-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="55e12-115">`ISVALIDCHARACTERISO7064 ("AT61")` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="55e12-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55e12-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="55e12-116">Additional resources</span></span>

[<span data-ttu-id="55e12-117">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="55e12-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]