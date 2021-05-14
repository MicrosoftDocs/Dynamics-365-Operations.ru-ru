---
title: Работа не заблокирована
description: Работа не заблокирована
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924212"
---
# <a name="work-isnt-blocked"></a>Работа не заблокирована

Код ошибки: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Симптомы

Система отобразит следующее сообщение об ошибке:

> Работа с кодом %1 не заблокирована.

## <a name="cause"></a>Причина

Параметр **Заблокированная волна** в волне задан как *Нет*. Работа не может быть разблокирована, поскольку в данный момент она не заблокирована.

## <a name="resolution"></a>Приказ

 Может быть разблокирована только та работа, параметр которой **Заблокированная волна** задан как *Да*.
