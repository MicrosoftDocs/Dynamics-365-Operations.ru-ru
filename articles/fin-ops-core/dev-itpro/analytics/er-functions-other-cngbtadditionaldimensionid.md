---
title: Функция ER CN_GBT_ADDITIONALDIMENSIONID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CN_GBT_ADDITIONALDIMENSIONID.
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744439"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="94a2f-103">Функция ER CN_GBT_ADDITIONALDIMENSIONID</span><span class="sxs-lookup"><span data-stu-id="94a2f-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94a2f-104">Функция `CN_GBT_ADDITIONALDIMENSIONID` возвращает *строковое* значение, представляющее один идентификатор финансовой аналитики, взятый из указанной строки.</span><span class="sxs-lookup"><span data-stu-id="94a2f-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="94a2f-105">Указанная строка представляет все аналитики в виде списка идентификаторов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="94a2f-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a2f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94a2f-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="94a2f-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="94a2f-107">Arguments</span></span>

<span data-ttu-id="94a2f-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="94a2f-108">`text`: *String*</span></span>

<span data-ttu-id="94a2f-109">Значение *строка* представляет все аналитики в виде списка идентификаторов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="94a2f-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="94a2f-110">`number`: Целочисленное</span><span class="sxs-lookup"><span data-stu-id="94a2f-110">`number`: Integer</span></span>

<span data-ttu-id="94a2f-111">*Целочисленное* значение определяет код серии запрошенной аналитики в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="94a2f-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="94a2f-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="94a2f-112">Return values</span></span>

<span data-ttu-id="94a2f-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="94a2f-113">*String*</span></span>

<span data-ttu-id="94a2f-114">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="94a2f-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="94a2f-115">Пример</span><span class="sxs-lookup"><span data-stu-id="94a2f-115">Example</span></span>

<span data-ttu-id="94a2f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` возвращает **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="94a2f-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94a2f-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="94a2f-117">Additional resources</span></span>

[<span data-ttu-id="94a2f-118">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="94a2f-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
