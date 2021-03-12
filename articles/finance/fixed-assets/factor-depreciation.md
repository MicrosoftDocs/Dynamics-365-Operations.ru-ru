---
title: Коэффициент амортизации
description: Эта статья содержит обзор метода коэффициента амортизации.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4920f7f90b859006ecdcd486eaa9f4449442e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976149"
---
# <a name="factor-depreciation"></a><span data-ttu-id="fd286-103">Коэффициент амортизации</span><span class="sxs-lookup"><span data-stu-id="fd286-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd286-104">Эта статья содержит обзор метода коэффициента амортизации.</span><span class="sxs-lookup"><span data-stu-id="fd286-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="fd286-105">Коэффициенты — это проценты, используемые для амортизации активов.</span><span class="sxs-lookup"><span data-stu-id="fd286-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="fd286-106">Когда производится настройка профиля амортизации основных средств и выбор значения **Коэффициент** в поле **Метод** на странице **Профили амортизации**, можно настроить прогрессивную амортизацию, дигрессивную амортизацию или линейную амортизацию:</span><span class="sxs-lookup"><span data-stu-id="fd286-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="fd286-107">При прогрессивной амортизации сумма амортизации увеличивается с каждым периодом амортизации.</span><span class="sxs-lookup"><span data-stu-id="fd286-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="fd286-108">При дигрессивной амортизации сумма амортизации в каждый следующий период уменьшается.</span><span class="sxs-lookup"><span data-stu-id="fd286-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="fd286-109">При линейной амортизации сумма амортизации одна и та же в каждом периоде.</span><span class="sxs-lookup"><span data-stu-id="fd286-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="fd286-110">Приведенные ниже правила и примеры показывают, как можно настроить коэффициенты для каждого типа амортизации.</span><span class="sxs-lookup"><span data-stu-id="fd286-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="fd286-111">Когда выбирается значение **Коэффициент** в поле **Метод**, отображается поле **Коэффициент** и поле **Интервал**.</span><span class="sxs-lookup"><span data-stu-id="fd286-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="fd286-112">Прогрессивная амортизация</span><span class="sxs-lookup"><span data-stu-id="fd286-112">Progressive depreciation</span></span>
<span data-ttu-id="fd286-113">Значение в поле **Коэффициент** больше чем **50**.</span><span class="sxs-lookup"><span data-stu-id="fd286-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="fd286-114">Пример</span><span class="sxs-lookup"><span data-stu-id="fd286-114">Example</span></span>

<span data-ttu-id="fd286-115">Стоимость приобретения равна 100 000, коэффициент равен 70, срок службы равен 10 годам, и амортизация начинается 1 января.</span><span class="sxs-lookup"><span data-stu-id="fd286-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="fd286-116">Суммы амортизации и суммы остаточной стоимости показаны только для первых шести лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="fd286-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="fd286-117">Год</span><span class="sxs-lookup"><span data-stu-id="fd286-117">Year</span></span> | <span data-ttu-id="fd286-118">Период</span><span class="sxs-lookup"><span data-stu-id="fd286-118">Period</span></span>      | <span data-ttu-id="fd286-119">Сумма амортизации</span><span class="sxs-lookup"><span data-stu-id="fd286-119">Depreciation amount</span></span> | <span data-ttu-id="fd286-120">Сумма остаточной стоимости</span><span class="sxs-lookup"><span data-stu-id="fd286-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="fd286-121">1</span><span class="sxs-lookup"><span data-stu-id="fd286-121">1</span></span>    | <span data-ttu-id="fd286-122">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-122">December 31</span></span> | <span data-ttu-id="fd286-123">307,69</span><span class="sxs-lookup"><span data-stu-id="fd286-123">307.69</span></span>              | <span data-ttu-id="fd286-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="fd286-124">99,692.31</span></span>             |
| <span data-ttu-id="fd286-125">2</span><span class="sxs-lookup"><span data-stu-id="fd286-125">2</span></span>    | <span data-ttu-id="fd286-126">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-126">December 31</span></span> | <span data-ttu-id="fd286-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="fd286-127">1,447.21</span></span>            | <span data-ttu-id="fd286-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="fd286-128">98,245.10</span></span>             |
| <span data-ttu-id="fd286-129">3</span><span class="sxs-lookup"><span data-stu-id="fd286-129">3</span></span>    | <span data-ttu-id="fd286-130">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-130">December 31</span></span> | <span data-ttu-id="fd286-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="fd286-131">3,104.50</span></span>            | <span data-ttu-id="fd286-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="fd286-132">95,140.60</span></span>             |
| <span data-ttu-id="fd286-133">4</span><span class="sxs-lookup"><span data-stu-id="fd286-133">4</span></span>    | <span data-ttu-id="fd286-134">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-134">December 31</span></span> | <span data-ttu-id="fd286-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="fd286-135">5,150.21</span></span>            | <span data-ttu-id="fd286-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="fd286-136">89,990.39</span></span>             |
| <span data-ttu-id="fd286-137">5</span><span class="sxs-lookup"><span data-stu-id="fd286-137">5</span></span>    | <span data-ttu-id="fd286-138">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-138">December 31</span></span> | <span data-ttu-id="fd286-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="fd286-139">7,522.95</span></span>            | <span data-ttu-id="fd286-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="fd286-140">82,467.44</span></span>             |
| <span data-ttu-id="fd286-141">6</span><span class="sxs-lookup"><span data-stu-id="fd286-141">6</span></span>    | <span data-ttu-id="fd286-142">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-142">December 31</span></span> | <span data-ttu-id="fd286-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="fd286-143">10,184.06</span></span>           | <span data-ttu-id="fd286-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="fd286-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="fd286-145">Дигрессивная амортизация</span><span class="sxs-lookup"><span data-stu-id="fd286-145">Digressive depreciation</span></span>
<span data-ttu-id="fd286-146">Значение в поле **Коэффициент** меньше чем **50**.</span><span class="sxs-lookup"><span data-stu-id="fd286-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="fd286-147">Пример</span><span class="sxs-lookup"><span data-stu-id="fd286-147">Example</span></span>

