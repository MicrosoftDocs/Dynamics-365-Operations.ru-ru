---
title: "Амортизация срока службы (прямолинейный метод)"
description: "Эта статья содержит обзор метода линейной амортизации."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b48cf3970379f8dd2ea529cd8a434c0bdc196a1e
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="c9f7b-103">Амортизация срока службы (прямолинейный метод)</span><span class="sxs-lookup"><span data-stu-id="c9f7b-103">Straight line service life depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f7b-104">Эта статья содержит обзор метода линейной амортизации.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="c9f7b-105">Если при настройке профиля амортизации основных средств выбрано значение "Срок службы (прямолинейный метод)" в поле "Метод" на странице "Профили амортизации", амортизация основных средств, назначенных этому профилю амортизации, основывается на общем сроке службы основного средства.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="c9f7b-106">Обычно это одна и та же сумма амортизации в каждый период амортизации.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="c9f7b-107">Разницу между суммой амортизации, рассчитанной между оставшимся сроком службы (прямолинейный метод) и сроком службы (прямолинейный метод), составляет разнесенная в актив переоценка.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="c9f7b-108">Чтобы установить линейную амортизацию по сроку службы, также необходимо выбрать параметры в полях "Год амортизации" и "Частота периода" на странице "Профили амортизации".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="c9f7b-109">Выбор года амортизации</span><span class="sxs-lookup"><span data-stu-id="c9f7b-109">Select a depreciation year</span></span>
<span data-ttu-id="c9f7b-110">Вы можете выбрать "Календарь" или "Фискальный" в поле "Год амортизации" на странице "Методы амортизации".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="c9f7b-111">Выбранный вариант определяет параметры, доступные в поле "Частота периода".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="c9f7b-112">Значение по умолчанию — "Календарь".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="c9f7b-113">Календарь</span><span class="sxs-lookup"><span data-stu-id="c9f7b-113">Calendar</span></span>

