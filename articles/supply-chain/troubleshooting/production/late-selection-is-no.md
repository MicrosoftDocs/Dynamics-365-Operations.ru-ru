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
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741964"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>"Выбрать позднее" не учитывается, когда производственные заказы сбрасываются с помощью пакетного задания

Номер статьи базы знаний: 4614634

## <a name="symptoms"></a>Симптомы

Если для сброса статуса производственного заказа используется повторяющееся пакетное задание, выборы с задержкой не учитываются.

## <a name="resolution"></a>Приказ

Текущая система не поддерживает использование отложенных выборов для процесса *Статус сброса*.
