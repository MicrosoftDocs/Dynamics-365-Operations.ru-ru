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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916737"
---
# <span data-ttu-id="c25a6-103"><a name="RIGHT">Функция ER RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="c25a6-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c25a6-104">Функция `RIGHT` возвращает *строковое* значение, которое представляет указанное число символов от конца указанной строки.</span><span class="sxs-lookup"><span data-stu-id="c25a6-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c25a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c25a6-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c25a6-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c25a6-106">Arguments</span></span>

<span data-ttu-id="c25a6-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c25a6-107">`text`: *String*</span></span>

<span data-ttu-id="c25a6-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="c25a6-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="c25a6-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="c25a6-109">`number`: *Integer*</span></span>

<span data-ttu-id="c25a6-110">Количество символов, которые должны быть возвращены с конца исходного текста.</span><span class="sxs-lookup"><span data-stu-id="c25a6-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="c25a6-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c25a6-111">Return values</span></span>

<span data-ttu-id="c25a6-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="c25a6-112">*String*</span></span>

<span data-ttu-id="c25a6-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="c25a6-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c25a6-114">Пример</span><span class="sxs-lookup"><span data-stu-id="c25a6-114">Example</span></span>

<span data-ttu-id="c25a6-115">`RIGHT ("Sample", 3)` возвращает **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="c25a6-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c25a6-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c25a6-116">Additional resources</span></span>

[<span data-ttu-id="c25a6-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="c25a6-117">Text functions</span></span>](er-functions-category-text.md)
