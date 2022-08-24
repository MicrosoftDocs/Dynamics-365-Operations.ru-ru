---
title: Функция ER COUNT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) COUNT.
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
ms.openlocfilehash: 64c8be659b564d612f3127d46e54535c73ae21ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287259"
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
