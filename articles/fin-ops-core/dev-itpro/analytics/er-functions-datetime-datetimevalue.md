---
title: Функция ER DATETIMEVALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) DATETIMEVALUE.
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
ms.openlocfilehash: 591c707ae7f57236386de0b4ef85d428c9ae31fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287349"
---
# <a name="datetimevalue-er-function"></a>Функция ER DATETIMEVALUE

[!include [banner](../includes/banner.md)]

Функция `DATETIMEVALUE` возвращает значение *[Дата и время](er-formula-supported-data-types-primitive.md#datetime)*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной [культуре](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) в значение даты/времени. Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Синтаксис 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Аргументы

`text`: *[Строка](er-formula-supported-data-types-primitive.md#string)*

Текст, представляющий значение для формата.

`format`: *Строка*

Формат указанного текста. Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Строка*

Культура, используемая для форматирования указанного текста. Сведения о поддерживаемых культурах см. в разделе [Культура](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Возвращаемые значения

*DateTime*

Результирующее значение даты/времени.

## <a name="usage-notes"></a>Примечания по использованию

Когда культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова. Например, если функция `DATETIMEVALUE` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры. Значение шаблона `culture` по умолчанию — **EN-US**.

## <a name="example-1"></a>Пример 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` возвращает **2:55:00 21 декабря 2016** на основе указанного пользовательского формата и культуры приложения по умолчанию **EN-US**.

## <a name="example-2"></a>Пример 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` возвращает **2:55:00 21 декабря 2016** на основе указанного пользовательского формата и культуры.

Однако вызов `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` вызывает исключение, информирующее пользователя, что указанная строка не распознана как допустимое значение даты/времени для указанной культуры.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
