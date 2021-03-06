---
title: Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018418"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.

## <a name="description"></a>описание

При открытии страницы заказа на продажу после синхронизации заказа появляется следующее сообщение об ошибке: "Тип оплаты должен быть кредитной картой, так как указан номер кредитной карты".

![Ошибка "Тип оплаты должен быть кредитной картой"](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Приказ

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Настройка типа платежа в Commerce headquarters

1. Перейдите в раздел **Расчеты с клиентами \> Настройка платежей \> Условия оплаты**.
1. В левой области переходов выберите условия оплаты.
1. Убедитесь, что в поле **Тип платежа** выбрана **кредитная карта**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Разноска интернет-продаж и платежей](../tasks/posting-online-sales-payments.md)
