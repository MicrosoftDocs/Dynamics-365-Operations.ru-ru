---
title: Функция ER DAYOFYEAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYOFYEAR.
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
ms.openlocfilehash: ba63c96355a6a7a1eccaddf39e47a3edb2d1e651
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563542"
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