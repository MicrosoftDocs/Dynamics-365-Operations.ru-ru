---
title: Функция ER FILTER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FILTER.
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746611"
---
# <a name="filter-er-function"></a>Функция ER FILTER

[!include [banner](../includes/banner.md)]

Функция `FILTER` возвращает указанный список в качестве значения *Список записей* после изменения запроса, чтобы он фильтровал для указанного состояния.

## <a name="syntax"></a>Синтаксис

```vb
FILTER (list, condition)
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

Эта функция отличается от функции [WHERE](er-functions-list-where.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Записи таблицы*. Список и условие могут определяться с помощью таблиц и связей.

Если один или оба аргумента, настроенные для этой функции (`list` и `condition`) не позволяют перевести этот запрос на прямой вызов SQL, во время разработке будет выдано исключение. Это исключение информирует пользователя о том, что `list` или `condition` невозможно использовать для запроса базы данных.

## <a name="example-1"></a>Пример 1

Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `FILTER (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.

## <a name="example-2"></a>Пример 2

Если **Поставщик** настроен в качестве источника данных ER, который ссылается на таблицу VendTable и если **parmVendorBankGroup** настроен как источник данных ER, который возвращает значение *строкового* типа данных, выражение `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` возвращает список только счетов поставщиков, входящих в конкретную банковскую группу.

## <a name="example-3"></a>Пример 3

Вы вводите источник данных **DS** типа *Вычисляемое поле*, и он содержит выражение `SPLIT ("A,B,C", ",")`. Затем вы вводите другое выражение, `FILTER( DS, DS.Value = "B")`. При попытке сохранить это выражение в конструкторе формул ER выдается следующее исключение: «Ошибка проверки: выражение списка функции FILTER не может быть запрошено».

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]