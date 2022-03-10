---
title: Накопление ретробонусов клиента не выполняется, когда используются группы ретробонусов номенклатур
description: При использовании соглашений о ретробонусах клиента в сочетании с группами ретробонусов номенклатур ретробонусы рассчитываются, но накопление не работает.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760378"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Накопление ретробонусов клиента не выполняется, когда используются группы ретробонусов номенклатур

Номер статьи базы знаний: 4611372

## <a name="symptoms"></a>Симптомы

При использовании соглашений о ретробонусах клиента (с типом *сумма*) в сочетании с группами ретробонусов номенклатур ретробонусы рассчитываются, но накопление не работает.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. Номенклатурные группы содержат только те номенклатуры, у которых одинаковое условие порога. Условие ретробонуса (порог) устанавливается на сумму для каждой номенклатуры, а не на совокупную сумму для каждой номенклатуры в группе номенклатур.
