---
title: Функция ER JSONVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 11f9ac680ea00622367ea56106fd22508628d85d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685915"
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
