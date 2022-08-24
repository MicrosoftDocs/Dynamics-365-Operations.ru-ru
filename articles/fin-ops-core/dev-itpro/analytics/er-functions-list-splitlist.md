---
title: Функция ER SPLITLIST
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) SPLITLIST.
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292537"
---
# <a name="splitlist-er-function"></a>Функция ER SPLITLIST

[!include [banner](../includes/banner.md)]

Функция `SPLITLIST` разделяет список на подсписки (или пакеты), каждый из которых содержит указанное число записей. Затем она возвращает результат в качестве нового значения *Список записей*, которое состоит из пакетов.

## <a name="syntax-1"></a>Синтаксис 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`number`: *Целочисленный*

Максимальное количество записей на один пакет.

`on-demand reading flag`: *Логический*

*Логическое* значение, которое указывает, должны ли при необходимости создаваться элементы вложенных списков.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Возвращаемый список пакетов содержит следующие элементы:

 - **Значение:** *Список*

    Список записей, относящихся к текущему пакету.

- **BatchNumber:** *Целочисленный*

    Номер текущего пакета в возвращенном списке.

Если флаг чтения по запросу имеет значение **True**, вложенные списки создаются после запроса, что позволяет уменьшить потребление памяти, но может привести к ухудшению производительности, если элементы не используются последовательно.

## <a name="example"></a>Пример

На следующем рисунке источник данных **Строки** создается как список записей, содержащий три записи. Этот список разделяется на пакеты, каждый из которых содержит до двух записей.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

На следующем рисунке показан созданный макет формата. В этом макете формата привязки к источнику данных **Строки** создаются для создания выходных данных в формате XML. Эти выходные данные представляют отдельные узлы для каждого пакета и записей в нем.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

На следующем рисунке показан результат выполнения созданного формата.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
