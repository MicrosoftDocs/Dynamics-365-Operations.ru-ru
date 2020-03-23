---
title: Обработка скидок по оплате наличными для переплат
description: В этой статье приведены сценарии, показывающие как платежа обрабатывается, когда клиент принимает скидку по оплате, но также переплачивает.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 803cb478bb7631439ebde66ad96182193d3dd1ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188357"
---
# <a name="handling-cash-discounts-for-overpayments"></a>Обработка скидок по оплате наличными для переплат

[!include [banner](../includes/banner.md)]

В этой статье приведены сценарии, показывающие как платежа обрабатывается, когда клиент принимает скидку по оплате, но также переплачивает. 

Счет считается переплаченным, если сумма платежа больше, чем сумма счета за вычетом скидки по оплате. Чтобы определить, как обрабатывать разницу скидки по оплате наличными в случае переплаты по накладной, используйте поля **Администрирование скидок по оплате наличными** и **Максимальная переплата или недоплата** на странице **Параметры модуля расчетов с клиентами**. В следующем примере клиент переплатил счет на 0,50.

| Общее количество по накладной | Доступная скидка по оплате | Сумма, которая должна быть выплачена и которая содержит скидку при оплате наличными | Сумма, фактически заплаченная клиентом |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Администрирование скидки по оплате = Конкретный
Когда **Конкретный** выбрано в поле **Администрирование скидок по оплате наличными** на странице **Счета для автоматических проводок**, применяется полная скидка по оплате наличными. Сумма переплаты разносится на счет ГК разницы по скидкам по оплате или остается в виде сальдо на счете клиента. Поведение зависит от того, находится ли сумма переплаты в диапазоне между 0,00 и суммой в поле **Максимальная переплата или недоплата**, или от того, больше ли сумма переплаты суммы **Максимальная переплата или недоплата**.

### <a name="scenario-1"></a>Сценарий 1

В этом сценарии, сумма переплаты находится между 0,00 и максимальной переплатой или недоплатой. Введена накладная на 105,00 с доступной скидкой по оплате, если счет будет оплачен в течение семи дней.

| Общее количество по накладной | Доступная скидка по оплате | Сумма, которая должна быть выплачена и которая содержит скидку при оплате наличными |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Клиент совершает оплату на 95,00 в период скидки по оплате. Платеж разносится со счетом на 105,00. После разноски счета и платежа в разделе "Расчеты с клиентами" будут созданы следующие проводки.

| Транзакция   | Cумма | Сальдо |
|---------------|--------|---------|
| Счет       | 105,00 | 0,00    |
| Платеж       | -95,00 | 0,00    |
| Скидка по оплате | -10,50 | 0,00    |

Для платежа и сопоставления создаются следующие записи учета. **Платеж**

| Учетная запись             | Сумма дебета | Сумма кредита |
|---------------------|--------------|---------------|
| Наличные                | 95,00        |               |
| Расчеты с клиентами |              | 95,00         |

**Сопоставление**

| Учетная запись                                                                                                          | Сумма дебета | Сумма кредита |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Скидка по оплате (поле **Счет ГК для скидок клиентам** на странице **Скидки по оплате**)                 | 10,50        |               |
| Расчеты с клиентами                                                                                              |              | 10,50         |
| Скидка по оплате для клиента (поле **Скидка по оплате по клиенту** на странице **Счет для автоматических проводок**) |              | 0,50          |
| Расчеты с клиентами                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Сценарий 2

В этом сценарии сумма переплаты превышает максимальную сумму переплаты или недоплаты. Введена накладная на 105,00 с доступной скидкой по оплате, если счет будет оплачен в течение семи дней.

| Общее количество по накладной | Доступная скидка по оплате | Сумма, которая должна быть выплачена и которая содержит скидку при оплате наличными |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Клиент совершает оплату на 95,00 в период скидки по оплате. Платеж разносится со счетом на 105,00. После разноски счета и платежа в разделе "Расчеты с клиентами" будут созданы следующие проводки.

| Транзакция   | Cумма | Сальдо |
|---------------|--------|---------|
| Счет       | 105,00 | 0,00    |
| Платеж       | -95,00 | -0,50   |
| Скидка по оплате | -10,50 | 0,00    |

Сумма переплаты 0,50 сохранится как открытое сальдо платежа, ее можно сопоставить с другим счетом. Для платежа и сопоставления создаются следующие записи учета. **Платеж**

| Учетная запись             | Сумма дебета | Сумма кредита |
|---------------------|--------------|---------------|
| Наличные                | 95,00        |               |
| Расчеты с клиентами |              | 95,00         |

**Сопоставление**

| Учетная запись                                                                                          | Сумма дебета | Сумма кредита |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Скидка по оплате (поле **Счет ГК для скидок клиентам** на странице **Скидки по оплате**) | 10,50        |               |
| Расчеты с клиентами                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Администрирование скидки по оплате = Неконкретный
Когда **Неконкретный** выбрано в поле **Администрирование скидок по оплате наличными** на странице **Счета для автоматических проводок**, сумма скидки по оплате наличными уменьшается на сумму переплаты. Это поведение всегда применяется независимо от того, больше или меньше сумма переплаты суммы, указанной в поле **Максимальная переплата или недоплата**.

### <a name="scenario-3"></a>Сценарий 3

В этом сценарии введена накладная на 105,00 с доступной скидкой по оплате, если счет будет оплачен в течение семи дней.

| Общее количество по накладной | Доступная скидка по оплате | Сумма, которая должна быть выплачена и которая содержит скидку при оплате наличными |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Клиент совершает оплату на 95,00 в пределах даты скидки по оплате. Платеж разносится со счетом на 105,00. После разноски счета и платежа в разделе "Расчеты с клиентами" будут созданы следующие проводки.

| Транзакция   | Cумма | Сальдо |
|---------------|--------|---------|
| Счет       | 105,00 | 0,00    |
| Платеж       | -95,00 | -0,00   |
| Скидка по оплате | -10,00 | 0,00    |

Сумма скидки при оплате наличными уменьшена с 10,50 до 10,00. Платеж и счет считаются сопоставленными. **Платеж**

| Счет             | Сумма дебета | Сумма кредита |
|---------------------|--------------|---------------|
| Касса за                | 95,00        |               |
| Расчеты с клиентами |              | 95,00         |

**Сопоставление**

| Учетная запись                                                                                          | Сумма дебета | Сумма кредита |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Скидка по оплате (поле **Счет ГК для скидок клиентам** на странице **Скидки по оплате**) | 10,50        |               |
| Расчеты с клиентами                                                                              |              | 10,50         |




