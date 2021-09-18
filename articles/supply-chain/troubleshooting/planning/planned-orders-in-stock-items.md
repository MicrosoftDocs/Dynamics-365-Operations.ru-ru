---
title: Спланированные заказы создаются для запасов в производственных заказах
description: Спланированные заказы создаются даже в том случае, если имеются номенклатуры в запасах и производственные заказы уже существуют для них
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
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477465"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Спланированные заказы создаются для запасов в производственных заказах

## <a name="symptoms"></a>Симптомы

Спланированные заказы создаются даже в том случае, если имеются номенклатуры в запасах и производственные заказы уже существуют для них.

## <a name="resolution"></a>Решение

Возможно, вы сможете устранить эту проблему, увеличив значение **Положительные дни** для соответствующих групп на странице **Группа покрытия**. Это изменение приведет к тому, что система определит, можно ли использовать запасы в наличии для спроса. Затем новый спланированный заказ не будет создаваться для номенклатур в наличии.
