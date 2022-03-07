---
title: Функция ER DAYS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYS
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0252a68aebaa9af95de561b88ceb0666b3460d79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563494"
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