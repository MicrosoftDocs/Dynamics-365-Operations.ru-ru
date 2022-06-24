---
title: Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию
description: В этой статье содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.
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
ms.openlocfilehash: 49d16c39fdcee0a22d1cabe14cd9b6d124d6f04d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901684"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию

[!include [banner](../../includes/banner.md)]

В этой статье содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.

## <a name="description"></a>описание

При синхронизации интернет-заказов появляется следующее сообщение об ошибке: "для обработки проводок кредитной карты должна использоваться служба платежей по умолчанию".

![Отсутствует ошибка службы платежа по умолчанию.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Решение

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Подтверждение или настройка службы платежа по умолчанию в Commerce headquarters

Для подтверждения или настройки службы платежа по умолчанию в Commerce headquarters, сделайте следующее.

1. Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Службы платежей**.
1. Убедитесь, что для параметра **Процессор по умолчанию для новых кредитных карт** установлен значение **Да** для одной службы платежей.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка, авторизация и проверка данных кредитной карты](../../finance/accounts-receivable/credit-card-authorizations.md)