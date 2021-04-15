---
title: Функция ER COUNTIF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNTIF.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: bebb3d3b810e68fa6a0d3f4deb92b750b7c9a9f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755308"
---
# <a name="countif-er-function"></a>Функция ER COUNTIF

[!include [banner](../includes/banner.md)]

Функция `COUNTIF` возвращает *целочисленное* значение, представляющее количество элементов формата, которые были собраны при использовании элементов формата для создания исходящего документа во время выполнения формата, и удовлетворяющее указанному условию. Условие состоит из диапазона ключей и значения ключа.

## <a name="syntax"></a>Синтаксис

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Аргументы

`condition range`: *Строка*

Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER).

`condition value`: *Строка*

Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER.

## <a name="return-values"></a>Возвращаемые значения

*Целочисленный*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Свойства **Имя ключа собранных данных** и **Значение ключа собранных данных** могут быть настроены как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.

Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.

В аргументе `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

В аргументе `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

## <a name="example"></a>Пример

Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции сбора данных](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]