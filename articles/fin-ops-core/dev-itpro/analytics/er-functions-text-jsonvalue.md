---
title: Функция ER JSONVALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) JSONVALUE.
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267974"
---
# <a name="jsonvalue-er-function"></a>Функция ER JSONVALUE

[!include [banner](../includes/banner.md)]

Функция `JSONVALUE` анализирует данные в формате JavaScript Object Notation (JSON), к которому осуществляется доступ по специальному пути и извлекает скалярное значение с указанным идентификатором. Затем она возвращает извлеченное скалярное значение как *строковое* значение.

## <a name="syntax"></a>Синтаксис

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Действительный путь источника данных типа *Строка*, содержащего данные JSON.

`path`: *Строка*

Код скалярного значения данных JSON. Используйте косую черту (/), чтобы отделить имена связанных узлов JSON. Используйте нотацию "скобка" (\[\]) для указания индекса конкретного значения в массиве JSON. Обратите внимание, что для этого индекса используется отсчет с нуля.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example-1"></a>Пример 1

Источник данных **JsonField** содержит следующие данные в формате JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. В этом случае выражение `JSONVALUE (JsonField, "BuildNumber")` возвращает следующее значение типа данных *Строка*: **"7.3.1234.1"**.

## <a name="example-2"></a>Пример 2

Источник данных **JsonField** типа *Вычисляемое поле* содержит следующее выражение: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Это выражение настроено на возврат [*строкового*](er-formula-supported-data-types-primitive.md#string) значения, представляющего следующие данные в формате JSON.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

В этом случае выражение `JSONVALUE(json, "workers/[1]/emails/[0]")` возвращает следующее значение типа данных *Строка*: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
