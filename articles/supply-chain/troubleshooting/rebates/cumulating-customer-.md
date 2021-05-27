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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026837"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="fa8f9-103">Накопление ретробонусов клиента не выполняется, когда используются группы ретробонусов номенклатур</span><span class="sxs-lookup"><span data-stu-id="fa8f9-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="fa8f9-104">Номер статьи базы знаний: 4611372</span><span class="sxs-lookup"><span data-stu-id="fa8f9-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="fa8f9-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="fa8f9-105">Symptoms</span></span>

<span data-ttu-id="fa8f9-106">При использовании соглашений о ретробонусах клиента (с типом *сумма*) в сочетании с группами ретробонусов номенклатур ретробонусы рассчитываются, но накопление не работает.</span><span class="sxs-lookup"><span data-stu-id="fa8f9-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="fa8f9-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="fa8f9-107">Resolution</span></span>

<span data-ttu-id="fa8f9-108">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="fa8f9-108">The system is behaving as designed.</span></span> <span data-ttu-id="fa8f9-109">Номенклатурные группы содержат только те номенклатуры, у которых одинаковое условие порога.</span><span class="sxs-lookup"><span data-stu-id="fa8f9-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="fa8f9-110">Условие ретробонуса (порог) устанавливается на сумму для каждой номенклатуры, а не на совокупную сумму для каждой номенклатуры в группе номенклатур.</span><span class="sxs-lookup"><span data-stu-id="fa8f9-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
