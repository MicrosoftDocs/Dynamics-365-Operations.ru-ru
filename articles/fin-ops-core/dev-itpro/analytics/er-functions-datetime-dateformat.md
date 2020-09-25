---
title: Функция ER DATEFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATEFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 4e9347937d088f15b4f489f0b85704a8688f8131
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743311"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="998cd-103">Функция ER DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="998cd-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="998cd-104">Функция `DATEFORMAT` возвращает значение *строки*, которое представляет заданное значение даты в виде текста в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="998cd-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="998cd-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="998cd-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="998cd-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="998cd-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="998cd-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="998cd-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="998cd-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="998cd-108">Arguments</span></span>

<span data-ttu-id="998cd-109">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="998cd-109">`date`: *Date*</span></span>

<span data-ttu-id="998cd-110">Значение даты, представляющее дату для формата.</span><span class="sxs-lookup"><span data-stu-id="998cd-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="998cd-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="998cd-111">`format`: *String*</span></span>

<span data-ttu-id="998cd-112">Формат строки вывода.</span><span class="sxs-lookup"><span data-stu-id="998cd-112">The format of the output string.</span></span>

<span data-ttu-id="998cd-113">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="998cd-113">`culture`: *String*</span></span>

<span data-ttu-id="998cd-114">Культура для форматирования.</span><span class="sxs-lookup"><span data-stu-id="998cd-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="998cd-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="998cd-115">Return values</span></span>

<span data-ttu-id="998cd-116">*Строка*</span><span class="sxs-lookup"><span data-stu-id="998cd-116">*String*</span></span>

<span data-ttu-id="998cd-117">Результирующее значение строки.</span><span class="sxs-lookup"><span data-stu-id="998cd-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="998cd-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="998cd-118">Usage notes</span></span>

<span data-ttu-id="998cd-119">Когда культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова.</span><span class="sxs-lookup"><span data-stu-id="998cd-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="998cd-120">Например, если функция `DATEFORMAT` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры.</span><span class="sxs-lookup"><span data-stu-id="998cd-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="998cd-121">Значение шаблона `culture` по умолчанию — **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="998cd-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="998cd-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="998cd-122">Example 1</span></span>

<span data-ttu-id="998cd-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` возвращает текущую дату сервера приложений, 24 декабря 2015, как строку **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="998cd-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="998cd-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="998cd-124">Example 2</span></span>

<span data-ttu-id="998cd-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.</span><span class="sxs-lookup"><span data-stu-id="998cd-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="998cd-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="998cd-126">Additional resources</span></span>

[<span data-ttu-id="998cd-127">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="998cd-127">Date and time functions</span></span>](er-functions-category-datetime.md)
