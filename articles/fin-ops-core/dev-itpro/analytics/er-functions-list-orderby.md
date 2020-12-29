---
title: Функция ER ORDERBY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ORDERBY.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c39700fab90265ed1915b4815a6bb27af58d9516
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686472"
---
# <a name="orderby-er-function"></a>Функция ER ORDERBY

[!include [banner](../includes/banner.md)]

Функция `ORDERBY` возвращает указанный список в качестве значения *Список записей* после того, как он был отсортирован в соответствии с указанными аргументами. Эти аргументы могут определяться как выражения.

## <a name="syntax"></a>Синтаксис

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`expression 1`: *Поле*

Действительный путь поля источника данных, на который ссылается аргумент `list` вызываемой функции. Поле, на которое есть ссылка, должно быть полем примитивного типа данных. Этот аргумент обязательный.

`expression N`: *Поле*

Действительный путь поля источника данных, на который ссылается аргумент `list` вызываемой функции. Поле, на которое есть ссылка, должно быть полем примитивного типа данных. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="example-1"></a>Пример 1

Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("C|B|A", "|")`, выражение `FIRST( ORDERBY( DS, DS. Value)).Value` возвращает текстовое значение **"A"**.

## <a name="example-2"></a>Пример 2

Если **Поставщик** настраивается в качестве источника данных электронной отчетности (ER), который ссылается на таблицу VendTable, выражение `ORDERBY (Vendors, Vendors.'name()')` возвращает список поставщиков, который отсортирован по имени в восходящем порядке.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)
