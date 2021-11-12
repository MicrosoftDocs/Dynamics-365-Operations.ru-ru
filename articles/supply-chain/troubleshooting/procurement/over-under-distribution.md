---
title: Распределения по бухгалтерским счетам выполнены с чрезмерным или недостаточным распределением
description: Одно или несколько распределений по бухгалтерским счетам выполнены с чрезмерным или недостаточным распределением.
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
ms.openlocfilehash: 7ff0172469df50da9e4272b3fa3f75001a4eb7eb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477414"
---
# <a name="accounting-distributions-are-either-over--or-under-distributed"></a>Распределения по бухгалтерским счетам выполнены с чрезмерным или недостаточным распределением


## <a name="symptoms"></a>Симптомы

Вы получите следующее сообщение об ошибке:

> Одно или несколько распределений по бухгалтерским счетам выполнено с чрезмерным или недостаточным распределением

## <a name="cause"></a>Причина

Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.

## <a name="resolution"></a>Решение

Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик*, перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**. Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).