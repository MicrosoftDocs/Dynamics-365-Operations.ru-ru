---
title: Ошибка "не задана ссылка на объект" в ходе подтверждения заказа на покупку
description: Ошибка "не задана ссылка на объект" в ходе подтверждения заказа на покупку
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477437"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>Ошибка "не задана ссылка на объект" в ходе подтверждения заказа на покупку

## <a name="symptoms"></a>Симптомы

При подтверждении заказа на покупку появится следующее исключение:

> Ссылка на объект не задана

## <a name="cause"></a>Причина

Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.

## <a name="resolution"></a>Решение

Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик*, перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**. Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).