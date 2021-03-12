---
title: Оценка стоимости производственного заказа
description: В Этой статья представлена информация об оценке производственных затрат. Оценка стоимости производства обеспечивает вас информацией о предполагаемых затратах на потребление материалов и мощностей при производстве номенклатуры в том количестве, которое указано в спланированном производственном заказе.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 53f54c64b1c78e7385f0fde5ad1023c5b4e0af4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967316"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="75560-104">Оценка стоимости производственного заказа</span><span class="sxs-lookup"><span data-stu-id="75560-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75560-105">В Этой статья представлена информация об оценке производственных затрат.</span><span class="sxs-lookup"><span data-stu-id="75560-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="75560-106">Оценка стоимости производства обеспечивает вас информацией о предполагаемых затратах на потребление материалов и мощностей при производстве номенклатуры в том количестве, которое указано в спланированном производственном заказе.</span><span class="sxs-lookup"><span data-stu-id="75560-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="75560-107">После создания производственного заказа, необходимо оценить производственных затрат.</span><span class="sxs-lookup"><span data-stu-id="75560-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="75560-108">Назначение данной операции заключается в оценке потребления номенклатур и потребления на маршруте, связанного с производственным процессом, поскольку эти оценки формируют основу для последующих процессов планирования и производства.</span><span class="sxs-lookup"><span data-stu-id="75560-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="75560-109">Оценка стоимости производства</span><span class="sxs-lookup"><span data-stu-id="75560-109">Production cost estimation</span></span>
<span data-ttu-id="75560-110">Оценки производственных затрат основаны на следующей информации:</span><span class="sxs-lookup"><span data-stu-id="75560-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="75560-111">Количество в производственном заказе</span><span class="sxs-lookup"><span data-stu-id="75560-111">The quantity on the production order</span></span>
-   <span data-ttu-id="75560-112">Компоненты в производственных спецификациях (BOM)</span><span class="sxs-lookup"><span data-stu-id="75560-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="75560-113">Операции маршрутизации в Маршруте Производства</span><span class="sxs-lookup"><span data-stu-id="75560-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="75560-114">Косвенные затраты, которые применяются к компонентам и операциям</span><span class="sxs-lookup"><span data-stu-id="75560-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="75560-115">Данные по активным затратам на дату расчета</span><span class="sxs-lookup"><span data-stu-id="75560-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="75560-116">Если в производственных спецификациях присутствуют строки искусственных номенклатур, расчеты отражают компоненты и операции маршрута искусственной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="75560-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="75560-117">Задача оценки может использоваться для повторного расчета оценочной стоимости, чтобы они отражали обновление информации.</span><span class="sxs-lookup"><span data-stu-id="75560-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="75560-118">Например, обновленная информация может представлять собой изменения количества по производственному заказу, компонентов производственной спецификации, операций маршрутизации в составе производственного маршрута, косвенных затрат, которые относятся к данным компонентам и операциям, а также активных данных по затратам на дату повторного расчета.</span><span class="sxs-lookup"><span data-stu-id="75560-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="75560-119">В рамках расчета оценочной стоимости также предлагается цена продажи производственной номенклатуры, рассчитанная по принципу "затраты плюс наценка".</span><span class="sxs-lookup"><span data-stu-id="75560-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="75560-120">Вычисления сметных затрат могут дополнительно применяться в отношении базисных заказов, отражающих другие производственные заказы, которые связаны с данным производственным заказом.</span><span class="sxs-lookup"><span data-stu-id="75560-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="75560-121">Просмотр оценочных стоимостей</span><span class="sxs-lookup"><span data-stu-id="75560-121">View the estimated costs</span></span>
<span data-ttu-id="75560-122">После выполнения оценки можно просматривать результаты на странице **Расчет цены**.</span><span class="sxs-lookup"><span data-stu-id="75560-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="75560-123">При проведении оценки вычисляются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="75560-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="75560-124">**Производственные затраты** – производственные затраты представляют собой верхнюю строку оценки.</span><span class="sxs-lookup"><span data-stu-id="75560-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="75560-125">Они отражают полные затраты на выполнение производственного заказа и итоговую цену продажи для этого производства.</span><span class="sxs-lookup"><span data-stu-id="75560-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="75560-126">Данные затраты представляют собой сумму всех строк затрат, включенных в эту оценку.</span><span class="sxs-lookup"><span data-stu-id="75560-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="75560-127">**Затраты маршрута или ресурса** — Затраты маршрута или ресурса — затраты по производственным операциям.</span><span class="sxs-lookup"><span data-stu-id="75560-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="75560-128">Они включают стоимость таких элементов, как время настройки, время выполнения и накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="75560-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="75560-129">**Затраты на материалы** — Затраты на материалы представляют собой себестоимости и цены компонентов спецификации, необходимых для производства номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="75560-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="75560-130">Они определены и введены в систему заранее.</span><span class="sxs-lookup"><span data-stu-id="75560-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="75560-131">Другие способы применения оценки затрат</span><span class="sxs-lookup"><span data-stu-id="75560-131">Other uses of cost estimation</span></span>
<span data-ttu-id="75560-132">Оценка затрат также содержит следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="75560-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="75560-133">Осмысленные предложения по ценам</span><span class="sxs-lookup"><span data-stu-id="75560-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="75560-134">Оценки прибыльности этого заказа</span><span class="sxs-lookup"><span data-stu-id="75560-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="75560-135">Оценки использования сырья</span><span class="sxs-lookup"><span data-stu-id="75560-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="75560-136">Сравнения с информацией о затратах на предыдущие производства</span><span class="sxs-lookup"><span data-stu-id="75560-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="75560-137">Бюджетную и прогнозную информацию</span><span class="sxs-lookup"><span data-stu-id="75560-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="75560-138">Оценки объемов производства, необходимых для достижения конкретной величины затрат</span><span class="sxs-lookup"><span data-stu-id="75560-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




