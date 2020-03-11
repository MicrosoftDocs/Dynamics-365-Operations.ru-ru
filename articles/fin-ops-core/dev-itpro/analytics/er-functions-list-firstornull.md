---
title: Функция ER FIRSTORNULL
description: Этот раздел объясняет способ использования функции электронной отчетности FIRSTORNULL.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 86c8a0ae21ffeb6268efbbd198f7c709c2ad54f6
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042121"
---
# <a name="FIRSTORNULL">Функция ER FIRSTORNULL</a>

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
