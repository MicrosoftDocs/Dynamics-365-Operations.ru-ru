---
title: Ручная амортизация
description: Эта статья содержит обзор метода ручной амортизации.
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
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187230"
---
# <a name="manual-depreciation"></a><span data-ttu-id="d8be5-103">Ручная амортизация</span><span class="sxs-lookup"><span data-stu-id="d8be5-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8be5-104">Эта статья содержит обзор метода ручной амортизации.</span><span class="sxs-lookup"><span data-stu-id="d8be5-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="d8be5-105">Если вы настроите профиль амортизации основных средств и выберете **Вручную** в поле **Метод** на странице **Профили амортизации**, то амортизация основных средств, назначенная этому профилю амортизации, будет определяться процентом, введенным для каждого интервала календарного года.</span><span class="sxs-lookup"><span data-stu-id="d8be5-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="d8be5-106">Интервалы, для которых вы настраиваете проценты, разносятся согласно значению, которое вы выбираете в поле **Частота периода** на экспресс-вкладке **Общие** на странице **Профили амортизации**.</span><span class="sxs-lookup"><span data-stu-id="d8be5-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="d8be5-107">Могут быть выбраны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d8be5-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="d8be5-108">Ежегодно</span><span class="sxs-lookup"><span data-stu-id="d8be5-108">Yearly</span></span>
-   <span data-ttu-id="d8be5-109">Помесячная</span><span class="sxs-lookup"><span data-stu-id="d8be5-109">Monthly</span></span>
-   <span data-ttu-id="d8be5-110">Ежеквартально</span><span class="sxs-lookup"><span data-stu-id="d8be5-110">Quarterly</span></span>
-   <span data-ttu-id="d8be5-111">Полгода</span><span class="sxs-lookup"><span data-stu-id="d8be5-111">Half-Yearly</span></span>
-   <span data-ttu-id="d8be5-112">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="d8be5-112">Daily</span></span>

<span data-ttu-id="d8be5-113">После того, как вы выбираете частоту периода, щелкните **Графики ручных операций**, и настройте проценты для каждого интервала разноски.</span><span class="sxs-lookup"><span data-stu-id="d8be5-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="d8be5-114">Графики списания и интервалы разноски вместе определяют сумму амортизации, как показано в приведенном ниже примере.</span><span class="sxs-lookup"><span data-stu-id="d8be5-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="d8be5-115">При амортизации вручную величина амортизации всегда рассчитывается как процент от цены приобретения.</span><span class="sxs-lookup"><span data-stu-id="d8be5-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="d8be5-116">При расчете амортизации вручную проценты, введенные для интервалов амортизации, в сумме могут не составлять 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="d8be5-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="d8be5-117">Ручная амортизация — это гибкий метод амортизации, который часто используется для определения нестандартных профилей амортизации на странице **Книги**, например для нерегулярного расчета амортизации в связи с особыми целями (например, связанными с расчетом налогов).</span><span class="sxs-lookup"><span data-stu-id="d8be5-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="d8be5-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="d8be5-118">Examples</span></span>
<span data-ttu-id="d8be5-119">Цена приобретения: 11 000,00 Ожидаемая ликвидационная стоимость: 1000,00 В следующей таблице показаны интервалы и проценты, настроенные на странице **Графики профилей амортизации основных средств**.</span><span class="sxs-lookup"><span data-stu-id="d8be5-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="d8be5-120">Номер интервала</span><span class="sxs-lookup"><span data-stu-id="d8be5-120">Interval number</span></span> | <span data-ttu-id="d8be5-121">Процент</span><span class="sxs-lookup"><span data-stu-id="d8be5-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="d8be5-122">1</span><span class="sxs-lookup"><span data-stu-id="d8be5-122">1</span></span>               | <span data-ttu-id="d8be5-123">10,00</span><span class="sxs-lookup"><span data-stu-id="d8be5-123">10.00</span></span>      |
| <span data-ttu-id="d8be5-124">2</span><span class="sxs-lookup"><span data-stu-id="d8be5-124">2</span></span>               | <span data-ttu-id="d8be5-125">50,00</span><span class="sxs-lookup"><span data-stu-id="d8be5-125">50.00</span></span>      |
| <span data-ttu-id="d8be5-126">3</span><span class="sxs-lookup"><span data-stu-id="d8be5-126">3</span></span>               | <span data-ttu-id="d8be5-127">8,00</span><span class="sxs-lookup"><span data-stu-id="d8be5-127">8.00</span></span>       |

