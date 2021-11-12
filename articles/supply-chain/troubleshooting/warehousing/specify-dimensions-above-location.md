---
title: Невозможно выпустить загрузку для частичного количества с иерархией выше партии
description: При использовании номенклатуры с иерархией резервирования выше партии в строках загрузки необходимо указать аналитики выше местоположения для распределения запасов.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477391"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Невозможно выпустить загрузку для частичного количества с иерархией резервирования выше партии

## <a name="symptoms"></a>Симптомы

При использовании номенклатуры, имеющей иерархию резервирования *партия выше*, команда **Запуск на склад** на странице **Рабочее место планирования загрузки** не работает, если попытаться выпустить загрузку для неполного количества. Появится следующее сообщение об ошибке:

> Для назначения волне в строках загрузки должны быть указаны аналитики, находящийся над местоположением. Чтобы назначить эти аналитики, зарезервируйте и заново создайте строку загрузки.

Однако при использовании номенклатуры, имеющей иерархию резервирования *партия ниже*, вы можете выпустить загрузку для частичного количества со страницы **Рабочее место планирования загрузки**.

## <a name="cause"></a>Причина

Когда аналитика находится над аналитикой **Местоположение** в иерархии резервирования, она должна быть указана до выпуска на склад. Запасы могут быть успешно распределены только в том случае, если в аналитиках выше местоположения нет разрывов.

## <a name="resolution"></a>Решение

Убедитесь, что все аналитики выше **местонахождение** назначены посредством резервирования и повторного создания строки загрузки.