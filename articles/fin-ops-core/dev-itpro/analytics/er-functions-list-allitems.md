---
title: Функция ER ALLITEMS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ALLITEMS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559232"
---
# <a name="allitems-er-function"></a>Функция ER ALLITEMS

[!include [banner](../includes/banner.md)]

Функция `ALLITEMS` выполняется как выбор в памяти и возвращает новое выровненное значение *Список записей* в виде списка записей, который представляет все элементы, которые соответствуют указанному пути.

## <a name="syntax"></a>Синтаксис

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Аргументы

`path`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Путь должен быть определен как действительный путь источника данных для элемента источника данных с типом данных *Список записей*. Элементы данных, такие как строка пути и дата, должны вызывать ошибку в построителе выражения электронной отчетности (ER) во время разработки.

Мы не рекомендуем использовать эту функцию для транзакционных источников данных, которые могут содержать большой объем данных. Вместо этого, лучше использовать функцию [ALLTEMSQUERY](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>Пример 1

Если вы вводите `SPLIT("abcdef" , 2)` в качестве источника данных **DS**, выражение `COUNT( ALLITEMS (DS))` возвращает **3**.

## <a name="example-2"></a>Пример 2

Если вы введете **Vend** в качестве источника данных для типа данных *Список записей*, ссылающегося на таблицу приложений VendTable, выражение `ALLITEMS (Vend.'<Relations'.ContactPerson)` возвращает выровненный список записей со структурой таблицы **ContactPerson** и содержит все контактные лица, к которым можно получить доступ с помощью отношения **ContactPerson.ContactForParty == vendTable.Party**, это доступно для всех поставщиков из таблицы поставщиков по ссылке.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]