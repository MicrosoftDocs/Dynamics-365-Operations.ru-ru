---
title: Цены продажи подписки
description: При создании подписки цена продажи извлекается из настройки цены продажи, созданной в форме "Цена продажи (подписка)".
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985873"
---
# <a name="subscription-sales-prices"></a>Цены продажи подписки   

[!include [banner](../includes/banner.md)]


При создании подписки цена продажи извлекается из настройки цены продажи, созданной в форме **Цена продажи (подписка)**.

В форме **Цена продажи (подписка)** можно создать цену продажи для конкретной подписки или цены продажи, которые будут применяться более широко. Чтобы цена продажи применялась для подписки, код периода и валюта подписки должны совпадать с кодом периода и валютой цены продажи.

Если код периода и валюта одинаковы для подписки и для цены продажи, цены продажи подписки выбираются на основе приоритетов, указанных в следующей таблице. Отсутствие знака в ячейке соответствуют пустому полю, знак "Х" указывает значение, равное значению в подписке, из которой создается проводка.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Приоритет</p></th>
<th><p><strong>Категория</strong></p></th>
<th><p><strong>Код проекта</strong></p></th>
<th><p><strong>Подписка</strong></p></th>
<th><p><strong>Валюта продажи</strong></p></th>
<th><p><strong>Код периода</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>Х</p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>Х</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>Х</p></td>
<td><p>Х</p></td>
</tr>
</tbody>
</table>


Когда создается сбор по подписке, в качестве цены продажи подписки выбирается цена продажи с наивысшим уровнем детализации (как показано в приведенной выше таблице).

## <a name="update-and-index-subscription-sales-prices"></a>Обновление и индексирование цен продажи подписки

Можно обновить цену продажи подписки, обновив базисную цену или индекс. Обновление может быть выполнено изменением на процент или до нового значения.

## <a name="subscription-fee-sales-prices"></a>Цены продажи для сборов по подписке

Когда создается сбор по подписке, цена продажи основывается на настройке цены продажи подписки. Можно использовать базисную цену из настройки цены подписки или создать индексированные цены продажи.

## <a name="example"></a>пример

Необходимо настроить цены продажи подписки в EUR 500 для нового проекта 9030. В форме **Цена продажи (подписка)** можно создать строки цены продажи подписки, как указано в следующей таблице.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Действительно с</p></th>
<th><p>Категория</p></th>
<th><p>Проект</p></th>
<th><p>Подписка</p></th>
<th><p>Код периода</p></th>
<th><p>Валюта реализации</p></th>
<th><p>Цена продажи</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Месяц</p></td>
<td><p>Евро</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Обратите внимание, что поля **Категория** и **Подписка** пусты.

Затем создайте следующие подписки.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Подписка на обслуживание</p></th>
<th><p>Проект</p></th>
<th><p>Группа подписок</p></th>
<th><p>Категория</p></th>
<th><p>Валюта</p></th>
<th><p>Код периода</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>евро</p></td>
<td><p>Ежемесячно</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>СубКат2</p></td>
<td><p>евро</p></td>
<td><p>Ежемесячно</p></td>
</tr>
</tbody>
</table>


Теперь вы создаете сборы по подписке для обеих подписок в группе подписок Sub1:

1.  Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Подписки на сервисное обслуживание** \> **Группы подписки**.

2.  В форме **Группы подписки** щелкните **Функция** \> **Создать сбор по подписке**.

3.  В форме **Создание сбора по подписке** введите соответствующую информацию. Дополнительные сведения см. в разделе [Создание проводок по сборам по подписке](create-subscription-fee-transactions.md).

Сборы по подписке с ценой продажи EUR 500 созданы для обеих подписок, как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Дата проекта</p></th>
<th><p>Подписка на обслуживание</p></th>
<th><p>Проект</p></th>
<th><p>Категория</p></th>
<th><p>Дата начала</p></th>
<th><p>Дата завершения</p></th>
<th><p>Валюта продаж</p></th>
<th><p>Цена продажи</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>евро</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>СубКат2</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>евро</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Позже вы решили, что необходимо указать цены продажи для категории SubCat1 для проекта 9030. Поэтому вы создаете новую строку цены продажи с ценой продажи EUR 550 для комбинации проекта 9030 и категории SubCat1. Теперь для проекта 9030 имеется две строки цены продажи подписки, как показано в следующей таблице.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Действительно с</p></th>
<th><p>Категория</p></th>
<th><p>Проект</p></th>
<th><p>Подписка</p></th>
<th><p>Код периода</p></th>
<th><p>Валюта</p></th>
<th><p>Цена продажи</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>месяц</p></td>
<td><p>евро</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>месяц</p></td>
<td><p>евро</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


Вы повторяете описанную выше процедуру для создания сборов по подписке для обеих подписок в группе подписок Sub1. В следующей таблице показаны проводки, созданные для каждой подписки, которая относится к группе подписок.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Дата проекта</p></th>
<th><p>Подписка</p></th>
<th><p>Проект</p></th>
<th><p>Категория</p></th>
<th><p>Дата начала</p></th>
<th><p>Дата завершения</p></th>
<th><p>Валюта продаж</p></th>
<th><p>Цена продажи</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>евро</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>СубКат2</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>Евро</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


В первой проводке для подписки 00020\_135 цена продажи EUR 550 извлекается из цены продажи подписки, настроенной для комбинации конкретного проекта и категории. Во второй проводке для подписки 00021\_135 в качестве цены продажи подписки для проекта используется цена продажи 500, поскольку для комбинации проекта 9030 и категории SubCat2 не настроена цена.

## <a name="see-also"></a>См. также

[Обновление и индексирование цен продажи подписки](update-and-index-subscription-sales-prices.md)

  


