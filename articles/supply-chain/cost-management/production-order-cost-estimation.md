---
title: Оценка стоимости производственного заказа
description: В Этой статья представлена информация об оценке производственных затрат. Оценка стоимости производства обеспечивает вас информацией о предполагаемых затратах на потребление материалов и мощностей при производстве номенклатуры в том количестве, которое указано в спланированном производственном заказе.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59b93b41b74bd3f4cc480c8e60e8c69b25e40e51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830256"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="d3e6b-104">Оценка стоимости производственного заказа</span><span class="sxs-lookup"><span data-stu-id="d3e6b-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3e6b-105">В Этой статья представлена информация об оценке производственных затрат.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="d3e6b-106">Оценка стоимости производства обеспечивает вас информацией о предполагаемых затратах на потребление материалов и мощностей при производстве номенклатуры в том количестве, которое указано в спланированном производственном заказе.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="d3e6b-107">После создания производственного заказа, необходимо оценить производственных затрат.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="d3e6b-108">Назначение данной операции заключается в оценке потребления номенклатур и потребления на маршруте, связанного с производственным процессом, поскольку эти оценки формируют основу для последующих процессов планирования и производства.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="d3e6b-109">Оценка стоимости производства</span><span class="sxs-lookup"><span data-stu-id="d3e6b-109">Production cost estimation</span></span>
<span data-ttu-id="d3e6b-110">Оценки производственных затрат основаны на следующей информации:</span><span class="sxs-lookup"><span data-stu-id="d3e6b-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="d3e6b-111">Количество в производственном заказе</span><span class="sxs-lookup"><span data-stu-id="d3e6b-111">The quantity on the production order</span></span>
-   <span data-ttu-id="d3e6b-112">Компоненты в производственных спецификациях (BOM)</span><span class="sxs-lookup"><span data-stu-id="d3e6b-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="d3e6b-113">Операции маршрутизации в Маршруте Производства</span><span class="sxs-lookup"><span data-stu-id="d3e6b-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="d3e6b-114">Косвенные затраты, которые применяются к компонентам и операциям</span><span class="sxs-lookup"><span data-stu-id="d3e6b-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="d3e6b-115">Данные по активным затратам на дату расчета</span><span class="sxs-lookup"><span data-stu-id="d3e6b-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="d3e6b-116">Если в производственных спецификациях присутствуют строки искусственных номенклатур, расчеты отражают компоненты и операции маршрута искусственной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="d3e6b-117">Задача оценки может использоваться для повторного расчета оценочной стоимости, чтобы они отражали обновление информации.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="d3e6b-118">Например, обновленная информация может представлять собой изменения количества по производственному заказу, компонентов производственной спецификации, операций маршрутизации в составе производственного маршрута, косвенных затрат, которые относятся к данным компонентам и операциям, а также активных данных по затратам на дату повторного расчета.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="d3e6b-119">В рамках расчета оценочной стоимости также предлагается цена продажи производственной номенклатуры, рассчитанная по принципу "затраты плюс наценка".</span><span class="sxs-lookup"><span data-stu-id="d3e6b-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="d3e6b-120">Вычисления сметных затрат могут дополнительно применяться в отношении базисных заказов, отражающих другие производственные заказы, которые связаны с данным производственным заказом.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="d3e6b-121">Просмотр оценочных стоимостей</span><span class="sxs-lookup"><span data-stu-id="d3e6b-121">View the estimated costs</span></span>
<span data-ttu-id="d3e6b-122">После выполнения оценки можно просматривать результаты на странице **Расчет цены**.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="d3e6b-123">При проведении оценки вычисляются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d3e6b-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="d3e6b-124">**Производственные затраты** – производственные затраты представляют собой верхнюю строку оценки.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="d3e6b-125">Они отражают полные затраты на выполнение производственного заказа и итоговую цену продажи для этого производства.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="d3e6b-126">Данные затраты представляют собой сумму всех строк затрат, включенных в эту оценку.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="d3e6b-127">**Затраты маршрута или ресурса** — Затраты маршрута или ресурса — затраты по производственным операциям.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="d3e6b-128">Они включают стоимость таких элементов, как время настройки, время выполнения и накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="d3e6b-129">**Затраты на материалы** — Затраты на материалы представляют собой себестоимости и цены компонентов спецификации, необходимых для производства номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="d3e6b-130">Они определены и введены в систему заранее.</span><span class="sxs-lookup"><span data-stu-id="d3e6b-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="d3e6b-131">Другие способы применения оценки затрат</span><span class="sxs-lookup"><span data-stu-id="d3e6b-131">Other uses of cost estimation</span></span>
<span data-ttu-id="d3e6b-132">Оценка затрат также содержит следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="d3e6b-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="d3e6b-133">Осмысленные предложения по ценам</span><span class="sxs-lookup"><span data-stu-id="d3e6b-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="d3e6b-134">Оценки прибыльности этого заказа</span><span class="sxs-lookup"><span data-stu-id="d3e6b-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="d3e6b-135">Оценки использования сырья</span><span class="sxs-lookup"><span data-stu-id="d3e6b-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="d3e6b-136">Сравнения с информацией о затратах на предыдущие производства</span><span class="sxs-lookup"><span data-stu-id="d3e6b-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="d3e6b-137">Бюджетную и прогнозную информацию</span><span class="sxs-lookup"><span data-stu-id="d3e6b-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="d3e6b-138">Оценки объемов производства, необходимых для достижения конкретной величины затрат</span><span class="sxs-lookup"><span data-stu-id="d3e6b-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]