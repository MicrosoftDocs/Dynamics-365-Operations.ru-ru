---
title: Функция ER DATEFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATEFORMAT.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: cdc1671f818bc2c4d8a78d0a35337298e83c5060
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/04/2021
ms.locfileid: "4826019"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="f8750-103">Функция ER DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="f8750-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8750-104">Функция `DATEFORMAT` возвращает значение *строки*, которое представляет заданное значение даты в виде текста в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="f8750-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="f8750-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="f8750-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f8750-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="f8750-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="f8750-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="f8750-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="f8750-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="f8750-108">Arguments</span></span>

<span data-ttu-id="f8750-109">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="f8750-109">`date`: *Date*</span></span>

<span data-ttu-id="f8750-110">Значение даты, представляющее дату для формата.</span><span class="sxs-lookup"><span data-stu-id="f8750-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="f8750-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="f8750-111">`format`: *String*</span></span>

<span data-ttu-id="f8750-112">Формат строки вывода.</span><span class="sxs-lookup"><span data-stu-id="f8750-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="f8750-113">В строке форматирования учитывается регистр при использовании стандартного или пользовательского формата.</span><span class="sxs-lookup"><span data-stu-id="f8750-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="f8750-114">Например, [стандартный](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) спецификатор формата "d" возвращает дату, используя короткий шаблон даты, в то время как стандартный спецификатор формата "D" возвращает дату, используя полный шаблон даты.</span><span class="sxs-lookup"><span data-stu-id="f8750-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="f8750-115">Кроме того, [пользовательский](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) спецификатор формата "M" возвращает месяц от 1 до 12, в то время как пользовательский спецификатор формата "m" возвращает минуты от 0 до 59.</span><span class="sxs-lookup"><span data-stu-id="f8750-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="f8750-116">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="f8750-116">`culture`: *String*</span></span>

<span data-ttu-id="f8750-117">Культура для форматирования.</span><span class="sxs-lookup"><span data-stu-id="f8750-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8750-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f8750-118">Return values</span></span>

<span data-ttu-id="f8750-119">*Строка*</span><span class="sxs-lookup"><span data-stu-id="f8750-119">*String*</span></span>

<span data-ttu-id="f8750-120">Результирующее значение строки.</span><span class="sxs-lookup"><span data-stu-id="f8750-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f8750-121">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="f8750-121">Usage notes</span></span>

<span data-ttu-id="f8750-122">Если культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова.</span><span class="sxs-lookup"><span data-stu-id="f8750-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="f8750-123">Например, если функция `DATEFORMAT` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры.</span><span class="sxs-lookup"><span data-stu-id="f8750-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="f8750-124">Значение шаблона `culture` по умолчанию — **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="f8750-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="f8750-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8750-125">Example 1</span></span>

<span data-ttu-id="f8750-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` возвращает текущую дату сервера приложений, 24 декабря 2015, как строку **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="f8750-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="f8750-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f8750-127">Example 2</span></span>

<span data-ttu-id="f8750-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.</span><span class="sxs-lookup"><span data-stu-id="f8750-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8750-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8750-129">Additional resources</span></span>

[<span data-ttu-id="f8750-130">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="f8750-130">Date and time functions</span></span>](er-functions-category-datetime.md)
