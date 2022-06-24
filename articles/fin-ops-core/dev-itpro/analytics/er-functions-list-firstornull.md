---
title: Функция ER FIRSTORNULL
description: В этой статье объясняется, как используется функция электронной отчетности (ER) FIRSTORNULL.
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: bae2916371cd00810f559ff2006b2b238c8ad918
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900261"
---
# <a name="firstornull-er-function"></a>Функция ER FIRSTORNULL

[!include [banner](../includes/banner.md)]

Функция `FIRSTORNULL` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если эта запись не пуста. Если запись пуста, эта функция возвращает нулевое значение *Контейнер (запись)*.

## <a name="syntax"></a>Синтаксис

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="example"></a>Пример

Выражение `FIRSTORNULL(SPLIT("",1)).Value` возвращает пустую строку (**""**).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]