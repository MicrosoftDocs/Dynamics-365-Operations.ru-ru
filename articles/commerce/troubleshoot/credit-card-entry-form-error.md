---
title: Страница запись кредитной карты отображает ошибку при оформлении заказа
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел "Способ платежа" не загружен и отображается сообщение об ошибке.
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910451"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Страница запись кредитной карты отображает ошибку при оформлении заказа

[!include [banner](../../includes/banner.md)]

В этой статье содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел **Способ платежа** не загружен и отображается сообщение об ошибке.

## <a name="description"></a>описание

При открытии страницы оформления заказа Интернет-магазина раздел **Способ платежа** не загружается, и отображается следующее сообщение об ошибке: "Возникла ошибка. Повторите попытку позже".

![Ошибка модуля платежа.](media/payment-module-error.jpg)

## <a name="resolution"></a>Решение

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Подождите, пока истечет срок действия кэша Commerce Scale Unit

Параметры службы платежа на странице оформления заказа в Интернет-магазине кэшируются в Commerce Scale Unit, и их отображение на сайте электронной коммерции может занять до 15 минут. Эти параметры службы платежа включают изменения кода счета продавца, ключа облачного API и различных параметров конфигурации, которые относятся к методу оплаты.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка канала онлайн-торговли](../channel-setup-online.md)
