---
title: "Обновление стандартных затрат в производственной среде"
description: "Эта статья содержит рекомендации по обновлению стандартных затрат в производственной среде."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="9a727-103">Обновление стандартных затрат в производственной среде</span><span class="sxs-lookup"><span data-stu-id="9a727-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9a727-104">Эта статья содержит рекомендации по обновлению стандартных затрат в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="9a727-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="9a727-105">Обновления могут отражать новые номенклатуры, категории затрат или формулы расчета косвенных затрат.</span><span class="sxs-lookup"><span data-stu-id="9a727-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="9a727-106">Они могут отражать также исправления и изменения затрат.</span><span class="sxs-lookup"><span data-stu-id="9a727-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="9a727-107">Тип обновления будет определять действия, необходимые для обновления стандартных затрат, что иллюстрируется следующими примерами.</span><span class="sxs-lookup"><span data-stu-id="9a727-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="9a727-108">Введите ожидаемые изменения стандартных затрат для приобретенных номенклатур, а затем измените статус записей затрат на номенклатуру (на **активно**) на соответствующую дату.</span><span class="sxs-lookup"><span data-stu-id="9a727-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="9a727-109">Но не перерассчитывайте затраты на произведенные номенклатуры, в которых используются приобретенные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="9a727-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="9a727-110">Введите стандартные затраты для новой приобретенной номенклатуры, но не перерассчитывайте затраты на произведенные номенклатуры с версией спецификации, содержащей новую приобретенную номенклатуру как компонент.</span><span class="sxs-lookup"><span data-stu-id="9a727-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="9a727-111">Исправьте или измените затраты на приобретенную номенклатуру или измените группу затрат, назначенную приобретенной номенклатуре, и рассчитайте затраты на все произведенные номенклатуры с версией спецификации, которая содержит приобретенную номенклатуру как компонент.</span><span class="sxs-lookup"><span data-stu-id="9a727-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="9a727-112">Измените затраты для категории затрат и рассчитайте затраты на все произведенные номенклатуры с версией маршрута, содержащей операции маршрута, которые используют категорию затрат.</span><span class="sxs-lookup"><span data-stu-id="9a727-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="9a727-113">Измените категории затрат, связанные с операциями маршрутизации, или группу затрат, связанные с категориями затрат.</span><span class="sxs-lookup"><span data-stu-id="9a727-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="9a727-114">Затем рассчитайте затраты на все произведенные номенклатуры с версией маршрута, содержащей операции маршрута, которые используют категорию затрат.</span><span class="sxs-lookup"><span data-stu-id="9a727-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="9a727-115">Измените формулу расчета косвенных затрат и рассчитайте затраты для всех произведенных номенклатур, на которые влияет это изменение.</span><span class="sxs-lookup"><span data-stu-id="9a727-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="9a727-116">Измените или добавьте производственный узел для произведенной номенклатуры и рассчитайте затраты для произведенной номенклатуры для этого узла.</span><span class="sxs-lookup"><span data-stu-id="9a727-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="9a727-117">Рассчитайте (или перерассчитайте) затраты для произведенной номенклатуры и перерассчитайте затраты для всех произведенных номенклатур с версией спецификации, содержащей произведенную номенклатуру как компонент.</span><span class="sxs-lookup"><span data-stu-id="9a727-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="9a727-118">Рассчитайте затраты для новой произведенной номенклатуры на основе сведений о ее определенной, утвержденной и активной спецификации и о маршруте.</span><span class="sxs-lookup"><span data-stu-id="9a727-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="9a727-119">Каждый пример требует тщательного изучения способа обновления стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="9a727-119">Each case requires careful consideration about how to update standard costs.</span></span>




