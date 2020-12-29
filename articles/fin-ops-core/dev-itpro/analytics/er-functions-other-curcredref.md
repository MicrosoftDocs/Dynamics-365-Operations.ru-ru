---
title: Функция ER CURCREDREF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CURCREDREF.
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
ms.openlocfilehash: 3923126060963122634d90c2ba8a380f534e9178
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686770"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="9563f-103">Функция ER CURCREDREF</span><span class="sxs-lookup"><span data-stu-id="9563f-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9563f-104">Функция `CURCREDREF` возвращает *строковое* значение, представляющее ссылку кредитора на основе цифр указанного номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="9563f-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9563f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9563f-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="9563f-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9563f-106">Arguments</span></span>

<span data-ttu-id="9563f-107">`invoice number digits`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="9563f-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="9563f-108">Текстовое значение, представляющее цифры номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="9563f-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="9563f-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9563f-109">Return values</span></span>

<span data-ttu-id="9563f-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9563f-110">*String*</span></span>

<span data-ttu-id="9563f-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="9563f-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9563f-112">Пример</span><span class="sxs-lookup"><span data-stu-id="9563f-112">Example</span></span>

<span data-ttu-id="9563f-113">`CURCredRef ("VEND-200002")` возвращает **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="9563f-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9563f-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9563f-114">Additional resources</span></span>

[<span data-ttu-id="9563f-115">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="9563f-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
