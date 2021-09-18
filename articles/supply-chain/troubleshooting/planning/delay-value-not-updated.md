---
title: Значение задержки не обновляется при перепланировании спланированного заказа
description: Значение задержки не обновляется при перепланировании спланированного заказа
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 566702913774cf002ab38e367f690a479d968657
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477439"
---
# <a name="the-delay-value-isnt-updated-when-you-reschedule-a-planned-order"></a>Значение задержки не обновляется при перепланировании спланированного заказа

## <a name="symptoms"></a>Симптомы

Значение задержки не обновляется при перепланировании спланированного заказа.

## <a name="resolution"></a>Решение

Чтобы обновить задержку для спланированных заказов, откройте диалоговое окно **Перепланирование** для спланированного заказа. На экспресс-вкладке **Развертывание** убедитесь, что параметр **Выполнить развертывание после перепланирования** имеет значение *Да*.
