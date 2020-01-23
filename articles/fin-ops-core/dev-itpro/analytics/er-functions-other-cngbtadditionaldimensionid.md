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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917036"
---
# <span data-ttu-id="5bfdb-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">Функция ER CN_GBT_ADDITIONALDIMENSIONID</a></span><span class="sxs-lookup"><span data-stu-id="5bfdb-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bfdb-104">Функция `CN_GBT_ADDITIONALDIMENSIONID` возвращает *строковое* значение, представляющее один идентификатор финансовой аналитики, взятый из указанной строки.</span><span class="sxs-lookup"><span data-stu-id="5bfdb-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="5bfdb-105">Указанная строка представляет все аналитики в виде списка идентификаторов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="5bfdb-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bfdb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bfdb-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5bfdb-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="5bfdb-107">Arguments</span></span>

<span data-ttu-id="5bfdb-108">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="5bfdb-108">`text`: *String*</span></span>

<span data-ttu-id="5bfdb-109">Значение *строка* представляет все аналитики в виде списка идентификаторов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="5bfdb-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="5bfdb-110">`number`: Целочисленное</span><span class="sxs-lookup"><span data-stu-id="5bfdb-110">`number`: Integer</span></span>

<span data-ttu-id="5bfdb-111">*Целочисленное* значение определяет код серии запрошенной аналитики в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="5bfdb-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="5bfdb-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5bfdb-112">Return values</span></span>

<span data-ttu-id="5bfdb-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="5bfdb-113">*String*</span></span>

<span data-ttu-id="5bfdb-114">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="5bfdb-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5bfdb-115">Пример</span><span class="sxs-lookup"><span data-stu-id="5bfdb-115">Example</span></span>

<span data-ttu-id="5bfdb-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` возвращает **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="5bfdb-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bfdb-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bfdb-117">Additional resources</span></span>

[<span data-ttu-id="5bfdb-118">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="5bfdb-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
