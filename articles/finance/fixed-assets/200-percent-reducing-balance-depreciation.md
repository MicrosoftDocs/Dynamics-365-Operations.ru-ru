---
title: Амортизация с уменьшаемым остатком в 200%
description: Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 200%.
author: saraschi2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e5a548f7963fad2b249c36c90ac19b812131d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827083"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="3763d-103">Амортизация с уменьшаемым остатком в 200%</span><span class="sxs-lookup"><span data-stu-id="3763d-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3763d-104">Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 200%.</span><span class="sxs-lookup"><span data-stu-id="3763d-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="3763d-105">После настройки профиля амортизации ОС и выбора значения **Уменьшаемое сальдо в 200%** в поле **Метод** на странице **Профили амортизации** процент амортизации ОС, назначенных профилю амортизации, одинаков во все периоды амортизации.</span><span class="sxs-lookup"><span data-stu-id="3763d-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="3763d-106">Проценты рассчитываются на основе срока службы актива.</span><span class="sxs-lookup"><span data-stu-id="3763d-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="3763d-107">Например, если срок службы актива составляет пять лет, проценты будут рассчитаны как 40 процентов (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="3763d-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="3763d-108">Этот метод также известен как метод уменьшающегося остатка при удвоенной норме амортизации.</span><span class="sxs-lookup"><span data-stu-id="3763d-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="3763d-109">Чтобы установить амортизацию с уменьшаемым сальдо в 200%, также необходимо выбрать параметры в полях **Год амортизации** и **Частота периода** на странице **Профили амортизации**.</span><span class="sxs-lookup"><span data-stu-id="3763d-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="3763d-110">Варианты, которые доступны в поле **Частота периода**, зависят от значения, которое выбрано в поле **Год амортизации**.</span><span class="sxs-lookup"><span data-stu-id="3763d-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="3763d-111">Выбор года амортизации</span><span class="sxs-lookup"><span data-stu-id="3763d-111">Select a depreciation year</span></span>
<span data-ttu-id="3763d-112">Вы можете выбрать **Календарь** или **Фискальный** в поле **Год амортизации** на странице **Методы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="3763d-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="3763d-113">Значение по умолчанию равно **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="3763d-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="3763d-114">Выбранный вариант определяет параметры, доступные в поле **Частота периода**.</span><span class="sxs-lookup"><span data-stu-id="3763d-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="3763d-115">Это поле определяет даты и суммы разноски амортизационных начислений в течении календарного года.</span><span class="sxs-lookup"><span data-stu-id="3763d-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="3763d-116">Календарь</span><span class="sxs-lookup"><span data-stu-id="3763d-116">Calendar</span></span>

<span data-ttu-id="3763d-117">Можно сохранить значение по умолчанию в поле **Год амортизации**, **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="3763d-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="3763d-118">Параметр **Календарь** обновляет базу амортизации 1-го января каждого года.</span><span class="sxs-lookup"><span data-stu-id="3763d-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="3763d-119">Обычно амортизация равна остаточной стоимости минус ликвидационная стоимость.</span><span class="sxs-lookup"><span data-stu-id="3763d-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="3763d-120">В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов.</span><span class="sxs-lookup"><span data-stu-id="3763d-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="3763d-121">Если для года амортизации выбран вариант **Календарь**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="3763d-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="3763d-122">**Ежегодно** — разноска суммы 31-го декабря.</span><span class="sxs-lookup"><span data-stu-id="3763d-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="3763d-123">**Ежемесячно** — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.</span><span class="sxs-lookup"><span data-stu-id="3763d-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="3763d-124">**Ежеквартально** — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="3763d-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="3763d-125">**Каждый полгода** — разноска суммы за полгода один раз в конце календарного полугодия (30 июня и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="3763d-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="3763d-126">**Ежедневно** — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.</span><span class="sxs-lookup"><span data-stu-id="3763d-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="3763d-127">Финансовый</span><span class="sxs-lookup"><span data-stu-id="3763d-127">Fiscal</span></span>

<span data-ttu-id="3763d-128">Если вы выберете **Финансовый** в поле **Год амортизации**, амортизация с уменьшаемым сальдо в 200% рассчитывается на основе финансового года для финансового календаря, заданного для книги, или по финансовому календарю, выбранному на странице **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="3763d-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="3763d-129">Финансовые календари настраиваются на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="3763d-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="3763d-130">Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля.</span><span class="sxs-lookup"><span data-stu-id="3763d-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="3763d-131">Финансовый год может быть длиннее или короче 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="3763d-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="3763d-132">Амортизация корректируется для каждого периода.</span><span class="sxs-lookup"><span data-stu-id="3763d-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="3763d-133">Длительность следующего финансового года определяется на основе настройки периодов, которые определяются на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="3763d-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="3763d-134">Если для года амортизации выбран вариант **Финансовый**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="3763d-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="3763d-135">**Ежегодно** — разноска общей суммы амортизации, рассчитанной для финансового года как единая сумма в последний день финансового года.</span><span class="sxs-lookup"><span data-stu-id="3763d-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="3763d-136">**Финансовый период** разносит полную сумму амортизации, вычисленную за финансовый год.</span><span class="sxs-lookup"><span data-stu-id="3763d-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="3763d-137">Это количество начисляется в фискальные периоды, которые определены на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="3763d-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="3763d-138">Пример амортизации с уменьшаемым сальдо в 200%</span><span class="sxs-lookup"><span data-stu-id="3763d-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="3763d-139">Стоимость приобретения</span><span class="sxs-lookup"><span data-stu-id="3763d-139">Acquisition cost</span></span>               | <span data-ttu-id="3763d-140">11 000</span><span class="sxs-lookup"><span data-stu-id="3763d-140">11,000</span></span> |
| <span data-ttu-id="3763d-141">Ликвидационная стоимость</span><span class="sxs-lookup"><span data-stu-id="3763d-141">Salvage value</span></span>                  | <span data-ttu-id="3763d-142">1 000</span><span class="sxs-lookup"><span data-stu-id="3763d-142">1, 000</span></span> |
| <span data-ttu-id="3763d-143">База амортизации</span><span class="sxs-lookup"><span data-stu-id="3763d-143">Depreciation base</span></span>              | <span data-ttu-id="3763d-144">10 000</span><span class="sxs-lookup"><span data-stu-id="3763d-144">10,000</span></span> |
| <span data-ttu-id="3763d-145">Годы срока службы</span><span class="sxs-lookup"><span data-stu-id="3763d-145">Service life years</span></span>             | <span data-ttu-id="3763d-146">5</span><span class="sxs-lookup"><span data-stu-id="3763d-146">5</span></span>      |
| <span data-ttu-id="3763d-147">Процент ежегодной амортизации</span><span class="sxs-lookup"><span data-stu-id="3763d-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="3763d-148">40%</span><span class="sxs-lookup"><span data-stu-id="3763d-148">40%</span></span>    |

<span data-ttu-id="3763d-149">В методе уменьшаемого остатка с коэффициентом 200% значение в 200 процентов делится на количество лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="3763d-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="3763d-150">Этот процент умножается на остаточную стоимость актива для определения суммы амортизационных начислений за год.</span><span class="sxs-lookup"><span data-stu-id="3763d-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="3763d-151">Период</span><span class="sxs-lookup"><span data-stu-id="3763d-151">Period</span></span> | <span data-ttu-id="3763d-152">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="3763d-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="3763d-153">Остаточная стоимость</span><span class="sxs-lookup"><span data-stu-id="3763d-153">Book value</span></span>             | <span data-ttu-id="3763d-154">Остаточная стоимость на конец года</span><span class="sxs-lookup"><span data-stu-id="3763d-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="3763d-155">1-й год</span><span class="sxs-lookup"><span data-stu-id="3763d-155">Year 1</span></span> | <span data-ttu-id="3763d-156">(11 000 – 1 000) × 40% = 4 000</span><span class="sxs-lookup"><span data-stu-id="3763d-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="3763d-157">11 000 – 4 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="3763d-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="3763d-158">11 000 – 1 000 – 4 000 = 6 000</span><span class="sxs-lookup"><span data-stu-id="3763d-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="3763d-159">2-й год</span><span class="sxs-lookup"><span data-stu-id="3763d-159">Year 2</span></span> | <span data-ttu-id="3763d-160">6 000 × 40% = 2 400</span><span class="sxs-lookup"><span data-stu-id="3763d-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="3763d-161">7 000 – 2 400 = 4 600</span><span class="sxs-lookup"><span data-stu-id="3763d-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="3763d-162">6 000 – 2 400 = 3 600</span><span class="sxs-lookup"><span data-stu-id="3763d-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="3763d-163">3-й год</span><span class="sxs-lookup"><span data-stu-id="3763d-163">Year 3</span></span> | <span data-ttu-id="3763d-164">3 600 × 40% = 1 440</span><span class="sxs-lookup"><span data-stu-id="3763d-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="3763d-165">4 600 – 1 440 = 3 160</span><span class="sxs-lookup"><span data-stu-id="3763d-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="3763d-166">3 600 – 1 440 = 2 160</span><span class="sxs-lookup"><span data-stu-id="3763d-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="3763d-167">Обычно если сумма, которая вычислена с помощью метода амортизации с уменьшаемым сальдо в 200%, становится меньше суммы, которая была бы получена при использовании метода прямой линии, производится переход на метод прямой линии на оставшийся срок службы.</span><span class="sxs-lookup"><span data-stu-id="3763d-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]