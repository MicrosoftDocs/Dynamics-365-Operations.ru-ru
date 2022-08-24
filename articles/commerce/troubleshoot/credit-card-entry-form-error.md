---
title: Страница запись кредитной карты отображает ошибку при оформлении заказа
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь в том случае, когда раздел "Способ платежа" не загружен и отображается сообщение об ошибке.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269764"
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
