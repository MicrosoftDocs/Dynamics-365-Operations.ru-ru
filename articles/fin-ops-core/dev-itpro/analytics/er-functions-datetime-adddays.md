---
title: Функция ER ADDDAYS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688451"
---
# <a name="adddays-er-function"></a>Функция ER ADDDAYS

[!include [banner](../includes/banner.md)]

Функция `ADDDAYS` вычисляет значение *DateTime*, которое является указанным числом дней до или после указанной даты начала.

## <a name="syntax"></a>Синтаксис

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Аргументы

`datetime`: *DateTime*

Значение даты/времени, представляющее дату начала.

`days`: *Целочисленный*

Количество дней до или после `datetime`.

## <a name="return-values"></a>Возвращаемые значения

*DateTime*

Результирующее значение даты/времени.

## <a name="usage-notes"></a>Примечания по использованию

Положительное значение для `days` дает будущую дату. Отрицательное значение дает прошлую дату.

## <a name="example-1"></a>Пример 1

`ADDDAYS (NOW(), 7)` возвращает дату и время на семь дней в будущем.

## <a name="example-2"></a>Пример 2

`ADDDAYS (NOW(), -3)` возвращает дату и время на три дня в прошлом.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)
