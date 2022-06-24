---
title: Функция ER STRINGJOIN
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) STRINGJOIN.
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
ms.openlocfilehash: 08ed76f4dc61ed8afd63ffe99cead4866b63aba9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908513"
---
# <a name="stringjoin-er-function"></a>Функция ER STRINGJOIN

[!include [banner](../includes/banner.md)]

Функция `STRINGJOIN` возвращает значение *строка*, состоящее из связанных значений указанного поля из указанного списка. Значения могут разделяться указанным разделителем.

## <a name="syntax"></a>Синтаксис

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`field`: *Поле*

Действительный путь поля типа данных *Строка* в указанном списке.

`delimiter`: *Строка*

Разделитель, который используется для разделения подстрок.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

Если вы вводите `SPLIT("abc" , 1)` в качестве источника данных **DS**, выражение `STRINGJOIN (DS, DS.Value, "-")` возвращает **"a-b-c"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]