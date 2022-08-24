---
title: Функция ER REVERSE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) REVERSE.
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
ms.openlocfilehash: 360878319bfa29395ae5deabec2e25e52d9e0fdc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284159"
---
# <a name="reverse-er-function"></a>Функция ER REVERSE

[!include [banner](../includes/banner.md)]

Функция `REVERSE` возвращает указанный список в качестве значения *Список записей* в обратном порядке сортировки.

## <a name="syntax"></a>Синтаксис

```vb
REVERSE (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="example-1"></a>Пример 1

Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("C|B|A", "|")`, выражение `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` возвращает текстовое значение **"C"**.

## <a name="example-2"></a>Пример 2

Если **Поставщик** настраивается в качестве источника данных электронной отчетности (ER), который ссылается на таблицу VendTable, выражение `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` возвращает список поставщиков, который отсортирован по имени в нисходящем порядке.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
