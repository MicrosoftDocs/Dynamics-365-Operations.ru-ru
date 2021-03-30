---
title: Ограничения на версии учета затрат для стандартных затрат
description: В этом разделе рассматриваются ограничения, которые применяются в отношении версии цены для стандартных затрат.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f8f5707b6f51372684606d135c0643b36e3a94f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245259"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="749dc-103">Ограничения на версии учета затрат для стандартных затрат</span><span class="sxs-lookup"><span data-stu-id="749dc-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="749dc-104">В этом разделе рассматриваются ограничения, которые применяются в отношении версии цены для стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="749dc-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="749dc-105">Следующие ограничения помогают обеспечить соблюдение принципов расчета стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="749dc-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="749dc-106">Накладные расходы должны быть включены в затраты по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="749dc-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="749dc-107">Накладные расходы для произведенной номенклатуры отражают амортизированные постоянные затраты в спецификации (BOM) и информации о маршруте.</span><span class="sxs-lookup"><span data-stu-id="749dc-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="749dc-108">Поэтому эти расходы необходимо включить в затраты на единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="749dc-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="749dc-109">Накладные расходы для приобретенной номенклатуры также включаются в затраты на единицу измерения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="749dc-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="749dc-110">Вычисление стандартных затрат для произведенных номенклатур должно быть основано на записях затрат в рамках версии цены для стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="749dc-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="749dc-111">Альтернативный источник данных по затратам можно использовать только с версией цены для плановых затрат, например, с торговыми соглашениями о закупочных ценах для приобретенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="749dc-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="749dc-112">Альтернативные источники данных по затратам определяются группой расчета спецификации.</span><span class="sxs-lookup"><span data-stu-id="749dc-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="749dc-113">Расчеты спецификации должны выполняться с использованием одноуровневого режима развертывания.</span><span class="sxs-lookup"><span data-stu-id="749dc-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="749dc-114">Данные о затратах по номенклатуре для стандартных затрат можно скопировать в другую версию цены, которая содержит стандартные затраты или плановые затраты.</span><span class="sxs-lookup"><span data-stu-id="749dc-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="749dc-115">Однако данные о затратах для плановых затрат невозможно скопировать в версию цены, содержащую стандартные затраты, поскольку ограничения, перечисленные раньше в этом разделе, не применяются по отношению к плановым затратам.</span><span class="sxs-lookup"><span data-stu-id="749dc-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="749dc-116">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="749dc-116">Related topics</span></span>
--------

[<span data-ttu-id="749dc-117">Обзор версий учета затрат</span><span class="sxs-lookup"><span data-stu-id="749dc-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="749dc-118">Обновление стандартных затрат в непроизводственной среде</span><span class="sxs-lookup"><span data-stu-id="749dc-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="749dc-119">Подготовка к поддержке стандартных затрат по произведенной номенклатуре</span><span class="sxs-lookup"><span data-stu-id="749dc-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]