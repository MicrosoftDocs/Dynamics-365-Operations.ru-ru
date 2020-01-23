---
title: Функция ER VALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917634"
---
# <span data-ttu-id="5a18c-103"><a name="VALUE">Функция ER VALUE</a></span><span class="sxs-lookup"><span data-stu-id="5a18c-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a18c-104">Функция `VALUE` возвращает *вещественное* значение, преобразованное из указанной строки.</span><span class="sxs-lookup"><span data-stu-id="5a18c-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a18c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a18c-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="5a18c-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="5a18c-106">Arguments</span></span>

<span data-ttu-id="5a18c-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="5a18c-107">`text`: *String*</span></span>

<span data-ttu-id="5a18c-108">Строковое значение, которое должно быть преобразовано в числовое значение.</span><span class="sxs-lookup"><span data-stu-id="5a18c-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="5a18c-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5a18c-109">Return values</span></span>

<span data-ttu-id="5a18c-110">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="5a18c-110">*Real*</span></span>

<span data-ttu-id="5a18c-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="5a18c-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5a18c-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="5a18c-112">Usage notes</span></span>

<span data-ttu-id="5a18c-113">Символы запятой и точки (.) считаются десятичными разделителями, и ведущий дефис (-) используются в качестве отрицательного знака.</span><span class="sxs-lookup"><span data-stu-id="5a18c-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="5a18c-114">Выдается исключение во время выполнения, если указанная строка содержит другие символы, не являющиеся цифрами.</span><span class="sxs-lookup"><span data-stu-id="5a18c-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="5a18c-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a18c-115">Example 1</span></span>

<span data-ttu-id="5a18c-116">`VALUE ("1 234,56")` выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="5a18c-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="5a18c-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a18c-117">Example 2</span></span>

<span data-ttu-id="5a18c-118">`VALUE ("1234,56")` возвращает **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="5a18c-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a18c-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a18c-119">Additional resources</span></span>

[<span data-ttu-id="5a18c-120">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="5a18c-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
