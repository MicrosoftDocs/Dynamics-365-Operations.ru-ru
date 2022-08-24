---
title: Функция ER INDEX
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) INDEX.
author: kfend
ms.date: 05/20/2021
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
ms.openlocfilehash: 1ecac869644b09ee6564a4cd0eb53a82de9df25f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274037"
---
# <a name="index-er-function"></a>Функция ER INDEX

[!include [banner](../includes/banner.md)]

Функция `INDEX` возвращает значение *Контейнер (запись)*, выбранное с помощью указанного числового индекса в указанном списке. Если индекс выходит за пределы диапазона записей в указанном списке, выдается исключение.

## <a name="syntax"></a>Синтаксис

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`index`: *Целочисленный*

Числовой индекс, указывающий положение желаемой записи в указанном списке.

> [!NOTE]
> Так как для этой функции используется нумерация, начинающаяся с единицы, следует указать значение **1**, чтобы вернуть первую запись указанного списка.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="example-1"></a>Пример 1

Если введен источник данных **DS** для типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `DS.Value` возвращает текстовое значение **"B"** для второй записи этого списка записей. Выражение `INDEX (SPLIT ("A|B|C", "|"), 2).Value` также возвращает значение текста **"B"**.

## <a name="example-2"></a>Пример 2

Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `INDEX (SPLIT ("A|B|C", "|"), 4).Value` выдает исключение во время выполнения.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
