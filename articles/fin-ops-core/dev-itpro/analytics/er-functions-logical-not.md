---
title: Функция ER NOT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NOT.
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916047"
---
# <span data-ttu-id="09211-103"><a name="NOT">Функция ER NOT</a></span><span class="sxs-lookup"><span data-stu-id="09211-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09211-104">Функция `NOT` возвращает обратное логическое значение указанного условия в качестве *логического* значения.</span><span class="sxs-lookup"><span data-stu-id="09211-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="09211-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09211-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="09211-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="09211-106">Arguments</span></span>

<span data-ttu-id="09211-107">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="09211-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="09211-108">Действительное условное выражение, которое должно быть реверсировано.</span><span class="sxs-lookup"><span data-stu-id="09211-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="09211-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="09211-109">Return values</span></span>

<span data-ttu-id="09211-110">*Логический*</span><span class="sxs-lookup"><span data-stu-id="09211-110">*Boolean*</span></span>

<span data-ttu-id="09211-111">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="09211-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="09211-112">Пример</span><span class="sxs-lookup"><span data-stu-id="09211-112">Example</span></span>

<span data-ttu-id="09211-113">`NOT (TRUE)` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="09211-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09211-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="09211-114">Additional resources</span></span>

[<span data-ttu-id="09211-115">Логические функции</span><span class="sxs-lookup"><span data-stu-id="09211-115">Logical functions</span></span>](er-functions-category-logical.md)
