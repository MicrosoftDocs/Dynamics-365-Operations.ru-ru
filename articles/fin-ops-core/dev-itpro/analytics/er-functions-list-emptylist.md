---
title: Функция ER EMPTYLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности EMPTYLIST.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559208"
---
# <a name="emptylist-er-function"></a>Функция ER EMPTYLIST

[!include [banner](../includes/banner.md)]

Функция `EMPTYLIST` возвращает пустое значение *Список записей* с использованием указанного списка в качестве источника для структуры списка.

## <a name="syntax"></a>Синтаксис

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="example"></a>Пример

`EMPTYLIST (SPLIT ("abc", 1))` возвращает новый пустой список, который имеет такую же структуру, как список, который возвращен функцией `SPLIT`.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]