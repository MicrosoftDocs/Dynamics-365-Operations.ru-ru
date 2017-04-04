---
title: "Объект стоимости запасов"
description: "В этой статье представлена информация о том, как рассчитываются значения объекта запасов."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Объект стоимости запасов

В этой статье представлена информация о том, как рассчитываются значения объекта запасов. 

Новые функциональные возможности, которая называется ** физическое количество ** служит для просмотра значений объекта конкретного запасов. Объект затрат представляет уровень объекта, на котором выполняется учет запасов. Дополнительные сведения об объектах затрат см. в разделе [Объекты затрат](cost-object.md). Чтобы просмотреть значения запасов для конкретного объекта, щелкните **физическое количество** на **объект стоимости** страницы. Ниже приведен способ расчета стоимости запасов объекта: объект запасов. Значение = объект стоимости. Средняя себестоимость единицы × складского объекта. Количество в следующем примере показано, как вычисляются значения складского объекта и объект стоимости. Два события поступления продуктов зарегистрированы в номенклатуре А:

-   Отборочная накладная 1: количество = 100 ПК., сумма = $1,000.00, узел = 1, склад = 11, номер партии = B1
-   Отборочная накладная 2: количество = 50 ПК., сумма = $800.00, узел = 1, склад = 11, номер партии = B2

В следующей таблицы показан результат расчета для объекта затрат. Результат можно просмотреть на странице **Объект затрат**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип объекта</th>
<th>Номер номенклатуры</th>
<th>Место</th>
<th>Количество</th>
<th>Ед. изм. складского учета</th>
<th>Значение</th>
<th>Средняя стоимость единицы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Объект затрат</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Шт.</td>
<td><p>1800,00 долларов США</p></td>
<td><p>12,00 долларов США</p></td>
</tr>
</tbody>
</table>

В следующей таблицы показан результат расчета для объекта запасов. Результат можно просмотреть на странице **Объект затрат**, щелкнув **Физическое количество**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип объекта</th>
<th>Номер номенклатуры</th>
<th>Сайт</th>
<th>Склад</th>
<th>Партия №</th>
<th>Количество</th>
<th>Ед. изм. складского учета</th>
<th>Значение</th>
<th>Средняя стоимость единицы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Объект запасов</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Шт.</td>
<td><p>1200,00 долларов США</p></td>
<td><p>12,00 долларов США</p></td>
</tr>
<tr class="even">
<td>Объект запасов</td>
<td>А</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Шт.</td>
<td><p>600,00 долларов США</p></td>
<td><p>12,00 долларов США</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>См. также
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Новые и измененные в Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


