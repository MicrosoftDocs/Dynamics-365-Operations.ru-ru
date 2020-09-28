---
title: Функция ER NULLCONTAINER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLCONTAINER.
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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743935"
---
# <a name="nullcontainer-er-function"></a>Функция ER NULLCONTAINER

[!include [banner](../includes/banner.md)]

Функция `NULLCONTAINER` возвращает нулевое значение *Контейнер (запись)*, у которого такая же структура, что и у указанного списка записей или записи.

## <a name="syntax"></a>Синтаксис

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей* или *Контейнер (запись)*

Действительный путь источника данных типа *Список записей* или *Контейнер (запись)*.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="usage-notes"></a>Примечания по использованию

> [!NOTE] 
> Эта функция является устаревшей. Вместо этого используйте функцию `EMPTYRECORD`. Дополнительные сведения см. в разделе [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Пример

`NULLCONTAINER (SPLIT ("abc", 1))` возвращает новую пустую запись, которая имеет такую же структуру, как список, который возвращен функцией `SPLIT`. Дополнительные сведения см. в разделе [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы с записями](er-functions-category-record.md)
