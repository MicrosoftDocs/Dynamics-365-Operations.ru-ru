---
title: Функция ER ROUND
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) ROUND.
author: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 57d41ed92a5577fdc5fffeccef2834e9b6fb5197
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286070"
---
# <a name="round-er-function"></a>Функция ER ROUND

[!include [banner](../includes/banner.md)]

Функция `ROUND` возвращает указанное число в виде *вещественного* значения после его округления до указанного числа десятичных знаков.

## <a name="syntax"></a>Синтаксис

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Аргументы

`number`: *Вещественный*

Числовое значение, которое должно быть округлено.

`decimals`: *Целочисленный*

Числовое значение, представляющее количество десятичных знаков.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Если значение аргумента `decimals` больше 0 (нуля), указанное число округляется до этого числа десятичных знаков.

Если значение аргумента `decimals` равно **0** (ноль), указанное число округляется до ближайшего четного целого.

Если значение аргумента `decimals` меньше 0 (нуля), указанное число округляется слева от десятичного разделителя.

## <a name="example-1"></a>Пример 1

`ROUND (1200.767, 2)` округляет до двух десятичных знаков и возвращает **1200.77**.

## <a name="example-2"></a>Пример 2

`ROUND (1200.767, -3)` округляет до ближайшего числа, кратного тысяче, и возвращает **1000**.

## <a name="example-3"></a>Пример 3

`ROUND (1200.5, 0)` округляет до ближайшего четного целого числа и возвращает **1200**, а `ROUND (1201.5, 0)` делает то же самое и возвращает **1202**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Математические функции](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
