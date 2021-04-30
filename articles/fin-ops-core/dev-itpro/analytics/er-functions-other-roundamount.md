---
title: Функция ER ROUNDAMOUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDAMOUNT.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 7dfc7817eab68e9dd70ce84e68f26d14fd8cf1df
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891217"
---
# <a name="roundamount-er-function"></a>Функция ER ROUNDAMOUNT

[!include [banner](../includes/banner.md)]

Функция `ROUNDAMOUNT` возвращает *вещественное* значение как результат округления указанного числа до ближайшего числа, кратного другому числу в соответствии с указанным правилом округления.

## <a name="syntax"></a>Синтаксис

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Аргументы

`number`: *Int* или *Вещественный*

Числовое значение, которое должно быть округлено.

`decimals`: *Int* или *Вещественный*

Кратное число, до которого значение параметра `number` должно быть округлено.

`round rule`: *Значение перечисления*

Значение перечисления **RoundOffType**, определяющее правило округления. Это перечисление обеспечивает следующие значения:

- Обычный (Ordinary)
- Вниз (RoundDown)
- В большую сторону (RoundUp)

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Полученное числовое значение является кратным значению, указанному параметром `decimals`, и ближе всего к значению, указанному параметром `number`.

## <a name="usage-notes"></a>Примечания по использованию

Когда параметр `number` равен нулю, эта функция всегда возвращает ноль.

Когда параметр `decimals` равен нулю, эта функция округляется до значения округления по умолчанию. Когда параметр `round rule` задан как **RoundOffType.Ordinary**, значение округления по умолчанию составляет **0,01**. В противном случае значение округления по умолчанию составляет **1,0**.

Когда параметр `round rule` задан как **RoundOffType.Ordinary**, эта функция округляет до ближайшей суммы округления.

Когда параметр `round rule` задан как **RoundOffType.RoundDown**, эта функция округляет до нуля для ближайшей суммы округления.

Когда параметр `round rule` задан как **RoundOffType.RoundUp**, эта функция округляет от нуля для ближайшей суммы округления.

Когда параметр `round rule` задан как **RoundOffType.Ordinary**, эта функция работает как функция Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) и функция X++ [ROUND](../dev-ref/xpp-math-run-time-functions.md#round).

## <a name="remarks"></a>Примечания

Для округления числового значения до определенного количества десятичных знаков используйте функцию [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Пример

Если параметр **model.RoundOff** задан как **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` возвращает 7.35. 

Если параметр **model.RoundOff** задан как **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` возвращает 7.35. 

Если параметр **model.RoundOff** задан как **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` возвращает 8.4.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)

[Математические функции](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]