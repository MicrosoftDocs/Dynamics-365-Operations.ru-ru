---
title: Правила политики аудита
description: Для оценки отчетов по расходам, накладных поставщиков и заказов на покупку в соответствии на предмет соответствия созданным правилам политики можно использовать политики аудита. Все правила, связанные с политиками аудита, применяются в пакетном режиме в соответствии с заданным графиком.  Каждое правило политики представляет собой экземпляр типа правила политики. Для каждого типа правила политики одновременно может быть активно только одно правило политики.
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: kfend
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8272cd516f1b31f20ded7c2fdb8bfc4c4d984d42
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710511"
---
# <a name="audit-policy-rules"></a>Правила политики аудита

[!include [banner](../includes/banner.md)]

Для оценки отчетов по расходам, накладных поставщиков и заказов на покупку в соответствии на предмет соответствия созданным правилам политики можно использовать политики аудита. Все правила, связанные с политиками аудита, применяются в пакетном режиме в соответствии с заданным графиком.  Каждое правило политики представляет собой экземпляр типа правила политики. Для каждого типа правила политики одновременно может быть активно только одно правило политики. 

## <a name="queries-and-query-types"></a>Запросы и типы запросов

При создании правила политики аудита необходимо сначала выбрать тип правила политики. Тип правила политики определяет запрос репозитория прикладных объектов (AOT), который будет использоваться в качестве отправной точки для создания правила политики. Он также определяет тип запроса, который будет использоваться для правила политики. Запрос определяет документ-источник, который будет оцениваться с помощью правила политики. Также он определяет поля в документе-источнике, которые идентифицируют юридическое лицо и дату, используемую при выборе документов для аудита. От типа запроса зависят поля по умолчанию на странице запроса и на странице правил политики аудита. В следующей таблице показаны типы запросов, предусмотренные для правил политики аудита.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип запроса</th>
<th>Назначение</th>
<th>Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Условный</td>
<td>Оценка атрибутов документа-источника относительно заданных значений.</td>
<td></td>
</tr>
<tr class="even">
<td>Агрегированное</td>
<td>Оценка нескольких документов-источников или строк документов-источников относительно правила политики путем агрегирования числовых значений.</td>
<td></td>
</tr>
<tr class="odd">
<td>Образец</td>
<td>Случайный выбор заданного процента документов-источников для оценки на предмет нарушений политики.</td>
<td>При выборе этого варианта используйте страницу Правило политики аудита для указания процента документов, случайным образом выбираемых для аудита.</td>
</tr>
<tr class="even">
<td>Дубликат</td>
<td>Оценка документов-источников на предмет наличия в них дублирующихся записей в заданных полях.</td>
<td>При выборе этого варианта в используйте страницу Правило политики аудита для указания числа дней, добавляемого в начало диапазона дат для выбора документов при оценке документов на предмет дублирующихся записей.</td>
</tr>
<tr class="odd">
<td>Поиск по списку</td>
<td>Оценка документов-источников для конкретных объектов.</td>
<td>Корневой документ запроса определяет документ, аудит которого проводится. Запрос должен быть запросом списка, который включает ссылку на таблицу dirpartytable. Этот вариант можно использовать только со следующими запросами AOT:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Сотрудники, отслеживаемые в отчете о расходах)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Поставщики, отслеживаемые в заказе на покупку)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Поставщики, отслеживаемые в накладной поставщика)</li>
</ul>
При выборе этого варианта необходимо указать контролируемые объекты на странице Правило политики аудита.</td>
</tr>
<tr class="even">
<td>Поиск по ключевым словам</td>
<td>Оценка документов-источников на предмет того, содержат ли они определенные слова.</td>
<td>При выборе этого варианта введите слова, которые искать, на странице Правило политики аудита. Страница Правило политики аудита также включает параметры, которые позволяют указать таблицы и поля, оцениваемые на предмет вхождения введенных слов.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Общие параметры
Во всех правилах политики для определенной политики аудита используются одни и те же пакетные параметры и один и тот же диапазон дат для выбора документов. Эти параметры задаются для политики в странице Дополнительные параметры.



## <a name="additional-resources"></a>Дополнительные ресурсы

[Нарушения политики аудита и соответствующие обращения](audit-policy-violations-cases.md)
[пределение политик аудита для документов-источников](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
