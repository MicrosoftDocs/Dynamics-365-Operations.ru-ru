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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719559"
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
