---
title: Функция ER SUMIF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SUMIF.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 8721e0115ab3c5ebe3071fe0b9ca5a80db766b0878d886b186f3f3d39f4a6397
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747625"
---
# <a name="sumif-er-function"></a>Функция ER SUMIF

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

Дополнительные сведения и примеры использования этой функции см в разделах [Отложить выполнение элементов последовательности в форматах ER](er-defer-sequence-element.md#Example)и [Отложить выполнение элементов XML в форматах ER](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции сбора данных](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]