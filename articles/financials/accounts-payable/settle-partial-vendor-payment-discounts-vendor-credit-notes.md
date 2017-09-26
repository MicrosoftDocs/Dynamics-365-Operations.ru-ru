---
title: "Настройка частичного платежа поставщика, имеющего скидки по кредит-нотам поставщика"
description: "Эта статья дает пошаговое руководство через сценарий где кредитное авизо сопоставляется относительно накладной."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f227a630f7d1245d5db810d6d48df2b20f699185
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017

---

# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Настройка частичного платежа поставщика, имеющего скидки по кредит-нотам поставщика

[!include[banner](../includes/banner.md)]


Эта статья дает пошаговое руководство через сценарий где кредитное авизо сопоставляется относительно накладной.

Поставщики Fabrikam дают скидки по оплате по кредит-нотам. Поставщик 3050 позволяет компании Fabrikam получить скидку на оплату в размере 1 %, если накладная оплачивается в течение 14 дней.

## <a name="invoice-and-credit-memo"></a>Накладная и кредитовое авизо
29 июня Эйприл создает накладную на 1 000,00 для поставщика 3050. 2 июля она создает кредит-ноту на 200,00. Со страницы **Поставщики** Эйприл открывает страницу **Сопоставление проводок**. Она может использовать страницу **Сопоставление проводок**, чтобы пометить и кредит-ноту и накладную для сопоставления. На кредит-ноту рассчитывается скидка в размере 2,00. Поэтому итоговое значение кредит-ноты уменьшается до 198,00.

| Пометка                     | Использовать скидку по оплате | Операция   | Учетная запись | Дата      | Срок выполнения  | Счет | Сумма в валюте проводки | Валютное | Сумма сопоставления |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Выбрано                 | Обычная            | Inv-10070 | 3050    | 29.06.2015 | 29.07.2015 | 10070   | -1 000,00                      | американский доллар      | -990,00          |
| Выбранный и выделенный | Обычная            | CR-10070  | 3050    | 02.07.2015  | 29.07.2015 |         | 200,00                         | американский доллар      | 198,00           |

Данные по скидкам для кредит-ноты появляются внизу страницы **Сопоставление открытых проводок**.

|                              |           |
|------------------------------|-----------|
| Дата скидки по оплате           | 13.07.2015 |
| Сумма скидки по оплате         | 2.00      |
| Использовать скидку по оплате            | Обычная    |
| Скидка по оплате          | 0,00      |
| Сумма скидки по оплате | 2.00      |

Эйприл щелкает **Разнести**. Затем она проверяет выполненное сопоставление. Эйприл видит, что сумма кредит-ноты в размере 198,00 применена и использована скидка 2,00. Следовательно, итоговая сумма — 200,00.

| Пометка                     | Использовать скидку по оплате | Операция   | Учетная запись | Дата      | Срок выполнения  | Счет  | Сумма в валюте проводки | Валютное | Сумма сопоставления |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Выбранный и выделенный | Обычная            | Inv-10070 | 3050    | 29.06.2015 | 29.07.2015 | 10070    | -1 000,00                      | американский доллар      | -200,00          |
| Установлен                 | Обычная            | CR-10070  | 3050    | 02.07.2015  | 29.07.2015 | CR-10070 | 200,00                         | американский доллар      | 198,00           |

Эйприл может просмотреть проводки по поставщику на странице **Проводки по поставщику**, выбрав поставщика на странице **Все поставщики** и затем на панели действий щелкнув **Проводки**. На этой странице Эйприл видит, что сальдо накладной — 800,00. Она также видит кредит-ноту на 198,00 и скидку 2,00.

| Операция    | Тип транзакции | Дата      | Счет | Дебетовая сумма в валюте проводки | Сумма кредита в валюте проводки | Сальдо | Валютное |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Счет          | 29.06.2015 | 10070   |                                      | 1 000,00                              | –800,00 | американский доллар      |
| Inv-10071  |                  | 02.07.2015  | CR10071 | 200,00                               |                                       | 0,00    | американский доллар      |
| DISC-10071 |  Скидка по оплате   | 02.07.2015  |         | 2.00                                 |                                       | 0,00    | американский доллар      |
| DISC-10071 |  Скидка по оплате   | 02.07.2015  |         |                                      | 2.00                                  | 0,00    | американский доллар      |





