---
title: Подготовка к поддержке стандартных затрат по произведенной номенклатуре
description: В этом разделе описываются шаги для подготовки к ведению затрат для произведенных номенклатур.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b35e424c582c173e3fa1f4d0a335106e413b6660
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967416"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="7af2b-103">Подготовка к поддержке стандартных затрат по произведенной номенклатуре</span><span class="sxs-lookup"><span data-stu-id="7af2b-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7af2b-104">В этом разделе описываются шаги для подготовки к ведению затрат для произведенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="7af2b-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="7af2b-105">Шаги для произведенных номенклатур немного отличаются от шагов для приобретенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="7af2b-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="7af2b-106">Политики, которые назначены произведенным номенклатурам, могут влиять на расчет затрат по родительским произведенным номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="7af2b-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="7af2b-107">Для подготовки к ведению затрат по произведенным номенклатурам выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7af2b-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="7af2b-108">Назначьте производимой номенклатуре группу номенклатурных моделей.</span><span class="sxs-lookup"><span data-stu-id="7af2b-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="7af2b-109">Группа номенклатурных моделей определяет, какие стандартные затраты будут использованы.</span><span class="sxs-lookup"><span data-stu-id="7af2b-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="7af2b-110">Назначьте произведенной номенклатуре номенклатурную группу.</span><span class="sxs-lookup"><span data-stu-id="7af2b-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="7af2b-111">Номенклатурная группа содержит счета ГК, которые относятся к произведенной номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="7af2b-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="7af2b-112">Счета ГК для произведенной номенклатуры, которая имеет складскую модель стандартных затрат, включают несколько отклонений цены производства от себестоимости, расхождение изменения себестоимости и переоценку себестоимости запасов.</span><span class="sxs-lookup"><span data-stu-id="7af2b-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="7af2b-113">Назначьте для номенклатуры единицу измерения складского учета.</span><span class="sxs-lookup"><span data-stu-id="7af2b-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="7af2b-114">Затраты по номенклатуре всегда выражаются в единицах измерения складского учета номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7af2b-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="7af2b-115">Не назначайте производимой номенклатуре группу затрат, если эта номенклатура не будет рассматриваться как приобретаемая номенклатура.</span><span class="sxs-lookup"><span data-stu-id="7af2b-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="7af2b-116">Назначьте произведенной номенклатуре группу расчета спецификации.</span><span class="sxs-lookup"><span data-stu-id="7af2b-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="7af2b-117">Группа расчета спецификации номенклатуры определяет действующие условия предупреждений.</span><span class="sxs-lookup"><span data-stu-id="7af2b-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="7af2b-118">Таким образом после завершения расчета спецификации могут создаваться предупреждающие сообщения о возможных источниках ошибок при расчете.</span><span class="sxs-lookup"><span data-stu-id="7af2b-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="7af2b-119">Например, предупреждающее сообщение может указать на то, что не существует активной спецификации или активного маршрута.</span><span class="sxs-lookup"><span data-stu-id="7af2b-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="7af2b-120">Группа расчета спецификации содержит политику развертывания, которая определяет, когда произведенную номенклатуру следует рассматривать как приобретенную номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="7af2b-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="7af2b-121">Если произведенная номенклатура имеет постоянные затраты, назначьте ей стандартное количество заказа.</span><span class="sxs-lookup"><span data-stu-id="7af2b-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="7af2b-122">Стандартное количество заказа — это размер учетного лота для амортизации постоянных затрат.</span><span class="sxs-lookup"><span data-stu-id="7af2b-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="7af2b-123">Примеры постоянных затрат включают время настройки в операциях маршрутизации и постоянное количество компонентов в спецификации.</span><span class="sxs-lookup"><span data-stu-id="7af2b-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="7af2b-124">Определите спецификацию для произведенной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7af2b-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="7af2b-125">Для произведенной номенклатуры можно определить одну или несколько версий спецификации.</span><span class="sxs-lookup"><span data-stu-id="7af2b-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="7af2b-126">Убедитесь в том, что версии, которые планируется использовать, утверждены и активны, а также в том, что даты действия этих версий соответствуют требуемым.</span><span class="sxs-lookup"><span data-stu-id="7af2b-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="7af2b-127">Версия спецификации может использоваться в масштабе компании или в рамках конкретного узла.</span><span class="sxs-lookup"><span data-stu-id="7af2b-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="7af2b-128">Определите маршрут для произведенной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7af2b-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="7af2b-129">Для произведенной номенклатуры можно определить одну или несколько версий маршрута.</span><span class="sxs-lookup"><span data-stu-id="7af2b-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="7af2b-130">Убедитесь в том, что версии, которые планируется использовать, утверждены и активны, а также в том, что даты действия этих версий соответствуют требуемым.</span><span class="sxs-lookup"><span data-stu-id="7af2b-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="7af2b-131">Версия маршрута должна использоваться в рамках конкретного узла.</span><span class="sxs-lookup"><span data-stu-id="7af2b-131">The route version must be site-specific.</span></span>

<span data-ttu-id="7af2b-132">Если требуется использовать информации о маршруте для целей калькуляции затрат, требуются дополнительные подготовительные шаги.</span><span class="sxs-lookup"><span data-stu-id="7af2b-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="7af2b-133">Например, потребуется обеспечить правильность и полноту категорий затрат, назначаемых операциям маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="7af2b-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="7af2b-134">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="7af2b-134">Related topics</span></span>
--------

[<span data-ttu-id="7af2b-135">Амортизации постоянных затрат для производимой номенклатуры</span><span class="sxs-lookup"><span data-stu-id="7af2b-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="7af2b-136">Настройка продуктов, которые можно произвести или приобрести</span><span class="sxs-lookup"><span data-stu-id="7af2b-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

