---
title: Функция электронной отчетности STARTSWITH
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) STARTSWITH.
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
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287229"
---
# <a name="startswith-er-function"></a>Функция электронной отчетности STARTSWITH

[!include [banner](../includes/banner.md)]

Функция `STARTSWITH` определяет, содержит ли заданный ввод начинается заданным текстом. Это возвращает *логическое* значение **TRUE**, если заданный ввод начинается заданным текстом. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может начинаться с второго аргумента.

`start text`: *Строка*

Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может быть в начале первого аргумента.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](/power-platform/admin/data-integrator). В противном случае исключение создается во время разработки. Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.

## <a name="example-1"></a>Пример 1

Выражение `STARTSWITH ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `STARTSWITH ("abc", "A")` возвращает значение **TRUE**.

## <a name="example-2"></a>Пример 2

Выражение `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** начинается со строки **123 Coffee Street**. В противном случае возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)
