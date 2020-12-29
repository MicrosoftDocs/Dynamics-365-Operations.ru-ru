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
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Список функций ER в категории даты и времени

[!include [banner](../includes/banner.md)]

Функции даты и времени электронной отчетности (ER) могут использоваться для извлечения информации из значений даты и времени, а также для выполнения операций с ними. В этой теме приводится краткое изложение этих функций.

## <a name="list-of-supported-functions"></a>Список поддерживаемых функций

| Функция | Описание |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Эта функция возвращает значение *DateTime*, которое является указанным числом дней до или после указанной даты начала. |
| [DateFormat](er-functions-datetime-dateformat.md) | Эта функция возвращает значение *строки*, которое представляет заданное значение даты в виде текста в указанном формате и в дополнительно указанной культуре. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Эта функция возвращает значение *строки*, которое представляет заданное значение даты/времени в виде текста в указанном формате и в дополнительно указанной культуре. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Эта функция возвращает значение *DateTime*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной культуре в значение даты/времени. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Эта функция возвращает значение *DateTime*, которое преобразуется из заданного значения даты в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Эта функция возвращает значение *Date*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной культуре в значение даты. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Эта функция возвращает *целочисленное* значение числа дней между 1 января и указанной датой. |
| [Дни](er-functions-datetime-days.md) | Эта функция возвращает *целочисленное* значение числа дней между одной указанной датой и второй указанной датой. |
| [Now](er-functions-datetime-now.md) | Эта функция возвращает значение *DateTime*, которое представляет текущую дату и время сервера приложения. |
| [NullDate](er-functions-datetime-nulldate.md) | Эта функция возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Эта функция возвращает значение *DateTime*, которое представляет значение **нулевой** даты/времени (1 января 1900 года) в формате UTC. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Эта функция возвращает значение *DateTime*, которое представляет текущую дату и время сеанса приложения. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Эта функция возвращает значение *Date*, которое представляет текущую дату сеанса приложения. |
| [Сегодня](er-functions-datetime-today.md) | Эта функция возвращает значение *Date*, которое представляет текущую дату сервера приложения. |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности](general-electronic-reporting.md)

[Конструктор формул в электронной отчетности](general-electronic-reporting-formula-designer.md)

[Язык формул электронной отчетности](er-formula-language.md)
