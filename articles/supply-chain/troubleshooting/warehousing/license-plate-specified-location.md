---
title: Для этого места хранения должно быть указано грузоместо
description: Если эта ошибка возникает после создания заказа на перемещение для склада, на котором включена система управления складом, для транзитного склада "Местоположение поступления по умолчанию" остается пустым.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477383"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Ошибка спецификации грузомест при подтверждении отгрузки для заказа на перемещение

## <a name="symptoms"></a>Симптомы

Это сообщение об ошибке появляется, если заказ на перемещение создается с использованием склада, который активирован для расширенного управления складом (WMS), а затем, после завершения работы, вы пытаетесь подтвердить отгрузку:

> Для этого места хранения должно быть указано грузоместо.

## <a name="cause"></a>Причина

Это происходит потому, что поле **Местоположение поступления по умолчанию** пусто для транзитного склада у склада "из".

## <a name="resolution"></a>Решение

Чтобы решить эту проблему, необходимо указать местоположение прихода по умолчанию на транзитном складе. Убедитесь, что это местоположение управляется грузоместом.