---
title: Функция ER INTVALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) INTVALUE.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282632"
---
# <a name="intvalue-er-function"></a>Функция ER INTVALUE

[!include [banner](../includes/banner.md)]

Функция `INTVALUE` возвращает значение *Int*, представляющее указанную строку.

## <a name="syntax-1"></a>Синтаксис 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Текстовое значение, которое должно быть преобразовано в число *Int*.

`number`: *Вещественный* или *Целочисленный*

Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int*.

## <a name="return-values"></a>Возвращаемые значения

*Int*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Все десятичные знаки усекаются.

## <a name="example-1"></a>Пример 1

`INTVALUE ("100.77")` возвращает значение *Int* **100**.

## <a name="example-2"></a>Пример 2

`INTVALUE (-100.77)` возвращает значение *Int* **-100**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции преобразования типов](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
