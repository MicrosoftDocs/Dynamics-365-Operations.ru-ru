---
title: Обновление задачи поступления продуктов подтверждает неподтвержденные заказы
description: После выполнения обновления поступлений продуктов система подтверждает неподтвержденные заказы, имеющие статус "зарегистрировано". Узнайте о функции, которая устраняет эту проблему.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477381"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Неподтвержденные заказы на покупку подтверждаются после обновления поступлений продуктов

## <a name="symptoms"></a>Симптомы

После запуска периодической задачи *Обновление поступлений продуктов* система автоматически подтверждает неподтвержденные заказы на покупку, имеющие статус складской проводки *Зарегистрировано*.

## <a name="resolution"></a>Решение

Новая функция обработки входящей загрузки *Получение сверх количества загрузки* решает эту проблему. Чтобы включить эту функцию, перейдите в рабочую область [Управление функциями](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) и включите следующие функции в порядке, в котором они перечислены:

1. Связать складские проводки по заказу на покупку с загрузкой
2. Получение сверх количества загрузки

Дополнительные сведения см. в разделе [Разноска зарегистрированных количеств товаров по заказам на покупку](/dynamics365/supply-chain/warehousing/inbound-load-handling).
