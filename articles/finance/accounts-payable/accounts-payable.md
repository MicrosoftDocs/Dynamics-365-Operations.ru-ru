---
title: Домашняя страница расчетов с поставщиками
description: В этой статье представлен обзор расчетов с поставщиками.
author: sunfzam
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "21901"
- intro-internal
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 5ed6aacb94de14bdb72185cd528f62e74cd3cc15
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946111"
---
# <a name="accounts-payable-home-page"></a>Домашняя страница расчетов с поставщиками

[!include [banner](../includes/banner.md)]

В этой статье представлен обзор расчетов с поставщиками. 

Накладные поставщиков можно вводить вручную или получать в электронном виде с использованием информационных объектов. После ввода или получения накладных поставщиков вы можете просматривать и утверждать их с помощью журнала утверждения накладных или страницы **Накладная поставщика**. Вы также можете автоматизировать процесс проверки с помощью функций сопоставления накладных, политик накладных поставщика и бизнес-правил, чтобы удовлетворяющие определенным критериям накладные утверждались автоматически. При этом остальные накладные будут помечаться для проверки уполномоченным пользователем.

**Бизнес-процессы**

[![Диаграмма бизнес-процессов.](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Настройка модуля "Расчеты с поставщиками"

Модуль "Расчеты с поставщиками" позволяет настроить группы поставщиков, поставщиков, профили разноски, параметры оплаты, а также параметры, связанные с поставщиками, накладными расходами, поставками и местами назначения, простыми векселями и другие сведения. 

[Обзор настройки модуля "Расчеты с поставщиками"](accounts-payable-overview.md)

[Распределения по бухгалтерским счетам и записи в журнале субкниги для накладных поставщиков](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Переоценка в иностранной валюте для расчетов с поставщиками и расчетов с клиентами](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Настройка накладных поставщиков

Модуль "Расчеты с поставщиками" позволяет отслеживать накладные и исходящие расходы на поставщиков.

[Обзор сопоставления накладных по расчетам с поставщиками](accounts-payable-invoice-matching.md)

[Профили разноски поставщиков](vendor-posting-profiles.md)

[Настройка проверки сопоставления накладных в модуле расчетов с поставщиками](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Политики трехсторонней проверки соответствия](three-way-matching-policies.md)

[Сопоставление накладных и внутрихолдинговые заказы на покупку](invoice-matching-intercompany-purchase-orders.md)

[Обзор устранения несоответствий во время сопоставления итогов по накладным](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Корреспондирующие счета по умолчанию для журналов накладных поставщика и журналов утверждения накладных](default-offset-accounts-vendor-invoice-journals.md)

[Утверждения накладных на мобильном устройстве](mobile-invoice-approvals.md)

[Рабочая область выставления накладных по совместной работе с поставщиками](vendor-portal-invoicing-workspace.md)

[Автоматизация накладных поставщиков](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Настройка платежей поставщикам 

Вы можете назначить определенный в системе тип платежей, например "Чек", "Электронный платеж" или "Простой вексель", любому пользовательскому способу оплаты. Указывать типы платежей необязательно, но они могут быть полезны при проверке электронных платежей, когда нужно быстро определить тип конкретного платежа. 

[Рабочая область платежей поставщику](vendor-payments-workspace.md)

[Определение сборов по платежам поставщикам](tasks/define-vendor-payment-fees.md)

[Определение условий оплаты для поставщиков](tasks/define-vendor-payment-terms.md)

[Обзор положительного платежа](positive-pay-overview.md)

[Настройка и создание файлов положительных платежей](set-up-generate-positive-pay-files.md)

[Создание платежей поставщику с помощью предложения по оплате](create-vendor-payments-payment-proposal.md)

[Платежи поставщику на частичную сумму](vendor-payments-partial-amount.md)

[Использование скидки, превышающей рассчитанную скидку для платежа поставщику](take-discount-more-calculated-discount-vendor-payment.md)

[Использование скидки по оплате вне периода скидки по оплате](take-cash-discount-outside-cash-discount-timeframe.md)

[Пример электронной отчетности для чеков поставщиков](electronic-reporting-sample-vendor-checks.md)

[Реверсирование платежа поставщику](reverse-vendor-payment.md)

[Счета по предоплате и предоплата](prepayments-invoices-vs-prepayments.md)

[Централизованные платежи для расчетов с поставщиками](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Сопоставления

Следующие темы содержат информацию о сопоставлениях. Сопоставление — это процесс сопоставления платежей со счетами-фактурами. 

[Настройка сопоставления](../cash-bank-management/configure-settlement.md)

[Сопоставление частичного платежа поставщику до даты скидки с окончательным платежом после даты скидки](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Настройка частичного платежа поставщику, имеющего скидки по кредит-нотам поставщика](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Сопоставление частичного платежа поставщику с несколькими периодами скидок](settle-partial-vendor-payment-multiple-discount-periods.md)

[Сопоставление частичного платежа поставщику и окончательного платежа в полном объеме до даты скидки](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Один ваучер с несколькими записями клиента или поставщика](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Дополнительные ресурсы

#### <a name="whats-new-and-in-development"></a>Новые возможности и текущие разработки

Перейдите на страницу [Планы выпусков Microsoft Dynamics 365](/dynamics365/release-plans/), чтобы узнать о новых и запланированных возможностях. 

#### <a name="blogs"></a>Блоги

Мнения, новости и другие сведения о расчетах с поставщиками и других решениях см. в [блоге по Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) и в [блоге по финансам в Microsoft Dynamics 365 Finance](https://community.dynamics.com/365/financeandoperations/b/financials).

[Блог сообщества партнеров Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) — это единый источник информации о новых возможностях и тенденциях в Dynamics 365, ориентированный на партнеров Microsoft Dynamics.

#### <a name="community-blogs"></a>Блоги сообщества

[Управление расчетами с поставщиками в Dynamics 365 Finance](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Проводники по задачам
Проводники по задачам в приложении — это еще один источник справочной информации. Чтобы перейти к проводникам по задачам, нажмите кнопку "Справка" на любой странице.

#### <a name="videos"></a>Видео

Смотрите видео с инструкциями на [канале Microsoft Dynamics 365 в YouTube](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
