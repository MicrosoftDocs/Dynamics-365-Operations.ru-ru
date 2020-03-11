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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042627"
---
# <span data-ttu-id="56161-103"><a name="VALUE">Функция ER VALUE</a></span><span class="sxs-lookup"><span data-stu-id="56161-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56161-104">Функция `VALUE` возвращает *вещественное* значение, преобразованное из указанной строки.</span><span class="sxs-lookup"><span data-stu-id="56161-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="56161-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56161-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="56161-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="56161-106">Arguments</span></span>

<span data-ttu-id="56161-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="56161-107">`text`: *String*</span></span>

<span data-ttu-id="56161-108">Строковое значение, которое должно быть преобразовано в числовое значение.</span><span class="sxs-lookup"><span data-stu-id="56161-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="56161-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="56161-109">Return values</span></span>

<span data-ttu-id="56161-110">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="56161-110">*Real*</span></span>

<span data-ttu-id="56161-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="56161-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="56161-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="56161-112">Usage notes</span></span>

<span data-ttu-id="56161-113">Символы запятой и точки (.) считаются десятичными разделителями, и ведущий дефис (-) используются в качестве отрицательного знака.</span><span class="sxs-lookup"><span data-stu-id="56161-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="56161-114">Выдается исключение во время выполнения, если указанная строка содержит другие символы, не являющиеся цифрами.</span><span class="sxs-lookup"><span data-stu-id="56161-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="56161-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56161-115">Example 1</span></span>

<span data-ttu-id="56161-116">`VALUE ("1 234,56")` выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="56161-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="56161-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="56161-117">Example 2</span></span>

<span data-ttu-id="56161-118">`VALUE ("1234,56")` возвращает **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="56161-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56161-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56161-119">Additional resources</span></span>

[<span data-ttu-id="56161-120">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="56161-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
