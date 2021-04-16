---
title: Функция ER MOD_97
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности MOD_97
author: NickSelin
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
ms.openlocfilehash: 1054407addaf6f7c2a7d2f72bf1479e9dc374389
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749173"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="87bd7-103">Функция ER MOD_97</span><span class="sxs-lookup"><span data-stu-id="87bd7-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87bd7-104">Функция `MOD_97` возвращает *строковое* значение, представляющее ссылку кредитора в качестве выражения MOD97, на основе цифр указанного номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="87bd7-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bd7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87bd7-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="87bd7-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="87bd7-106">Arguments</span></span>

<span data-ttu-id="87bd7-107">`invoice number digits`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="87bd7-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="87bd7-108">Текстовое значение, представляющее цифры номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="87bd7-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="87bd7-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="87bd7-109">Return values</span></span>

<span data-ttu-id="87bd7-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="87bd7-110">*String*</span></span>

<span data-ttu-id="87bd7-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="87bd7-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="87bd7-112">Пример</span><span class="sxs-lookup"><span data-stu-id="87bd7-112">Example</span></span>

<span data-ttu-id="87bd7-113">`MOD_97 ("VEND-200002")` возвращает **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="87bd7-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87bd7-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87bd7-114">Additional resources</span></span>

[<span data-ttu-id="87bd7-115">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="87bd7-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]