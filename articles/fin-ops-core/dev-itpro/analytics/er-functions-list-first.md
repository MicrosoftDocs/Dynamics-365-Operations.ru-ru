---
title: Функция ER FIRST
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) FIRST.
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
ms.openlocfilehash: a1f841fe11f025be95ffee2750da74ad7be51624
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906586"
---
# <a name="first-er-function"></a>Функция ER FIRST

[!include [banner](../includes/banner.md)]

Функция `FIRST` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если этот список не пуст. Если список пуст, эта функция выдает исключение.

## <a name="syntax"></a>Синтаксис

```vb
FIRST (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="example-1"></a>Пример 1

Выражение `FIRST(SPLIT("ABC",1)).Value` возвращает значение текста **"A"**.

## <a name="example-2"></a>Пример 2

Выражение `FIRST(SPLIT("",1)).Value` выдает исключение во время выполнения.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]