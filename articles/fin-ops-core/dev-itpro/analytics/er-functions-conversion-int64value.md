---
title: Функция ER INT64VALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INT64VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561502"
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