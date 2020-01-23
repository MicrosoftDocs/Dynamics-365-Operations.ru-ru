---
title: Функция ER IF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности IF.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b29302ffe534f2439519e57c6a6b8c94c1df8d62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917151"
---
# <a name="IF">Функция ER IF</a>

[!include [banner](../includes/banner.md)]

Функция `IF` возвращает первое указанное значение, если выполняется указанное условие. В противном случае возвращает второе указанное значение. Возвращаемое значение может быть значением любого из поддерживаемых типов данных.

## <a name="syntax"></a>Синтаксис

```
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Аргументы

`condition`: *Логический*

Действительное условное выражение, которое должно быть протестировано.

`first value`: *Любой из поддерживаемых типов данных*

Результат, который возвращается при выполнении условия.

`second value`: *Любой из поддерживаемых типов данных*

Результат, который возвращается при невыполнении условия.

## <a name="return-values"></a>Возвращаемые значения

*Любой из поддерживаемых типов данных*

Полученное значение любого из поддерживаемых типов данных.

## <a name="usage-notes"></a>Примечания по использованию

Аргументы `first value` и `second value` должны быть указаны с помощью одного и того же типа данных. Исключение выдается во время разработки, если типы данных настроенных значений не совпадают.

Если первое значение и второе значение являются значениями типа данных *Контейнер (запись)* или *Список записей*, то в результате есть только поля, которые существуют в обоих значениях.

## <a name="example"></a>Пример

`IF (1=2, "condition is met", "condition is not met")` возвращает строку **"условие не выполняется"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)
