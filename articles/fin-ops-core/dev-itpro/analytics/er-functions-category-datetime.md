---
title: Список функций ER в категории даты и времени
description: В этой теме содержится информация о функциях даты и времени, которые поддерживаются в электронной отчетности (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2745298ae1f6787c3de5a4aaf6a2a6350f5f3e85
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686227"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="31810-103">Список функций ER в категории даты и времени</span><span class="sxs-lookup"><span data-stu-id="31810-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31810-104">Функции даты и времени электронной отчетности (ER) могут использоваться для извлечения информации из значений даты и времени, а также для выполнения операций с ними.</span><span class="sxs-lookup"><span data-stu-id="31810-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="31810-105">В этой теме приводится краткое изложение этих функций.</span><span class="sxs-lookup"><span data-stu-id="31810-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="31810-106">Список поддерживаемых функций</span><span class="sxs-lookup"><span data-stu-id="31810-106">List of supported functions</span></span>

| <span data-ttu-id="31810-107">Функция</span><span class="sxs-lookup"><span data-stu-id="31810-107">Function</span></span> | <span data-ttu-id="31810-108">Описание</span><span class="sxs-lookup"><span data-stu-id="31810-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="31810-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="31810-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="31810-110">Эта функция возвращает значение *DateTime*, которое является указанным числом дней до или после указанной даты начала.</span><span class="sxs-lookup"><span data-stu-id="31810-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="31810-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="31810-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="31810-112">Эта функция возвращает значение *строки*, которое представляет заданное значение даты в виде текста в указанном формате и в дополнительно указанной культуре.</span><span class="sxs-lookup"><span data-stu-id="31810-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="31810-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="31810-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="31810-114">Эта функция возвращает значение *строки*, которое представляет заданное значение даты/времени в виде текста в указанном формате и в дополнительно указанной культуре.</span><span class="sxs-lookup"><span data-stu-id="31810-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="31810-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="31810-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="31810-116">Эта функция возвращает значение *DateTime*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной культуре в значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="31810-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="31810-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="31810-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="31810-118">Эта функция возвращает значение *DateTime*, которое преобразуется из заданного значения даты в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="31810-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="31810-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="31810-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="31810-120">Эта функция возвращает значение *Date*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной культуре в значение даты.</span><span class="sxs-lookup"><span data-stu-id="31810-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="31810-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="31810-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="31810-122">Эта функция возвращает *целочисленное* значение числа дней между 1 января и указанной датой.</span><span class="sxs-lookup"><span data-stu-id="31810-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="31810-123">Дни</span><span class="sxs-lookup"><span data-stu-id="31810-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="31810-124">Эта функция возвращает *целочисленное* значение числа дней между одной указанной датой и второй указанной датой.</span><span class="sxs-lookup"><span data-stu-id="31810-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="31810-125">Now</span><span class="sxs-lookup"><span data-stu-id="31810-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="31810-126">Эта функция возвращает значение *DateTime*, которое представляет текущую дату и время сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="31810-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="31810-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="31810-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="31810-128">Эта функция возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года).</span><span class="sxs-lookup"><span data-stu-id="31810-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="31810-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="31810-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="31810-130">Эта функция возвращает значение *DateTime*, которое представляет значение **нулевой** даты/времени (1 января 1900 года) в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="31810-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="31810-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="31810-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="31810-132">Эта функция возвращает значение *DateTime*, которое представляет текущую дату и время сеанса приложения.</span><span class="sxs-lookup"><span data-stu-id="31810-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="31810-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="31810-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="31810-134">Эта функция возвращает значение *Date*, которое представляет текущую дату сеанса приложения.</span><span class="sxs-lookup"><span data-stu-id="31810-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="31810-135">Сегодня</span><span class="sxs-lookup"><span data-stu-id="31810-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="31810-136">Эта функция возвращает значение *Date*, которое представляет текущую дату сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="31810-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="31810-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="31810-137">Additional resources</span></span>

[<span data-ttu-id="31810-138">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="31810-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="31810-139">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="31810-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="31810-140">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="31810-140">Electronic reporting formula language</span></span>](er-formula-language.md)
