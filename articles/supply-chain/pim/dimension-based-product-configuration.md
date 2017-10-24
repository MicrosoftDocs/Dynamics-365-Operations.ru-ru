---
title: "Конфигурация продукта на основе аналитик"
description: "Конфигурация продукта на основе аналитик представляет простое решение для создания нескольких вариантов продукта из одного шаблона продукта и его спецификации."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e2ce0e95a5e1230df970b5d5249fdb248113cf54
ms.openlocfilehash: b6895726af6028035830893fdbb01a4a407d7076
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="fc354-103">Конфигурация продукта на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="fc354-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fc354-104">Конфигурация продукта на основе аналитик представляет простое решение для создания нескольких вариантов продукта из одного шаблона продукта и его спецификации.</span><span class="sxs-lookup"><span data-stu-id="fc354-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="fc354-105">Конфигурация продукта на основе аналитик — это одна из трех встроенных технологий конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="fc354-106">Две другие технологии — это предопределенные варианты и конфигурация на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="fc354-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="fc354-107">Все три технологии используют шаблон продукта как отправную точку и позволяют пользователю создавать множество вариантов продукта для одного шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="fc354-108">Ключевые понятия</span><span class="sxs-lookup"><span data-stu-id="fc354-108">Key concepts</span></span>
<span data-ttu-id="fc354-109">Конфигурация продукта на основе аналитики основана на следующих ключевых понятиях:</span><span class="sxs-lookup"><span data-stu-id="fc354-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="fc354-110">Шаблоны продукта</span><span class="sxs-lookup"><span data-stu-id="fc354-110">Product masters</span></span>
-   <span data-ttu-id="fc354-111">Аналитика продукта конфигурации</span><span class="sxs-lookup"><span data-stu-id="fc354-111">Configuration product dimension</span></span>
-   <span data-ttu-id="fc354-112">Конфигурационные группы</span><span class="sxs-lookup"><span data-stu-id="fc354-112">Configuration groups</span></span>
-   <span data-ttu-id="fc354-113">Спецификация (BOM)</span><span class="sxs-lookup"><span data-stu-id="fc354-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="fc354-114">Конфигурационный маршрут</span><span class="sxs-lookup"><span data-stu-id="fc354-114">Configuration route</span></span>
-   <span data-ttu-id="fc354-115">Правила конфигурации</span><span class="sxs-lookup"><span data-stu-id="fc354-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="fc354-116">Шаблоны продукта</span><span class="sxs-lookup"><span data-stu-id="fc354-116">Product masters</span></span>

<span data-ttu-id="fc354-117">Шаблон продукта — это отправная точка для любого процесса конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="fc354-118">В случае конфигурации продукта на основе аналитики необходим шаблон продукта с этой определенной технологией конфигурации и группа аналитик продукта, которая включает аналитику продукта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fc354-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="fc354-119">Аналитика продукта конфигурации</span><span class="sxs-lookup"><span data-stu-id="fc354-119">Configuration product dimension</span></span>

<span data-ttu-id="fc354-120">Аналитика продукта конфигурации используется для определения вариантов продукта для шаблона продукта с технологией конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="fc354-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="fc354-121">Значение аналитики конфигурации вводится пользователем и должно помочь определить отдельные варианты продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="fc354-122">Конфигурационные группы</span><span class="sxs-lookup"><span data-stu-id="fc354-122">Configuration groups</span></span>

<span data-ttu-id="fc354-123">Конфигурационные группы определяются в центральном репозитории и могут использоваться для всех моделей конфигурации продукта на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="fc354-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="fc354-124">Конфигурационные группы связаны с отдельными строками спецификации и вместе составляют группу строк, которые являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="fc354-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="fc354-125">Это значит что только одну строку в группе можно выбрать для одного варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="fc354-126">Спецификация (BOM)</span><span class="sxs-lookup"><span data-stu-id="fc354-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="fc354-127">Спецификация представляет строительные блоки для конфигурации продукта на основе аналитики.</span><span class="sxs-lookup"><span data-stu-id="fc354-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="fc354-128">Она должна включать все различные продукты, которые можно использовать в любом варианте продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="fc354-129">Каждая строка в конфигурации может ссылаться на конфигурационную группу.</span><span class="sxs-lookup"><span data-stu-id="fc354-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="fc354-130">Если строка не ссылается на конфигурационную группу, она будет включена во все варианты продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="fc354-131">Конфигурационный маршрут</span><span class="sxs-lookup"><span data-stu-id="fc354-131">Configuration route</span></span>

