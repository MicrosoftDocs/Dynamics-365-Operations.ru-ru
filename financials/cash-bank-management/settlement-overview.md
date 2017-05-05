---
title: "Обзор сопоставления"
description: "В этой статье приводятся общие сведения о процессе сопоставления. В ней описываются типы проводок, которые могут быть сопоставлены, когда и как можно сопоставлять проводки, и результаты процесса сопоставления."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: adbfa6f99c481129e8cbf4a2dc4b23b4be1e8b34
ms.lasthandoff: 03/31/2017


---

# <a name="settlement-overview"></a>Обзор сопоставления

[!include[banner](../includes/banner.md)]


В этой статье приводятся общие сведения о процессе сопоставления. В ней описываются типы проводок, которые могут быть сопоставлены, когда и как можно сопоставлять проводки, и результаты процесса сопоставления.

Во время сопоставления проводки на одном документе применяются к проводкам в другом документе для того, чтобы увеличить или уменьшить сальдо каждого документа. Например, платеж можно применить к накладной. Различные типы проводок можно сопоставить в различное время и различными методами. Сопоставление может также вызывать создание новых проводок.

## <a name="what-transactions-can-be-settled"></a>Какие проводки можно сопоставить
Сопоставления в пределах модулей "Расчеты с поставщиками" и "Расчеты с клиентами" могут выполняться между любыми типами проводок, которые влияют на сальдо поставщика или сальдо клиента, такими как накладные, платежи, кредитовые авизо и сборы. Любой тип проводки можно сопоставить с любым другим типом проводки. Например, вы можете сопоставить платеж с накладной, кредитовое авизо с накладной, накладную с накладной и платеж с платежом. Вы можете сопоставлять платежи с проводкой в том же юридическом лице или в другом юридическом лице. В организациях, которые используют централизованную модель платежей, [централизованные платежи](set-up-centralized-payments.md) могут помочь упростить процесс платежей.

## <a name="when-to-settle-transactions"></a>Когда следует сопоставлять проводки
Сделки можно сопоставлять во время ввода платежа. Например, когда вы делаете оплату поставщику, вы обычно выбираете оплачиваемую накладную. Выбирая накладные, вы отмечаете их для сопоставления с платежом. Когда клерки платежей "Расчеты с клиентами" записывают платеж клиента, они могут отметить соответствующие накладные для сопоставления на основе информации, которая включена в платеж клиента. Страница **Сопоставление проводок** используется для отметки проводок для сопоставления. Эту страницу можно открыть из любых неразнесенных накладных или платежей. Когда проводка разносится, сопоставление также разносится. Проводки можно также сопоставлять после их разноски. Вы можете ввести и разнести платеж клиента, не сопоставляя его ни с какими накладными. Однако сначала может потребоваться провести некоторое исследование, чтобы убедиться, что платеж сопоставлен с правильной накладной. Страницу **Сопоставление проводок** можно открыть со страницы **Все клиенты** или **Все поставщики**, а также со страницы **Проводки** для любого клиента или поставщика. Вы можете также зарезервировать разнесенные предоплаты для накладной, отметив платеж для сопоставления с заказом на покупку или заказом на продажу. В этом случае платеж все еще будет иметь открытый баланс, но его нельзя будет сопоставить с другой накладной. Оплата автоматически будет сопоставлена с накладной, созданной из заказа на покупку или заказа на продажу.

## <a name="how-to-settle-transactions"></a>Как следует сопоставлять проводки
Проводки можно сопоставлять вручную, автоматически или путем использования сочетания этих двух методов. Выбор метода сопоставления зависит от бизнес-процессов, который можно после этого реализовать через настройку сопоставления на страницах "Параметры модуля расчетов с поставщиками" и "Параметры модуля расчетов с клиентами". Вы можете создавать платежи поставщика и прямые дебетовые платежи клиента с помощью предложения платежа, которое используется для того, чтобы выбрать оплачиваемые накладные. Предложение платежа инициируется вручную, но затем Microsoft Dynamics 365 for Operations автоматически отмечает выбранные накладные для сопоставления, когда создаются платежи. Если платежи созданы вручную, вы можете использовать страницу **Сопоставление проводок** для того, чтобы выбрать накладные для сопоставления. Вы можете вручную выбрать накладные или можете использовать параметр **Пометить по приоритетам**, чтобы накладные автоматически отмечались для сопоставления. Параметр **Пометить по приоритетам** доступен только для модуля "Расчеты с клиентами". Чтобы включить этот параметр, используйте страницу **Приоритет сопоставления** в "Параметры модуля расчетов с клиентами". Если клерк по платежам вводит платеж, но не сопоставляет платеж до его разноски, платеж сопоставляется автоматически. Вы можете включить автоматическое сопоставление в "Параметрах модуля расчетов с клиентами" и "Параметрах модуля расчетов с поставщиками". Когда вы используете автоматическое сопоставление, вы можете использовать предопределенный порядок сопоставления или вы можете определить ваш собственный порядок приоритета сопоставления в "Параметрах модуля расчетов с клиентами". Эта функциональность доступна только для модуля "Расчеты с клиентами".

## <a name="results-of-settlement"></a>Результаты сопоставления
При сопоставлении проводок неуплаченное сальдо каждой проводки соответствующим образом увеличивается или уменьшается. В типичном сценарии, когда сопоставляются накладная и платеж, статус и сальдо каждой проводки обновляются согласно следующим правилам:

-   Если сумма платежа больше суммы накладной, сальдо накладной уменьшается до 0,00 и накладная закрывается. Платеж остается открытым, и сальдо равно сумме, на которую платеж превышает сумму накладной.
-   Если сумма платежа меньше суммы накладной, сальдо платежа уменьшается до 0,00 и платеж закрывается. накладная остается открытой, и сальдо равно сумме, на которую платеж меньше суммы накладной.
-   Если сумма платежа равна сумме накладной, то платеж и накладная закрываются, а сальдо обоих равно 0,00.

Если [платеж меньше суммы по накладной](../accounts-payable/vendor-payments-partial-amount.md) из-за скидки по оплате, списания или недоплаты, то накладная и платеж все равно могут быть закрыты, в зависимости от настройки сопоставления в параметрах модуля расчетов с поставщиками и параметрах модуля расчетов с клиентами. Сопоставление может также создавать проводки. Например, сопоставление накладной и платежа могут создавать скидку по оплате, реализованную прибыль или убыток, корректировки налога, списание или допустимое расхождение.