<span data-ttu-id="fd286-148">Стоимость приобретения равна 100 000, коэффициент равен 20, срок службы равен 10 годам, и амортизация начинается 1 января.</span><span class="sxs-lookup"><span data-stu-id="fd286-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="fd286-149">Суммы амортизации и суммы остаточной стоимости показаны только для первых шести лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="fd286-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="fd286-150">Год</span><span class="sxs-lookup"><span data-stu-id="fd286-150">Year</span></span> | <span data-ttu-id="fd286-151">Период</span><span class="sxs-lookup"><span data-stu-id="fd286-151">Period</span></span>      | <span data-ttu-id="fd286-152">Сумма амортизации</span><span class="sxs-lookup"><span data-stu-id="fd286-152">Depreciation amount</span></span> | <span data-ttu-id="fd286-153">Сумма остаточной стоимости</span><span class="sxs-lookup"><span data-stu-id="fd286-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="fd286-154">1</span><span class="sxs-lookup"><span data-stu-id="fd286-154">1</span></span>    | <span data-ttu-id="fd286-155">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-155">December 31</span></span> | <span data-ttu-id="fd286-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="fd286-156">56,080.43</span></span>           | <span data-ttu-id="fd286-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="fd286-157">43,919.57</span></span>             |
| <span data-ttu-id="fd286-158">2</span><span class="sxs-lookup"><span data-stu-id="fd286-158">2</span></span>    | <span data-ttu-id="fd286-159">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-159">December 31</span></span> | <span data-ttu-id="fd286-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="fd286-160">10,665.70</span></span>           | <span data-ttu-id="fd286-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="fd286-161">33,253.87</span></span>             |
| <span data-ttu-id="fd286-162">3</span><span class="sxs-lookup"><span data-stu-id="fd286-162">3</span></span>    | <span data-ttu-id="fd286-163">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-163">December 31</span></span> | <span data-ttu-id="fd286-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="fd286-164">7,156.22</span></span>            | <span data-ttu-id="fd286-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="fd286-165">26,097.65</span></span>             |
| <span data-ttu-id="fd286-166">4</span><span class="sxs-lookup"><span data-stu-id="fd286-166">4</span></span>    | <span data-ttu-id="fd286-167">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-167">December 31</span></span> | <span data-ttu-id="fd286-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="fd286-168">5,538.06</span></span>            | <span data-ttu-id="fd286-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="fd286-169">20,559.59</span></span>             |
| <span data-ttu-id="fd286-170">5</span><span class="sxs-lookup"><span data-stu-id="fd286-170">5</span></span>    | <span data-ttu-id="fd286-171">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-171">December 31</span></span> | <span data-ttu-id="fd286-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="fd286-172">4,579.89</span></span>            | <span data-ttu-id="fd286-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="fd286-173">15,979.70</span></span>             |
| <span data-ttu-id="fd286-174">6</span><span class="sxs-lookup"><span data-stu-id="fd286-174">6</span></span>    | <span data-ttu-id="fd286-175">31 декабря</span><span class="sxs-lookup"><span data-stu-id="fd286-175">December 31</span></span> | <span data-ttu-id="fd286-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="fd286-176">3,937.36</span></span>            | <span data-ttu-id="fd286-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="fd286-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="fd286-178">Линейная амортизация</span><span class="sxs-lookup"><span data-stu-id="fd286-178">Straight line depreciation</span></span>
<span data-ttu-id="fd286-179">Значение в поле **Коэффициент** равно **50**.</span><span class="sxs-lookup"><span data-stu-id="fd286-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="fd286-180">В этом случае амортизация одинакова в каждом периоде, и следует рассмотреть результаты выбора значений в других полях, как это показано в разделе [Амортизация срока службы (прямолинейный метод)](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="fd286-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



