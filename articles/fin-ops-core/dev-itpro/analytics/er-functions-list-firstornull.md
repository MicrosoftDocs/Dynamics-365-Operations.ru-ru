---
title: Функция ER FIRSTORNULL
description: В этой статье объясняется, как используется функция электронной отчетности (ER) FIRSTORNULL.
author: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 7ee1a5c1b6ac13581608f9adbda42fae0706d225
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273199"
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
