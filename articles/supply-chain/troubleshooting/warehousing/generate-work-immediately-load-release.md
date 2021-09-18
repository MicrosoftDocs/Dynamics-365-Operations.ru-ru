---
title: Сразу после выпуска груза создайте работы комплектации
description: Если работа должна быть создана сразу после выпуска загрузки, необходимо соответствующим образом настроить шаблон волны. Эта страница поможет выполнить все этапы.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477434"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Работа комплектации не создается сразу после выпуска исходящей загрузки

## <a name="symptoms"></a>Симптомы

Исходящую загрузку можно создать с помощью заказа на продажу или заказа на перемещение и выпустить загрузку на склад. Однако вы заметили, что никакая работа по комплектации еще не создана.

## <a name="resolution"></a>Решение

Если работа должна быть создана сразу после выпуска загрузки, необходимо соответствующим образом настроить шаблон волны. В шаблоне волны задайте для следующих параметров значение *Да*:

- Создавать волны автоматически
- Обрабатывать волну перед запуском на склад
- Автоматический запуск волны
