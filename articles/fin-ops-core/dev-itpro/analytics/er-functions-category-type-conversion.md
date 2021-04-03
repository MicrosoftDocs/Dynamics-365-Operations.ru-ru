---
title: Список функций ER в категории преобразования типа
description: В этой теме содержится информация о функциях преобразования, которые поддерживаются в электронной отчетности (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561526"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="ee4d0-103">Список функций ER в категории преобразования типа</span><span class="sxs-lookup"><span data-stu-id="ee4d0-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee4d0-104">Функции преобразования типа электронной отчетности (ER) могут использоваться для преобразования типов значений.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="ee4d0-105">В этой теме приводится краткое изложение этих функций.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="ee4d0-106">Функции преобразования типов</span><span class="sxs-lookup"><span data-stu-id="ee4d0-106">Type conversion functions</span></span>

| <span data-ttu-id="ee4d0-107">Функция</span><span class="sxs-lookup"><span data-stu-id="ee4d0-107">Function</span></span> | <span data-ttu-id="ee4d0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ee4d0-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee4d0-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="ee4d0-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="ee4d0-110">Эта функция возвращает значение *Int64*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="ee4d0-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="ee4d0-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="ee4d0-112">Эта функция возвращает значение *Int*, представляющее указанную строку.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="ee4d0-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="ee4d0-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="ee4d0-114">Эта функция возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="ee4d0-115">При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="ee4d0-116">Стоимость</span><span class="sxs-lookup"><span data-stu-id="ee4d0-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="ee4d0-117">Эта функция возвращает *вещественное* значение, преобразованное из указанного *строкового* значения.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="ee4d0-118">Функции преобразования типа в категории контейнеров</span><span class="sxs-lookup"><span data-stu-id="ee4d0-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="ee4d0-119">В следующей таблице описаны функции преобразования типов в категории [контейнеров](er-functions-category-container.md).</span><span class="sxs-lookup"><span data-stu-id="ee4d0-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="ee4d0-120">Функция</span><span class="sxs-lookup"><span data-stu-id="ee4d0-120">Function</span></span> | <span data-ttu-id="ee4d0-121">описание</span><span class="sxs-lookup"><span data-stu-id="ee4d0-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee4d0-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="ee4d0-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="ee4d0-123">Эта функция преобразует заданный ввод типа *Строка* в элемент данных типа *Контейнер*.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="ee4d0-124">Функции преобразования типа в категории даты и времени</span><span class="sxs-lookup"><span data-stu-id="ee4d0-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="ee4d0-125">В следующей таблице описаны функции преобразования типов в категории [Дата и время](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="ee4d0-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="ee4d0-126">Функция</span><span class="sxs-lookup"><span data-stu-id="ee4d0-126">Function</span></span> | <span data-ttu-id="ee4d0-127">Описание</span><span class="sxs-lookup"><span data-stu-id="ee4d0-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee4d0-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ee4d0-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="ee4d0-129">Эта функция возвращает значение *DateTime*, которое преобразуется из *строкового* значения в указанном формате и в дополнительно указанной культуре в значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="ee4d0-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="ee4d0-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="ee4d0-131">Эта функция возвращает значение *DateTime*, которое преобразуется из заданного значения *Дата* в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="ee4d0-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="ee4d0-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="ee4d0-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="ee4d0-133">Эта функция возвращает значение *Дата*, которое преобразуется из *строкового* значения в указанном формате и в дополнительно указанной культуре в значение даты.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="ee4d0-134">Функции преобразования типа в категории списков</span><span class="sxs-lookup"><span data-stu-id="ee4d0-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="ee4d0-135">В следующей таблице описаны функции преобразования типов в [категории списков](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="ee4d0-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="ee4d0-136">Функция</span><span class="sxs-lookup"><span data-stu-id="ee4d0-136">Function</span></span> | <span data-ttu-id="ee4d0-137">Описание</span><span class="sxs-lookup"><span data-stu-id="ee4d0-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee4d0-138">Список</span><span class="sxs-lookup"><span data-stu-id="ee4d0-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="ee4d0-139">Эта функция возвращает значение *Список записей* в качестве нового списка, созданного из указанных аргументов типа *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="ee4d0-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="ee4d0-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="ee4d0-141">Эта функция возвращает значение *Список записей*, созданное на основе структуры указанного аргумента типа *Перечисление* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="ee4d0-142">Разбиение</span><span class="sxs-lookup"><span data-stu-id="ee4d0-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="ee4d0-143">Эта функция разделяет указанное *строковое* значение на подстроки и возвращает результат в виде нового значения *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="ee4d0-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="ee4d0-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="ee4d0-145">Эта функция возвращает значение *строка*, состоящее из связанных значений указанного поля из указанного значения *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="ee4d0-146">Значения могут разделяться указанным разделителем.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="ee4d0-147">Функции преобразования типа в категории текста</span><span class="sxs-lookup"><span data-stu-id="ee4d0-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="ee4d0-148">В следующей таблице описаны функции преобразования типов в [категории текста](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="ee4d0-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="ee4d0-149">Функция</span><span class="sxs-lookup"><span data-stu-id="ee4d0-149">Function</span></span> | <span data-ttu-id="ee4d0-150">Описание</span><span class="sxs-lookup"><span data-stu-id="ee4d0-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee4d0-151">Char</span><span class="sxs-lookup"><span data-stu-id="ee4d0-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="ee4d0-152">Эта функция возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="ee4d0-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="ee4d0-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="ee4d0-154">Эта функция преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="ee4d0-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="ee4d0-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="ee4d0-156">Эта функция возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной культуре.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ee4d0-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="ee4d0-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="ee4d0-158">Эта функция возвращает значение *Контейнер*, которое представляет изображение Quick Response (QR) для указанной строки в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="ee4d0-159">Текст</span><span class="sxs-lookup"><span data-stu-id="ee4d0-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="ee4d0-160">Эта функция возвращает указанное число в качестве *строкового* значения, представляющее указанное число после его преобразования в текстовую строку, которая отформатирована в соответствии с параметрами языкового стандарта сервера текущего экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="ee4d0-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ee4d0-161">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ee4d0-161">Additional resources</span></span>

[<span data-ttu-id="ee4d0-162">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="ee4d0-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ee4d0-163">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="ee4d0-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ee4d0-164">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="ee4d0-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]