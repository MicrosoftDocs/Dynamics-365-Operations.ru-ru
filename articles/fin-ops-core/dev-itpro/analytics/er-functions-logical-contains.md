---
title: Функция электронной отчетности CONTAINS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CONTAINS.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c1d2d761a38d0edfb9abd439e0f710b336f54927
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745433"
---
# <a name="contains-er-function"></a>Функция электронной отчетности CONTAINS

[!include [banner](../includes/banner.md)]

Функция `CONTAINS` определяет, содержит ли заданный ввод заданный текст. Это возвращает *логическое* значение **TRUE**, если заданный ввод содержит заданный текст. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может содержать второй аргумент.

`search text`: *Строка*

Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может содержаться в первом аргументе.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](../data-entities/data-integration-cds.md). В противном случае исключение создается во время разработки. Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.

## <a name="example-1"></a>Пример 1

Выражение `CONTAINS ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `CONTAINS ("abc", "C")` возвращает значение **TRUE**.

## <a name="example-2"></a>Пример 2

Выражение `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** содержит строку **DEU**. В противном случае возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)
