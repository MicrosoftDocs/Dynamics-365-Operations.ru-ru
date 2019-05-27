---
title: Амортизация с уменьшаемым остатком
description: Эта статья содержит обзор метода амортизации с уменьшаемым остатком.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e36a7e1a5d83a95de53b70b8e3c3b667aae9c6c0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553676"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="bf04e-103">Амортизация с уменьшаемым остатком</span><span class="sxs-lookup"><span data-stu-id="bf04e-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf04e-104">Эта статья содержит обзор метода амортизации с уменьшаемым остатком.</span><span class="sxs-lookup"><span data-stu-id="bf04e-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="bf04e-105">При настройке профиля амортизации ОС и выборе значения "Уменьшаемое сальдо" в поле "Метод" на странице "Методы амортизации" средства, имеющие этот профиль амортизации, назначенный им, амортизируются с одинаковым для всех периодов амортизации процентом.</span><span class="sxs-lookup"><span data-stu-id="bf04e-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="bf04e-106">Для настройки амортизации с уменьшаемым остатком необходимо заполнить поля на экспресс-вкладке "Общие" на странице "Метод амортизации".</span><span class="sxs-lookup"><span data-stu-id="bf04e-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="bf04e-107">Сначала в поле "Год амортизации" выберите год.</span><span class="sxs-lookup"><span data-stu-id="bf04e-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="bf04e-108">В зависимости от того, чтобы было выбрано, в поле "Частота периода" появятся различные варианты, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="bf04e-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="bf04e-109">Требуется также ввести значение в поле "Процент" для метода амортизации.</span><span class="sxs-lookup"><span data-stu-id="bf04e-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="bf04e-110">Если выбран параметр "Полная амортизация", основание амортизации с уменьшаемым остатком берется в последнем периоде амортизации и может составлять большую сумму.</span><span class="sxs-lookup"><span data-stu-id="bf04e-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="bf04e-111">В некоторых странах и регионах не применяется переключение на прямолинейный метод амортизации.</span><span class="sxs-lookup"><span data-stu-id="bf04e-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="bf04e-112">Переключение используется, когда сумма в альтернативном методе больше суммы в основном профиле амортизации, будет использоваться сумма амортизации из альтернативного метода.</span><span class="sxs-lookup"><span data-stu-id="bf04e-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="bf04e-113">Поскольку средства никогда не амортизируются в полном объеме на основании расчета процента, следует выбрать параметр "Полная амортизация", чтобы амортизировать средства полностью.</span><span class="sxs-lookup"><span data-stu-id="bf04e-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="bf04e-114">Выбор года амортизации</span><span class="sxs-lookup"><span data-stu-id="bf04e-114">Select a depreciation year</span></span>
<span data-ttu-id="bf04e-115">Вы можете выбрать "Календарь" или "Фискальный" в поле "Год амортизации" на странице "Методы амортизации".</span><span class="sxs-lookup"><span data-stu-id="bf04e-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="bf04e-116">Выбранный вариант определяет параметры, доступные в поле "Частота периода".</span><span class="sxs-lookup"><span data-stu-id="bf04e-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="bf04e-117">Значение по умолчанию — "Календарь".</span><span class="sxs-lookup"><span data-stu-id="bf04e-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="bf04e-118">Календарь</span><span class="sxs-lookup"><span data-stu-id="bf04e-118">Calendar</span></span>

<span data-ttu-id="bf04e-119">Параметр "Календарь" обновляет базу амортизации (обычно остаточная стоимость минус ликвидационная стоимость) 1-го января каждого года.</span><span class="sxs-lookup"><span data-stu-id="bf04e-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="bf04e-120">В приведенном ниже примере амортизации с уменьшаемым остатком база амортизации — числитель в первом выражении в вычислениях столбца.</span><span class="sxs-lookup"><span data-stu-id="bf04e-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="bf04e-121">Если выбран "Календарь", то в поле "Частота периода" имеются следующие параметры, которые определяют даты и суммы разноски амортизационных начислений в течение календарного года:</span><span class="sxs-lookup"><span data-stu-id="bf04e-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="bf04e-122">Ежегодные разноски 31 декабря.</span><span class="sxs-lookup"><span data-stu-id="bf04e-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="bf04e-123">Ежемесячно — разноска ежемесячной суммы выполняется в конце каждого календарного месяца.</span><span class="sxs-lookup"><span data-stu-id="bf04e-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="bf04e-124">Ежеквартально — выполняется разноска квартальной суммы в конце каждого календарного квартала (31 марта, 30 июня, 30 сентября и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="bf04e-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="bf04e-125">Полгода — разноска суммы за полгода один раз в конце каждого календарного полугодия (30 июня и 31 декабря).</span><span class="sxs-lookup"><span data-stu-id="bf04e-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="bf04e-126">Ежедневная — разноска суммы амортизации выполняется ежедневно, причем каждый день создается одна соответствующая проводка.</span><span class="sxs-lookup"><span data-stu-id="bf04e-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="bf04e-127">Например, если выбрать параметр "Ежегодно", годовая амортизация разносится только один раз, каждый год 31 декабря.</span><span class="sxs-lookup"><span data-stu-id="bf04e-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="bf04e-128">Если выбрать параметр "Ежемесячно", месячная амортизация разносится каждый месяц в сумме, равной 1/12 от суммы за год.</span><span class="sxs-lookup"><span data-stu-id="bf04e-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="bf04e-129">Финансовый</span><span class="sxs-lookup"><span data-stu-id="bf04e-129">Fiscal</span></span>

