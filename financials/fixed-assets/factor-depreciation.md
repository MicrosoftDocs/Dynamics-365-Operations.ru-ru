---
title: "Коэффициент амортизации"
description: "Эта статья содержит обзор метода коэффициента амортизации."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: ru-ru
ms.lasthandoff: 06/29/2017


---

# <a name="factor-depreciation"></a><span data-ttu-id="43a3a-103">Коэффициент амортизации</span><span class="sxs-lookup"><span data-stu-id="43a3a-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="43a3a-104">Эта статья содержит обзор метода коэффициента амортизации.</span><span class="sxs-lookup"><span data-stu-id="43a3a-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="43a3a-105">Коэффициенты — это проценты, используемые для амортизации активов.</span><span class="sxs-lookup"><span data-stu-id="43a3a-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="43a3a-106">Когда производится настройка профиля амортизации основных средств и выбор значения **Коэффициент** в поле **Метод** на странице **Профили амортизации**, можно настроить прогрессивную амортизацию, дигрессивную амортизацию или линейную амортизацию:</span><span class="sxs-lookup"><span data-stu-id="43a3a-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="43a3a-107">При прогрессивной амортизации сумма амортизации увеличивается с каждым периодом амортизации.</span><span class="sxs-lookup"><span data-stu-id="43a3a-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="43a3a-108">При дигрессивной амортизации сумма амортизации в каждый следующий период уменьшается.</span><span class="sxs-lookup"><span data-stu-id="43a3a-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="43a3a-109">При линейной амортизации сумма амортизации одна и та же в каждом периоде.</span><span class="sxs-lookup"><span data-stu-id="43a3a-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="43a3a-110">Приведенные ниже правила и примеры показывают, как можно настроить коэффициенты для каждого типа амортизации.</span><span class="sxs-lookup"><span data-stu-id="43a3a-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="43a3a-111">Когда выбирается значение **Коэффициент** в поле **Метод**, отображается поле **Коэффициент** и поле **Интервал**.</span><span class="sxs-lookup"><span data-stu-id="43a3a-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="43a3a-112">Прогрессивная амортизация</span><span class="sxs-lookup"><span data-stu-id="43a3a-112">Progressive depreciation</span></span>
<span data-ttu-id="43a3a-113">Значение в поле **Коэффициент** больше чем **50**.</span><span class="sxs-lookup"><span data-stu-id="43a3a-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="43a3a-114">Пример</span><span class="sxs-lookup"><span data-stu-id="43a3a-114">Example</span></span>

<span data-ttu-id="43a3a-115">Стоимость приобретения равна 100 000, коэффициент равен 70, срок службы равен 10 годам, и амортизация начинается 1 января.</span><span class="sxs-lookup"><span data-stu-id="43a3a-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="43a3a-116">Суммы амортизации и суммы остаточной стоимости показаны только для первых шести лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="43a3a-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="43a3a-117">Год</span><span class="sxs-lookup"><span data-stu-id="43a3a-117">Year</span></span> | <span data-ttu-id="43a3a-118">Период</span><span class="sxs-lookup"><span data-stu-id="43a3a-118">Period</span></span>      | <span data-ttu-id="43a3a-119">Сумма амортизации</span><span class="sxs-lookup"><span data-stu-id="43a3a-119">Depreciation amount</span></span> | <span data-ttu-id="43a3a-120">Сумма остаточной стоимости</span><span class="sxs-lookup"><span data-stu-id="43a3a-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="43a3a-121">1</span><span class="sxs-lookup"><span data-stu-id="43a3a-121">1</span></span>    | <span data-ttu-id="43a3a-122">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-122">December 31</span></span> | <span data-ttu-id="43a3a-123">307,69</span><span class="sxs-lookup"><span data-stu-id="43a3a-123">307.69</span></span>              | <span data-ttu-id="43a3a-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="43a3a-124">99,692.31</span></span>             |
| <span data-ttu-id="43a3a-125">2</span><span class="sxs-lookup"><span data-stu-id="43a3a-125">2</span></span>    | <span data-ttu-id="43a3a-126">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-126">December 31</span></span> | <span data-ttu-id="43a3a-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="43a3a-127">1,447.21</span></span>            | <span data-ttu-id="43a3a-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="43a3a-128">98,245.10</span></span>             |
| <span data-ttu-id="43a3a-129">3</span><span class="sxs-lookup"><span data-stu-id="43a3a-129">3</span></span>    | <span data-ttu-id="43a3a-130">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-130">December 31</span></span> | <span data-ttu-id="43a3a-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="43a3a-131">3,104.50</span></span>            | <span data-ttu-id="43a3a-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="43a3a-132">95,140.60</span></span>             |
| <span data-ttu-id="43a3a-133">4</span><span class="sxs-lookup"><span data-stu-id="43a3a-133">4</span></span>    | <span data-ttu-id="43a3a-134">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-134">December 31</span></span> | <span data-ttu-id="43a3a-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="43a3a-135">5,150.21</span></span>            | <span data-ttu-id="43a3a-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="43a3a-136">89,990.39</span></span>             |
| <span data-ttu-id="43a3a-137">5</span><span class="sxs-lookup"><span data-stu-id="43a3a-137">5</span></span>    | <span data-ttu-id="43a3a-138">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-138">December 31</span></span> | <span data-ttu-id="43a3a-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="43a3a-139">7,522.95</span></span>            | <span data-ttu-id="43a3a-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="43a3a-140">82,467.44</span></span>             |
| <span data-ttu-id="43a3a-141">6</span><span class="sxs-lookup"><span data-stu-id="43a3a-141">6</span></span>    | <span data-ttu-id="43a3a-142">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-142">December 31</span></span> | <span data-ttu-id="43a3a-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="43a3a-143">10,184.06</span></span>           | <span data-ttu-id="43a3a-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="43a3a-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="43a3a-145">Дигрессивная амортизация</span><span class="sxs-lookup"><span data-stu-id="43a3a-145">Digressive depreciation</span></span>
<span data-ttu-id="43a3a-146">Значение в поле **Коэффициент** меньше чем **50**.</span><span class="sxs-lookup"><span data-stu-id="43a3a-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="43a3a-147">Пример</span><span class="sxs-lookup"><span data-stu-id="43a3a-147">Example</span></span>

