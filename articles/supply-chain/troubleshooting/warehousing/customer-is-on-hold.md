---
title: Невозможно подтвердить отгрузку, так как клиент заблокирован
description: Невозможно подтвердить отгрузку, так как клиент заблокирован.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344272"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Невозможно подтвердить отгрузку, так как клиент заблокирован

Код ошибки: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Симптомы

При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:

> Отгрузка %1 не может быть подтверждена, так как клиент заблокирован для %2.

Поэтому невозможно подтвердить отгрузку для загрузки.

## <a name="cause"></a>Причина

Счет клиента для загрузки или отгрузки заблокирован. Таким образом, статус клиента предотвращает подтверждение отгрузки.

## <a name="resolution"></a>Решение

Чтобы разблокировать счет клиента, необходимо выполнить следующие действия.

1. Перейдите в раздел **Расчеты с клиентами \> Клиенты \> Все клиенты**.
1. Открыть счет клиента, для которого невозможно подтвердить отгрузку.
1. На экспресс-вкладке **кредит и сборы** установите для поля **Блокировка выставления накладных и поставки** значение *нет*.
1. Повторите эту процедуру для всех заблокированных клиентов для загрузки.
