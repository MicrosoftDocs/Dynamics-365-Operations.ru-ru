---
title: Функция ER DATEFORMAT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) DATEFORMAT.
author: kfend
ms.date: 09/08/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5a21e65df705e33c0bd502ea2c17e18b5385c0d4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287409"
---
# <a name="dateformat-er-function"></a>Функция ER DATEFORMAT

[!include [banner](../includes/banner.md)]

Функция `DATEFORMAT` возвращает значение типа *[Строка](er-formula-supported-data-types-primitive.md#string)*, которое представляет заданное значение даты в виде текста в указанном формате и в дополнительно указанной [культуре](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Синтаксис 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Аргументы

`date`: *[Дата](er-formula-supported-data-types-primitive.md#date)*

Значение даты, представляющее дату для формата.

`format`: *Строка*

Формат строки вывода. Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> В строке форматирования учитывается регистр при использовании стандартного или пользовательского формата. Например, [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) спецификатор формата "d" возвращает дату, используя короткий шаблон даты, в то время как стандартный спецификатор формата "D" возвращает дату, используя полный шаблон даты. Кроме того, [пользовательский](/dotnet/standard/base-types/custom-date-and-time-format-strings) спецификатор формата "M" возвращает месяц от 1 до 12, в то время как пользовательский спецификатор формата "m" возвращает минуты от 0 до 59.

`culture`: *Строка*

Культура для форматирования. Сведения о поддерживаемых культурах см. в разделе [Культура](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее значение строки.

## <a name="usage-notes"></a>Примечания по использованию

Если культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова. Например, если функция `DATEFORMAT` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры. Значение шаблона `culture` по умолчанию — **EN-US**.

## <a name="example-1"></a>Пример 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` возвращает текущую дату сервера приложений, 24 декабря 2015, как строку **"24-12-2015"**, на основе указанного настраиваемого формата.

## <a name="example-2"></a>Пример 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
