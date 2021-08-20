---
title: Функция ER JSONVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности JSONVALUE.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: b034755602a2f999892d2b976c80550b7a3d7f3cd179816dd7aa1edefe6a0270
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733781"
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

Код скалярного значения данных JSON.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

Источник данных **JsonField** содержит следующие данные в формате JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. В этом случае выражение `JSONVALUE (JsonField, "BuildNumber")` возвращает следующее значение типа данных *Строка*: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]