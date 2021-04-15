---
title: Страница запись кредитной карты отображает ошибку при оформлении заказа
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел "Способ платежа" не загружен и отображается сообщение об ошибке.
author: Reza-Assadi
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801779"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Страница запись кредитной карты отображает ошибку при оформлении заказа

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел **Способ платежа** не загружен и отображается сообщение об ошибке.

## <a name="description"></a>описание

При открытии страницы оформления заказа Интернет-магазина раздел **Способ платежа** не загружается, и отображается следующее сообщение об ошибке: "Возникла ошибка. Повторите попытку позже".

![Ошибка модуля платежа](media/payment-module-error.jpg)

## <a name="resolution"></a>Приказ

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Подождите, пока истечет срок действия кэша Commerce Scale Unit

Параметры службы платежа на странице оформления заказа в Интернет-магазине кэшируются в Commerce Scale Unit, и их отображение на сайте электронной коммерции может занять до 15 минут. Эти параметры службы платежа включают изменения кода счета продавца, ключа облачного API и различных параметров конфигурации, которые относятся к методу оплаты.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка канала онлайн-торговли](../channel-setup-online.md)
