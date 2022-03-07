---
title: Невозможно подтвердить отгрузку из-за проблемы с календарем
description: Невозможно подтвердить отгрузку из-за проблемы с календарем
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938541"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Невозможно подтвердить отгрузку из-за проблемы с календарем

Код ошибки: TRX2716

## <a name="symptoms"></a>Симптомы

При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:

> Тип календаря %1 требует отметки прихода на встречу %2 и ухода с нее.

Поэтому невозможно подтвердить отгрузку для загрузки.

## <a name="cause"></a>Причина

Для данной загрузки имеются активные встречи. Например, имеется правило, требующее прибытия водителя. Поэтому загрузка в данный момент находится в состоянии, когда подтверждение отгрузки не выполняется.

## <a name="resolution"></a>Приказ

Необходимо изучить и устранить все проблемы с активными встречами, связанными с данной загрузкой.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Выберите загрузку, для которой невозможно подтвердить отгрузку.
1. В области действий на вкладке **Транспортировка** в группе **Встречи** выберите **Планирование встречи**.
1. Выполните одно из следующих действий.

    - Убедитесь, что для встречи завершено прибытие/отбытие водителя.
    - Завершите или отмените встречу.
    - Отключите параметр **Требуется регистрация прибытия водителя** для соответствующего правила встречи.
