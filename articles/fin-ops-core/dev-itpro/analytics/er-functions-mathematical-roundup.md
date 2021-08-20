---
title: Функция ER ROUNDUP
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDUP.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 0d397a43712b349bc6eb5e88f38dbc7d8a5231a909f38608d45b4e08861b6b7b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743247"
---
# <a name="roundup-er-function"></a>Функция ER ROUNDUP

[!include [banner](../includes/banner.md)]

Функция `ROUNDUP` возвращает указанное число в виде *вещественного* значения после его округления вверх до указанного числа десятичных знаков.

## <a name="syntax"></a>Синтаксис

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Аргументы

`number`: *Вещественный*

Числовое значение, которое должно быть округлено вверх.

`decimals`: *Целочисленный*

Числовое значение, представляющее количество десятичных знаков.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция поступает как [ROUND](er-functions-mathematical-round.md), но она всегда округляет указанное число вверх (в направлении от нуля).

## <a name="example-1"></a>Пример 1

`ROUNDUP (1200.763, 2)` округляет верх до двух десятичных знаков и возвращает **1200.77**.

## <a name="example-2"></a>Пример 2

`ROUNDUP (1200.767, -3)` округляет вверх до ближайшего числа, кратного тысяче, и возвращает **2000**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Математические функции](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]