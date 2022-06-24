---
title: Функция ER DATEVALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) DATEVALUE.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 396d6823531d8bf2c5b5f61f2483422c84e54c62
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883798"
---
# <a name="datevalue-er-function"></a>Функция ER DATEVALUE

[!include [banner](../includes/banner.md)]

Функция `DATEVALUE` возвращает значение *[Дата](er-formula-supported-data-types-primitive.md#date)*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной [культуре](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) в значение даты. Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Синтаксис 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Аргументы

`text`: *[Строка](er-formula-supported-data-types-primitive.md#string)*

Текст, представляющий значение для формата.

`format`: *Строка*

Формат указанного текста. Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Строка*

Культура, используемая для форматирования указанного текста. Сведения о поддерживаемых культурах см. в разделе [Культура](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="usage-notes"></a>Примечания по использованию

Когда культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова. Например, если функция `DATEVALUE` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры. Значение шаблона `culture` по умолчанию — **EN-US**.

## <a name="example-1"></a>Пример 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` возвращает значение данных **21 декабря 2016** на основе указанного пользовательского формата и культуры приложения по умолчанию **EN-US**.

## <a name="example-2"></a>Пример 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` возвращает значение даты **21 января2016** на основе указанного пользовательского формата и культуры.

Однако вызов `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` вызывает исключение, информирующее пользователя, что указанная строка не распознана как допустимое значение даты для указанной культуры.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
