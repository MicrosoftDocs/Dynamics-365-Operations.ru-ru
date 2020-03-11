---
title: Функция ER INT64VALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INT64VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042696"
---
# <a name="INT64VALUE">Функция ER INT64VALUE</a>

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
