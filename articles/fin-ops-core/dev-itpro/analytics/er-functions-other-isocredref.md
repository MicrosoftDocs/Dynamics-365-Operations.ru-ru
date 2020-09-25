---
title: Функция ER ISOCREDREF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISOCREDREF.
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744103"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="85295-103">Функция ER ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="85295-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85295-104">Функция `ISOCREDREF` возвращает *строковое* значение, представляющее ссылку кредитора международной организации по стандартизации (ISO) на основе цифр и алфавитных символов определенного номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="85295-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="85295-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85295-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="85295-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="85295-106">Arguments</span></span>

<span data-ttu-id="85295-107">`invoice number digits`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="85295-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="85295-108">Текстовое значение, представляющее цифры номера счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="85295-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="85295-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="85295-109">Return values</span></span>

<span data-ttu-id="85295-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="85295-110">*String*</span></span>

<span data-ttu-id="85295-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="85295-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="85295-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="85295-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="85295-113">Чтобы исключить символы из алфавитов, не совместимых с ISO, аргумент `invoice number digits` необходимо перевести до передачи к этой функции.</span><span class="sxs-lookup"><span data-stu-id="85295-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="85295-114">Пример</span><span class="sxs-lookup"><span data-stu-id="85295-114">Example</span></span>

<span data-ttu-id="85295-115">`ISOCredRef ("VEND-200002")` возвращает **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="85295-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85295-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="85295-116">Additional resources</span></span>

[<span data-ttu-id="85295-117">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="85295-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
