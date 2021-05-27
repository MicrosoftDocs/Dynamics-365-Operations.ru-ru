---
title: Физически полученные заказы на покупку не отображаются в отчете закрытия склада
description: Физически полученные заказы на покупку не отображаются в отчете закрытия склада "Проверка открытых количеств".
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026847"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Физически полученные заказы на покупку не отображаются в отчете закрытия склада

Номер статьи базы знаний: 4612595

## <a name="symptoms"></a>Симптомы

Физически полученные заказы на покупку не отображаются в отчете закрытия склада **Проверка открытых количеств**.

## <a name="resolution"></a>Приказ

В отчете **Проверка открытых количеств** отображаются проводки расхода, которые невозможно сопоставить с финансово обновленными приходами запасов по состоянию на выбранную дату закрытия. Можно включить в отчет физические приходы. В этом случае физические приходы будут отображаться, если они могут охватывать проводки расхода, которые невозможно сопоставить. Дополнительные сведения см. в разделе [Подготовка к закрытию складов](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
