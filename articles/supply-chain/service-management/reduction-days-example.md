---
title: Пример дней сокращения
description: Пример дней сокращения.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564516"
---
# <a name="reduction-days-example"></a>Пример дней сокращения 

[!include [banner](../includes/banner.md)]


Вы создали проводку по подписке клиента на обслуживание, как указано в следующей таблице.

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
<th><p>Начальная дата</p></th>
<th><p>До даты</p></th>
<th><p>Подписка</p></th>
<th><p>Тип подписки</p></th>
<th><p>Project</p></th>
<th><p>Категория</p></th>
<th><p>Валюта реализации</p></th>
<th><p>Цена продажи</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01 марта 2011</p></td>
<td><p>31 марта 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Периодически</strong></p></td>
<td><p>9013</p></td>
<td><p>СубКат2</p></td>
<td><p>Евро</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Клиент уведомил, что в течение двух дней (10 и 11 марта) сервисное обслуживание не потребуется. Вы соглашаетесь уменьшить подписку на эти два дня.

Вы создаете новую проводку типа **Дни сокращения**, как описано в следующей таблице.

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
<th><p>с даты</p></th>
<th><p>До даты</p></th>
<th><p>Подписка</p></th>
<th><p>Тип подписки</p></th>
<th><p>Project</p></th>
<th><p>Категория</p></th>
<th><p>Валюта реализации</p></th>
<th><p>Цена продажи</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10 марта 2011</p></td>
<td><p>11 марта 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Дни сокращения</strong></p></td>
<td><p>9013</p></td>
<td><p>СубКат2</p></td>
<td><p>Евро</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


При выставлении счета за операции марта 2011 года цена продажи евро 200 уменьшается на сумму 12,90 EUR. Сумма к оплате за операцию по подписке составляет, таким образом, 187,10 EUR, и по двум операциям выставляется счет на общую сумму 187,10 EUR.

## <a name="see-also"></a>См. также

[Уменьшение дней в сборах по подписке](reduce-the-days-on-subscription-fees.md)

  


