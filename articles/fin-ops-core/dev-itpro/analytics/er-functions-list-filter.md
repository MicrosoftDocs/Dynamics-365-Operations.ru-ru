---
title: Функция ER FILTER
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) FILTER.
author: kfend
ms.date: 12/14/2021
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
ms.openlocfilehash: cfaf76daa8118942c3650e6b39c853434a20ee30
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272599"
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

## <a name="usage-notes"></a><a name="usage-notes"></a>Примечания по использованию

Эта функция отличается от функции [WHERE](er-functions-list-where.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Записи таблицы*. Список и условие могут определяться с помощью таблиц и связей.

Если один или оба аргумента, настроенные для этой функции (`list` и `condition`) не позволяют перевести этот запрос на прямой вызов SQL, во время разработке будет выдано исключение. Это исключение информирует пользователя о том, что `list` или `condition` невозможно использовать для запроса базы данных.

> [!NOTE]
> Функция `FILTER` ведет себя иначе, чем функция `WHERE`, когда функция [`VALUEIN`](er-functions-logical-valuein.md) используется для указания критериев выбора.
> 
> - Если функция `VALUEIN` используется в области действия функции `WHERE`, а второй аргумент функции `VALUEIN` ссылается на источник данных, который не возвращает записей, учитывается логическое значение *[False](er-formula-supported-data-types-primitive.md#boolean)*, которое возвращается функцией `VALUEIN`. Поэтому выражение `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` не возвращает записей поставщика, если источник данных **VendGroups** не возвращает записей групп поставщиков.
> - Если функция `VALUEIN` используется в области действия функции `FILTER`, а второй аргумент функции `VALUEIN` ссылается на источник данных, который не возвращает записей, логическое значение *[False](er-formula-supported-data-types-primitive.md#boolean)*, которое возвращается функцией `VALUEIN`, игнорируется. Поэтому выражение `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` возвращает все записи поставщиков из источника данных **Поставщики**, даже если источник данных **VendGroups** не возвращает записей групп поставщиков.

## <a name="example-1"></a>Пример 1

Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `FILTER (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.

## <a name="example-2"></a>Пример 2

Если **Поставщик** настроен в качестве источника данных ER, который ссылается на таблицу VendTable и если **parmVendorBankGroup** настроен как источник данных ER, который возвращает значение *строкового* типа данных, выражение `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` возвращает список только счетов поставщиков, входящих в конкретную банковскую группу.

## <a name="example-3"></a>Пример 3

Вы вводите источник данных **DS** типа *Вычисляемое поле*, и он содержит выражение `SPLIT ("A,B,C", ",")`. Затем вы вводите другое выражение, `FILTER( DS, DS.Value = "B")`. При попытке сохранить это выражение в конструкторе формул ER выдается следующее исключение: «Ошибка проверки: выражение списка функции FILTER не может быть запрошено».

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
