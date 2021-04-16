---
title: Амортизация с уменьшаемым остатком в 150%
description: Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 150 %.
author: saraschi2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1c6b7e92ea8b20123c0b1c1747c49847b0e2420
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827178"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="39f72-103">Амортизация с уменьшаемым остатком в 150%</span><span class="sxs-lookup"><span data-stu-id="39f72-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39f72-104">Эта статья содержит обзор метода амортизации с уменьшаемым остатком в 150 %.</span><span class="sxs-lookup"><span data-stu-id="39f72-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="39f72-105">После настройки профиля амортизации ОС и выбора значения **Уменьшаемое сальдо в 150%** в поле **Метод** на странице **Профили амортизации** процент амортизации ОС, назначенных профилю амортизации, одинаков во все периоды амортизации.</span><span class="sxs-lookup"><span data-stu-id="39f72-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="39f72-106">Этот процент рассчитывается на основе срока службы актива.</span><span class="sxs-lookup"><span data-stu-id="39f72-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="39f72-107">Например, если срок службы актива составляет пять лет, проценты будут рассчитаны как 30 процентов (150% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="39f72-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="39f72-108">Чтобы установить амортизацию с уменьшаемым сальдо в 150%, также необходимо выбрать параметры в полях **Год амортизации** и **Частота периода** на странице **Профили амортизации**.</span><span class="sxs-lookup"><span data-stu-id="39f72-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="39f72-109">Варианты, которые доступны в поле **Частота периода**, зависят от значения, которое выбрано в поле **Год амортизации**.</span><span class="sxs-lookup"><span data-stu-id="39f72-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="39f72-110">Выбор года амортизации</span><span class="sxs-lookup"><span data-stu-id="39f72-110">Selection of depreciation year</span></span>
<span data-ttu-id="39f72-111">Вы можете выбрать **Календарь** или **Фискальный** в поле **Год амортизации** на странице **Методы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="39f72-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="39f72-112">Значение по умолчанию равно **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="39f72-112">The default value is **Calendar**.</span></span> <span data-ttu-id="39f72-113">Выбранный вариант определяет параметры, доступные в поле **Частота периода**.</span><span class="sxs-lookup"><span data-stu-id="39f72-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="39f72-114">Это поле определяет даты и суммы разноски амортизационных начислений в течении календарного года.</span><span class="sxs-lookup"><span data-stu-id="39f72-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="39f72-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="39f72-115">Calendar</span></span>

<span data-ttu-id="39f72-116">Можно сохранить значение по умолчанию в поле **Год амортизации**, **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="39f72-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="39f72-117">Параметр **Календарь** обновляет базу амортизации 1-го января каждого года.</span><span class="sxs-lookup"><span data-stu-id="39f72-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="39f72-118">Обычно базой амортизации является остаточная стоимость минус ликвидационная стоимость.</span><span class="sxs-lookup"><span data-stu-id="39f72-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="39f72-119">В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов.</span><span class="sxs-lookup"><span data-stu-id="39f72-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="39f72-120">Если для года амортизации выбран вариант **Календарь**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="39f72-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="39f72-121">**Ежегодно** — разноска суммы 31-го декабря.</span><span class="sxs-lookup"><span data-stu-id="39f72-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="39f72-122">**Ежемесячно** — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.</span><span class="sxs-lookup"><span data-stu-id="39f72-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="39f72-123">**Ежеквартально** — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="39f72-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="39f72-124">**Каждый полгода** — разноска суммы за полгода один раз в конце календарного полугодия (30 июня и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="39f72-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="39f72-125">**Ежедневно** — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.</span><span class="sxs-lookup"><span data-stu-id="39f72-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="39f72-126">Финансовый</span><span class="sxs-lookup"><span data-stu-id="39f72-126">Fiscal</span></span>

<span data-ttu-id="39f72-127">Если вы выберете **Финансовый** в поле **Год амортизации**, амортизация с уменьшаемым сальдо в 150% рассчитывается на основе финансового года для финансового календаря, заданного для книги, или по финансовому календарю, выбранному на странице **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="39f72-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="39f72-128">Финансовые календари настраиваются на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="39f72-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="39f72-129">Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля.</span><span class="sxs-lookup"><span data-stu-id="39f72-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="39f72-130">Финансовый год может быть длиннее или короче 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="39f72-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="39f72-131">Амортизация корректируется для каждого периода.</span><span class="sxs-lookup"><span data-stu-id="39f72-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="39f72-132">Длительность следующего финансового года определяется на основе настройки периодов, которые определяются на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="39f72-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="39f72-133">Если для года амортизации выбран вариант **Финансовый**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="39f72-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="39f72-134">**Ежегодно** — разноска общей суммы амортизации, рассчитанной для финансового года в последний день финансового года.</span><span class="sxs-lookup"><span data-stu-id="39f72-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="39f72-135">**Финансовый период** разносит полную сумму амортизации, вычисленную за финансовый год.</span><span class="sxs-lookup"><span data-stu-id="39f72-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="39f72-136">Это количество начисляется в фискальные периоды, которые определены на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="39f72-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="39f72-137">Пример амортизации с уменьшаемым остатком в 150%</span><span class="sxs-lookup"><span data-stu-id="39f72-137">Example of 150% reducing balance depreciation</span></span>

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| <span data-ttu-id="39f72-138">Стоимость приобретения</span><span class="sxs-lookup"><span data-stu-id="39f72-138">Acquisition cost</span></span>               | <span data-ttu-id="39f72-139">11,000</span><span class="sxs-lookup"><span data-stu-id="39f72-139">11,000</span></span> |
| <span data-ttu-id="39f72-140">Ликвидационная стоимость</span><span class="sxs-lookup"><span data-stu-id="39f72-140">Salvage value</span></span>                  | <span data-ttu-id="39f72-141">1,000</span><span class="sxs-lookup"><span data-stu-id="39f72-141">1,000</span></span>  |
| <span data-ttu-id="39f72-142">База амортизации</span><span class="sxs-lookup"><span data-stu-id="39f72-142">Depreciation base</span></span>              | <span data-ttu-id="39f72-143">10,000</span><span class="sxs-lookup"><span data-stu-id="39f72-143">10,000</span></span> |
| <span data-ttu-id="39f72-144">Годы срока службы</span><span class="sxs-lookup"><span data-stu-id="39f72-144">Service life years</span></span>             | <span data-ttu-id="39f72-145">5</span><span class="sxs-lookup"><span data-stu-id="39f72-145">5</span></span>      |
| <span data-ttu-id="39f72-146">Процент ежегодной амортизации</span><span class="sxs-lookup"><span data-stu-id="39f72-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="39f72-147">30%</span><span class="sxs-lookup"><span data-stu-id="39f72-147">30%</span></span>    |

<span data-ttu-id="39f72-148">В методе уменьшаемого остатка с коэффициентом 150% значение в 150 процентов делится на количество лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="39f72-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="39f72-149">Этот процент умножается на остаточную стоимость актива для определения суммы амортизационных начислений за год.</span><span class="sxs-lookup"><span data-stu-id="39f72-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="39f72-150">Период</span><span class="sxs-lookup"><span data-stu-id="39f72-150">Period</span></span> | <span data-ttu-id="39f72-151">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="39f72-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="39f72-152">Остаточная стоимость</span><span class="sxs-lookup"><span data-stu-id="39f72-152">Book value</span></span>             | <span data-ttu-id="39f72-153">Остаточная стоимость на конец года</span><span class="sxs-lookup"><span data-stu-id="39f72-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="39f72-154">1-й год</span><span class="sxs-lookup"><span data-stu-id="39f72-154">Year 1</span></span> | <span data-ttu-id="39f72-155">(11000 – 1000) × 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="39f72-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="39f72-156">11000 – 3000 = 8000</span><span class="sxs-lookup"><span data-stu-id="39f72-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="39f72-157">11000 – 1000 – 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="39f72-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="39f72-158">2-й год</span><span class="sxs-lookup"><span data-stu-id="39f72-158">Year 2</span></span> | <span data-ttu-id="39f72-159">7000 × 30% = 2100</span><span class="sxs-lookup"><span data-stu-id="39f72-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="39f72-160">8,000 – 2,100 = 5,900</span><span class="sxs-lookup"><span data-stu-id="39f72-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="39f72-161">7,000 – 2,100 = 4,900</span><span class="sxs-lookup"><span data-stu-id="39f72-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="39f72-162">3-й год</span><span class="sxs-lookup"><span data-stu-id="39f72-162">Year 3</span></span> | <span data-ttu-id="39f72-163">4900 × 30% = 1470</span><span class="sxs-lookup"><span data-stu-id="39f72-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="39f72-164">5900 – 1470 = 4430</span><span class="sxs-lookup"><span data-stu-id="39f72-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="39f72-165">4900 – 1470 = 3430</span><span class="sxs-lookup"><span data-stu-id="39f72-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="39f72-166">Обычно если сумма, которая вычислена с помощью метода амортизации с уменьшаемым сальдо в 150%, становится меньше суммы, которая была бы получена при использовании метода прямой линии, производится переход на метод прямой линии на оставшийся срок службы.</span><span class="sxs-lookup"><span data-stu-id="39f72-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]