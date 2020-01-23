---
title: Список функций ER в категории преобразования типа
description: В этой теме содержится информация о функциях преобразования, которые поддерживаются в электронной отчетности (ER).
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
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917657"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="9af88-103">Список функций ER в категории преобразования типа</span><span class="sxs-lookup"><span data-stu-id="9af88-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9af88-104">Функции преобразования типа электронной отчетности (ER) могут использоваться для преобразования типов значений.</span><span class="sxs-lookup"><span data-stu-id="9af88-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="9af88-105">В этой теме приводится краткое изложение этих функций.</span><span class="sxs-lookup"><span data-stu-id="9af88-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="9af88-106">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="9af88-106">Type conversion functions</span></span>

| <span data-ttu-id="9af88-107">Функция</span><span class="sxs-lookup"><span data-stu-id="9af88-107">Function</span></span> | <span data-ttu-id="9af88-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9af88-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9af88-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="9af88-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="9af88-110">Эта функция возвращает значение *Int64*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="9af88-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="9af88-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="9af88-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="9af88-112">Эта функция возвращает значение *Int*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="9af88-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="9af88-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="9af88-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="9af88-114">Эта функция возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="9af88-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="9af88-115">При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.</span><span class="sxs-lookup"><span data-stu-id="9af88-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="9af88-116">Стоимость</span><span class="sxs-lookup"><span data-stu-id="9af88-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="9af88-117">Эта функция возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="9af88-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="9af88-118">Функции преобразования типа в категории даты и времени</span><span class="sxs-lookup"><span data-stu-id="9af88-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="9af88-119">В следующей таблице описаны функции преобразования типов в категории [Дата и время](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="9af88-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="9af88-120">Функция</span><span class="sxs-lookup"><span data-stu-id="9af88-120">Function</span></span> | <span data-ttu-id="9af88-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9af88-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9af88-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="9af88-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="9af88-123">Эта функция возвращает значение *DateTime*, которое преобразуется из *строкового* значения в указанном формате и в дополнительно указанной культуре в значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="9af88-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="9af88-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="9af88-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="9af88-125">Эта функция возвращает значение *DateTime*, которое преобразуется из заданного значения *Дата* в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="9af88-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="9af88-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="9af88-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="9af88-127">Эта функция возвращает значение *Дата*, которое преобразуется из *строкового* значения в указанном формате и в дополнительно указанной культуре в значение даты.</span><span class="sxs-lookup"><span data-stu-id="9af88-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="9af88-128">Функции преобразования типа в категории списков</span><span class="sxs-lookup"><span data-stu-id="9af88-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="9af88-129">В следующей таблице описаны функции преобразования типов в [категории списков](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="9af88-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="9af88-130">Функция</span><span class="sxs-lookup"><span data-stu-id="9af88-130">Function</span></span> | <span data-ttu-id="9af88-131">Описание</span><span class="sxs-lookup"><span data-stu-id="9af88-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9af88-132">Список</span><span class="sxs-lookup"><span data-stu-id="9af88-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="9af88-133">Эта функция возвращает значение *Список записей* в качестве нового списка, созданного из указанных аргументов типа *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="9af88-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="9af88-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="9af88-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="9af88-135">Эта функция возвращает значение *Список записей*, созданное на основе структуры указанного аргумента типа *Перечисление* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="9af88-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="9af88-136">Разбиение</span><span class="sxs-lookup"><span data-stu-id="9af88-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="9af88-137">Эта функция разделяет указанное *строковое* значение на подстроки и возвращает результат в виде нового значения *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="9af88-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="9af88-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="9af88-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="9af88-139">Эта функция возвращает значение *строка*, состоящее из связанных значений указанного поля из указанного значения *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="9af88-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="9af88-140">Значения могут разделяться указанным разделителем.</span><span class="sxs-lookup"><span data-stu-id="9af88-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="9af88-141">Функции преобразования типа в категории текста</span><span class="sxs-lookup"><span data-stu-id="9af88-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="9af88-142">В следующей таблице описаны функции преобразования типов в [категории текста](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="9af88-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="9af88-143">Функция</span><span class="sxs-lookup"><span data-stu-id="9af88-143">Function</span></span> | <span data-ttu-id="9af88-144">Описание</span><span class="sxs-lookup"><span data-stu-id="9af88-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9af88-145">Char</span><span class="sxs-lookup"><span data-stu-id="9af88-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="9af88-146">Эта функция возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.</span><span class="sxs-lookup"><span data-stu-id="9af88-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="9af88-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="9af88-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="9af88-148">Эта функция преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*.</span><span class="sxs-lookup"><span data-stu-id="9af88-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="9af88-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="9af88-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="9af88-150">Эта функция возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной культуре.</span><span class="sxs-lookup"><span data-stu-id="9af88-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="9af88-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="9af88-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="9af88-152">Эта функция возвращает значение *Контейнер*, которое представляет изображение Quick Response (QR) для указанной строки в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="9af88-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="9af88-153">Текст</span><span class="sxs-lookup"><span data-stu-id="9af88-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="9af88-154">Эта функция возвращает указанное число в качестве *строкового* значения, представляющее указанное число после его преобразования в текстовую строку, которая отформатирована в соответствии с параметрами языкового стандарта сервера текущего экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="9af88-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9af88-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9af88-155">Additional resources</span></span>

[<span data-ttu-id="9af88-156">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="9af88-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="9af88-157">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="9af88-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="9af88-158">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="9af88-158">Electronic reporting formula language</span></span>](er-formula-language.md)
