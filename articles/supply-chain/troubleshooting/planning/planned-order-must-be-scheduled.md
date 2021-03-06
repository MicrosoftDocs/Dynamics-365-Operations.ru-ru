---
title: Спланированный производственный заказ должен быть запланирован до утверждения
description: При попытке утверждения спланированного заказа выводится сообщение об ошибке, в котором указывается, что заказ должен быть запланирован до утверждения.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294168"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Спланированный производственный заказ должен быть запланирован до утверждения

Код ошибки: SYS309802

## <a name="symptoms"></a>Симптомы

При попытке утвердить спланированный заказ выводится следующее сообщение об ошибке:

> Спланированный производственный заказ необходимо запланировать до его утверждения.

## <a name="cause"></a>Причина

Запланированные даты начала и окончания не могут быть пустыми.

## <a name="resolution"></a>Решение

Чтобы указать даты начала и окончания для спланированного заказа, выполните следующие действия.

1. Перейдите в раздел **Сводное планирование \> Сводное планирование \> Спланированные заказы**.
1. Откройте соответствующий спланированный заказ.
1. На экспресс-вкладке **Общие** в разделе **Запланировано** укажите даты в полях **Дата начала** и **Дата окончания**.
