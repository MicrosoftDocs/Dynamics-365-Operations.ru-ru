---
title: Функция ER DAYOFYEAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYOFYEAR.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: ab252b6194267836ba9e1d85f3b96fb100c9f598c783bd9c849c6490c2e54e21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712317"
---
# <a name="dayofyear-er-function"></a>Функция ER DAYOFYEAR

[!include [banner](../includes/banner.md)]

Функция `DAYOFYEAR` возвращает *целочисленное* значение числа дней между 1 января и указанной датой.

## <a name="syntax"></a>Синтаксис

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Аргументы

`date`: *Дата*

Значение даты, представляющее дату для использования для расчета количества дней.

## <a name="return-values"></a>Возвращаемые значения

*Целочисленный*

Результирующее числовое значение.

## <a name="example-1"></a>Пример 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` возвращает **61**.

## <a name="example-2"></a>Пример 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` возвращает **1**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]