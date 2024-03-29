---
title: Функция ER COUNTIFS
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) COUNTIFS.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: db5fb5b7c4faf749cf17da261130e3e9c3edf41b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280845"
---
# <a name="countifs-er-function"></a>Функция ER COUNTIFS

[!include [banner](../includes/banner.md)]

Функция `COUNTIFS` возвращает *целочисленное* значение, представляющее количество элементов формата, которые были собраны при использовании элементов формата для создания исходящего документа во время выполнения формата, и удовлетворяющее указанным условиям. Каждое условие состоит из диапазона ключей и значения ключа.

## <a name="syntax"></a>Синтаксис

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
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

*Целочисленный*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Свойства **Имя ключа собранных данных** и **Значение ключа собранных данных** могут быть настроены как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.

Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.

В аргументах `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

В аргументах `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.

## <a name="example"></a>Пример

Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции сбора данных](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
