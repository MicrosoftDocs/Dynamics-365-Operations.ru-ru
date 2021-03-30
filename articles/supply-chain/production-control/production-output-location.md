---
title: Местонахождение получения из производства
description: В этой теме описывается иерархия, которая используется для идентификации местоположения получения из производства.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8fa4f7d844c178ee603778fa2f1def6bfc33db97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209451"
---
# <a name="production-output-location"></a><span data-ttu-id="9b412-103">Местонахождение получения из производства</span><span class="sxs-lookup"><span data-stu-id="9b412-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b412-104">В этой теме описывается иерархия, которая используется для идентификации местоположения получения из производства.</span><span class="sxs-lookup"><span data-stu-id="9b412-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="9b412-105">Местонахождение получения из производства является местоположением, в котором готовая продукция сначала хранится после производства.</span><span class="sxs-lookup"><span data-stu-id="9b412-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="9b412-106">Как правило, это местонахождение находится близко к производственному процессу, в котором производится готовая продукция.</span><span class="sxs-lookup"><span data-stu-id="9b412-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="9b412-107">Местоположение получения из производства используется как промежуточное хранилище материала до его перемещения в область отгрузки, местонахождение хранения, местонахождение поступлений на производство для дальнейшего производственного процесса и т. д.</span><span class="sxs-lookup"><span data-stu-id="9b412-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="9b412-108">Местонахождение получения из производства по умолчанию задается, когда готовая продукция регистрируется в производственном или партионном заказе.</span><span class="sxs-lookup"><span data-stu-id="9b412-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="9b412-109">Для идентификации этого местонахождения получения используется следующая иерархия:</span><span class="sxs-lookup"><span data-stu-id="9b412-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="9b412-110">Используйте местонахождение получения, определенное в заголовке производственного или партионного заказа.</span><span class="sxs-lookup"><span data-stu-id="9b412-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="9b412-111">Если местонахождение не обнаружено, используйте местоположение получения, которое определено в ресурсе, который используется в последней операции, определенной в маршруте производства.</span><span class="sxs-lookup"><span data-stu-id="9b412-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="9b412-112">Если местонахождение не обнаружено, используйте местоположение получения, которое определено в группе ресурсов, которая используется ресурсом в последней операции, определенной в маршруте производства.</span><span class="sxs-lookup"><span data-stu-id="9b412-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="9b412-113">Если местонахождение не обнаружено, используйте местоположение получения, которое определено в складе, определенном для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="9b412-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="9b412-114">Местонахождение получения из производства по умолчанию задается только для продуктов, которые были настроены с помощью расширенных процессов складов.</span><span class="sxs-lookup"><span data-stu-id="9b412-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="9b412-115">Когда принимается этот тип номенклатуры, создается работа склада типа **Размещение готовой продукции** или **Размещение побочных и попутных продуктов**.</span><span class="sxs-lookup"><span data-stu-id="9b412-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="9b412-116">Этот тип работы использует местонахождение получения из производства в качестве местонахождения комплектации.</span><span class="sxs-lookup"><span data-stu-id="9b412-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="9b412-117">Местонахождение размещения определяется директивами местонахождения.</span><span class="sxs-lookup"><span data-stu-id="9b412-117">The put-away location is determined by the location directives.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]