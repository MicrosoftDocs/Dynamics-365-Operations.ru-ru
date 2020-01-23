---
title: Функция ER COUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNT.
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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916254"
---
# <a name="COUNT">Функция ER COUNT</a>

[!include [banner](../includes/banner.md)]

Функция `COUNT` возвращает *целочисленное* значение, представляющее количество записей в указанном списке, если список не пуст. Если список пуст, эта функция возвращает **0** (ноль).

## <a name="syntax"></a>Синтаксис

```
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
