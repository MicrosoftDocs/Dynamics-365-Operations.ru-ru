---
title: Функция ER WHERE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) WHERE.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 90b9309b30986837855fb96389b234e504dadd4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847527"
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