---
title: Функция электронной отчетности ENDSWITH
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ENDSWITH.
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
ms.openlocfilehash: bdd2f364e2d0b80d3df20592ec827dcabf99a06c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745409"
---
# <a name="endswith-er-function"></a>Функция электронной отчетности ENDSWITH

[!include [banner](../includes/banner.md)]

Функция `ENDSWITH` определяет, содержит ли заданный ввод заканчивается заданным текстом. Это возвращает *логическое* значение **TRUE**, если заданный ввод заканчивается заданным текстом. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может заканчиваться с второго аргумента.

`start text`: *Строка*

Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может быть в конце первого аргумента.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](../data-entities/data-integration-cds.md). В противном случае исключение создается во время разработки. Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.

## <a name="example-1"></a>Пример 1

Выражение `ENDSWITH ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `ENDSWITH ("abc", "C")` возвращает значение **TRUE**.

## <a name="example-2"></a>Пример 2

Выражение `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** заканчивается строкой **USA**. В противном случае возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)
