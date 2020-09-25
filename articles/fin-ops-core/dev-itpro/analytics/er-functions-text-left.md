---
title: Функция ER LEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LEFT
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743791"
---
# <a name="left-er-function"></a><span data-ttu-id="17e88-103">Функция ER LEFT</span><span class="sxs-lookup"><span data-stu-id="17e88-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17e88-104">Функция `LEFT` возвращает *строковое* значение, которое представляет указанное число символов от начала указанной строки.</span><span class="sxs-lookup"><span data-stu-id="17e88-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17e88-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="17e88-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="17e88-106">Arguments</span></span>

<span data-ttu-id="17e88-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="17e88-107">`text`: *String*</span></span>

<span data-ttu-id="17e88-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="17e88-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="17e88-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="17e88-109">`number`: *Integer*</span></span>

<span data-ttu-id="17e88-110">Количество символов, которые должны быть возвращены с начала исходного текста.</span><span class="sxs-lookup"><span data-stu-id="17e88-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="17e88-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="17e88-111">Return values</span></span>

<span data-ttu-id="17e88-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="17e88-112">*String*</span></span>

<span data-ttu-id="17e88-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="17e88-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="17e88-114">Пример</span><span class="sxs-lookup"><span data-stu-id="17e88-114">Example</span></span>

<span data-ttu-id="17e88-115">`LEFT ("Sample", 3)` возвращает **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="17e88-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17e88-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="17e88-116">Additional resources</span></span>

[<span data-ttu-id="17e88-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="17e88-117">Text functions</span></span>](er-functions-category-text.md)
