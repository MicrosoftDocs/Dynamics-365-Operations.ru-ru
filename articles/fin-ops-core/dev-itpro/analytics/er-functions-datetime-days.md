---
title: Функция ER DAYS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYS
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746899"
---
# <a name="days-er-function"></a>Функция ER DAYS

[!include [banner](../includes/banner.md)]

Функция `DAYS` возвращает *целочисленное* значение числа дней между одной указанной датой и второй указанной датой.

## <a name="syntax"></a>Синтаксис

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Аргументы

`date 1`: *Дата*

Значение даты, представляющее дату начала для расчета количества дней.

`date 2`: *Дата*

Значение даты, представляющее дату окончания для расчета количества дней.

## <a name="return-values"></a>Возвращаемые значения

*Целочисленный*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Функция `DAYS` возвращает положительное значение, если первая дата позднее второй даты, возвращает **0** (ноль), когда первая дата равна второй дате, и возвращает отрицательное значение, когда первая дата раньше, чем вторая дата.

## <a name="example"></a>Пример

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` возвращает **-1**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]