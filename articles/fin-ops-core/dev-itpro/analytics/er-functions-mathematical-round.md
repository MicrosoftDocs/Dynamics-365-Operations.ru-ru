---
title: Функция ER ROUND
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUND.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
ms.topic: article
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570406"
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