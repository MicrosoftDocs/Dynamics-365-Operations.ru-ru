---
title: Отмененные поступления продуктов не обновляют статус проводки на "Зарегистрировано"
description: После отмены поступления продуктов при входящей загрузке система автоматически обновляет статус складской проводки с "Получено" на "Заказано".
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294162"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Отмененные поступления продуктов не обновляют статус проводки на "Зарегистрировано"

## <a name="symptoms"></a>Симптомы

После выполнения действия **Отмена поступления продуктов** при входящей загрузке система автоматически обновляет статус проводок по запасам с *Получено* на *Заказано*.

## <a name="resolution"></a>Решение

При отмене отборочных накладных для исходящих загрузок статус проводок по запасам остается *Скомплектовано*. Однако когда отменяются поступления продуктов из входящей загрузки, статус проводок по запасам не восстанавливается на *Зарегистрировано*. Поэтому после того, как поступление продуктов из входящей загрузки отменяется, работник склада должен повторно зарегистрировать количества номенклатур для загрузок.

Дополнительные сведения см. в разделе [Регистрация количества номенклатур, поступивших во входящей загрузке](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
