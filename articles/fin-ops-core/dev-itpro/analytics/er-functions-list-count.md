---
title: Функция ER COUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNT.
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746635"
---
# <a name="count-er-function"></a>Функция ER COUNT

[!include [banner](../includes/banner.md)]

Функция `COUNT` возвращает *целочисленное* значение, представляющее количество записей в указанном списке, если список не пуст. Если список пуст, эта функция возвращает **0** (ноль).

## <a name="syntax"></a>Синтаксис

```vb
COUNT (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Целочисленный*

Результирующее числовое значение.

## <a name="example"></a>Пример

`COUNT (SPLIT("abcd" , 3))` возвращает **2**, потому что функция `SPLIT`, которая используется в этом примере, создает список, который состоит из двух записей.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]