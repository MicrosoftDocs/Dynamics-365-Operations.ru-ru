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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041730"
---
# <span data-ttu-id="744cc-103"><a name="NOT">Функция ER NOT</a></span><span class="sxs-lookup"><span data-stu-id="744cc-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="744cc-104">Функция `NOT` возвращает обратное логическое значение указанного условия в качестве *логического* значения.</span><span class="sxs-lookup"><span data-stu-id="744cc-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="744cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="744cc-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="744cc-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="744cc-106">Arguments</span></span>

<span data-ttu-id="744cc-107">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="744cc-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="744cc-108">Действительное условное выражение, которое должно быть реверсировано.</span><span class="sxs-lookup"><span data-stu-id="744cc-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="744cc-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="744cc-109">Return values</span></span>

<span data-ttu-id="744cc-110">*Логический*</span><span class="sxs-lookup"><span data-stu-id="744cc-110">*Boolean*</span></span>

<span data-ttu-id="744cc-111">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="744cc-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="744cc-112">Пример</span><span class="sxs-lookup"><span data-stu-id="744cc-112">Example</span></span>

<span data-ttu-id="744cc-113">`NOT (TRUE)` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="744cc-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="744cc-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="744cc-114">Additional resources</span></span>

[<span data-ttu-id="744cc-115">Логические функции</span><span class="sxs-lookup"><span data-stu-id="744cc-115">Logical functions</span></span>](er-functions-category-logical.md)
