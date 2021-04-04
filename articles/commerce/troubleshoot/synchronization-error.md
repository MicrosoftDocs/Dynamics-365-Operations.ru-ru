---
title: Ошибка синхронизации заказа, которая связана со службой платежей по умолчанию
description: В этом разделе содержатся инструкции по устранению неполадок, которые могут помочь исправить ошибку, которая может возникнуть при синхронизации интернет-заказов.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585495"
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

[Настройка, авторизация и проверка данных кредитной карты](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