<span data-ttu-id="fc354-132">Конфигурационный маршрут определяет последовательность конфигурационных групп по мере того, как они отображаются пользователю в процессе конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="fc354-133">Правила конфигурации</span><span class="sxs-lookup"><span data-stu-id="fc354-133">Configuration rules</span></span>

<span data-ttu-id="fc354-134">Правила конфигурации представляют механизм, гарантирующий, что продукт, включенный в одну конфигурационную группу в спецификации, приведет либо к включению, либо исключению продукта в другой конфигурационной группе в той же спецификации.</span><span class="sxs-lookup"><span data-stu-id="fc354-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="fc354-135">Процесс моделирования продукта</span><span class="sxs-lookup"><span data-stu-id="fc354-135">Product modeling process</span></span>
<span data-ttu-id="fc354-136">Естественная последовательность создания модели продукта для продукта на основе аналитики начинается с определения соответствующих конфигурационных групп.</span><span class="sxs-lookup"><span data-stu-id="fc354-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="fc354-137">Важно гарантировать, что все продукты, которые будут использоваться в конфигурации, были выпущены в компании, для которой создается модель продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="fc354-138">С помощью этих строительных блоков пользователь может создать спецификацию и назначить конфигурационные группы всем соответствующим строкам спецификации.</span><span class="sxs-lookup"><span data-stu-id="fc354-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="fc354-139">По завершении спецификации можно определить конфигурационный маршрут для организации конфигурационных групп в правильной последовательности.</span><span class="sxs-lookup"><span data-stu-id="fc354-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="fc354-140">[![Процесс моделирования продуктов на основе аналитик](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Если имеются определенные продукты из других конфигурационных групп, которые должны или не должны использоваться вместе, можно создать правила конфигурации, которые будут определять отношения этих продуктов.</span><span class="sxs-lookup"><span data-stu-id="fc354-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="fc354-141">После привязки спецификации к шаблону продукта на основе аналитики с помощью версии спецификации, их утверждения и активации можно создать конфигурации продукта и ввести имя для каждой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fc354-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="fc354-142">Конфигурации можно определить перед созданием проводок, или когда есть потребность в определенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fc354-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="fc354-143">Предполагаемое использование</span><span class="sxs-lookup"><span data-stu-id="fc354-143">Suggested use</span></span>

<span data-ttu-id="fc354-144">Технология конфигурация на основе аналитик рекомендуется использовать для продуктов с ограниченной изменчивостью, и когда сочетание стандартного размера, цвета, стиля и конфигурации аналитик продукта не подходит для определения конкретного варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="fc354-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="fc354-145">Примером может служить велосипед с высотой рамы, размером колес, типами тормозов и различными передачами.</span><span class="sxs-lookup"><span data-stu-id="fc354-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="fc354-146">Далее</span><span class="sxs-lookup"><span data-stu-id="fc354-146">Next step</span></span> 

<span data-ttu-id="fc354-147">Следующие восемь проводников по задачам указаны в том в порядке, в каком их следует выполнять.</span><span class="sxs-lookup"><span data-stu-id="fc354-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="fc354-148">Создание шаблона продукта на основе аналитик (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="fc354-149">Выпуск шаблона продукта на основе аналитик (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="fc354-150">Завершение базовой настройки шаблона запущенных в производство продуктов (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="fc354-151">Определение конфигурационных групп (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="fc354-152">Создание спецификации для шаблона продукта на основе аналитик (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="fc354-153">Определение конфигурационных маршрутов (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="fc354-154">Создание правил конфигурации (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="fc354-155">Создание конфигураций на основе аналитик (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc354-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)


