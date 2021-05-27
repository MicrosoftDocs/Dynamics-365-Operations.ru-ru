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
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="3f0ed-103">"Выбрать позднее" не учитывается, когда производственные заказы сбрасываются с помощью пакетного задания</span><span class="sxs-lookup"><span data-stu-id="3f0ed-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="3f0ed-104">Номер статьи базы знаний: 4614634</span><span class="sxs-lookup"><span data-stu-id="3f0ed-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="3f0ed-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="3f0ed-105">Symptoms</span></span>

<span data-ttu-id="3f0ed-106">Если для сброса статуса производственного заказа используется повторяющееся пакетное задание, выборы с задержкой не учитываются.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="3f0ed-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="3f0ed-107">Resolution</span></span>

<span data-ttu-id="3f0ed-108">Текущая система не поддерживает использование отложенных выборов для процесса *Статус сброса*.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
