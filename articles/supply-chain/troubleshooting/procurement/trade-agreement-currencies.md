---
title: Проблемы при конвертации валюты в коммерческом соглашении
description: Цены коммерческого соглашения не пересчитываются в соответствии с валютой, когда валюта отличается в заказе на покупку.
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
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477380"
---
# <a name="trade-agreement-currency-conversion-issues"></a>Проблемы при конвертации валюты в коммерческом соглашении

## <a name="symptoms"></a>Симптомы

Цены коммерческого соглашения не пересчитываются в соответствии с валютой, когда валюта отличается в заказе на покупку.

## <a name="resolution"></a>Решение

Функция *Универсальная валюта* позволяет определять цены и скидки только в одной валюте. Затем можно выполнить преобразование в другие валюты по мере необходимости. Более того, после выполнения преобразования функция может автоматически применять психологическое округление.
