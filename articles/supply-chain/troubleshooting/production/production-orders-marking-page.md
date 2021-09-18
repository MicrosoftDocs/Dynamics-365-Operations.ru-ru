---
title: Производственные заказы не отображаются на странице маркировки
description: Некоторые производственные заказы не отображаются на странице Маркировка. В этом разделе описываются три конфигурации продукта, которые недоступны для маркировки.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477362"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Производственные заказы не отображаются на странице маркировки

## <a name="symptoms"></a>Симптомы

При работе с дискретным производством некоторые производственные заказы не отображаются на странице **маркировка**.

## <a name="resolution"></a>Решение

Продукты, имеющие следующую конфигурации, недоступны для маркировки. Поэтому они не будут отображаться на странице **Маркировка**:

- Продукты определяются как продукты типа *учет в двух единицах измерения*.
- Они включены для дополнительных складских процессов.
- Они настраиваются для управления с помощью принципа *Стандартные затраты*.
