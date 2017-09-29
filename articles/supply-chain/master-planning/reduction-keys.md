---
title: "Ключи сокращения"
description: "В этой статье приведены примеры с описанием порядка настройки ключа сокращения. Она включает сведения о нескольких настройках ключа сокращения и результатах каждого. Можно использовать ключ сокращения для определения способа снижения требований прогноза."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 30634b0af343ad171c385a95c4ba0934180f70cf
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="d6761-105">Ключи сокращения</span><span class="sxs-lookup"><span data-stu-id="d6761-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d6761-106">В этой статье приведены примеры с описанием порядка настройки ключа сокращения.</span><span class="sxs-lookup"><span data-stu-id="d6761-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="d6761-107">Она включает сведения о нескольких настройках ключа сокращения и результатах каждого.</span><span class="sxs-lookup"><span data-stu-id="d6761-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="d6761-108">Можно использовать ключ сокращения для определения способа снижения требований прогноза.</span><span class="sxs-lookup"><span data-stu-id="d6761-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="d6761-109">Пример 1. Проценты — принцип сокращения прогноза ключа сокращения</span><span class="sxs-lookup"><span data-stu-id="d6761-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="d6761-110">В этом примере показано, как ключ сокращения уменьшает требования к прогнозу спроса в соответствии с процентами и периодами, определенными ключом сокращения.</span><span class="sxs-lookup"><span data-stu-id="d6761-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="d6761-111">На странице **Ключи сокращения** настройте следующие строки.</span><span class="sxs-lookup"><span data-stu-id="d6761-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="d6761-112">Сдача</span><span class="sxs-lookup"><span data-stu-id="d6761-112">Change</span></span> | <span data-ttu-id="d6761-113">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="d6761-113">Unit</span></span>  | <span data-ttu-id="d6761-114">Процент</span><span class="sxs-lookup"><span data-stu-id="d6761-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="d6761-115">1</span><span class="sxs-lookup"><span data-stu-id="d6761-115">1</span></span>      | <span data-ttu-id="d6761-116">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-116">Month</span></span> | <span data-ttu-id="d6761-117">100</span><span class="sxs-lookup"><span data-stu-id="d6761-117">100</span></span>     |
    | <span data-ttu-id="d6761-118">2</span><span class="sxs-lookup"><span data-stu-id="d6761-118">2</span></span>      | <span data-ttu-id="d6761-119">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-119">Month</span></span> | <span data-ttu-id="d6761-120">75</span><span class="sxs-lookup"><span data-stu-id="d6761-120">75</span></span>      |
    | <span data-ttu-id="d6761-121">3</span><span class="sxs-lookup"><span data-stu-id="d6761-121">3</span></span>      | <span data-ttu-id="d6761-122">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-122">Month</span></span> | <span data-ttu-id="d6761-123">50</span><span class="sxs-lookup"><span data-stu-id="d6761-123">50</span></span>      |
    | <span data-ttu-id="d6761-124">4</span><span class="sxs-lookup"><span data-stu-id="d6761-124">4</span></span>      | <span data-ttu-id="d6761-125">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-125">Month</span></span> | <span data-ttu-id="d6761-126">25</span><span class="sxs-lookup"><span data-stu-id="d6761-126">25</span></span>      |

