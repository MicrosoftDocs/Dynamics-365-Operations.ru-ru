---
title: Использование скидки, превышающей вычисленную скидку для платежа поставщика
description: В этой статье рассматривается сценарий, в котором скидка по оплате используется для суммы, которая превышает скидку, первоначально доступную для накладной. Такая ситуация может возникнуть, если организация пришла с поставщиком к соглашению о том, что сумма оплаты по накладной будет снижена.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179658"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Использование скидки, превышающей вычисленную скидку для платежа поставщика

[!include [banner](../includes/banner.md)]

В этой статье рассматривается сценарий, в котором скидка по оплате используется для суммы, которая превышает скидку, первоначально доступную для накладной. Такая ситуация может возникнуть, если организация пришла с поставщиком к соглашению о том, что сумма оплаты по накладной будет снижена. 

Поставщик 3051 предоставляет Fabrikam скидку на оплату в размере 4 %, если счет будет оплачен в течение 7 дней. 29 июня Эйприл вводит счет на 1 000,00 в систему. Поставщик позволяет Эйприл использовать скидку 60,00 вместо скидки по умолчанию 40,00, доступной для данного счета. Эйприл записывает одноразовую оплату путем использования журнала платежей по расчетам с поставщиками. Она вводит поставщика для платежа, после этого открывает страницу **Сопоставление проводок**. Она отмечает накладную и изменяет значение в поле **Сумма скидки по оплате** на **60,00**.

| Пометка     | Использовать скидку по оплате | Операция   | Учетная запись | Дата      | Срок выполнения  | Счет | Сумма в валюте проводки | Валютное | Сумма сопоставления |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Выбрано | Обычная            | Inv-10040 | 3051    | 29.06.2015 | 29.07.2015 | 10040   | 1 000,00                       | американский доллар      | 940,00           |

Данные по скидкам появляются внизу страницы **Сопоставление проводок**.

|                              |           |
|------------------------------|-----------|
| Дата скидки по оплате           | 12.07.2015 |
| Сумма скидки по оплате         | 60,00     |
| Использовать скидку по оплате            | Обычная    |
| Скидка по оплате          | 0,00      |
| Сумма скидки по оплате | 60,00     |

Эйприл разносил журнал платежей. Счет полностью сопоставлен с платежом 940,00 и скидкой 60,00.


