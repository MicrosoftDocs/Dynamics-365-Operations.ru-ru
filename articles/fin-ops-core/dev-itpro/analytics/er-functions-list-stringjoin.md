---
title: Функция ER STRINGJOIN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности STRINGJOIN.
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
ms.openlocfilehash: 4f5d6b9a0f43902160d1ff7fa91b86a7e2c3422d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743503"
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
