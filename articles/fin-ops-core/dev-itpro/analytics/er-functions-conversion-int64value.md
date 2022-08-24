---
title: Функция ER INT64VALUE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) INT64VALUE.
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
ms.openlocfilehash: 4af6cd4ba8b08fe00f53e9dfb1a9156354ec17fc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292597"
---
# <a name="int64value-er-function"></a>Функция ER INT64VALUE

[!include [banner](../includes/banner.md)]

Функция `INT64VALUE` возвращает значение *Int64*, представляющее указанную строку.

## <a name="syntax-1"></a>Синтаксис 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Текстовое значение, которое должно быть преобразовано в число *Int64*.

`number`: *Вещественный* или *Целочисленный*

Числовое *вещественное* или *целочисленное* значение, которое должно быть преобразовано в число *Int64*.

## <a name="return-values"></a>Возвращаемые значения

*Int64*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Все десятичные знаки усекаются.

## <a name="example-1"></a>Пример 1

`INT64VALUE ("22565422744")` возвращает значение *Int64* **22565422744**.

## <a name="example-2"></a>Пример 2

`INT64VALUE ( VALUE("22565422744.77"))` возвращает значение *Int64* **22565422744**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции преобразования типов](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
