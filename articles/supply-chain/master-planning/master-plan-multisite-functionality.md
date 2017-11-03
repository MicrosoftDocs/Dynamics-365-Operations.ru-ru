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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6800668741bfd86555b72faf8cce01f73cb9a278
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="8fb11-103">Сводное планирование и функция работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="8fb11-103">Master planning and multisite functionality</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8fb11-104">При сводном планировании учитываются настройки складских аналитик сайта и склада.</span><span class="sxs-lookup"><span data-stu-id="8fb11-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="8fb11-105">Аналитика сайта является обязательной; аналитику склада можно настроить как обязательную.</span><span class="sxs-lookup"><span data-stu-id="8fb11-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="8fb11-106">Если аналитика является обязательной, значение этой аналитики должно быть введено во всех складских проводках.</span><span class="sxs-lookup"><span data-stu-id="8fb11-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="8fb11-107">Поэтому при сводном планировании узел и склад для начального спроса известны.</span><span class="sxs-lookup"><span data-stu-id="8fb11-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="8fb11-108">Аналитика узла также согласована, так что во время развертывания спроса нижнего уровня значение узла не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8fb11-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="8fb11-109">Если склад не настроен как обязательный, он может быть неизвестен для начального спроса.</span><span class="sxs-lookup"><span data-stu-id="8fb11-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="8fb11-110">Механизм планирования должен определить, какой склад использовать, на основе настроек, которые определяются для номенклатуры, отдельных складов и сведений строки заказа.</span><span class="sxs-lookup"><span data-stu-id="8fb11-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="8fb11-111">Следующие разделы описывают работу механизма планирования с различными настройками для определения склада, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="8fb11-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="8fb11-112">Сводное планирование — покрытие объекта и склада, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="8fb11-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="8fb11-113">Сводное планирование — покрытие объекта, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="8fb11-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="8fb11-114">Сводное планирование — покрытие объекта и склада, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="8fb11-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="8fb11-115">Сводное планирование — покрытие объекта, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="8fb11-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="8fb11-116">Сводное планирование — Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="8fb11-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




