---
title: Использование одного платежа для сопоставления накладных, охватывающих несколько периодов скидок
description: В этом разделе показано, как оплачиваются несколько накладных, когда для каждой накладной действует скидка по оплате. Сценарии в этой статье показывают, как изменяются используемые скидки по оплате в зависимости от времени выполнения платежа.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56d74b6700b48a8c523d02a1affc421ee370215e
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027754"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Использование одного платежа для сопоставления накладных, охватывающих несколько периодов скидок

[!include [banner](../includes/banner.md)]

В этом разделе показано, как оплачиваются несколько накладных, когда для каждой накладной действует скидка по оплате. Сценарии в этой статье показывают, как изменяются используемые скидки по оплате в зависимости от времени выполнения платежа.

Компания Fabrikam продает товары клиенту 4032. Компания Fabrikam предлагает скидку на оплату в размере 1 %, если счет будет оплачен в течение 14 дней. Fabrikam также предлагает скидки по оплате на частичные платежи. Параметры сопоставления расположены на странице **Параметры модуля расчетов с клиентами**.

## <a name="invoices"></a>Накладные
Клиент 4032 имеет три накладных на общую сумму 3 000,00:

-   Накладная FTI-10040 на 1 000,00, была введена 15 мая. На эту накладную распространяется скидка на оплату в размере 1 %, если она будет оплачена в течение 14 дней.
-   Накладная FTI-10041 на 1 000,00, была введена 25 июня. На эту накладную распространяется скидка на оплату в размере 1 %, если она будет оплачена в течение 14 дней.
-   Накладная FTI-10042 на 1 000,00, была введена 25 июня. На эту накладную распространяется скидка на оплату в размере 2%, если она оплачивается в течение пяти дней, и скидка в размере 1% при оплате в течение 14 дней.

## <a name="settle-all-invoices-on-june-29"></a>Сопоставьте все накладные 29-го июня
Если Арни создает журнал платежей для полного сопоставления этих накладных 29 июня, платеж равен 2 970,00. Сумма всех сумм скидок будет равна 30,00. Арни создает платеж для клиента 4032 и затем открывает страницу **Сопоставление проводок**. На странице **Сопоставление проводок** Арни отмечает все строки трех накладных для сопоставления:

-   Оплата для накладной FTI-10040 равна 1 000,00. Скидка по оплате не используется.
-   Оплата для накладной FTI-10041 равна 990,00. Используется скидка по оплате 1 процент или 10,00.
-   Оплата для накладной FTI-10042 равна 980,00. Используется скидка по оплате 2 процента или 20,00.

| Пометка                     | Использовать скидку по оплате | Операция   | Учетная запись | Дата      | Срок выполнения  | Счет | Дебетовая сумма в валюте проводки | Сумма кредита в валюте проводки | Валютное | Сумма сопоставления |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Выбрано                 | Обычная            | FTI-10040 | 4032    | 15.05.2015 | 15.06.2015 | 10040   | 1 000,00                             |                                       | американский доллар      | 1 000,00         |
| Установлен                 | Обычная            | FTI-10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1 000,00                             |                                       | американский доллар      | 990,00           |
| Выбранный и выделенный | Обычная            | FTI-10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1 000,00                             |                                       | американский доллар      | 980,00           |

После разноски платежа сальдо клиента равно 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Сопоставьте все накладные 1-го июля
Если Арни создает журнал платежей для полного сопоставления этих накладных 1 июля, платеж равен 2 980,00. Арни создает платеж для клиента 4032 и затем открывает страницу **Сопоставление проводок**. На странице **Сопоставление проводок** Арни отмечает все строки трех накладных для сопоставления:

-   Оплата для накладной FTI-10040 равна 1 000,00. Скидка по оплате не используется.
-   Оплата для накладной FTI-10041 равна 990,00. Используется скидка по оплате 1 процент или 10,00.
-   Оплата для накладной FTI-10042 равна 990,00. Используется скидка по оплате 1 процент или 10,00. Хотя 1 июля не входит в период предоставления 2-процентной скидки, в это время все еще можно получить 1-процентную скидку.

