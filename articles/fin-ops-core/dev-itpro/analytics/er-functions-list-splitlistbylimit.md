---
title: Функция ER SPLITLISTBYLIMIT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLITLISTBYLIMIT.
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
ms.openlocfilehash: 54c78f36c93e1bdb472b84fc7ca6428d20088bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041868"
---
# <a name="SPLITLISTBYLIMIT">Функция ER SPLITLISTBYLIMIT</a>

[!include [banner](../includes/banner.md)]

Функция `SPLITLISTBYLIMIT` разделяет указанный список на новый список подсписков (пакетов). Количество записей в каждом пакете рассчитывается динамически. Затем функция возвращает результат в качестве нового значения *Список записей*, которое состоит из пакетов.

## <a name="syntax"></a>Синтаксис

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

`limit value`: *Целочисленный* или *Вещественный*

Максимальное значение лимита, используемого для разделения исходного списка на пакеты.

`limit source`: *Поле*

Действительный путь поля типа *Целочисленный* или *Вещественный* в указанном списке. Значение этого поля определяет шаг, на который увеличивается общая сумма.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Возвращаемый список пакетов содержит следующие элементы:

- **Значение**: *Список*

    Список записей, относящихся к текущему пакету.

- **BatchNumber**: *Целочисленный*

    Номер текущего пакета в возвращенном списке.

Предел не применяется к одному элементу исходного списка, если источник предела превышает заданный предел.

## <a name="example"></a>Пример

На следующем рисунке показан формат электронной отчетности (ER).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

На следующих рисунках показаны источники данных, которые используются для формата.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

На следующем рисунке показан результат выполнения формата. В этом случае выводится плоский список товарных номенклатур.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

На следующих рисунках этот же формат был скорректирован для представления списка товарных номенклатур в партиях, когда одна партия может содержать товары с общим весом, который не должен превышать 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

На следующем рисунке показан результат выполнения скорректированного формата.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Предел не применяется к последнему элементу исходного списка, так как значение (**11**) источника предела (**вес**) превышает заданный предел (**9**). Чтобы игнорировать подсписки во время создания отчета, используйте функцию `WHERE` или выражение **Включено** соответствующего элемента формата по мере необходимости.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)