2.  <span data-ttu-id="d6761-127">Свяжите ключ сокращения с группой покрытия номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="d6761-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="d6761-128">На странице **Сводные планы** в поле **Принцип сокращения** выберите значение **Процент - ключ сокращения**.</span><span class="sxs-lookup"><span data-stu-id="d6761-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="d6761-129">Создайте прогноз спроса на 1 000 штук в месяц.</span><span class="sxs-lookup"><span data-stu-id="d6761-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="d6761-130">Если начать прогнозное планирование 1-го января, требования к прогнозу спроса используются в соответствии с процентами, которые настроены на странице **Ключи сокращения**.</span><span class="sxs-lookup"><span data-stu-id="d6761-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="d6761-131">Следующие требуемые количества передаются в сводный план.</span><span class="sxs-lookup"><span data-stu-id="d6761-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="d6761-132">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-132">Month</span></span>                | <span data-ttu-id="d6761-133">Необходимое количество фрагментов</span><span class="sxs-lookup"><span data-stu-id="d6761-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="d6761-134">Январь</span><span class="sxs-lookup"><span data-stu-id="d6761-134">January</span></span>              | <span data-ttu-id="d6761-135">0</span><span class="sxs-lookup"><span data-stu-id="d6761-135">0</span></span>                         |
| <span data-ttu-id="d6761-136">Февраль</span><span class="sxs-lookup"><span data-stu-id="d6761-136">February</span></span>             | <span data-ttu-id="d6761-137">250</span><span class="sxs-lookup"><span data-stu-id="d6761-137">250</span></span>                       |
| <span data-ttu-id="d6761-138">Март</span><span class="sxs-lookup"><span data-stu-id="d6761-138">March</span></span>                | <span data-ttu-id="d6761-139">500</span><span class="sxs-lookup"><span data-stu-id="d6761-139">500</span></span>                       |
| <span data-ttu-id="d6761-140">апреля</span><span class="sxs-lookup"><span data-stu-id="d6761-140">April</span></span>                | <span data-ttu-id="d6761-141">750</span><span class="sxs-lookup"><span data-stu-id="d6761-141">750</span></span>                       |
| <span data-ttu-id="d6761-142">Май – декабрь</span><span class="sxs-lookup"><span data-stu-id="d6761-142">May through December</span></span> | <span data-ttu-id="d6761-143">1000</span><span class="sxs-lookup"><span data-stu-id="d6761-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="d6761-144">Пример 2. Проводки — принцип сокращения прогноза ключа сокращения</span><span class="sxs-lookup"><span data-stu-id="d6761-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="d6761-145">В этом примере показано, как фактические заказы, которые возникают в течение периодов, которые определены ключом сокращения, уменьшают требования к прогнозу спроса.</span><span class="sxs-lookup"><span data-stu-id="d6761-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="d6761-146">На странице **Сводные планы** в поле **Принцип сокращения** выберите значение **Проводки - ключ сокращения**.</span><span class="sxs-lookup"><span data-stu-id="d6761-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="d6761-147">На 1 января существуют следующие заказы.</span><span class="sxs-lookup"><span data-stu-id="d6761-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="d6761-148">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-148">Month</span></span>    | <span data-ttu-id="d6761-149">Количество заказанных единиц</span><span class="sxs-lookup"><span data-stu-id="d6761-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="d6761-150">Январь</span><span class="sxs-lookup"><span data-stu-id="d6761-150">January</span></span>  | <span data-ttu-id="d6761-151">956</span><span class="sxs-lookup"><span data-stu-id="d6761-151">956</span></span>                      |
| <span data-ttu-id="d6761-152">Февраль</span><span class="sxs-lookup"><span data-stu-id="d6761-152">February</span></span> | <span data-ttu-id="d6761-153">1 176</span><span class="sxs-lookup"><span data-stu-id="d6761-153">1,176</span></span>                    |
| <span data-ttu-id="d6761-154">Март</span><span class="sxs-lookup"><span data-stu-id="d6761-154">March</span></span>    | <span data-ttu-id="d6761-155">451</span><span class="sxs-lookup"><span data-stu-id="d6761-155">451</span></span>                      |
| <span data-ttu-id="d6761-156">Апрель</span><span class="sxs-lookup"><span data-stu-id="d6761-156">April</span></span>    | <span data-ttu-id="d6761-157">119</span><span class="sxs-lookup"><span data-stu-id="d6761-157">119</span></span>                      |

