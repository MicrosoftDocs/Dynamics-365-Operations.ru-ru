---
title: "Начисление подписок"
description: "С помощью подписок на обслуживание можно вручную начислять доход в периодах, следующих за датой выставления накладной по проводке по сборам."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: acbf7432c9487cbefaf24a2a98772c8f0ec7ffe6
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="accruing-subscriptions"></a>Начисление подписок 

[!include [banner](../includes/banner.md)]


С помощью подписок на обслуживание можно вручную начислять доход в периодах, следующих за датой выставления накладной по проводке по сборам.

Периоды начисления создаются для периода накладной, который настраивается для проводки по сборам. Периоды начисления основываются на коде периода для подписки.

Можно выполнить начисление и сторнировать начисленный доход.

## <a name="reverse-accruals-of-credit-amounts"></a>Реверсирование начислений сумм кредитов

Если кредитуются суммы накладной по подписке, можно использовать 2 метода для реверсирования сумм начисления:

  - Можно выполнить реверсирование каждой проводки по начисленному доходу по отдельности перед созданием предложения кредит-ноты для этой проводки. Это ручной метод. (вручную)

  - Можно выполнить реверсирование начисленных сумм по дате, когда разносится кредит-нота, или по первоначальной дате начисления.

Дополнительные сведения см. в разделе [Параметры подписки (форма)](https://technet.microsoft.com/en-us/library/aa619615.aspx).

## <a name="setup-requirements"></a>Требования для настройки

Чтобы начислить доход, убедитесь, что выполняются следующие требования к данным.

## <a name="account-setup"></a>Настройка счета

Должны быть настроены счета **НЗП - подписка** и **Начисленная выручка - подписка** в модуле **Проект**.

При разноске начисленного дохода счет **НЗП - подписка** дебетуется на сумму начисления, а счет **Начисленная выручка - подписка** кредитуется на сумму начисления.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Настройка счетов для начисления дохода для подписки

1.  Щелкните **Управление и учет по проектам** \> **Настройка** \> **Разноска** \> **Настройка разноски ГК**.

2.  Перейдите на вкладку **Счета выручки** и выберите **НЗП - подписка** или **Начисленная выручка - подписка**, чтобы настроить счета.

## <a name="subscription-group-setup"></a>Настройка группы подписок

Для обеспечения возможности начисления выручки по подпискам должен быть установлен флажок **Начислить выручку**. Он находится в форме **Группы подписки** для группы, которая присоединена к подписке. Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Подписки на сервисное обслуживание** \> **Группы подписки**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Включение начисления дохода в группе подписок

1.  Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Подписки на сервисное обслуживание** \> **Группы подписки**.

## <a name="periods"></a>Периоды

Следует настроить код периода выставления накладных. Также необходимо настроить период начисления, если начисление дохода будет производиться не в тех же временных интервалах, которые использованы для выставления накладных.

В следующей таблице приводятся общие сведения о том, какие периоды начислений могут быть настроены для каждого периода обработки накладной.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Период выписки накладной</p></th>
<th><p>Период начисления</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Годы</strong></p></td>
<td><ul>
<li><p><strong>Годы</strong></p></li>
<li><p><strong>Квартал</strong></p></li>
<li><p><strong>Месяц</strong></p></li>
<li><p><strong>день</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Квартал</strong></p></td>
<td><ul>
<li><p><strong>Квартал</strong></p></li>
<li><p><strong>Месяц</strong></p></li>
<li><p><strong>день</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Месяц</strong></p></td>
<td><ul>
<li><p><strong>Месяц</strong></p></li>
<li><p><strong>день</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Неделя</strong></p></td>
<td><ul>
<li><p><strong>день</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>день</strong></p></td>
<td><ul>
<li><p><strong>день</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Настройка периода выставления накладных является обязательной частью общей настройки групп подписок. Также можно определить, необходимо ли настроить период начисления для группы подписок. Если настраивается период начисления для группы подписок, этот период предлагается в поле **Код периода**. Это поле находится в форме **Начисление выручки по подписке**, когда начисляется выручка по подписке. Однако период начисления — это дополнительная информация о группе подписок.


> [!NOTE]
> <P>Используйте следующий путь, чтобы открыть форму <STRONG>Начисление выручки по подписке</STRONG>. Щелкните <STRONG>Управление сервисным обслуживанием</STRONG> &gt; <STRONG>Периодические операции</STRONG> &gt; <STRONG>Подписки на сервисное обслуживание</STRONG> &gt; <STRONG>Начисление выручки по подписке</STRONG>.</P>


## <a name="transactions"></a>Транзакции

Можно регулировать количество проводок ГК, которые создаются при разноске начисленной выручки. В подписках укажите, должны ли проводки ГК должны создаваться по итоговому значению или по строкам.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Указание уровня данных разноски, которые будут отображаться для проводок начисления

1.  Щелкните **Управление и учет по проектам** \> **Настройка** \> **Параметры модуля "Управление и учет по проектам"**.

2.  На вкладке **Финансы** в поле **Накладная** выберите **Итог** или **Строка**.


## <a name="see-also"></a>См. также

[Начислить выручку по подписке](accrue-subscription-revenue.md)

  


