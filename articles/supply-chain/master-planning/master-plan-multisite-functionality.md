---
title: "Сводное планирование и функция работы с несколькими узлами"
description: "При сводном планировании учитываются настройки складских аналитик сайта и склада."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 10981e0fe201566c83fd28c792000865bc533cd3
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="e7535-103">Сводное планирование и функция работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="e7535-103">Master planning and multisite functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7535-104">При сводном планировании учитываются настройки складских аналитик сайта и склада.</span><span class="sxs-lookup"><span data-stu-id="e7535-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="e7535-105">Аналитика сайта является обязательной; аналитику склада можно настроить как обязательную.</span><span class="sxs-lookup"><span data-stu-id="e7535-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="e7535-106">Если аналитика является обязательной, значение этой аналитики должно быть введено во всех складских проводках.</span><span class="sxs-lookup"><span data-stu-id="e7535-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="e7535-107">Поэтому при сводном планировании узел и склад для начального спроса известны.</span><span class="sxs-lookup"><span data-stu-id="e7535-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="e7535-108">Аналитика узла также согласована, так что во время развертывания спроса нижнего уровня значение узла не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e7535-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="e7535-109">Если склад не настроен как обязательный, он может быть неизвестен для начального спроса.</span><span class="sxs-lookup"><span data-stu-id="e7535-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="e7535-110">Механизм планирования должен определить, какой склад использовать, на основе настроек, которые определяются для номенклатуры, отдельных складов и сведений строки заказа.</span><span class="sxs-lookup"><span data-stu-id="e7535-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="e7535-111">Следующие разделы описывают работу механизма планирования с различными настройками для определения склада, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="e7535-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="e7535-112">Сводное планирование — покрытие объекта и склада, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="e7535-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="e7535-113">Сводное планирование — покрытие объекта, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="e7535-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="e7535-114">Сводное планирование — покрытие объекта и склада, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="e7535-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="e7535-115">Сводное планирование — покрытие объекта, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="e7535-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="e7535-116">Сводное планирование — Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="e7535-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




