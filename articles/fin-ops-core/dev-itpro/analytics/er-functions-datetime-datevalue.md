---
title: Функция ER DATEVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATEVALUE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ef617ebfcaeb75e0284ea3cb4e889a204120b3d3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042374"
---
# <a name="DATEVALUE">Функция ER DATEVALUE</a>

[!include [banner](../includes/banner.md)]

Функция `DATEVALUE` возвращает значение *Date*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) в значение даты. Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Синтаксис 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Текст, представляющий значение для формата.

`format`: *Строка*

Формат указанного текста.

`culture`: *Строка*

Культура, используемая для форматирования указанного текста.

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
