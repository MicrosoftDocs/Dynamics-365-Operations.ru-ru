---
title: Функция ER FIRST
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) FIRST.
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
ms.openlocfilehash: b06f07c4cfef5c74c22f60dfa37986ee88c544cf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275490"
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
