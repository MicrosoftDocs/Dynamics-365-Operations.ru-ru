---
title: Невозможно подтвердить отгрузку, так как имеется нулевое количество
description: Невозможно подтвердить отгрузку, так как имеется нулевое количество
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938538"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Невозможно подтвердить отгрузку, так как имеется нулевое количество

Код ошибки: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Симптомы

При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:

> Строка загрузки для номенклатуры %1 и отгрузки %2 обновлена и теперь имеет нулевое количество из-за настройки недопоставки, что позволяет не отгружать какие-либо количества для этого номенклатуры.

Поэтому невозможно подтвердить отгрузку для загрузки.

## <a name="cause"></a>Причина

Система проверяет, находится ли скомплектованное количество в ожидаемых пределах на основе скомплектованного количества, количества в строке загрузки и процента недопоставки. Если система обнаруживает, что скомплектованное количество в строке загрузки равно 0 (нулю), невозможно подтвердить отгрузку. Например, эта проблема может возникнуть, если работа была отменена, а процент недопоставки в строке загрузки равен 100 процентам.

## <a name="resolution"></a>Приказ

Проверьте строки загрузки, чтобы убедиться, что процент недопоставки и количества недопоставки соответствуют скомплектованной работе.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Выберите загрузку, для которой невозможно подтвердить отгрузку.
1. На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент недопоставки.
1. Измените значение в поле **Недопоставка** или в поле **Количество**, как необходимо.

> [!TIP]
> Если проблема все еще не исправлена, возможно, придется выполнить дополнительную работу комплектации для соответствующих заказов на продажу или заказов на перемещение до тех пор, пока доступное количество не будет соответствовать загрузке или отгрузке.
