---
title: Функция ER ALLITEMSQUERY
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) ALLITEMSQUERY.
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
ms.openlocfilehash: f5f8c69e7f67377c2e3d9ccc5a0da1fefe488921
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877164"
---
# <a name="allitemsquery-er-function"></a>Функция ER ALLITEMSQUERY

[!include [banner](../includes/banner.md)]

Функция `ALLITEMSQUERY` работает как объединенный SQL-запрос. Возвращает новое выровненное значение *Список записей*, состоящее из списка записей, представляющих все элементы, которые соответствуют указанному пути.

## <a name="syntax"></a>Синтаксис

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Аргументы

`path`: *Список записей*

Действительный путь источника данных типа данных *Список записей*. Должен содержать по крайней мере одно отношение.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Указанный путь должен быть определен как действительный путь источника данных для элемента источника данных с типом данных *Список записей*. Должен также содержать по крайней мере одно отношение. Элементы данных, такие как *строка* и *дата* пути, должны вызывать ошибку в построителе выражения электронной отчетности (ER) во время разработки.

Когда эта функция применяется к источникам данных для типа данных *Список записей*, которые относятся к объекту приложения, который может быть непосредственно вызван с помощью SQL (например, таблица, объект или запрос), она выполняется как объединенный SQL-запрос. В противном случае она работает в памяти как функция [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>Пример

Определите следующие источники данных в соответствии вашей модели:

- Источник данных **CustInv** типа *Записи таблицы*, который относится к таблице CustInvoiceTable
- Источник данных **FilteredInv** типа *Вычисляемое поле*, содержащий выражение `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- **JourLines** типа *Вычисляемое поле*, содержащий выражение `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

При выполнении сопоставления модели для обращения к источнику данных **JourLines**, выполняется следующая инструкция SQL:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]