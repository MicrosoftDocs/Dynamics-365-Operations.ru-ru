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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e385e60e10146a0855a467af57a0a31fcc53bd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "331008"
---
# <a name="manual-depreciation"></a><span data-ttu-id="06c29-103">Ручная амортизация</span><span class="sxs-lookup"><span data-stu-id="06c29-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06c29-104">Эта статья содержит обзор метода ручной амортизации.</span><span class="sxs-lookup"><span data-stu-id="06c29-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="06c29-105">Если вы настроите профиль амортизации основных средств и выберете **Вручную** в поле **Метод** на странице **Профили амортизации**, то амортизация основных средств, назначенная этому профилю амортизации, будет определяться процентом, введенным для каждого интервала календарного года.</span><span class="sxs-lookup"><span data-stu-id="06c29-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="06c29-106">Интервалы, для которых вы настраиваете проценты, разносятся согласно значению, которое вы выбираете в поле **Частота периода** на экспресс-вкладке **Общие** на странице **Профили амортизации**.</span><span class="sxs-lookup"><span data-stu-id="06c29-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="06c29-107">Могут быть выбраны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="06c29-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="06c29-108">Ежегодно</span><span class="sxs-lookup"><span data-stu-id="06c29-108">Yearly</span></span>
-   <span data-ttu-id="06c29-109">Помесячная</span><span class="sxs-lookup"><span data-stu-id="06c29-109">Monthly</span></span>
-   <span data-ttu-id="06c29-110">Ежеквартально</span><span class="sxs-lookup"><span data-stu-id="06c29-110">Quarterly</span></span>
-   <span data-ttu-id="06c29-111">Полгода</span><span class="sxs-lookup"><span data-stu-id="06c29-111">Half-Yearly</span></span>
-   <span data-ttu-id="06c29-112">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="06c29-112">Daily</span></span>

<span data-ttu-id="06c29-113">После того, как вы выбираете частоту периода, щелкните **Графики ручных операций**, и настройте проценты для каждого интервала разноски.</span><span class="sxs-lookup"><span data-stu-id="06c29-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="06c29-114">Графики списания и интервалы разноски вместе определяют сумму амортизации, как показано в приведенном ниже примере.</span><span class="sxs-lookup"><span data-stu-id="06c29-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="06c29-115">При амортизации вручную величина амортизации всегда рассчитывается как процент от цены приобретения.</span><span class="sxs-lookup"><span data-stu-id="06c29-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="06c29-116">При расчете амортизации вручную проценты, введенные для интервалов амортизации, в сумме могут не составлять 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="06c29-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="06c29-117">Ручная амортизация — это гибкий метод амортизации, который часто используется для определения нестандартных профилей амортизации на странице **Книги**, например для нерегулярного расчета амортизации в связи с особыми целями (например, связанными с расчетом налогов).</span><span class="sxs-lookup"><span data-stu-id="06c29-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="06c29-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="06c29-118">Examples</span></span>
<span data-ttu-id="06c29-119">Цена приобретения: 11 000,00 Ожидаемая ликвидационная стоимость: 1000,00 В следующей таблице показаны интервалы и проценты, настроенные на странице **Графики профилей амортизации основных средств**.</span><span class="sxs-lookup"><span data-stu-id="06c29-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="06c29-120">Номер интервала</span><span class="sxs-lookup"><span data-stu-id="06c29-120">Interval number</span></span> | <span data-ttu-id="06c29-121">Процент</span><span class="sxs-lookup"><span data-stu-id="06c29-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="06c29-122">1</span><span class="sxs-lookup"><span data-stu-id="06c29-122">1</span></span>               | <span data-ttu-id="06c29-123">10,00</span><span class="sxs-lookup"><span data-stu-id="06c29-123">10.00</span></span>      |
| <span data-ttu-id="06c29-124">2</span><span class="sxs-lookup"><span data-stu-id="06c29-124">2</span></span>               | <span data-ttu-id="06c29-125">50,00</span><span class="sxs-lookup"><span data-stu-id="06c29-125">50.00</span></span>      |
| <span data-ttu-id="06c29-126">3</span><span class="sxs-lookup"><span data-stu-id="06c29-126">3</span></span>               | <span data-ttu-id="06c29-127">8,00</span><span class="sxs-lookup"><span data-stu-id="06c29-127">8.00</span></span>       |

