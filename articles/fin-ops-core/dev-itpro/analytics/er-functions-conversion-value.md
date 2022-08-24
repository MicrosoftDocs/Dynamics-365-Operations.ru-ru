---
title: Функция ER VALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) VALUE.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 0a47637c47ca6c947451efa1230191779401b4e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277673"
---
# <a name="value-er-function"></a>Функция ER VALUE

[!include [banner](../includes/banner.md)]

Функция `VALUE` возвращает *вещественное* значение, преобразованное из указанной строки.

## <a name="syntax"></a>Синтаксис

```vb
VALUE (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Строковое значение, которое должно быть преобразовано в числовое значение.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Символы запятой и точки (.) считаются десятичными разделителями, и ведущий дефис (-) используются в качестве отрицательного знака. Выдается исключение во время выполнения, если указанная строка содержит другие символы, не являющиеся цифрами.

## <a name="example-1"></a>Пример 1

`VALUE ("1 234,56")` выдает исключение.

## <a name="example-2"></a>Пример 2

`VALUE ("1234,56")` возвращает **1234.56**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции преобразования типов](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
