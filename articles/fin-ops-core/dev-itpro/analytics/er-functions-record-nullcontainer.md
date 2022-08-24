---
title: Функция ER NULLCONTAINER
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NULLCONTAINER.
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
ms.openlocfilehash: 8efa4cce3bda1707eff052e882b74e3da9542353
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291775"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
