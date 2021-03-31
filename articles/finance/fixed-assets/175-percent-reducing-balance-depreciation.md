---
title: Амортизация с уменьшаемым остатком в 175 %
description: Этот раздел содержит обзор метода амортизации с уменьшаемым остатком в 175 %.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8138003971ace280b08760df718671b1779bd101
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230354"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="26543-103">Амортизация с уменьшаемым остатком в 175 %</span><span class="sxs-lookup"><span data-stu-id="26543-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26543-104">Этот раздел содержит обзор метода амортизации с уменьшаемым остатком в 175 %.</span><span class="sxs-lookup"><span data-stu-id="26543-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="26543-105">После настройки профиля амортизации ОС и выбора значения **Уменьшаемое сальдо в 175%** в поле **Метод** на странице **Профили амортизации** процент амортизации ОС, назначенных профилю амортизации, одинаков во все периоды амортизации.</span><span class="sxs-lookup"><span data-stu-id="26543-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="26543-106">Чтобы установить амортизацию с уменьшаемым сальдо в 175%, также необходимо выбрать параметры в полях **Год амортизации** и **Частота периода** на странице **Профили амортизации**.</span><span class="sxs-lookup"><span data-stu-id="26543-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="26543-107">Варианты, которые доступны в поле **Частота периода**, зависят от значения, которое выбрано в поле **Год амортизации**.</span><span class="sxs-lookup"><span data-stu-id="26543-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="26543-108">Выбор года амортизации</span><span class="sxs-lookup"><span data-stu-id="26543-108">Select a depreciation year</span></span>
<span data-ttu-id="26543-109">Вы можете выбрать **Календарь** или **Фискальный** в поле **Год амортизации** на странице **Методы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="26543-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="26543-110">Значение по умолчанию равно **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="26543-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="26543-111">Выбранный вариант определяет параметры, доступные в поле **Частота периода**.</span><span class="sxs-lookup"><span data-stu-id="26543-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="26543-112">Это поле определяет даты и суммы разноски амортизационных начислений в течении календарного года.</span><span class="sxs-lookup"><span data-stu-id="26543-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="26543-113">Календарь</span><span class="sxs-lookup"><span data-stu-id="26543-113">Calendar</span></span>

