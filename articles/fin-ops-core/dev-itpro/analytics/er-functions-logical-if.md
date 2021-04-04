---
title: Функция ER IF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности IF.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565912"
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