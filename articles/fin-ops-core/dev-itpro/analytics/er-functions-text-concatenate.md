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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04c7b32e2a9578f8864570a552817ec3ce28fa43
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041194"
---
# <span data-ttu-id="2f7f8-103"><a name="CONCATENATE">Функция ER CONCATENATE</a></span><span class="sxs-lookup"><span data-stu-id="2f7f8-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f7f8-104">Функция `CONCATENATE` возвращает все указанные строки текста как значение *Строка* после того, как они были объединены в одну строку.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f7f8-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="2f7f8-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2f7f8-106">Arguments</span></span>

<span data-ttu-id="2f7f8-107">`text 1`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2f7f8-107">`text 1`: *String*</span></span>

<span data-ttu-id="2f7f8-108">Ссылка на источник данных типа данных *Строка*.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="2f7f8-109">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-109">This argument is required.</span></span>

<span data-ttu-id="2f7f8-110">`text N`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2f7f8-110">`text N`: *String*</span></span>

<span data-ttu-id="2f7f8-111">Ссылка на источник данных типа данных *Строка*.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="2f7f8-112">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2f7f8-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2f7f8-113">Return values</span></span>

<span data-ttu-id="2f7f8-114">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2f7f8-114">*String*</span></span>

<span data-ttu-id="2f7f8-115">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2f7f8-116">Пример</span><span class="sxs-lookup"><span data-stu-id="2f7f8-116">Example</span></span>

<span data-ttu-id="2f7f8-117">`CONCATENATE ("abc", "def")` возвращает **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2f7f8-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="2f7f8-118">Usage notes</span></span>

<span data-ttu-id="2f7f8-119">Выражение `"abc" & "def"` также возвращает **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="2f7f8-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f7f8-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2f7f8-120">Additional resources</span></span>

[<span data-ttu-id="2f7f8-121">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="2f7f8-121">Text functions</span></span>](er-functions-category-text.md)
