---
title: Функция ER DATETIMEFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATETIMEFORMAT.
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
ms.openlocfilehash: 65b988e6c58aed35577288e01157b8c1f76e6efd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744871"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="c0d7c-103">Функция ER DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="c0d7c-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0d7c-104">Функция `DATETIMEFORMAT` возвращает значение *строки*, которое представляет заданное значение даты/времени в виде текста в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="c0d7c-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="c0d7c-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="c0d7c-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c0d7c-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="c0d7c-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="c0d7c-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="c0d7c-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="c0d7c-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c0d7c-108">Arguments</span></span>

<span data-ttu-id="c0d7c-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="c0d7c-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="c0d7c-110">Значение даты/времени, представляющее дату и время для формата.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="c0d7c-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c0d7c-111">`format`: *String*</span></span>

<span data-ttu-id="c0d7c-112">Формат строки вывода.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-112">The format of the output string.</span></span>

<span data-ttu-id="c0d7c-113">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c0d7c-113">`culture`: *String*</span></span>

<span data-ttu-id="c0d7c-114">Культура для форматирования.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0d7c-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c0d7c-115">Return values</span></span>

<span data-ttu-id="c0d7c-116">*Строка*</span><span class="sxs-lookup"><span data-stu-id="c0d7c-116">*String*</span></span>

<span data-ttu-id="c0d7c-117">Результирующее значение строки.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c0d7c-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="c0d7c-118">Usage notes</span></span>

<span data-ttu-id="c0d7c-119">Когда культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="c0d7c-120">Например, если функция `DATETIMEFORMAT` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="c0d7c-121">Значение шаблона `culture` по умолчанию — **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="c0d7c-122">Когда функция `DATETIMEFORMAT` преобразует заданное значение даты/времени, она учитывает настройки часового пояса пользователя приложения, который использует формат ER, в контексте которого вызывается функция.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0d7c-123">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0d7c-123">Example 1</span></span>

<span data-ttu-id="c0d7c-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` возвращает текущую дату/время сервера приложений, 24 декабря 2015, как **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0d7c-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0d7c-125">Example 2</span></span>

<span data-ttu-id="c0d7c-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` возвращает значение текущей даты/времени сеанса приложения, 24 декабря 2015 года, как строку **"24.12.2015"** на основе выбранной немецкой культуры и указанного формата.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="c0d7c-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c0d7c-127">Example 3</span></span>

<span data-ttu-id="c0d7c-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` возвращает значение строки **2019-11-12T08:00:00.0000000-08:00**, когда оно называется во время процесса, инициированного пользователем приложения со значением часового пояса **(GMT-08:00), Тихоокеанское время (США и Канада)** в разделе **Настройки языка и страны/региона**.</span><span class="sxs-lookup"><span data-stu-id="c0d7c-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0d7c-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c0d7c-129">Additional resources</span></span>

[<span data-ttu-id="c0d7c-130">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="c0d7c-130">Date and time functions</span></span>](er-functions-category-datetime.md)
