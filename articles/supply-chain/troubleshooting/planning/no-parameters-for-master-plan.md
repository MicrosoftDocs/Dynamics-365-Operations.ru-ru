---
title: Параметры для сводного плана не существуют
description: При попытке утверждения спланированного заказа выводится сообщение об ошибке, в котором говорится, что для сводного плана не существует параметров.
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
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294166"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Параметры для сводного плана не существуют

Код ошибки: SYS25368

## <a name="symptoms"></a>Симптомы

При попытке утвердить спланированный заказ выводится следующее сообщение об ошибке:

> Параметры для сводного плана %1 не существуют.

## <a name="cause"></a>Причина

Из-за ошибок конфигурации система не может найти настройки для указанного плана.

## <a name="resolution"></a>Решение

- Перейдите **Сводное планирование \> Настройка \> Планы \> Сводные планы** и убедитесь, что существует план с указанным именем.
