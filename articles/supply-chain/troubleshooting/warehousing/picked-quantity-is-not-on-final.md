---
title: Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы
description: Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938539"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы

Код ошибки: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Симптомы

При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:

> Некоторые из номенклатур, которые требуются для загрузки %1, еще не скомплектованы и не перемещены в местонахождение конечной отгрузки.

Поэтому невозможно подтвердить отгрузку для загрузки.

## <a name="cause"></a>Причина

Невозможно подтвердить загрузку в ее текущем состоянии, так как могут существовать следующие условия:

- Связанная работа еще не скомплектована и не перемещена в конечную ячейку отгрузки.
- Скомплектованное количество работы не соответствует созданному количеству работы в строке загрузки.

## <a name="resolution"></a>Приказ

Проверьте соответствующие заказы на продажу или заказы на перемещение для загрузки или отгрузки. Убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Выберите загрузку, для которой невозможно подтвердить отгрузку.
1. На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.
1. Запишите значение поля **Созданное количество работы**.
1. В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.
1. Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.
1. Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.
