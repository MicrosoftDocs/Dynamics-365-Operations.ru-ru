---
title: Функция ER WEEKNUM
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) WEEKNUM.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268157"
---
# <a name="weeknum-er-function"></a>Функция ER WEEKNUM

[!include [banner](../includes/banner.md)]

Функция `WEEKNUM` возвращает *[целочисленное](er-formula-supported-data-types-primitive.md#integer)* значение недели года, которая содержит указанное значение *[Дата](er-formula-supported-data-types-primitive.md#date)*. Расчет базируется на правилах, зависящих от языка и региона, которые определяют календарную неделю и первый день недели.

## <a name="syntax"></a>Синтаксис

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Аргументы</a>

`date`: *Дата*

Значение даты, представляющее дату для использования для расчета недели года.

`culture`: *[Строка](er-formula-supported-data-types-primitive.md#string)*

Культура для использования при расчете. Можно использовать коды языков и региональных параметров, которые поддерживаются в соответствии со [стандартами](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0) .NET.

## <a name="return-values"></a>Возвращаемые значения

*Целое число*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Неделя года рассчитывается на основе стандарта [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html), если этот стандарт был принят страной или регионом, для которого предоставляется языковая настройка во время выполнения. В противном случае расчет будет основываться на национальных стандартах, зависящих от страны/региона.

Если в качестве аргумента функции `WEEKNUM` во время выполнения указан неподдерживаемый код [культуры](#arguments), создается исключение. Если в качестве кода культуры указана пустая строка, для расчета номера недели используется английский календарь, нейтральный для страны/региона.

## <a name="examples"></a>Примеры

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` возвращает **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` возвращает **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` возвращает **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` возвращает **21**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
