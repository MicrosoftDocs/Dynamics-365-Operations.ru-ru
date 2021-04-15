---
title: Функция ER RIGHT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности RIGHT.
author: NickSelin
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746131"
---
# <a name="right-er-function"></a><span data-ttu-id="8e9bd-103">Функция ER RIGHT</span><span class="sxs-lookup"><span data-stu-id="8e9bd-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e9bd-104">Функция `RIGHT` возвращает *строковое* значение, которое представляет указанное число символов от конца указанной строки.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e9bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e9bd-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="8e9bd-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8e9bd-106">Arguments</span></span>

<span data-ttu-id="8e9bd-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="8e9bd-107">`text`: *String*</span></span>

<span data-ttu-id="8e9bd-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="8e9bd-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="8e9bd-109">`number`: *Integer*</span></span>

<span data-ttu-id="8e9bd-110">Количество символов, которые должны быть возвращены с конца исходного текста.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="8e9bd-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8e9bd-111">Return values</span></span>

<span data-ttu-id="8e9bd-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="8e9bd-112">*String*</span></span>

<span data-ttu-id="8e9bd-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8e9bd-114">Пример</span><span class="sxs-lookup"><span data-stu-id="8e9bd-114">Example</span></span>

<span data-ttu-id="8e9bd-115">`RIGHT ("Sample", 3)` возвращает **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e9bd-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8e9bd-116">Additional resources</span></span>

[<span data-ttu-id="8e9bd-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="8e9bd-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]