<span data-ttu-id="43a3a-148">Стоимость приобретения равна 100 000, коэффициент равен 20, срок службы равен 10 годам, и амортизация начинается 1 января.</span><span class="sxs-lookup"><span data-stu-id="43a3a-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="43a3a-149">Суммы амортизации и суммы остаточной стоимости показаны только для первых шести лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="43a3a-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="43a3a-150">Год</span><span class="sxs-lookup"><span data-stu-id="43a3a-150">Year</span></span> | <span data-ttu-id="43a3a-151">Период</span><span class="sxs-lookup"><span data-stu-id="43a3a-151">Period</span></span>      | <span data-ttu-id="43a3a-152">Сумма амортизации</span><span class="sxs-lookup"><span data-stu-id="43a3a-152">Depreciation amount</span></span> | <span data-ttu-id="43a3a-153">Сумма остаточной стоимости</span><span class="sxs-lookup"><span data-stu-id="43a3a-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="43a3a-154">1</span><span class="sxs-lookup"><span data-stu-id="43a3a-154">1</span></span>    | <span data-ttu-id="43a3a-155">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-155">December 31</span></span> | <span data-ttu-id="43a3a-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="43a3a-156">56,080.43</span></span>           | <span data-ttu-id="43a3a-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="43a3a-157">43,919.57</span></span>             |
| <span data-ttu-id="43a3a-158">2</span><span class="sxs-lookup"><span data-stu-id="43a3a-158">2</span></span>    | <span data-ttu-id="43a3a-159">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-159">December 31</span></span> | <span data-ttu-id="43a3a-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="43a3a-160">10,665.70</span></span>           | <span data-ttu-id="43a3a-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="43a3a-161">33,253.87</span></span>             |
| <span data-ttu-id="43a3a-162">3</span><span class="sxs-lookup"><span data-stu-id="43a3a-162">3</span></span>    | <span data-ttu-id="43a3a-163">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-163">December 31</span></span> | <span data-ttu-id="43a3a-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="43a3a-164">7,156.22</span></span>            | <span data-ttu-id="43a3a-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="43a3a-165">26,097.65</span></span>             |
| <span data-ttu-id="43a3a-166">4</span><span class="sxs-lookup"><span data-stu-id="43a3a-166">4</span></span>    | <span data-ttu-id="43a3a-167">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-167">December 31</span></span> | <span data-ttu-id="43a3a-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="43a3a-168">5,538.06</span></span>            | <span data-ttu-id="43a3a-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="43a3a-169">20,559.59</span></span>             |
| <span data-ttu-id="43a3a-170">5</span><span class="sxs-lookup"><span data-stu-id="43a3a-170">5</span></span>    | <span data-ttu-id="43a3a-171">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-171">December 31</span></span> | <span data-ttu-id="43a3a-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="43a3a-172">4,579.89</span></span>            | <span data-ttu-id="43a3a-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="43a3a-173">15,979.70</span></span>             |
| <span data-ttu-id="43a3a-174">6</span><span class="sxs-lookup"><span data-stu-id="43a3a-174">6</span></span>    | <span data-ttu-id="43a3a-175">31 декабря</span><span class="sxs-lookup"><span data-stu-id="43a3a-175">December 31</span></span> | <span data-ttu-id="43a3a-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="43a3a-176">3,937.36</span></span>            | <span data-ttu-id="43a3a-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="43a3a-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="43a3a-178">Линейная амортизация</span><span class="sxs-lookup"><span data-stu-id="43a3a-178">Straight line depreciation</span></span>
<span data-ttu-id="43a3a-179">Значение в поле **Коэффициент** равно **50**.</span><span class="sxs-lookup"><span data-stu-id="43a3a-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="43a3a-180">В этом случае амортизация одинакова в каждом периоде, и следует рассмотреть результаты выбора значений в других полях, как это показано в разделе [Амортизация срока службы (прямолинейный метод)](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="43a3a-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




