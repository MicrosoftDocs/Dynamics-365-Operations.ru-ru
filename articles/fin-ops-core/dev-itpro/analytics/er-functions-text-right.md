---
title: Функция ER RIGHT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности RIGHT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040879"
---
# <span data-ttu-id="9d547-103"><a name="RIGHT">Функция ER RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="9d547-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d547-104">Функция `RIGHT` возвращает *строковое* значение, которое представляет указанное число символов от конца указанной строки.</span><span class="sxs-lookup"><span data-stu-id="9d547-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d547-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d547-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9d547-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9d547-106">Arguments</span></span>

<span data-ttu-id="9d547-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="9d547-107">`text`: *String*</span></span>

<span data-ttu-id="9d547-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="9d547-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9d547-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="9d547-109">`number`: *Integer*</span></span>

<span data-ttu-id="9d547-110">Количество символов, которые должны быть возвращены с конца исходного текста.</span><span class="sxs-lookup"><span data-stu-id="9d547-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d547-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9d547-111">Return values</span></span>

<span data-ttu-id="9d547-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9d547-112">*String*</span></span>

<span data-ttu-id="9d547-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="9d547-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9d547-114">Пример</span><span class="sxs-lookup"><span data-stu-id="9d547-114">Example</span></span>

<span data-ttu-id="9d547-115">`RIGHT ("Sample", 3)` возвращает **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="9d547-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d547-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9d547-116">Additional resources</span></span>

[<span data-ttu-id="9d547-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="9d547-117">Text functions</span></span>](er-functions-category-text.md)
