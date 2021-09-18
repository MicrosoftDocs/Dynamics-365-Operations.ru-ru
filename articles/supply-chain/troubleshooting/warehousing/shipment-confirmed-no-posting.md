---
title: Отгрузка для загрузки подтверждена, но строки не разнесены
description: Подтверждение отгрузки не влияет на разноску. Оно просто обновляет отгрузку и статус загрузки. Разноска должна выполняться в отдельном процессе.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e754f1461672c1e9f2d8dd1a7ceffc81f3809120
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477451"
---
# <a name="shipment-for-load-has-been-confirmed-but-no-lines-are-posted"></a>Отгрузка для загрузки подтверждена, но строки не разнесены

## <a name="symptoms"></a>Симптомы

При работе с исходящими складскими операциями можно получить следующее сообщение:

> Отгрузка для загрузки 1% подтверждена.

Однако дальнейшая разноска не выполнена.

## <a name="resolution"></a>Решение

Это предусмотрено разработчиками. Подтверждение отгрузки не влияет на разноску. Оно просто обновляет отгрузку и статус загрузки. Разноска должна выполняться в отдельном процессе.
