---
title: Функция ER NUMBERVALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NUMBERVALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 9701fe7a1ce2a96fa5fa8df8aeda125c861a117a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871537"
---
# <a name="numbervalue-er-function"></a>Функция ER NUMBERVALUE

[!include [banner](../includes/banner.md)]

Функция `NUMBERVALUE` возвращает *вещественное* значение, преобразованное из указанного *строкового* значения. При преобразовании учитываются указанные десятичные разделители и разделители групп цифр.

## <a name="syntax"></a>Синтаксис

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Текстовое значение, которое должно быть преобразовано в *вещественное* число.

`decimal separator`: Строка

Десятичный разделитель. Он используется для разделения целых и дробных частей десятичного числа.

`digit grouping separator`: *Строка*

Разделитель групп цифр. Он используется в качестве разделителя тысяч.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="example"></a>Пример

`NUMBERVALUE( "1 234,56", ",", " ")` возвращает **1234.56**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции преобразования типов](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]