<span data-ttu-id="06c29-128">Способ расчета амортизации каждому по интервалу показан в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="06c29-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="06c29-129">Номер интервала</span><span class="sxs-lookup"><span data-stu-id="06c29-129">Interval number</span></span> | <span data-ttu-id="06c29-130">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="06c29-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="06c29-131">Остаточная стоимость на конец интервала</span><span class="sxs-lookup"><span data-stu-id="06c29-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="06c29-132">1</span><span class="sxs-lookup"><span data-stu-id="06c29-132">1</span></span>                | <span data-ttu-id="06c29-133">(11000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="06c29-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="06c29-134">10000 (11000 – 1000)</span><span class="sxs-lookup"><span data-stu-id="06c29-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="06c29-135">2</span><span class="sxs-lookup"><span data-stu-id="06c29-135">2</span></span>                | <span data-ttu-id="06c29-136">(11000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="06c29-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="06c29-137">5000 (10000 – 5000)</span><span class="sxs-lookup"><span data-stu-id="06c29-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="06c29-138">3</span><span class="sxs-lookup"><span data-stu-id="06c29-138">3</span></span>                | <span data-ttu-id="06c29-139">(11000 – 1000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="06c29-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="06c29-140">4200 (5000 – 800)</span><span class="sxs-lookup"><span data-stu-id="06c29-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="06c29-141">Если выбрать **Ежемесячно** в поле **Частота периода**, необходимо будет вручную настроить 12 интервалов графика списания.</span><span class="sxs-lookup"><span data-stu-id="06c29-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="06c29-142">Суммы амортизации для первых двух интервалов показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="06c29-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="06c29-143">Диапазон</span><span class="sxs-lookup"><span data-stu-id="06c29-143">Interval</span></span> | <span data-ttu-id="06c29-144">Сумма начисленной амортизации</span><span class="sxs-lookup"><span data-stu-id="06c29-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="06c29-145">Январь</span><span class="sxs-lookup"><span data-stu-id="06c29-145">January</span></span>  | <span data-ttu-id="06c29-146">(11000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="06c29-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="06c29-147">Февраль</span><span class="sxs-lookup"><span data-stu-id="06c29-147">February</span></span> | <span data-ttu-id="06c29-148">(11000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="06c29-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="06c29-149">Если выбрать <strong>Полгода</strong> в поле *<strong><em>Частота периода</em>*</strong>, необходимо будет вручную настроить два интервала графика списания.</span><span class="sxs-lookup"><span data-stu-id="06c29-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="06c29-150">Суммы амортизации для таких двух интервалов показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="06c29-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="06c29-151">Диапазон</span><span class="sxs-lookup"><span data-stu-id="06c29-151">Interval</span></span>    | <span data-ttu-id="06c29-152">Сумма начисленной амортизации</span><span class="sxs-lookup"><span data-stu-id="06c29-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="06c29-153">30 июня</span><span class="sxs-lookup"><span data-stu-id="06c29-153">June 30</span></span>     | <span data-ttu-id="06c29-154">(11000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="06c29-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="06c29-155">31 декабря</span><span class="sxs-lookup"><span data-stu-id="06c29-155">December 31</span></span> | <span data-ttu-id="06c29-156">(11000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="06c29-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="06c29-157">Общая сумма процентов для всех интервалов не должна быть обязательно равна 100.</span><span class="sxs-lookup"><span data-stu-id="06c29-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="06c29-158">Однако вы получите сообщение, если значение в поле **Суммарный процент** на странице **Графики профилей амортизации основных средств** не равно **100**.</span><span class="sxs-lookup"><span data-stu-id="06c29-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



