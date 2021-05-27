---
title: Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию
description: В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021135"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.

## <a name="description"></a>описание

При синхронизации интернет-заказов появляется следующее сообщение об ошибке: "для обработки проводок кредитной карты должна использоваться служба платежей по умолчанию".

![Отсутствует ошибка службы платежа по умолчанию](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Приказ

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Подтверждение или настройка службы платежа по умолчанию в Commerce headquarters

Для подтверждения или настройки службы платежа по умолчанию в Commerce headquarters, сделайте следующее.

1. Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Службы платежей**.
1. Убедитесь, что для параметра **Процессор по умолчанию для новых кредитных карт** установлен значение **Да** для одной службы платежей.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка, авторизация и проверка данных кредитной карты](../../finance/accounts-receivable/credit-card-authorizations.md)