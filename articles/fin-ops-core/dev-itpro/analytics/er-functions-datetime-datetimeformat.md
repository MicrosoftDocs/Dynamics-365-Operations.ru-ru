---
title: Функция ER DATETIMEFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATETIMEFORMAT.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 3e141c445a81f3b436d540265533836b8c775deadbf2a85e47127bb28674a3ea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767176"
---
# <a name="datetimeformat-er-function"></a>Функция ER DATETIMEFORMAT

[!include [banner](../includes/banner.md)]

Функция `DATETIMEFORMAT` возвращает значение *строки*, которое представляет заданное значение даты/времени в виде текста в указанном формате и в дополнительно указанной [культуре](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Синтаксис 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Аргументы

`datetime`: *DateTime*

Значение даты/времени, представляющее дату и время для формата.

`format`: *Строка*

Формат строки вывода.

> [!NOTE]
> В строке форматирования учитывается регистр при использовании стандартного или пользовательского формата. Например, [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) спецификатор формата "d" возвращает дату, используя короткий шаблон даты, в то время как стандартный спецификатор формата "D" возвращает дату, используя полный шаблон даты. Кроме того, [пользовательский](/dotnet/standard/base-types/custom-date-and-time-format-strings) спецификатор формата "M" возвращает месяц от 1 до 12, в то время как пользовательский спецификатор формата "m" возвращает минуты от 0 до 59.

`culture`: *Строка*

Культура для форматирования.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее значение строки.

## <a name="usage-notes"></a>Примечания по использованию

Если культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова. Например, если функция `DATETIMEFORMAT` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры. Значение шаблона `culture` по умолчанию — **EN-US**.

Когда функция `DATETIMEFORMAT` преобразует заданное значение даты/времени, она учитывает настройки часового пояса пользователя приложения, который использует формат ER, в контексте которого вызывается функция.

## <a name="example-1"></a>Пример 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` возвращает текущую дату/время сервера приложений, 24 декабря 2015, как **"24-12-2015"**, на основе указанного настраиваемого формата.

## <a name="example-2"></a>Пример 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` возвращает значение текущей даты/времени сеанса приложения, 24 декабря 2015 года, как строку **"24.12.2015"** на основе выбранной немецкой культуры и указанного формата.

## <a name="example-3"></a>Пример 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` возвращает значение строки **2019-11-12T08:00:00.0000000-08:00**, когда эта функция вызывается во время процесса, инициированного пользователем приложения со значением часового пояса **(GMT-08:00), Тихоокеанское время (США и Канада)** в разделе **Настройки языка и страны/региона**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]