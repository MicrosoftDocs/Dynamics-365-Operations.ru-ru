---
title: Ретробонус поставщика не накапливается на основе накладных
description: Ретробонус поставщика не накапливается на основе накладных
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477459"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Ретробонус поставщика не накапливается на основе накладных

## <a name="symptoms"></a>Симптомы

Если накладные, которые разносятся, имеют разные сроки исполнения, эти накладные не отражаются в бонусах поставщика, которые создаются из них.

## <a name="resolution"></a>Решение

Срок выполнения не учитывается при расчете бонуса поставщика. Рассмотрите возможность настройки системы таким образом, чтобы дата исполнения и связь с накладной были более очевидны по отношению к фактической бонусу поставщика.
