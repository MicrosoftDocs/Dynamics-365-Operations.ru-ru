---
title: "\"Выбрать позднее\" не учитывается, когда производственные заказы сбрасываются с помощью пакетного задания"
description: Если для сброса статуса производственного заказа используется повторяющееся пакетное задание, выборы с задержкой не учитываются.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026841"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>"Выбрать позднее" не учитывается, когда производственные заказы сбрасываются с помощью пакетного задания

Номер статьи базы знаний: 4614634

## <a name="symptoms"></a>Симптомы

Если для сброса статуса производственного заказа используется повторяющееся пакетное задание, выборы с задержкой не учитываются.

## <a name="resolution"></a>Приказ

Текущая система не поддерживает использование отложенных выборов для процесса *Статус сброса*.
