---
title: Функция ER INTVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INTVALUE.
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
ms.openlocfilehash: 5e06236bf1d158a4cf579b8b89cc0a5f7d815c38
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042666"
---
# <a name="INTVALUE">Функция ER INTVALUE</a>

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