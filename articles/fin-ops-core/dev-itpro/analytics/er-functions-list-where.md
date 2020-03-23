---
title: Функция ER WHERE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности WHERE.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041845"
---
# <a name="WHERE">Функция ER WHERE</a>

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