<span data-ttu-id="c9f7b-114">При выборе значения "Календарь" используется год с 1-го января по 31-е декабря, даже если финансовый календарь задан иначе.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="c9f7b-115">Параметр "Календарь" обновляет базу амортизации (обычно остаточная стоимость минус ликвидационная стоимость) 1-го января каждого года.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="c9f7b-116">В примерах ниже база амортизации является числителем в первом выражении в столбце расчетов.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="c9f7b-117">Если выбран "Календарь", то в поле "Частота периода" имеются следующие параметры, которые определяют даты и суммы разноски амортизационных начислений в течение календарного года:</span><span class="sxs-lookup"><span data-stu-id="c9f7b-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="c9f7b-118">Ежегодно — разноска суммы 31-го декабря.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="c9f7b-119">Ежемесячно — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="c9f7b-120">Ежеквартально — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="c9f7b-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="c9f7b-121">Полгода — разноска суммы за полгода один раз в конце каждого календарного полугодия (30 июня и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="c9f7b-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="c9f7b-122">Ежедневная — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="c9f7b-123">Например, если выбрать параметр "Ежегодно", годовая амортизация разносится только один раз, каждый год 31 декабря.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="c9f7b-124">Если выбрать параметр "Ежемесячно", месячная амортизация разносится каждый месяц в сумме, равной 1/12 от суммы за год.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="c9f7b-125">Финансовый</span><span class="sxs-lookup"><span data-stu-id="c9f7b-125">Fiscal</span></span>

<span data-ttu-id="c9f7b-126">При выборе параметра "Финансовый" в поле "Год амортизации" используется линейная амортизация по сроку службы.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="c9f7b-127">Эта сумма рассчитывается на основе финансового года, который определен финансовым календарем, указанным для книги, или финансовым календарем, выбранным на странице "Книга учета".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="c9f7b-128">Финансовые календари настраиваются на странице "Финансовые календари".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="c9f7b-129">Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="c9f7b-130">Финансовый год может быть длиннее или короче 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="c9f7b-131">Амортизация корректируется автоматически для каждого финансового периода.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="c9f7b-132">Продолжительность следующего финансового года определяется по финансовым периодам, настроенным при создании нового финансового года в форме "Финансовые календари".</span><span class="sxs-lookup"><span data-stu-id="c9f7b-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="c9f7b-133">Если выбрать "Финансовый" в поле "Частота периода", доступны следующие параметры частоты периода:</span><span class="sxs-lookup"><span data-stu-id="c9f7b-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="c9f7b-134">"Ежегодно" — разноска общей суммы амортизации, рассчитанной для финансового года как единая сумма в последний день финансового года.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="c9f7b-135">"Финансовый период" — расчет общей суммы амортизации, вычисленной для финансового года, начисляемой в финансовые периоды, которые определяются в форме "Финансовые календари" для финансового календаря.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="c9f7b-136">Пример: линейная амортизации неизменного основного средства</span><span class="sxs-lookup"><span data-stu-id="c9f7b-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="c9f7b-137">Предположим, что ОС обладает следующими характеристиками:</span><span class="sxs-lookup"><span data-stu-id="c9f7b-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="c9f7b-138">Стоимость приобретения</span><span class="sxs-lookup"><span data-stu-id="c9f7b-138">Acquisition cost</span></span>    | <span data-ttu-id="c9f7b-139">11 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-139">11,000</span></span> |
| <span data-ttu-id="c9f7b-140">Ликвидационная стоимость</span><span class="sxs-lookup"><span data-stu-id="c9f7b-140">Salvage value</span></span>       | <span data-ttu-id="c9f7b-141">1000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-141">1,000</span></span>  |
| <span data-ttu-id="c9f7b-142">База амортизации</span><span class="sxs-lookup"><span data-stu-id="c9f7b-142">Depreciation base</span></span>   | <span data-ttu-id="c9f7b-143">10 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-143">10,000</span></span> |
| <span data-ttu-id="c9f7b-144">Годы срока службы</span><span class="sxs-lookup"><span data-stu-id="c9f7b-144">Service life years</span></span>  | <span data-ttu-id="c9f7b-145">5</span><span class="sxs-lookup"><span data-stu-id="c9f7b-145">5</span></span>      |
| <span data-ttu-id="c9f7b-146">Ежегодная амортизация</span><span class="sxs-lookup"><span data-stu-id="c9f7b-146">Yearly depreciation</span></span> | <span data-ttu-id="c9f7b-147">2 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-147">2,000</span></span>  |

<span data-ttu-id="c9f7b-148">Ежегодно вы получаете одну и ту же сумму амортизации.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="c9f7b-149">(Затраты на приобретение -стоимость ликвидации) / годы срока службы</span><span class="sxs-lookup"><span data-stu-id="c9f7b-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="c9f7b-150">Период</span><span class="sxs-lookup"><span data-stu-id="c9f7b-150">Period</span></span> | <span data-ttu-id="c9f7b-151">Расчет суммы ежегодной амортизации</span><span class="sxs-lookup"><span data-stu-id="c9f7b-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="c9f7b-152">Остаточная стоимость в конце года</span><span class="sxs-lookup"><span data-stu-id="c9f7b-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="c9f7b-153">Год 1</span><span class="sxs-lookup"><span data-stu-id="c9f7b-153">Year 1</span></span> | <span data-ttu-id="c9f7b-154">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c9f7b-155">9000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-155">9,000</span></span>                                 |
| <span data-ttu-id="c9f7b-156">Год 2</span><span class="sxs-lookup"><span data-stu-id="c9f7b-156">Year 2</span></span> | <span data-ttu-id="c9f7b-157">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c9f7b-158">7 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-158">7,000</span></span>                                 |
| <span data-ttu-id="c9f7b-159">Год 3</span><span class="sxs-lookup"><span data-stu-id="c9f7b-159">Year 3</span></span> | <span data-ttu-id="c9f7b-160">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c9f7b-161">5 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-161">5,000</span></span>                                 |
| <span data-ttu-id="c9f7b-162">Год 4</span><span class="sxs-lookup"><span data-stu-id="c9f7b-162">Year 4</span></span> | <span data-ttu-id="c9f7b-163">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c9f7b-164">3 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-164">3,000</span></span>                                 |
| <span data-ttu-id="c9f7b-165">Год 5</span><span class="sxs-lookup"><span data-stu-id="c9f7b-165">Year 5</span></span> | <span data-ttu-id="c9f7b-166">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c9f7b-167">1000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="c9f7b-168">Пример: Амортизация (прямолинейный метод) неизменного ОС</span><span class="sxs-lookup"><span data-stu-id="c9f7b-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="c9f7b-169">предположим, что вы добавили переоценку ввода в эксплуатацию, равную 4 000 в год 2 к тому же ОС.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="c9f7b-170">Срок службы переоценки ввода в эксплуатацию равен сроку службы ОС и начинается с момента ввода в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="c9f7b-171">Остаточная стоимость в конце года 5 соответствует остаточной стоимости переоценки приобретения.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="c9f7b-172">Способ расчета амортизации по периоду показан в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="c9f7b-173">Период</span><span class="sxs-lookup"><span data-stu-id="c9f7b-173">Period</span></span> | <span data-ttu-id="c9f7b-174">Расчет суммы ежегодной амортизации</span><span class="sxs-lookup"><span data-stu-id="c9f7b-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="c9f7b-175">Остаточная стоимость в конце года</span><span class="sxs-lookup"><span data-stu-id="c9f7b-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="c9f7b-176">Год 1</span><span class="sxs-lookup"><span data-stu-id="c9f7b-176">Year 1</span></span> | <span data-ttu-id="c9f7b-177">10 000 / 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="c9f7b-178">11 000 - 2 000 = 9 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="c9f7b-179">Год 2</span><span class="sxs-lookup"><span data-stu-id="c9f7b-179">Year 2</span></span> | <span data-ttu-id="c9f7b-180">4 000 (Переоценка стоимости ввода в эксплуатацию)</span><span class="sxs-lookup"><span data-stu-id="c9f7b-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="c9f7b-181">9 000 + 4 000 =13 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="c9f7b-182">Год 2</span><span class="sxs-lookup"><span data-stu-id="c9f7b-182">Year 2</span></span> | <span data-ttu-id="c9f7b-183">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="c9f7b-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c9f7b-184">13 000 - 2 800 = 10 200</span><span class="sxs-lookup"><span data-stu-id="c9f7b-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="c9f7b-185">Год 3</span><span class="sxs-lookup"><span data-stu-id="c9f7b-185">Year 3</span></span> | <span data-ttu-id="c9f7b-186">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="c9f7b-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c9f7b-187">10 200 - 2 800 = 7 400</span><span class="sxs-lookup"><span data-stu-id="c9f7b-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="c9f7b-188">Год 4</span><span class="sxs-lookup"><span data-stu-id="c9f7b-188">Year 4</span></span> | <span data-ttu-id="c9f7b-189">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="c9f7b-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c9f7b-190">7 400 - 2 800 = 4 600</span><span class="sxs-lookup"><span data-stu-id="c9f7b-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="c9f7b-191">Год 5</span><span class="sxs-lookup"><span data-stu-id="c9f7b-191">Year 5</span></span> | <span data-ttu-id="c9f7b-192">14 000 / 5 = 2 800</span><span class="sxs-lookup"><span data-stu-id="c9f7b-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c9f7b-193">4 600 - 2 800 = 1 800</span><span class="sxs-lookup"><span data-stu-id="c9f7b-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="c9f7b-194">Год 6</span><span class="sxs-lookup"><span data-stu-id="c9f7b-194">Year 6</span></span> | <span data-ttu-id="c9f7b-195">Остаток 800\*</span><span class="sxs-lookup"><span data-stu-id="c9f7b-195">Remaining 800\*</span></span>                           | <span data-ttu-id="c9f7b-196">1 800 – 800 = 1 000</span><span class="sxs-lookup"><span data-stu-id="c9f7b-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="c9f7b-197">\*Так как сумма остатка меньше суммы амортизации, в расчет берется только сумма остатка, которая меньше ликвидационной стоимости.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