<span data-ttu-id="d6761-158">Если использовать тот же самый прогноз спроса на 1 000 шт. в месяц, в сводный план попадут следующие требуемые количества.</span><span class="sxs-lookup"><span data-stu-id="d6761-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="d6761-159">Месяц</span><span class="sxs-lookup"><span data-stu-id="d6761-159">Month</span></span>                | <span data-ttu-id="d6761-160">Необходимое количество фрагментов</span><span class="sxs-lookup"><span data-stu-id="d6761-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="d6761-161">Январь</span><span class="sxs-lookup"><span data-stu-id="d6761-161">January</span></span>              | <span data-ttu-id="d6761-162">44</span><span class="sxs-lookup"><span data-stu-id="d6761-162">44</span></span>                        |
| <span data-ttu-id="d6761-163">Февраль</span><span class="sxs-lookup"><span data-stu-id="d6761-163">February</span></span>             | <span data-ttu-id="d6761-164">0</span><span class="sxs-lookup"><span data-stu-id="d6761-164">0</span></span>                         |
| <span data-ttu-id="d6761-165">Март</span><span class="sxs-lookup"><span data-stu-id="d6761-165">March</span></span>                | <span data-ttu-id="d6761-166">549</span><span class="sxs-lookup"><span data-stu-id="d6761-166">549</span></span>                       |
| <span data-ttu-id="d6761-167">апреля</span><span class="sxs-lookup"><span data-stu-id="d6761-167">April</span></span>                | <span data-ttu-id="d6761-168">881</span><span class="sxs-lookup"><span data-stu-id="d6761-168">881</span></span>                       |
| <span data-ttu-id="d6761-169">Май – декабрь</span><span class="sxs-lookup"><span data-stu-id="d6761-169">May through December</span></span> | <span data-ttu-id="d6761-170">1000</span><span class="sxs-lookup"><span data-stu-id="d6761-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="d6761-171">Пример 3. Проводки — принцип сокращения прогноза динамического периода</span><span class="sxs-lookup"><span data-stu-id="d6761-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="d6761-172">В большинстве случаев системы настроены так, что проводки уменьшают прогноз спроса в пределах определенных периодов прогноза: недели, месяцы и так далее.</span><span class="sxs-lookup"><span data-stu-id="d6761-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="d6761-173">Эти периоды определены в ключе сокращения.</span><span class="sxs-lookup"><span data-stu-id="d6761-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="d6761-174">Однако время между двумя строками прогноза спроса также может *подразумевать* период.</span><span class="sxs-lookup"><span data-stu-id="d6761-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="d6761-175">Создайте прогноз спроса для следующих дат и количеств.</span><span class="sxs-lookup"><span data-stu-id="d6761-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="d6761-176">Дата</span><span class="sxs-lookup"><span data-stu-id="d6761-176">Date</span></span>       | <span data-ttu-id="d6761-177">Прогноз спроса</span><span class="sxs-lookup"><span data-stu-id="d6761-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="d6761-178">1 января</span><span class="sxs-lookup"><span data-stu-id="d6761-178">January 1</span></span>  | <span data-ttu-id="d6761-179">1000</span><span class="sxs-lookup"><span data-stu-id="d6761-179">1,000</span></span>           |
    | <span data-ttu-id="d6761-180">5 января</span><span class="sxs-lookup"><span data-stu-id="d6761-180">January 5</span></span>  | <span data-ttu-id="d6761-181">500</span><span class="sxs-lookup"><span data-stu-id="d6761-181">500</span></span>             |
    | <span data-ttu-id="d6761-182">12 января</span><span class="sxs-lookup"><span data-stu-id="d6761-182">January 12</span></span> | <span data-ttu-id="d6761-183">1000</span><span class="sxs-lookup"><span data-stu-id="d6761-183">1,000</span></span>           |

    <span data-ttu-id="d6761-184">В этом прогнозе нет явного периода между датами прогноза: между первой и второй датами имеется период в четыре дня, и между второй и третьей датами имеется период в семь дней.</span><span class="sxs-lookup"><span data-stu-id="d6761-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="d6761-185">Эти различные периоды представляют собой динамические периоды.</span><span class="sxs-lookup"><span data-stu-id="d6761-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="d6761-186">Создайте строки заказа на продажу, как указано ниже.</span><span class="sxs-lookup"><span data-stu-id="d6761-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="d6761-187">Дата</span><span class="sxs-lookup"><span data-stu-id="d6761-187">Date</span></span>                             | <span data-ttu-id="d6761-188">Количество заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="d6761-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="d6761-189">15-е декабря предыдущего года</span><span class="sxs-lookup"><span data-stu-id="d6761-189">December 15 in the previous year</span></span> | <span data-ttu-id="d6761-190">500</span><span class="sxs-lookup"><span data-stu-id="d6761-190">500</span></span>                  |
    | <span data-ttu-id="d6761-191">3 января</span><span class="sxs-lookup"><span data-stu-id="d6761-191">January 3</span></span>                        | <span data-ttu-id="d6761-192">100</span><span class="sxs-lookup"><span data-stu-id="d6761-192">100</span></span>                  |
    | <span data-ttu-id="d6761-193">10 января</span><span class="sxs-lookup"><span data-stu-id="d6761-193">January 10</span></span>                       | <span data-ttu-id="d6761-194">200</span><span class="sxs-lookup"><span data-stu-id="d6761-194">200</span></span>                  |

