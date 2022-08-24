---
title: Функция ER ADDDAYS
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) ADDDAYS.
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274150"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
