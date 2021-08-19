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
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012205"
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
