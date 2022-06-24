---
title: Функция ER EMPTYRECORD
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) EMPTYRECORD.
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
ms.openlocfilehash: 6f339347187f145b90f14d56017097ff3d7712e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886830"
---
# <a name="emptyrecord-er-function"></a>Функция ER EMPTYRECORD

[!include [banner](../includes/banner.md)]

Функция `EMPTYRECORD` возвращает нулевое значение *Контейнер (запись)*, у которого такая же структура, что и у указанного списка записей или записи.

## <a name="syntax"></a>Синтаксис

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей* или *Контейнер (запись)*

Действительный путь источника данных типа *Список записей* или *Контейнер (запись)*.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="usage-notes"></a>Примечания по использованию

> [!NOTE] 
> Запись null является записью, в которой все поля имеют пустое значение. Пустое значения равно **0** (ноль) для чисел, пустой строке для строк и т. д.

## <a name="example"></a>Пример

`EMPTYRECORD (SPLIT ("abc", 1))` возвращает новую пустую запись, которая имеет такую же структуру, как список, который возвращен функцией `SPLIT`. Дополнительные сведения см. в разделе [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы с записями](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]