| Пометка                     | Использовать скидку по оплате | Операция   | Учетная запись | Дата      | Срок выполнения  | Счет | Дебетовая сумма в валюте проводки | Сумма кредита в валюте проводки | Валютное | Сумма сопоставления |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Выбрано                 | Обычная            | FTI-10040 | 4032    | 15.05.2015 | 15.06.2015 | 10040   | 1 000,00                             |                                       | американский доллар      | 1 000,00         |
| Установлен                 | Обычная            | FTI-10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1 000,00                             |                                       | американский доллар      | 990,00           |
| Выбранный и выделенный | Обычная            | FTI-10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1 000,00                             |                                       | американский доллар      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Частичное сопоставление 29-го июня
Клиент 4032 может оплатить часть суммы, например половину каждого счета. Арни создает платеж для клиента 4032 и затем открывает страницу **Сопоставление проводок**. На странице **Сопоставление проводок** Арни отмечает все строки трех накладных для сопоставления. В каждой строке Арни входит сумму для сопоставления на основе инструкций, предоставленных клиентом. Когда Арни выбирает строку, Арни видит сумму скидки для этой строки и сумму использованной скидки по оплате. Поскольку клиент оплачивает половину накладной, Арни видит, что значение в поле **Сумма скидки по оплате** для FTI-10042 равно **20,00**, но значение в поле **Скидка по оплате** равно **10,00**. Сумма платежа — 1 485,00.

| Пометка                     | Использовать скидку по оплате | Операция   | Учетная запись | Дата      | Срок выполнения  | Счет | Дебетовая сумма в валюте проводки | Сумма кредита в валюте проводки | Валютное | Сумма сопоставления |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Выбрано                 | Обычная            | FTI-10040 | 4032    | 15.05.2015 | 15.06.2015 | 10040   | 1 000,00                             |                                       | американский доллар      | 500,00           |
| Установлен                 | Обычная            | FTI-10041 | 4032    | 25.06.2015 | 25.07.2015 | 10041   | 1 000,00                             |                                       | американский доллар      | 495,00           |
| Выбранный и выделенный | Обычная            | FTI-10042 | 4032    | 25.06.2015 | 25.07.2015 | 10042   | 1 000,00                             |                                       | американский доллар      | 490,00           |

Арни также может вручную ввести сумму платежа 1485,00 до того, как он откроет страницу **Сопоставление проводок**. Если Арни вручную вводит сумму платежа, а затем помечает все три проводки, но он не корректирует значение в поле **Сумма сопоставления** для каждой проводки, Арни получает следующее сообщение, когда закрывает страницу:

> Общая сумма помеченных проводок отличается от суммы журнала. Изменить сумму журнала?

Если Арни нужно, чтобы сумма платежа составляла всего 1485,00, Арни щелкает **Нет** и разносит журнал. Проводки сопоставляются следующим образом:

1.  Накладная FTI-10040 полностью сопоставляется на 1 000,00, поскольку она была введена 15 мая и является самой старой накладной. Скидка по оплате не используется. Сумма остатка по проводке по платежу — 485,00.
2.  Накладная FTI-10041 не сопоставляется совсем. Накладные FTI-10041 и FTI-10042 введены в тот же день. Однако скидка 1 процент доступна для накладной FTI-10041, скидка 2 процента доступна для накладной FTI-10042. Так как лучшая скидка доступна для накладной FTI-10042, остальные 485,00 сопоставляются с накладной FTI-10042.
3.  Накладная FTI-10042 сопоставляется с остальными 485,00. Fabrikam предлагает скидки на частичную оплату. В этом случае скидка составляет 9,90 (= 485,00 ÷ 0,98 × 0,02). Сумма (485,00) делится на 0,98, потому что скидка — 2 % (поэтому клиент оплачивает 98 % накладной). Результат затем умножается на процент скидки, т. е. на 2 процента. Платеж 485,00 плюс скидка 9,90 составляют 494,90. Сумма исходной накладной равна 1 000,00. Поэтому проводка имеет сальдо 505,10 (= 1 000,00 – 494,90).

Арни просматривает эту информацию на странице **Проводки по клиенту**.

| Операция    | Тип транзакции | Дата      | Счет | Дебетовая сумма в валюте проводки | Сумма кредита в валюте проводки | Сальдо  | Валютное |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Счет          | 15.05.2015 | 10040   | 1 000,00                             |                                       | 0,00     | американский доллар      |
| FTI-10041  | Накладная          | 25.06.2015 | 10041   | 1 000,00                             |                                       | 1 000,00 | американский доллар      |
| FTI-10042  | Счет          | 25.06.2015 | 10042   | 1 000,00                             |                                       | 505,10   | американский доллар      |
| ARP-10040  | Платеж          | 29.06.2015 |         |                                      | 1 485,00                              | 0,00     | американский доллар      |
| DISC-10040 | Скидка по оплате    | 29.06.2015 |         |                                      | 9,90                                  | 0,00     | американский доллар      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]