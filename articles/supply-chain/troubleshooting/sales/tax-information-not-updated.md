---
title: При изменении местонахождения заказа на продажу налоговая информация не обновляется
description: Если сайт, склад или адрес доставки изменяется в заголовке заказа на продажу, налоговая информация не обновляется автоматически для строк. Это необходимо сделать вручную.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477420"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>При изменении местонахождения в заголовке заказа на продажу налоговая информация не обновляется

## <a name="symptoms"></a>Симптомы

Если сайт, склад или адрес доставки изменяется в заголовке заказа на продажу, налоговая информация не обновляется автоматически для строк.

## <a name="resolution"></a>Решение

Такое поведение предусмотрено разработчиками. Проблема возникает потому, что адрес доставки, сайт и склад не изменяются автоматически на уровне строки. Их необходимо обновить вручную.
