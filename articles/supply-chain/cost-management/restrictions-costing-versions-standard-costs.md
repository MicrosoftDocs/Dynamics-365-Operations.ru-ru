---
title: "Ограничения на версии учета затрат для стандартных затрат"
description: "В этом разделе рассматриваются ограничения, которые применяются в отношении версии цены для стандартных затрат."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: adc77f632fecebc39e818fa38f78071842ec8de4
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="90012-103">Ограничения на версии учета затрат для стандартных затрат</span><span class="sxs-lookup"><span data-stu-id="90012-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90012-104">В этом разделе рассматриваются ограничения, которые применяются в отношении версии цены для стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="90012-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="90012-105">Следующие ограничения помогают обеспечить соблюдение принципов расчета стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="90012-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="90012-106">Накладные расходы должны быть включены в затраты по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="90012-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="90012-107">Накладные расходы для произведенной номенклатуры отражают амортизированные постоянные затраты в спецификации (BOM) и информации о маршруте.</span><span class="sxs-lookup"><span data-stu-id="90012-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="90012-108">Поэтому эти расходы необходимо включить в затраты на единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="90012-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="90012-109">Накладные расходы для приобретенной номенклатуры также включаются в затраты на единицу измерения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="90012-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="90012-110">Вычисление стандартных затрат для произведенных номенклатур должно быть основано на записях затрат в рамках версии цены для стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="90012-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="90012-111">Альтернативный источник данных по затратам можно использовать только с версией цены для плановых затрат, например, с торговыми соглашениями о закупочных ценах для приобретенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="90012-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="90012-112">Альтернативные источники данных по затратам определяются группой расчета спецификации.</span><span class="sxs-lookup"><span data-stu-id="90012-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="90012-113">Расчеты спецификации должны выполняться с использованием одноуровневого режима развертывания.</span><span class="sxs-lookup"><span data-stu-id="90012-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="90012-114">Данные о затратах по номенклатуре для стандартных затрат можно скопировать в другую версию цены, которая содержит стандартные затраты или плановые затраты.</span><span class="sxs-lookup"><span data-stu-id="90012-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="90012-115">Однако данные о затратах для плановых затрат невозможно скопировать в версию цены, содержащую стандартные затраты, поскольку ограничения, перечисленные раньше в этом разделе, не применяются по отношению к плановым затратам.</span><span class="sxs-lookup"><span data-stu-id="90012-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="90012-116">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="90012-116">Related topics</span></span>
--------

[<span data-ttu-id="90012-117">Версии цены</span><span class="sxs-lookup"><span data-stu-id="90012-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="90012-118">Обновление стандартных затрат в непроизводственной среде</span><span class="sxs-lookup"><span data-stu-id="90012-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="90012-119">Подготовка к поддержке стандартных затрат по произведенной номенклатуре</span><span class="sxs-lookup"><span data-stu-id="90012-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


