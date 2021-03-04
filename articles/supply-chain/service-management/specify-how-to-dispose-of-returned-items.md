---
title: Определение порядка списания возврата
description: Определение порядка списания возврата.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2b1468328433a67253bafc21ac9c9b3a2398872
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435707"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Определение порядка списания возврата 

[!include [banner](../includes/banner.md)]


При обработке заказа на возврат следует указать код причины, чтобы определить, почему продукт возвращается. Необходимо также указать код расстановки и действие метода обработки, чтобы указать, что следует сделать с возвращаемым продуктом.

Код метода обработки может применяться при создании заказа на возврат, регистрации прибытия номенклатуры или обновления отборочных накладных при прибытии номенклатуры и завершения карантинного заказа.

Можно определить коды методов обработки, которые необходимы для поддержки бизнес-процессов. В следующей таблице представлено множество обычно используемых кодов для назначения методов обработки возвращаемого элемента номенклатуры.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип метода обработки</p></th>
<th><p>Общий код</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Выбытие</p></td>
<td><p>SC</p></td>
<td><p>Отходы/уничтожение</p></td>
</tr>
<tr class="even">
<td><p>Выбытие</p></td>
<td><p>DC</p></td>
<td><p>Благотворительные пожертвования</p></td>
</tr>
<tr class="odd">
<td><p>Выбытие</p></td>
<td><p>TD</p></td>
<td><p>Утилизация третьих сторон</p></td>
</tr>
<tr class="even">
<td><p>Выбытие</p></td>
<td><p>SL</p></td>
<td><p>Ликвидация</p></td>
</tr>
<tr class="odd">
<td><p>Выбытие</p></td>
<td><p>TS</p></td>
<td><p>Продажи третьих лиц (вторичные рынки)</p></td>
</tr>
<tr class="even">
<td><p>Ремонт/модификация</p></td>
<td><p>RW</p></td>
<td><p>Доработка</p></td>
</tr>
<tr class="odd">
<td><p>Ремонт/модификация</p></td>
<td><p>RF</p></td>
<td><p>Повторное изготовление/Восстановление</p></td>
</tr>
<tr class="even">
<td><p>Ремонт/модификация</p></td>
<td><p>MD</p></td>
<td><p>Изменить</p></td>
</tr>
<tr class="odd">
<td><p>Ремонт/модификация</p></td>
<td><p>RP</p></td>
<td><p>Ремонт</p></td>
</tr>
<tr class="even">
<td><p>Ремонт/модификация</p></td>
<td><p>RV</p></td>
<td><p>Возврат поставщику</p></td>
</tr>
<tr class="odd">
<td><p>Прочее</p></td>
<td><p>AI</p></td>
<td><p>Использовать "как есть"</p></td>
</tr>
<tr class="even">
<td><p>Прочее</p></td>
<td><p>RS</p></td>
<td><p>Перепродажа</p></td>
</tr>
<tr class="odd">
<td><p>Прочее</p></td>
<td><p>EX</p></td>
<td><p>Биржа</p></td>
</tr>
<tr class="even">
<td><p>Прочее</p></td>
<td><p>MS</p></td>
<td><p>Разное</p></td>
</tr>
</tbody>
</table>


Для каждого кода расстановки, который вы определяете, необходимо выбрать действие метода обработки. Действие метода обработки определяет физические и финансовые последствия кодов расстановки. Например, действие метода обработки определяет физическую обработку возвращенной номенклатуры, финансовые последствия возврата номенклатуры, и необходимость отправки заменяющей номенклатуры клиенту. Можно определить неограниченное количество кодов расстановки согласно вашим бизнес-потребностям, но есть только шесть предопределенных действия метода обработки, которые можно выбирать. В приведенной ниже таблице показаны действия метода обработки и их определения.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Действие метода обработки</p></th>
<th><p>описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>По кредиту</strong></p></td>
<td><p>Возврат номенклатуры на склад и кредитование клиента.</p></td>
</tr>
<tr class="even">
<td><p><strong>Только по кредиту</strong></p></td>
<td><p>Кредитование клиента без необходимости или ожидания возврата номенклатуры.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Отходы</strong></p></td>
<td><p>Отбраковка номенклатуру и кредитование клиента.</p></td>
</tr>
<tr class="even">
<td><p><strong>Заменить и кредитовать</strong></p></td>
<td><p>Возврат номенклатуры на склад, создание заказа на замену и кредитование клиента.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Заменить и списать в отходы</strong></p></td>
<td><p>Отбраковки номенклатуры, создание заказа на замену и кредитование клиента.</p></td>
</tr>
<tr class="even">
<td><p><strong>Вернуть клиенту</strong></p></td>
<td><p>Отклонение возвращенной номенклатуры и возврат ее клиенту.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Выберите код метода обработки для карантинного заказа

1.  Щелкните **Управление запасами** \> **Периодические операции** \> **Управление качеством** \> **Карантинные заказы**.

2.  Для существующего карантинного заказа выберите действие из поля **Код метода обработки** на вкладке **Обзор**.



## <a name="see-also"></a>См. также

[Карантинный заказ (форма)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[Коды методов обработки (форма)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]