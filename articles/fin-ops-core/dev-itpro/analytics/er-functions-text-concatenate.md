---
title: Функция ER CONCATENATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CONCATENATE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687946"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="b3ebc-103">Функция ER CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="b3ebc-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3ebc-104">Функция `CONCATENATE` возвращает все указанные строки текста как значение *Строка* после того, как они были объединены в одну строку.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ebc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3ebc-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="b3ebc-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b3ebc-106">Arguments</span></span>

<span data-ttu-id="b3ebc-107">`text 1`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b3ebc-107">`text 1`: *String*</span></span>

<span data-ttu-id="b3ebc-108">Ссылка на источник данных типа данных *Строка*.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="b3ebc-109">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-109">This argument is required.</span></span>

<span data-ttu-id="b3ebc-110">`text N`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b3ebc-110">`text N`: *String*</span></span>

<span data-ttu-id="b3ebc-111">Ссылка на источник данных типа данных *Строка*.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="b3ebc-112">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3ebc-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b3ebc-113">Return values</span></span>

<span data-ttu-id="b3ebc-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="b3ebc-114">*String*</span></span>

<span data-ttu-id="b3ebc-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b3ebc-116">Пример</span><span class="sxs-lookup"><span data-stu-id="b3ebc-116">Example</span></span>

<span data-ttu-id="b3ebc-117">`CONCATENATE ("abc", "def")` возвращает **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b3ebc-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="b3ebc-118">Usage notes</span></span>

<span data-ttu-id="b3ebc-119">Выражение `"abc" & "def"` также возвращает **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="b3ebc-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3ebc-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b3ebc-120">Additional resources</span></span>

[<span data-ttu-id="b3ebc-121">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="b3ebc-121">Text functions</span></span>](er-functions-category-text.md)
