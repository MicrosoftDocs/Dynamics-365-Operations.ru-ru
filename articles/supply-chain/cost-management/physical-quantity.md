---
title: Значения объекта запасов
description: В этой статье представлена информация о том, как рассчитываются значения объекта запасов.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f14248ffa8f9f5a460b090ca5754442cd50bf45a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263550"
---
# <a name="inventory-object-values"></a>Значения объекта запасов

[!include [banner](../includes/banner.md)]

В этой статье представлена информация о том, как рассчитываются значения объекта запасов. 

Новая функция **Физическое количество** позволяет просматривать значения определенного объекта запасов. 

Объект затрат представляет уровень объекта, на котором выполняется учет запасов. Дополнительные сведения об объектах затрат см. в разделе [Объекты затрат](cost-object.md). 

Чтобы просмотреть значения определенного объекта запасов, щелкните **Физическое количество** на странице **Объект затрат**. Вот как вычисляется значение объекта запасов: 

Объект запасов.Значение = Объект затрат.Средняя себестоимость единицы × Объект запасов.Количество 

В следующем примере показано, как вычисляются значения объекта запасов и объекта затрат. Два события поступления продуктов зарегистрированы в номенклатуре А:

-   Поступление продуктов 1: количество = 100 шт., сумма = 1000,00 долларов США, сайт = 1, склад =11, номер партии = B1
-   Поступление продуктов 2: количество = 50 шт., сумма = 800,00 долларов США, сайт = 1, склад =11, номер партии = B2

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
<td>A</td>
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



<a name="additional-resources"></a>Дополнительные ресурсы
--------

[Объекты затрат](cost-object.md)

[Записи затрат](cost-entries.md)

[Что нового и что изменилось](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]