<span data-ttu-id="d6761-195">Прогноз будет уменьшен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6761-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="d6761-196">Первый заказ на продажу не входит ни в один из периодов, поэтому он не уменьшит никакой прогноз.</span><span class="sxs-lookup"><span data-stu-id="d6761-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="d6761-197">Второй заказ на продажу лежит между 1 января и 5 января, поэтому он уменьшит прогноз на 1-е января на 100.</span><span class="sxs-lookup"><span data-stu-id="d6761-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="d6761-198">Третий заказ на продажу лежит между 5 января и 12 января, поэтому он уменьшит прогноз на 5-е января на 200.</span><span class="sxs-lookup"><span data-stu-id="d6761-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="d6761-199">Следующий запланированный заказ будет создан для того, чтобы выполнить прогноз.</span><span class="sxs-lookup"><span data-stu-id="d6761-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="d6761-200">Дата прогноза спроса</span><span class="sxs-lookup"><span data-stu-id="d6761-200">Demand forecast date</span></span> | <span data-ttu-id="d6761-201">Уменьшенное количество</span><span class="sxs-lookup"><span data-stu-id="d6761-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="d6761-202">1 января</span><span class="sxs-lookup"><span data-stu-id="d6761-202">January 1</span></span>            | <span data-ttu-id="d6761-203">900</span><span class="sxs-lookup"><span data-stu-id="d6761-203">900</span></span>              |
| <span data-ttu-id="d6761-204">5 января</span><span class="sxs-lookup"><span data-stu-id="d6761-204">January 5</span></span>            | <span data-ttu-id="d6761-205">300</span><span class="sxs-lookup"><span data-stu-id="d6761-205">300</span></span>              |
| <span data-ttu-id="d6761-206">12 января</span><span class="sxs-lookup"><span data-stu-id="d6761-206">January 12</span></span>           | <span data-ttu-id="d6761-207">1000</span><span class="sxs-lookup"><span data-stu-id="d6761-207">1,000</span></span>            |

<span data-ttu-id="d6761-208">Ниже приведена сводка сокращения **Проводки - динамический период**:</span><span class="sxs-lookup"><span data-stu-id="d6761-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="d6761-209">Требования прогноза уменьшаются на проводки фактических заказов, которые приходятся на динамический период.</span><span class="sxs-lookup"><span data-stu-id="d6761-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="d6761-210">Динамический период охватывает даты текущего прогноза и заканчивается в начале следующего прогноза.</span><span class="sxs-lookup"><span data-stu-id="d6761-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="d6761-211">Этот метод не использует ключ сокращения и не требует его.</span><span class="sxs-lookup"><span data-stu-id="d6761-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="d6761-212">Когда используется этот вариант, поведение будет следующим:</span><span class="sxs-lookup"><span data-stu-id="d6761-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="d6761-213">Если прогноз уменьшен полностью, то требования прогноза для текущего прогноза будут равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="d6761-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="d6761-214">Если будущие прогнозы отсутствуют, сокращаются прогнозируемые требования из последнего введенного прогноза.</span><span class="sxs-lookup"><span data-stu-id="d6761-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="d6761-215">Временные границы включаются в расчеты уменьшения прогноза.</span><span class="sxs-lookup"><span data-stu-id="d6761-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="d6761-216">Положительные дни включаются в расчеты уменьшения прогноза.</span><span class="sxs-lookup"><span data-stu-id="d6761-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="d6761-217">Если фактические проводки по заказам превышают прогнозированные требования, то остальные проводки не передаются в следующий период прогноза.</span><span class="sxs-lookup"><span data-stu-id="d6761-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="d6761-218">См. также</span><span class="sxs-lookup"><span data-stu-id="d6761-218">See also</span></span>
--------

[<span data-ttu-id="d6761-219">Сводные планы</span><span class="sxs-lookup"><span data-stu-id="d6761-219">Master plans</span></span>](master-plans.md)




