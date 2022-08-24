---
title: Функция ER IF
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) IF.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b674a6f3e86af3763a251cbdc7c30fb8c5ed0f55
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275560"
---
# <a name="if-er-function"></a>Функция ER IF

[!include [banner](../includes/banner.md)]

Функция `IF` возвращает первое указанное значение, если выполняется указанное условие. В противном случае возвращает второе указанное значение. Возвращаемое значение может быть значением любого из поддерживаемых типов данных.

## <a name="syntax"></a>Синтаксис

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
