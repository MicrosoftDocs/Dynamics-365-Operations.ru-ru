---
title: Номенклатура набора не поддерживается во внутрихолдинговом процессе
description: Номенклатура набора недоступна для покупки. Заказ на продажу покупает только компоненты номенклатуры набора, но не саму номенклатуру набора.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477418"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Номенклатура набора не поддерживается во внутрихолдинговом процессе

## <a name="symptoms"></a>Симптомы

Номенклатура набора недоступна для заказа на покупку, поскольку, если исследовать строки заказа на продажу для номенклатуры набора, вы увидите, что количество равно *0* (нулю) и статус *Отменено*.

## <a name="resolution"></a>Решение

Такое поведение предусмотрено разработчиками. Заказ на продажу покупает только компоненты номенклатуры набора. Он не покупает саму номенклатуру набора. Если необходимо купить набор, подумайте, следует ли помечать его как номенклатуру набора, так как эта функция разработана для сценариев распознавания выручки. Дополнительные сведения о номенклатурах наборов см. в разделе [Наборы](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
