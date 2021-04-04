---
title: Ошибка "Тип оплаты должен быть кредитной картой" на странице заказа на продажу
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при появлении сообщения об ошибке на странице заказа на продажу после синхронизации заказа.
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585502"
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
