---
title: Амортизация с уменьшаемым остатком в 125%
description: Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 125%.
author: saraschi2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d05ec02d47a563c0d7ae7cb0fafdbad45bd140
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827202"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="d2506-103">Амортизация с уменьшаемым остатком в 125%</span><span class="sxs-lookup"><span data-stu-id="d2506-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2506-104">Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 125%.</span><span class="sxs-lookup"><span data-stu-id="d2506-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="d2506-105">После настройки профиля амортизации ОС и выбора значения **Уменьшаемое сальдо в 125%** в поле **Метод** на странице **Методы амортизации** процент амортизации ОС, назначенных профилю амортизации, одинаков во все периоды амортизации.</span><span class="sxs-lookup"><span data-stu-id="d2506-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="d2506-106">Этот процент рассчитывается на основе срока службы актива.</span><span class="sxs-lookup"><span data-stu-id="d2506-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="d2506-107">Например, если срок службы актива составляет пять лет, проценты будут рассчитаны как 25 процентов (125% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="d2506-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="d2506-108">Чтобы установить амортизацию с уменьшаемым сальдо в 125%, также необходимо выбрать параметры в полях **Год амортизации** и **Частота периода** на странице **Методы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="d2506-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d2506-109">Варианты, которые доступны в поле **Частота периода**, зависят от значения, которое выбрано в поле **Год амортизации**.</span><span class="sxs-lookup"><span data-stu-id="d2506-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="d2506-110">Выбор года амортизации</span><span class="sxs-lookup"><span data-stu-id="d2506-110">Select a depreciation year</span></span>
<span data-ttu-id="d2506-111">Вы можете выбрать **Календарь** или **Фискальный** в поле **Год амортизации** на странице **Методы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="d2506-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d2506-112">Значение по умолчанию равно **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="d2506-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="d2506-113">Выбранный вариант определяет параметры, доступные в поле **Частота периода**.</span><span class="sxs-lookup"><span data-stu-id="d2506-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="d2506-114">Это поле определяет даты и суммы разноски амортизационных начислений в течении календарного года.</span><span class="sxs-lookup"><span data-stu-id="d2506-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="d2506-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="d2506-115">Calendar</span></span>

<span data-ttu-id="d2506-116">Можно сохранить значение по умолчанию в поле **Год амортизации**, **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="d2506-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="d2506-117">Параметр **Календарь** обновляет базу амортизации 1-го января каждого года.</span><span class="sxs-lookup"><span data-stu-id="d2506-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="d2506-118">Обычно базой амортизации является остаточная стоимость минус ликвидационная стоимость.</span><span class="sxs-lookup"><span data-stu-id="d2506-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="d2506-119">В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов.</span><span class="sxs-lookup"><span data-stu-id="d2506-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="d2506-120">Если для года амортизации выбран вариант **Календарь**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="d2506-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d2506-121">**Ежегодно** — разноска суммы 31-го декабря.</span><span class="sxs-lookup"><span data-stu-id="d2506-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="d2506-122">**Ежемесячно** — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.</span><span class="sxs-lookup"><span data-stu-id="d2506-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="d2506-123">**Ежеквартально** — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="d2506-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="d2506-124">**Каждый полгода** — разноска суммы за полгода один раз в конце календарного полугодия (30 июня и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="d2506-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="d2506-125">**Ежедневно** — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.</span><span class="sxs-lookup"><span data-stu-id="d2506-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="d2506-126">Финансовый</span><span class="sxs-lookup"><span data-stu-id="d2506-126">Fiscal</span></span>

<span data-ttu-id="d2506-127">Если вы выберете **Финансовый** в поле **Год амортизации**, амортизация с уменьшением в 125% рассчитывается на основе финансового года для финансового календаря, заданного для книги, или по финансовому календарю, выбранному на странице **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="d2506-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="d2506-128">Финансовые календари настраиваются на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="d2506-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d2506-129">Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля.</span><span class="sxs-lookup"><span data-stu-id="d2506-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="d2506-130">Финансовый год может быть длиннее или короче 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="d2506-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="d2506-131">Амортизация автоматически регулируется для каждого финансового периода, а длительность следующего финансового года определяется на настройкой периодов на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="d2506-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d2506-132">Если для года амортизации выбран вариант **Финансовый**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="d2506-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d2506-133">**Ежегодно** — разноска общей суммы амортизации, рассчитанной для финансового года как единая сумма в последний день финансового года.</span><span class="sxs-lookup"><span data-stu-id="d2506-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="d2506-134">**Финансовый период** разносит полную сумму амортизации, вычисленную за финансовый год.</span><span class="sxs-lookup"><span data-stu-id="d2506-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="d2506-135">Это количество начисляется в фискальные периоды, которые определены на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="d2506-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="d2506-136">Пример амортизации уменьшаемого сальдо в 125%</span><span class="sxs-lookup"><span data-stu-id="d2506-136">Example of 125% reducing balance depreciation</span></span>

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| <span data-ttu-id="d2506-137">Стоимость приобретения</span><span class="sxs-lookup"><span data-stu-id="d2506-137">Acquisition cost</span></span>               | <span data-ttu-id="d2506-138">11 000</span><span class="sxs-lookup"><span data-stu-id="d2506-138">11,000</span></span> |
| <span data-ttu-id="d2506-139">Ликвидационная стоимость</span><span class="sxs-lookup"><span data-stu-id="d2506-139">Salvage value</span></span>                  | <span data-ttu-id="d2506-140">1,000</span><span class="sxs-lookup"><span data-stu-id="d2506-140">1,000</span></span>  |
| <span data-ttu-id="d2506-141">База амортизации</span><span class="sxs-lookup"><span data-stu-id="d2506-141">Depreciation base</span></span>              | <span data-ttu-id="d2506-142">10 000</span><span class="sxs-lookup"><span data-stu-id="d2506-142">10,000</span></span> |
| <span data-ttu-id="d2506-143">Годы срока службы</span><span class="sxs-lookup"><span data-stu-id="d2506-143">Service life years</span></span>             | <span data-ttu-id="d2506-144">5</span><span class="sxs-lookup"><span data-stu-id="d2506-144">5</span></span>      |
| <span data-ttu-id="d2506-145">Процент ежегодной амортизации</span><span class="sxs-lookup"><span data-stu-id="d2506-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="d2506-146">25%</span><span class="sxs-lookup"><span data-stu-id="d2506-146">25%</span></span>    |

<span data-ttu-id="d2506-147">В методе уменьшаемого остатка с коэффициентом 125% значение в 125 процентов делится на количество лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="d2506-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="d2506-148">Этот процент умножается на остаточную стоимость актива для определения суммы амортизационных начислений за год.</span><span class="sxs-lookup"><span data-stu-id="d2506-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="d2506-149">Период</span><span class="sxs-lookup"><span data-stu-id="d2506-149">Period</span></span> | <span data-ttu-id="d2506-150">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="d2506-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="d2506-151">Остаточная стоимость</span><span class="sxs-lookup"><span data-stu-id="d2506-151">Book value</span></span>                    | <span data-ttu-id="d2506-152">Остаточная стоимость на конец года</span><span class="sxs-lookup"><span data-stu-id="d2506-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="d2506-153">1-й год</span><span class="sxs-lookup"><span data-stu-id="d2506-153">Year 1</span></span> | <span data-ttu-id="d2506-154">(11000 – 1000) × 25% = 2500</span><span class="sxs-lookup"><span data-stu-id="d2506-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="d2506-155">(11000 – 2500) = 8500</span><span class="sxs-lookup"><span data-stu-id="d2506-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="d2506-156">(11000 – 1000 – 2500) = 7500</span><span class="sxs-lookup"><span data-stu-id="d2506-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="d2506-157">2-й год</span><span class="sxs-lookup"><span data-stu-id="d2506-157">Year 2</span></span> | <span data-ttu-id="d2506-158">7500 × 25% = 1875</span><span class="sxs-lookup"><span data-stu-id="d2506-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="d2506-159">(8500 – 1875) = 6625</span><span class="sxs-lookup"><span data-stu-id="d2506-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="d2506-160">(7500 – 1875) = 5625</span><span class="sxs-lookup"><span data-stu-id="d2506-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="d2506-161">3-й год</span><span class="sxs-lookup"><span data-stu-id="d2506-161">Year 3</span></span> | <span data-ttu-id="d2506-162">5625 × 25% = 1406,25</span><span class="sxs-lookup"><span data-stu-id="d2506-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="d2506-163">(6625 – 1406,25) = 5218,75</span><span class="sxs-lookup"><span data-stu-id="d2506-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="d2506-164">(5625 – 1406,25) = 4218,75</span><span class="sxs-lookup"><span data-stu-id="d2506-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="d2506-165">Обычно если сумма, которая вычислена с помощью метода амортизации с уменьшаемым сальдо в 125%, становится меньше суммы, которая была бы получена при использовании метода прямой линии, производится переход на метод прямой линии на оставшийся срок службы.</span><span class="sxs-lookup"><span data-stu-id="d2506-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]