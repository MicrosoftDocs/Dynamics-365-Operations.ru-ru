---
title: Функция ER MOD_97
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности MOD_97
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
ms.openlocfilehash: b2e4e40fbd953b31225ccc0f54912b26933ccc48
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680646"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="9bcfd-103">Функция ER MOD_97</span><span class="sxs-lookup"><span data-stu-id="9bcfd-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bcfd-104">Функция `MOD_97` возвращает *строковое* значение, представляющее ссылку кредитора в качестве выражения MOD97, на основе цифр указанного номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcfd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bcfd-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="9bcfd-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9bcfd-106">Arguments</span></span>

<span data-ttu-id="9bcfd-107">`invoice number digits`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="9bcfd-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="9bcfd-108">Текстовое значение, представляющее цифры номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="9bcfd-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9bcfd-109">Return values</span></span>

<span data-ttu-id="9bcfd-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9bcfd-110">*String*</span></span>

<span data-ttu-id="9bcfd-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9bcfd-112">Пример</span><span class="sxs-lookup"><span data-stu-id="9bcfd-112">Example</span></span>

<span data-ttu-id="9bcfd-113">`MOD_97 ("VEND-200002")` возвращает **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bcfd-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9bcfd-114">Additional resources</span></span>

[<span data-ttu-id="9bcfd-115">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
