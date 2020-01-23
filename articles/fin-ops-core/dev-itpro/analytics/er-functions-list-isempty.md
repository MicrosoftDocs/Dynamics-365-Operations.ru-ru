---
title: Функция ER ISEMPTY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISEMPTY.
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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916139"
---
# <a name="ISEMPTY">Функция ER ISEMPTY</a>

[!include [banner](../includes/banner.md)]

Функция `ISEMPTY` возвращает *логическое* значение **TRUE**, если указанный список не содержит записей. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```
ISEMPTY (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="example-1"></a>Пример 1

Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `ISEMPTY(DS)` возвращает **FALSE**.

## <a name="example-2"></a>Пример 2

Выражение `ISEMPTY (SPLIT ("",1))` возвращает **TRUE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)
