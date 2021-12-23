---
title: Функция ER WEEKNUM
description: Эта тема содержит общие сведения об использовании функции электронной отчетности WEEKNUM.
author: NickSelin
ms.date: 12/03/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891347"
---
# <a name="weeknum-er-function"></a>Функция ER WEEKNUM

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

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
