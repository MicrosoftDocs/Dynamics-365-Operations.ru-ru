---
title: Владельцу запасов не разрешается при обработке передвижений
description: Возможно появление сообщения об ошибке "Владелец запасов %1 не разрешен." Процессы управления складом поддерживают только запасы, которыми владеет юридическое лицо.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477392"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Владельцу запасов не разрешается при обработке передвижений в приложении склада

## <a name="symptoms"></a>Симптомы

Вы получаете это сообщение об ошибке в мобильном приложении Warehouse Management при обработке передвижений:

> Владелец запасов %1 разрешен в этом процессе.

## <a name="cause"></a>Причина

Это происходит потому, что аналитика отслеживания **Владелец** отсутствует, если мобильное приложение Warehouse Management используется для выполнения перемещений. Обычный журнал перемещения запасов из клиента Supply Chain Management будет работать правильно и может быть разнесен только в том случае, если заполнена аналитика **Владелец**.

## <a name="resolution"></a>Решение

Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции. В настоящее время процессы управления складом поддерживают только запасы, которыми владеет юридическое лицо.