<span data-ttu-id="bf04e-130">При выборе параметра "Финансовый" в поле "Амортизация" применяется метод линейной амортизации.</span><span class="sxs-lookup"><span data-stu-id="bf04e-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="bf04e-131">Амортизация рассчитывается на основе финансового года, который настраивается на странице "Финансовые календари" для финансового календаря, выбранного на странице "Книга учета".</span><span class="sxs-lookup"><span data-stu-id="bf04e-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="bf04e-132">Например, для финансового года с 1 июля по 30 июня расчет амортизации начинается 1 июля.</span><span class="sxs-lookup"><span data-stu-id="bf04e-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="bf04e-133">Финансовый год может быть длиннее или короче 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="bf04e-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="bf04e-134">Амортизация корректируется для каждого финансового периода.</span><span class="sxs-lookup"><span data-stu-id="bf04e-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="bf04e-135">Продолжительность следующего финансового года определяется по финансовым периодам, настроенным при создании нового финансового года на странице "Финансовые календари".</span><span class="sxs-lookup"><span data-stu-id="bf04e-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="bf04e-136">Если выбрать "Финансовый" в поле "Частота периода", доступны следующие параметры частоты периода:</span><span class="sxs-lookup"><span data-stu-id="bf04e-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="bf04e-137">Ежегодно — разноска общей суммы амортизации, рассчитанной для финансового года как единая сумма в последний день финансового года.</span><span class="sxs-lookup"><span data-stu-id="bf04e-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="bf04e-138">Финансовый период разносит общую сумму амортизации, вычисленную для финансового года и начисленную по финансовым периодам, заданным для финансового календаря, выбранного на странице "Книга учета", или для финансового календаря, выбранного для основного средства.</span><span class="sxs-lookup"><span data-stu-id="bf04e-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="bf04e-139">Пример амортизации с уменьшаемым сальдо</span><span class="sxs-lookup"><span data-stu-id="bf04e-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="bf04e-140">Предположим, что цена ввода в эксплуатацию ОС составляет 11 000, ликвидационная стоимость — 1000, а коэффициент процента амортизации — 30.</span><span class="sxs-lookup"><span data-stu-id="bf04e-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="bf04e-141">Применяя метод "Уменьшаемое сальдо", 30 процентов базы амортизации (остаточная стоимость минус ликвидационная стоимость) рассчитывается в конце предыдущего периода амортизации.</span><span class="sxs-lookup"><span data-stu-id="bf04e-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="bf04e-142">В следующей таблице показана амортизация для первых трех лет.</span><span class="sxs-lookup"><span data-stu-id="bf04e-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="bf04e-143">Период</span><span class="sxs-lookup"><span data-stu-id="bf04e-143">Period</span></span> | <span data-ttu-id="bf04e-144">Расчет суммы амортизационных начислений за год</span><span class="sxs-lookup"><span data-stu-id="bf04e-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="bf04e-145">Остаточная стоимость на конец года</span><span class="sxs-lookup"><span data-stu-id="bf04e-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="bf04e-146">1-й год</span><span class="sxs-lookup"><span data-stu-id="bf04e-146">Year 1</span></span> | <span data-ttu-id="bf04e-147">(11 000 - 1 000) \* 30% = 3 000</span><span class="sxs-lookup"><span data-stu-id="bf04e-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="bf04e-148">(11 000 - 1 000) - 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="bf04e-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="bf04e-149">2-й год</span><span class="sxs-lookup"><span data-stu-id="bf04e-149">Year 2</span></span> | <span data-ttu-id="bf04e-150">(7 000 - 1 000) \* 30% = 1 800</span><span class="sxs-lookup"><span data-stu-id="bf04e-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="bf04e-151">(7 000 -1 800) = 5 200</span><span class="sxs-lookup"><span data-stu-id="bf04e-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="bf04e-152">3-й год</span><span class="sxs-lookup"><span data-stu-id="bf04e-152">Year 3</span></span> | <span data-ttu-id="bf04e-153">(5 200 - 1 000) \* 30% = 1 260</span><span class="sxs-lookup"><span data-stu-id="bf04e-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="bf04e-154">(5 200 - 1 260) = 3 940</span><span class="sxs-lookup"><span data-stu-id="bf04e-154">(5,200 - 1,260) = 3,940</span></span>               |


-





