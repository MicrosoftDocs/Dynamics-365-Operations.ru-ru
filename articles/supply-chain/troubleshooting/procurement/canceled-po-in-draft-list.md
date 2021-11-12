---
title: Отмененные заказы на покупку отображаются в списке черновиков в рабочей области
description: Отмененные заказы на покупку отображаются в списке черновиков в рабочей области подготовки заказов на покупку
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477438"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Отмененные заказы на покупку отображаются в списке черновиков в рабочей области

## <a name="symptoms"></a>Симптомы

После отмены заказов на покупку, которые были в состоянии *Подтверждено*, отмененные заказы на покупку все равно появляются в списке черновиков заказов на покупку в рабочей области **Подготовка заказов на покупку**.

## <a name="resolution"></a>Решение

Эта проблема возникает только для заказов на покупку, для которых используется управление изменениями. Это происходит из-за того, что отмена рассматривается как изменение, которое необходимо утвердить. Утверждение может быть выполнено автоматически системой. Таким образом, процесс заключается в отправке отмененного заказа на покупку в рабочий поток утверждения, чтобы он мог перейти в состояние *Утверждено*. В этот момент заказ на покупку больше не будет отображаться в списке черновиков заказов на покупку в рабочей области **Подготовка заказов на покупку**.