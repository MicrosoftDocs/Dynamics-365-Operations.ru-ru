---
title: Домашняя страница расчетов с клиентами
description: Расчеты с клиентами используются для отслеживания накладных и входящих платежей клиентов.
author: abruer
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerInvoiceWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "20671"
- intro-internal
ms.assetid: 1040678e-ffcb-47fb-a1bc-626db8046504
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7c92ae7972344a6c740f5d4d94334ba0e81fd7e
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715590"
---
# <a name="accounts-receivable-home-page"></a>Домашняя страница расчетов с клиентами

[!include [banner](../includes/banner.md)]

Расчеты с клиентами используются для отслеживания накладных и входящих платежей клиентов. 

Вы можете создавать накладные клиентов, основанные на заказах на продажу или на отборочных накладных. Вы также можете вводить накладные с произвольным текстом, которые не связаны с заказами на продажу. Для получения платежей можно использовать один из нескольких типов платежей. К ним относятся переводные векселя, наличные деньги, чеки, кредитные карты и электронные платежи. Если в организации имеется несколько юридические лиц, для записи платежей в одном юридическом лице от имени других юридических лиц можно использовать централизованные платежи.


**Бизнес-процессы**

[![Бизнес-процесс.](./media/AR-process.PNG)](./media/AR-process.PNG)

## <a name="set-up-accounts-receivable"></a>Настройка расчетов с клиентами

Модуль "Расчеты с клиентами" служит для отслеживания накладных клиентов и получаемых от клиентов платежей. В модуле "Расчеты с клиентами" вы можете настраивать группы клиентов, клиентов, профили разноски, процент-ноты, письма-напоминания, комиссии, параметры клиентов, накладных расходов, поставок и назначений, переводных векселей и других типов. 

- [Распределения по бухгалтерским счетам и записи в журнале субкниги для накладных с произвольным текстом](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
- [Профили разноски по клиенту](customer-posting-profiles.md)
- [Настройка, авторизация и проверка данных кредитной карты](credit-card-authorizations.md)
- [Создание накладной клиента](configure-customer-invoices.md)
- [Настройка и обработка периодических накладных](set-up-process-recurring-invoices.md)
- [Исправление накладной с произвольным текстом](correct-free-text-invoice.md)
- [Настройка переводных векселей](set-up-bills-exchange.md)
- [Настройка процентных ставок для кода процента](set-up-interest-rates-interest-code.md)
- [Отказ, возобновление или реверсирование процентных сборов](waive-reinstate-reverse-interest-fees.md)
- [Обзор прямого дебетования SEPA](sepa-direct-debit-overview.md)
- [Настройка поручения прямого дебетования SEPA](sepa-direct-debit-mandate.md)
- [Закрытие модуля "Расчеты с клиентами"](close-accounts-receivable.md)
    
## <a name="set-up-credit-and-collections"></a>Настройка модуля "Кредит и сборы"

Управление сведениями по сбору задолженностей осуществляется централизованно на странице "Сборы". Менеджеры по кредитам и сборам могут использовать его для управления сборами задолженностей. Агенты по сбору задолженностей могут начинать обработку сборов по спискам клиентов, которые создаются с помощью заранее определенных критериев по сборам, или на странице "Клиенты".

- [Кредит и сборы в расчетах с клиентами](collections-credit-accounts-receivable.md)
- [Настройка модулей "Расчеты с клиентами" и "Кредит и сборы"](accounts-receivables-set-up-overview.md)
- [Настройка модуля "Кредит и сборы"](set-up-collections.md)

## <a name="set-up-payments-and-settlements"></a>Настройка платежей и сопоставлений

Вы можете принимать от клиентов платежи различных типов, например переводные векселя, наличные, чеки, кредитные карты и электронные платежи. 

- [Использование платежа клиента для сопоставления нескольких накладных, охватывающих несколько периодов скидок](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
- [Централизованные платежи для расчетов с поставщиками](centralized-payments-accounts-receivable.md)
- [Сопоставление частичного платежа клиента и окончательного платежа в полном объеме до даты скидки](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
- [Сопоставление частичного платежа клиента до даты скидки с окончательным платежом после даты скидки](settle-partial-customer-payment-before-discount-or-final-payment-after.md)
- [Настройка частичного платежа клиента, имеющего скидки по кредит-нотам](settle-partial-customer-payment-discounts-credit-notes.md)
- [Сопоставление частичного платежа клиента с несколькими периодами скидок](settle-partial-customer-payment-multiple-discount-periods.md)
- [Возмещение клиентам](reimburse-customers.md)
- [Платежи клиентов на частичную сумму](customer-payments-partial-amount.md)
   
### <a name="additional-resources"></a>Дополнительные ресурсы

#### <a name="whats-new-and-in-development"></a>Новые возможности и текущие разработки

Перейдите в раздел [Дорожная карта Microsoft Dynamics 365](/dynamics365/release-plans/), чтобы узнать о новых и запланированных возможностях. 

#### <a name="blogs"></a>Блоги

Мнения, новости и другую информацию о расчетах с клиентами и других решениях см. в [блоге по Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) и в [блоге по финансам в приложениях для управления финансами и операциями Microsoft Dynamics 365](https://community.dynamics.com/365/financeandoperations/b/financials).

[Блог сообщества партнеров Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) — это единый источник информации о новых возможностях и тенденциях в Dynamics 365, ориентированный на партнеров Microsoft Dynamics.

#### <a name="task-guides"></a>Проводники по задачам
Проводники по задачам в приложении — это еще один источник справочной информации. Чтобы перейти к проводникам по задачам, нажмите кнопку "Справка" на любой странице.

#### <a name="videos"></a>Видео

Смотрите видео с инструкциями на [канале Microsoft Dynamics 365 в YouTube](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).









[!INCLUDE[footer-include](../../includes/footer-banner.md)]