<span data-ttu-id="d8be5-128">Способ расчета амортизации каждому по интервалу показан в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d8be5-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="d8be5-129">Номер интервала</span><span class="sxs-lookup"><span data-stu-id="d8be5-129">Interval number</span></span> | <span data-ttu-id="d8be5-130">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="d8be5-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="d8be5-131">Остаточная стоимость на конец интервала</span><span class="sxs-lookup"><span data-stu-id="d8be5-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d8be5-132">1</span><span class="sxs-lookup"><span data-stu-id="d8be5-132">1</span></span>                | <span data-ttu-id="d8be5-133">(11000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="d8be5-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="d8be5-134">10000 (11000 – 1000)</span><span class="sxs-lookup"><span data-stu-id="d8be5-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="d8be5-135">2</span><span class="sxs-lookup"><span data-stu-id="d8be5-135">2</span></span>                | <span data-ttu-id="d8be5-136">(11000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="d8be5-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="d8be5-137">5000 (10000 – 5000)</span><span class="sxs-lookup"><span data-stu-id="d8be5-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="d8be5-138">3</span><span class="sxs-lookup"><span data-stu-id="d8be5-138">3</span></span>                | <span data-ttu-id="d8be5-139">(11000 – 1000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="d8be5-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="d8be5-140">4200 (5000 – 800)</span><span class="sxs-lookup"><span data-stu-id="d8be5-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="d8be5-141">Если выбрать **Ежемесячно** в поле **Частота периода**, необходимо будет вручную настроить 12 интервалов графика списания.</span><span class="sxs-lookup"><span data-stu-id="d8be5-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="d8be5-142">Суммы амортизации для первых двух интервалов показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d8be5-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="d8be5-143">Диапазон</span><span class="sxs-lookup"><span data-stu-id="d8be5-143">Interval</span></span> | <span data-ttu-id="d8be5-144">Сумма начисленной амортизации</span><span class="sxs-lookup"><span data-stu-id="d8be5-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="d8be5-145">Январь</span><span class="sxs-lookup"><span data-stu-id="d8be5-145">January</span></span>  | <span data-ttu-id="d8be5-146">(11000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="d8be5-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="d8be5-147">Февраль</span><span class="sxs-lookup"><span data-stu-id="d8be5-147">February</span></span> | <span data-ttu-id="d8be5-148">(11000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="d8be5-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="d8be5-149">Если выбрать <strong>Полгода</strong> в поле *<strong><em>Частота периода</em>*</strong>, необходимо будет вручную настроить два интервала графика списания.</span><span class="sxs-lookup"><span data-stu-id="d8be5-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="d8be5-150">Суммы амортизации для таких двух интервалов показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d8be5-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="d8be5-151">Диапазон</span><span class="sxs-lookup"><span data-stu-id="d8be5-151">Interval</span></span>    | <span data-ttu-id="d8be5-152">Сумма начисленной амортизации</span><span class="sxs-lookup"><span data-stu-id="d8be5-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="d8be5-153">30 июня</span><span class="sxs-lookup"><span data-stu-id="d8be5-153">June 30</span></span>     | <span data-ttu-id="d8be5-154">(11000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="d8be5-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="d8be5-155">31 декабря</span><span class="sxs-lookup"><span data-stu-id="d8be5-155">December 31</span></span> | <span data-ttu-id="d8be5-156">(11000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="d8be5-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="d8be5-157">Общая сумма процентов для всех интервалов не должна быть обязательно равна 100.</span><span class="sxs-lookup"><span data-stu-id="d8be5-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="d8be5-158">Однако вы получите сообщение, если значение в поле **Суммарный процент** на странице **Графики профилей амортизации основных средств** не равно **100**.</span><span class="sxs-lookup"><span data-stu-id="d8be5-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>


