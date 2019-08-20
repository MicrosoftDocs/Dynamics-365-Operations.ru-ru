---
title: Расчет спецификации с помощью многоуровневой структуры (февраль 2016 г.)
description: В этой процедуре показано, как рассчитать затраты на готовую продукцию с помощью многоуровневого развертывания, основанного на схеме калькуляции.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0834baf42ed6aa10acec6529513e44ff52ab754
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845650"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="92aaf-103">Расчет спецификации с помощью многоуровневой структуры (февраль 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="92aaf-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92aaf-104">В этой процедуре показано, как рассчитать затраты на готовую продукцию с помощью многоуровневого развертывания, основанного на схеме калькуляции.</span><span class="sxs-lookup"><span data-stu-id="92aaf-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="92aaf-105">Это седьмая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="92aaf-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="92aaf-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="92aaf-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="92aaf-107">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="92aaf-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="92aaf-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="92aaf-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="92aaf-109">Выберите продукт BOM_1.</span><span class="sxs-lookup"><span data-stu-id="92aaf-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="92aaf-110">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="92aaf-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="92aaf-111">Щелкните "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="92aaf-111">Click Item price.</span></span>
5. <span data-ttu-id="92aaf-112">Щелкните "Расчет себестоимости номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="92aaf-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="92aaf-113">Может потребоваться нажать кнопку с многоточием (...), чтобы увидеть этот параметр в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="92aaf-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="92aaf-114">В поле "Версия стоимости" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="92aaf-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="92aaf-115">Выберите версию расчета себестоимости 20, поскольку это тип запланированных затрат и режим развертывания — многоуровневый.</span><span class="sxs-lookup"><span data-stu-id="92aaf-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="92aaf-116">Многоуровневой режим развертывания предназначен для запланированных затрат и моделирования.</span><span class="sxs-lookup"><span data-stu-id="92aaf-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="92aaf-117">Он не используется для стандартной себестоимости.</span><span class="sxs-lookup"><span data-stu-id="92aaf-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="92aaf-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="92aaf-118">Click OK.</span></span>
8. <span data-ttu-id="92aaf-119">Щелкните "Просмотреть сведения расчета".</span><span class="sxs-lookup"><span data-stu-id="92aaf-119">Click View calculation details.</span></span>
    * <span data-ttu-id="92aaf-120">Может потребоваться нажать кнопку с многоточием (...), чтобы увидеть этот параметр в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="92aaf-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="92aaf-121">В этом случае обратите внимание на то, как была рассчитана BOM_2, учитывая сырье, процесс и накладные расходы общей суммой 29,40, вместо стандартной себестоимости 10, которая была активирована в первоначальном руководстве по задаче в этой серии.</span><span class="sxs-lookup"><span data-stu-id="92aaf-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="92aaf-122">Перейдите на вкладку "Схема калькуляции".</span><span class="sxs-lookup"><span data-stu-id="92aaf-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="92aaf-123">Если перейти на вкладку "Схема калькуляции", итоговые значения по группам затрат отличаются по сравнению с расчетом, выполненным в предыдущем руководстве по задаче.</span><span class="sxs-lookup"><span data-stu-id="92aaf-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="92aaf-124">В поле "Уровень" выберите "Мульти".</span><span class="sxs-lookup"><span data-stu-id="92aaf-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="92aaf-125">При выборе значения "Мульти" затраты классифицируются согласно составу BOM_2, где 10 — производное значение от группы затрат M1 (ITEM_C), а 15,60 — от производства, где группой затрат является L2.</span><span class="sxs-lookup"><span data-stu-id="92aaf-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="92aaf-126">Косвенные затраты также отличаются.</span><span class="sxs-lookup"><span data-stu-id="92aaf-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="92aaf-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="92aaf-127">Close the page.</span></span>
12. <span data-ttu-id="92aaf-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="92aaf-128">Close the page.</span></span>

