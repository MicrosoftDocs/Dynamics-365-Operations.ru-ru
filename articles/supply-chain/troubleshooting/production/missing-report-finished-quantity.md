---
title: Обновление приемки завершилось с ошибкой отсутствия количества
description: Если вы попытаетесь завершить производственный заказ, сообщая количество ошибок, но не время или количество материала, обновление приемки завершится ошибкой.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477387"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Обновление приемки завершилось с ошибкой отсутствия количества

## <a name="symptoms"></a>Симптомы

Вы пытаетесь сообщить о завершении производственного заказа, сообщая ошибочное количество, но не сообщая о времени или количестве материала. Обновление приемки завершилось с ошибкой при попытке завершения производственного заказа, и появится следующее сообщение об ошибке:

> Отсутствует количество, готовое к приемке.

## <a name="resolution"></a>Решение

Если вы сообщаете ошибочное количество по производственному заказу, вы также должны сообщить количество товаров.
