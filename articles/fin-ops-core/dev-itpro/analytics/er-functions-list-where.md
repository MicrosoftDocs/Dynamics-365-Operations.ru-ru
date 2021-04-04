---
title: Функция ER WHERE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности WHERE.
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
ms.openlocfilehash: ca218f87eb1f9235ab475809fbbdfecf3fe0c7fb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566050"
---
# <a name="where-er-function"></a>Функция ER WHERE

[!include [banner](../includes/banner.md)]

Функция `WHERE` возвращает указанный список в качестве значения *Список записей* после того, как он был отфильтрован в соответствии с указанным условием.

## <a name="syntax"></a>Синтаксис

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`condition`: *Логический*

Действительное условное выражение, используемое для фильтрации записей указанного списка.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция отличается от функции [FILTER](er-functions-list-filter.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Список записей*, присутствующему в памяти.

Если аргументы, настроенные для этой функции (`list` и `condition`) позволяют перевести этот запрос на прямой вызов SQL, во время разработки будет выдано предупреждающее сообщение. Это сообщение информирует пользователя о том, что производительность может быть улучшена, если функцию [FILTER](er-functions-list-filter.md) использовать вместо `WHERE`.

## <a name="example-1"></a>Пример 1

Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `WHERE (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.

## <a name="example-2"></a>Пример 2

Если введен источник данных **DS** для типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `WHERE( DS, DS.Value = "B")` возвращает список только одной записи, содержащей текст **"B"** в поле **Значение**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]