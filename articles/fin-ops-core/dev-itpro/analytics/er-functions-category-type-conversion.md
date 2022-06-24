---
title: Список функций ER в категории преобразования типа
description: В этой статье содержится информация о функциях преобразования, которые поддерживаются в электронной отчетности (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37516ced402e0204ebd09d5b175ff56b040b9043
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889324"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Список функций ER в категории преобразования типа

[!include [banner](../includes/banner.md)]

Функции преобразования типа электронной отчетности (ER) могут использоваться для преобразования типов значений. В данной статье приводится краткое описание этих функций.

## <a name="type-conversion-functions"></a>Функции преобразования типов

| Функция | Описание |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Эта функция возвращает значение *Int64*, представляющее указанную строку. |
| [IntValue](er-functions-conversion-intvalue.md)       | Эта функция возвращает значение *Int*, представляющее указанную строку. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Эта функция возвращает *вещественное* значение, преобразованное из указанного *строкового* значения. При преобразовании учитываются указанные десятичные разделители и разделители групп цифр. |
| [Стоимость](er-functions-conversion-value.md)             | Эта функция возвращает *вещественное* значение, преобразованное из указанного *строкового* значения. |

## <a name="type-conversion-functions-in-the-container-category"></a>Функции преобразования типа в категории контейнеров

В следующей таблице описаны функции преобразования типов в категории [контейнеров](er-functions-category-container.md).

| Функция | описание |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Эта функция преобразует заданный ввод типа *Строка* в элемент данных типа *Контейнер*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Функции преобразования типа в категории даты и времени

В следующей таблице описаны функции преобразования типов в категории [Дата и время](er-functions-category-datetime.md).

| Функция | Описание |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Эта функция возвращает значение *DateTime*, которое преобразуется из *строкового* значения в указанном формате и в дополнительно указанной культуре в значение даты/времени. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Эта функция возвращает значение *DateTime*, которое преобразуется из заданного значения *Дата* в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Эта функция возвращает значение *Дата*, которое преобразуется из *строкового* значения в указанном формате и в дополнительно указанной культуре в значение даты. |

## <a name="type-conversion-functions-in-the-list-category"></a>Функции преобразования типа в категории списков

В следующей таблице описаны функции преобразования типов в [категории списков](er-functions-category-list.md).

| Функция | Описание |
|----------|-------------|
| [Список](er-functions-list-list.md)                 | Эта функция возвращает значение *Список записей* в качестве нового списка, созданного из указанных аргументов типа *Контейнер (запись)*. |
| [ListOfFields](er-functions-list-listoffields.md) | Эта функция возвращает значение *Список записей*, созданное на основе структуры указанного аргумента типа *Перечисление* или *Контейнер (запись)*. |
| [Разбиение](er-functions-list-split.md)               | Эта функция разделяет указанное *строковое* значение на подстроки и возвращает результат в виде нового значения *Список записей*. |
| [StringJoin](er-functions-list-stringjoin.md)     | Эта функция возвращает значение *строка*, состоящее из связанных значений указанного поля из указанного значения *Список записей*. Значения могут разделяться указанным разделителем. |

## <a name="type-conversion-functions-in-the-text-category"></a>Функции преобразования типа в категории текста

В следующей таблице описаны функции преобразования типов в [категории текста](er-functions-category-text.md).

| Функция | Описание |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Эта функция возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode. |
| [GuidValue](er-functions-text-guidvalue.md)       | Эта функция преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Эта функция возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной культуре. |
| [QrCode](er-functions-text-qrcode.md)             | Эта функция возвращает значение *Контейнер*, которое представляет изображение Quick Response (QR) для указанной строки в двоичном формате. |
| [Текст](er-functions-text-text.md)                 | Эта функция возвращает указанное число в качестве *строкового* значения, представляющее указанное число после его преобразования в текстовую строку, которая отформатирована в соответствии с параметрами языкового стандарта сервера текущего экземпляра приложения. |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности](general-electronic-reporting.md)

[Конструктор формул в электронной отчетности](general-electronic-reporting-formula-designer.md)

[Язык формул электронной отчетности](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]