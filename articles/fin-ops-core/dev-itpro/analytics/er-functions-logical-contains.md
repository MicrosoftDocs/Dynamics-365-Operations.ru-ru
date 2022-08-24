---
title: Функция электронной отчетности CONTAINS
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) CONTAINS.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273139"
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

Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](/power-platform/admin/data-integrator). В противном случае исключение создается во время разработки. Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.

## <a name="example-1"></a>Пример 1

Выражение `CONTAINS ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `CONTAINS ("abc", "C")` возвращает значение **TRUE**.

## <a name="example-2"></a>Пример 2

Выражение `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** содержит строку **DEU**. В противном случае возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)
