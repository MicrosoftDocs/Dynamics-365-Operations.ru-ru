---
title: Функция ER ENUMERATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ENUMERATE.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34ebbec94644276be4ef9beb1c77638606dd37a0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679470"
---
# <a name="enumerate-er-function"></a>Функция ER ENUMERATE

[!include [banner](../includes/banner.md)]

Функция `ENUMERATE` возвращает новое значение *Список записей*, состоящее из перечисленных записей указанного списка.

## <a name="syntax"></a>Синтаксис

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Список перечисленных записей, которые возвращаются, открывает следующие дополнительные элементы:

- Запись полей (компонент **Значение**)
- Индекс текущей записи (**Номер** компонента)

## <a name="example"></a>Пример

На следующем рисунке источник данных **Enumerated** создается как нумерованный список записей поставщика из источника данных **Vendors**, который ссылается на таблицу VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

На следующем рисунке показан формат электронной отчетности (ER). В этом формате привязки данных создаются для создания выходных данных в формате XML. Эти выходные данные представляют отдельных поставщиков как перечислимые узлы.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

На следующем рисунке показан результат выполнения созданного формата.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)
