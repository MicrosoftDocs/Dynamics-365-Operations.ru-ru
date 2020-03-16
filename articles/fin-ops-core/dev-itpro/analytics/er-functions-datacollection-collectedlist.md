---
title: Функция ER COLLECTEDLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COLLECTEDLIST.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 8a66ba364a7d06cd5ac03b57f07e2c5d4eb7a46d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042604"
---
# <a name="COLLECTEDLIST">Функция ER COLLECTEDLIST</a>

[!include [banner](../includes/banner.md)]

Функция `COLLECTEDLIST` возвращает значение *Список записей*, содержащее список значений, которые были возвращены свойством **Значение ключа собранных данных** формата элементов и собраны, когда элементы формата использовались для создания исходящих документов во время выполнения формата, и что удовлетворяет указанным условиям. Каждое условие состоит из диапазона ключей и значения ключа.

## <a name="syntax"></a>Синтаксис

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Аргументы

`condition 1 range`: *Строка*

Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER). Этот аргумент является обязательным.

`condition 1 value`: *Строка*

Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER. Этот аргумент является обязательным.

`condition N range`: *Строка*

Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата ER. Эти дополнительные аргументы являются необязательными.

`condition N value`: *Строка*

Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Свойства **Имя ключа собранных данных** и **Значение ключа собранных данных** могут быть настроены как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.

Эта функция возвращает пустой список, когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File**.

В аргументах `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

В аргументах `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

## <a name="example"></a>Пример

Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции сбора данных](er-functions-category-data-collection.md)
