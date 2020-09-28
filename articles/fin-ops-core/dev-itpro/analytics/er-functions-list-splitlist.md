---
title: Функция ER SPLITLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLITLIST.
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
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744799"
---
# <a name="splitlist-er-function"></a>Функция ER SPLITLIST

[!include [banner](../includes/banner.md)]

Функция `SPLITLIST` разделяет список на подсписки (или пакеты), каждый из которых содержит указанное число записей. Затем она возвращает результат в качестве нового значения *Список записей*, которое состоит из пакетов.

## <a name="syntax"></a>Синтаксис

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`number`: *Целочисленный*

Максимальное количество записей на один пакет.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Возвращаемый список пакетов содержит следующие элементы:

 - **Значение:** *Список*

    Список записей, относящихся к текущему пакету.

- **BatchNumber:** *Целочисленный*

    Номер текущего пакета в возвращенном списке.

## <a name="example"></a>Пример

На следующем рисунке источник данных **Строки** создается как список записей, содержащий три записи. Этот список разделяется на пакеты, каждый из которых содержит до двух записей.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

На следующем рисунке показан созданный макет формата. В этом макете формата привязки к источнику данных **Строки** создаются для создания выходных данных в формате XML. Эти выходные данные представляют отдельные узлы для каждого пакета и записей в нем.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

На следующем рисунке показан результат выполнения созданного формата.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)