<span data-ttu-id="26543-114">Можно сохранить значение по умолчанию в поле **Год амортизации**, **Календарь**.</span><span class="sxs-lookup"><span data-stu-id="26543-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="26543-115">Параметр **Календарь** обновляет базу амортизации 1-го января каждого года.</span><span class="sxs-lookup"><span data-stu-id="26543-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="26543-116">Обычно базой амортизации является остаточная стоимость минус ликвидационная стоимость.</span><span class="sxs-lookup"><span data-stu-id="26543-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="26543-117">В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов.</span><span class="sxs-lookup"><span data-stu-id="26543-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="26543-118">Если для года амортизации выбран вариант **Календарь**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="26543-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="26543-119">**Ежегодно** — разноска суммы 31-го декабря.</span><span class="sxs-lookup"><span data-stu-id="26543-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="26543-120">**Ежемесячно** — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.</span><span class="sxs-lookup"><span data-stu-id="26543-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="26543-121">**Ежеквартально** — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="26543-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="26543-122">**Каждый полгода** — разноска суммы за полгода один раз в конце календарного полугодия (30 июня и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="26543-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="26543-123">**Ежедневно** — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.</span><span class="sxs-lookup"><span data-stu-id="26543-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="26543-124">Финансовый</span><span class="sxs-lookup"><span data-stu-id="26543-124">Fiscal</span></span>

<span data-ttu-id="26543-125">Если вы выберете **Финансовый** в поле **Год амортизации**, амортизация с уменьшаемым сальдо в 175% рассчитывается на основе финансового года для финансового календаря, заданного для книги, или по финансовому календарю, выбранному на странице **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="26543-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="26543-126">Финансовые календари настраиваются на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="26543-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="26543-127">Подробные сведения см. на странице [Финансовые календари, финансовые годы и периоды](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="26543-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="26543-128">Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля.</span><span class="sxs-lookup"><span data-stu-id="26543-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="26543-129">Финансовый год может быть длиннее или короче 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="26543-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="26543-130">Амортизация автоматически регулируется для каждого финансового периода, а длительность следующего финансового года определяется на настройкой периодов на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="26543-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="26543-131">Если для года амортизации выбран вариант **Финансовый**, в поле **Частота периода** доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="26543-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="26543-132">**Ежегодно** — разноска общей суммы амортизации, рассчитанной для финансового года в последний день финансового года.</span><span class="sxs-lookup"><span data-stu-id="26543-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="26543-133">**Финансовый период** — высчитывает полную сумму амортизации за финансовый год.</span><span class="sxs-lookup"><span data-stu-id="26543-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="26543-134">Это количество начисляется в фискальные периоды, которые определены на странице **Финансовые календари**.</span><span class="sxs-lookup"><span data-stu-id="26543-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="26543-135">Пример амортизации уменьшаемого сальдо в 175%</span><span class="sxs-lookup"><span data-stu-id="26543-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="26543-136">Стоимость приобретения</span><span class="sxs-lookup"><span data-stu-id="26543-136">Acquisition cost</span></span>               | <span data-ttu-id="26543-137">11 000</span><span class="sxs-lookup"><span data-stu-id="26543-137">11,000</span></span> |
| <span data-ttu-id="26543-138">Ликвидационная стоимость</span><span class="sxs-lookup"><span data-stu-id="26543-138">Salvage value</span></span>                  | <span data-ttu-id="26543-139">1,000</span><span class="sxs-lookup"><span data-stu-id="26543-139">1,000</span></span>  |
| <span data-ttu-id="26543-140">База амортизации</span><span class="sxs-lookup"><span data-stu-id="26543-140">Depreciation base</span></span>              | <span data-ttu-id="26543-141">10 000</span><span class="sxs-lookup"><span data-stu-id="26543-141">10,000</span></span> |
| <span data-ttu-id="26543-142">Срок службы в годах</span><span class="sxs-lookup"><span data-stu-id="26543-142">Service life years</span></span>             | <span data-ttu-id="26543-143">5</span><span class="sxs-lookup"><span data-stu-id="26543-143">5</span></span>      |
| <span data-ttu-id="26543-144">Процент ежегодной амортизации</span><span class="sxs-lookup"><span data-stu-id="26543-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="26543-145">35%</span><span class="sxs-lookup"><span data-stu-id="26543-145">35%</span></span>    |

<span data-ttu-id="26543-146">В методе амортизации с уменьшаемым остатком 175% значение в 175 процентов делится на количество лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="26543-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="26543-147">Этот процент умножается на остаточную стоимость актива для определения суммы амортизационных начислений за год.</span><span class="sxs-lookup"><span data-stu-id="26543-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="26543-148">Период</span><span class="sxs-lookup"><span data-stu-id="26543-148">Period</span></span> | <span data-ttu-id="26543-149">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="26543-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="26543-150">Остаточная стоимость</span><span class="sxs-lookup"><span data-stu-id="26543-150">Book value</span></span>                  | <span data-ttu-id="26543-151">Остаточная стоимость на конец года</span><span class="sxs-lookup"><span data-stu-id="26543-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="26543-152">1-й год</span><span class="sxs-lookup"><span data-stu-id="26543-152">Year 1</span></span> | <span data-ttu-id="26543-153">(11000 – 1000) × 35% = 3500</span><span class="sxs-lookup"><span data-stu-id="26543-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="26543-154">11000 – 3500 = 7500</span><span class="sxs-lookup"><span data-stu-id="26543-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="26543-155">11000 – 1000 – 3500 = 6500</span><span class="sxs-lookup"><span data-stu-id="26543-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="26543-156">2-й год</span><span class="sxs-lookup"><span data-stu-id="26543-156">Year 2</span></span> | <span data-ttu-id="26543-157">6500 × 35% = 2275</span><span class="sxs-lookup"><span data-stu-id="26543-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="26543-158">7500 – 2275 = 5225</span><span class="sxs-lookup"><span data-stu-id="26543-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="26543-159">6500 – 2275 = 4225</span><span class="sxs-lookup"><span data-stu-id="26543-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="26543-160">3-й год</span><span class="sxs-lookup"><span data-stu-id="26543-160">Year 3</span></span> | <span data-ttu-id="26543-161">4225 × 35% = 1478,75</span><span class="sxs-lookup"><span data-stu-id="26543-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="26543-162">5225 – 1478,75 = 3746,25</span><span class="sxs-lookup"><span data-stu-id="26543-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="26543-163">4225 – 1478,75 = 2746,25</span><span class="sxs-lookup"><span data-stu-id="26543-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="26543-164">Обычно если сумма, которая вычислена с помощью метода амортизации с уменьшаемым сальдо в 175%, становится меньше суммы, которая была бы получена при использовании метода прямой линии, производится переход на метод прямой линии на оставшийся срок службы.</span><span class="sxs-lookup"><span data-stu-id="26543-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]