---
title: Функция ER SUMIF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SUMIF.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 374569d3bbe59f1b96eee9c789b97b7b2a6004bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042489"
---
# <a name="SUMIF">Функция ER SUMIF</a>

[!include [banner](../includes/banner.md)]

Функция `SUMIF` возвращает *вещественное* значение, представляющее сумму значений, которые были возвращены привязками элементов формата и собраны во время использования для создания исходящего документа во время выполнения формата, и удовлетворяющее указанному условию. Условие состоит из диапазона ключей и значения ключа.

## <a name="syntax"></a>Синтаксис

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Аргументы

`key name for summing`: *Строка*

Значение, возвращаемое выражением, настроенным в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER), для которого значение привязки должно использоваться для целей суммирования.

Свойство **Значение ключа собранных данных** можно настроить как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.

В аргументе `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

В аргументе `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

## <a name="example"></a>Пример

Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции сбора данных](er-functions-category-data-collection.md)
