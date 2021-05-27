---
title: Спланированный заказ на покупку создается, когда в течение отрицательных дней существует покупка
description: Если код покрытия — мин/макс, оптимизация планирования создает спланированный заказ на покупку, когда в течение отрицательных дней существует покупка.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026853"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="25e51-103">Спланированный заказ на покупку создается, когда в течение отрицательных дней существует покупка</span><span class="sxs-lookup"><span data-stu-id="25e51-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="25e51-104">Номер статьи базы знаний: 4614298</span><span class="sxs-lookup"><span data-stu-id="25e51-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="25e51-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="25e51-105">Symptoms</span></span>

<span data-ttu-id="25e51-106">Если код покрытия — *Мин/макс*, оптимизация планирования создает спланированный заказ на покупку, когда в течение отрицательных дней существует покупка.</span><span class="sxs-lookup"><span data-stu-id="25e51-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="25e51-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="25e51-107">Resolution</span></span>

<span data-ttu-id="25e51-108">Оптимизация планирования не поддерживает отрицательные дни.</span><span class="sxs-lookup"><span data-stu-id="25e51-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="25e51-109">Однако всегда гарантируется, что спланированные заказы не будут планироваться в течение времени упреждения относительно текущей даты.</span><span class="sxs-lookup"><span data-stu-id="25e51-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="25e51-110">Например, время упреждения покупки — 10 дней, а прибытие заказа на покупку ожидается через восемь дней от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="25e51-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="25e51-111">В этом случае заказ на покупку будет использоваться как поставка для спроса, которая составляет пять дней от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="25e51-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="25e51-112">Таким образом, рекомендуется настроить времена упреждения, чтобы охватить все (или почти все) сценарии.</span><span class="sxs-lookup"><span data-stu-id="25e51-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
