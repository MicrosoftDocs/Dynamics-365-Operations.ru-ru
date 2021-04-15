---
title: Функция ER INDEX
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INDEX.
author: NickSelin
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
ms.openlocfilehash: 14f10359a3f20fb9d23639babce764b9ef64243d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750468"
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