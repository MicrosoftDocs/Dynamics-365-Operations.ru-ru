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
ms.openlocfilehash: 49faa2c68d496c5c0d8c7e4abfd93d9a917857220dd23c09a050fa3436e1d49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746875"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Физически полученные заказы на покупку не отображаются в отчете закрытия склада

Номер статьи базы знаний: 4612595

## <a name="symptoms"></a>Симптомы

Физически полученные заказы на покупку не отображаются в отчете закрытия склада **Проверка открытых количеств**.

## <a name="resolution"></a>Приказ

В отчете **Проверка открытых количеств** отображаются проводки расхода, которые невозможно сопоставить с финансово обновленными приходами запасов по состоянию на выбранную дату закрытия. Можно включить в отчет физические приходы. В этом случае физические приходы будут отображаться, если они могут охватывать проводки расхода, которые невозможно сопоставить. Дополнительные сведения см. в разделе [Подготовка к закрытию складов](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
