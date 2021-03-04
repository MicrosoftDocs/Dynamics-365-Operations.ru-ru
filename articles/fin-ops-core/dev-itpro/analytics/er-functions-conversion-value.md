---
title: Функция ER VALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681216"
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