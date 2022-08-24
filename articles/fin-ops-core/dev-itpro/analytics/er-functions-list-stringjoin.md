---
title: Функция ER STRINGJOIN
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) STRINGJOIN.
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
ms.openlocfilehash: 6510c271ac5e01d841722fdf2c5fd8c7deaf8caf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271654"
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
