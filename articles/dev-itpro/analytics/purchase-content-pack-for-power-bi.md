---
title: Содержимое Power BI "Анализ расходов на закупку"
description: В этой теме описывается, что входит в содержимое Power BI "Анализ расходов на закупку". В нем описывается порядок доступа к отчетам, входящим в содержимое, и предоставляется информация о модели данных и объектах, используемых для построения содержимого.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850027"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="77d11-104">Содержимое Power BI "Анализ расходов на закупку"</span><span class="sxs-lookup"><span data-stu-id="77d11-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77d11-105">В этой теме описывается, что входит в содержимое Power BI **Анализ расходов на закупку**.</span><span class="sxs-lookup"><span data-stu-id="77d11-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="77d11-106">В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые используются для построения пакета содержимого.</span><span class="sxs-lookup"><span data-stu-id="77d11-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="77d11-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="77d11-107">Overview</span></span>

<span data-ttu-id="77d11-108">Содержимое **Анализ расходов на закупку** Power BI было создано, чтобы помочь менеджерам по закупкам и менеджерам, которые отвечают за бюджеты, отслеживать расходы на закупки.</span><span class="sxs-lookup"><span data-stu-id="77d11-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="77d11-109">Менеджеры могут анализировать расходы на закупки следующими способами:</span><span class="sxs-lookup"><span data-stu-id="77d11-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="77d11-110">Покупки с начала года (по группам поставщиков и отдельным поставщикам, категориям закупок и отдельным продуктам и местонахождению поставщиков)</span><span class="sxs-lookup"><span data-stu-id="77d11-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="77d11-111">Изменение закупок по годам (по группам поставщиков и категориям закупок)</span><span class="sxs-lookup"><span data-stu-id="77d11-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="77d11-112">В содержимом используются данные проводок по закупкам для формирования как агрегированного представления показателей закупок по всей компании, так и разбивки затрат на закупки по поставщикам и продуктам.</span><span class="sxs-lookup"><span data-stu-id="77d11-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="77d11-113">В отчете выделены изменения расходов на покупку со временем.</span><span class="sxs-lookup"><span data-stu-id="77d11-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="77d11-114">Поэтому отчеты можно использовать для оповещения менеджеров о положительных и отрицательных тенденциях расходов по отдельным поставщикам и продуктам.</span><span class="sxs-lookup"><span data-stu-id="77d11-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="77d11-115">Кроме того, диаграммы иллюстрируют расходы на закупку по различным категориям закупок и группам поставщиков.</span><span class="sxs-lookup"><span data-stu-id="77d11-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="77d11-116">Категорийные и региональные менеджеры могут использовать эти диаграммы для выявления изменений в поведении расходов.</span><span class="sxs-lookup"><span data-stu-id="77d11-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="77d11-117">Доступ к содержимому Power BI</span><span class="sxs-lookup"><span data-stu-id="77d11-117">Accessing the Power BI content</span></span>
<span data-ttu-id="77d11-118">Содержимое Power BI **Анализ расходов на покупки** отображается на странице **Анализ покупок и расходов** (**Закупки и источники** \> **Запросы и отчеты** \> **Анализ производительности покупок** \> **Анализ покупок и расходов**).</span><span class="sxs-lookup"><span data-stu-id="77d11-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="77d11-119">Показатели, включенные в пакет содержимого Power BI</span><span class="sxs-lookup"><span data-stu-id="77d11-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="77d11-120">Пакет содержимого Power BI **Анализ расходов на закупку** включает отчет, состоящий из набора показателей.</span><span class="sxs-lookup"><span data-stu-id="77d11-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="77d11-121">Эти показатели отображаются в виде диаграмм, плиток и таблиц.</span><span class="sxs-lookup"><span data-stu-id="77d11-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="77d11-122">В следующем разделе приведен обзор визуализаций.</span><span class="sxs-lookup"><span data-stu-id="77d11-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="77d11-123">Страница отчета "Покупки по поставщикам"</span><span class="sxs-lookup"><span data-stu-id="77d11-123">Purchase by vendor report page</span></span>
<span data-ttu-id="77d11-124">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="77d11-124">**Charts**</span></span>
- <span data-ttu-id="77d11-125">10 лучших поставщиков по закупкам (линейчатая диаграмма с накоплением)</span><span class="sxs-lookup"><span data-stu-id="77d11-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="77d11-126">Итоговая сумма закупок по группам поставщиков/странам/наименованиям (круговая диаграмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="77d11-127">Покупки по группам поставщиков/странам/наименованиям (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="77d11-128">Средние покупки по группам поставщиков/странам/наименованиям (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="77d11-129">**Плитки**</span><span class="sxs-lookup"><span data-stu-id="77d11-129">**Tiles**</span></span>
- <span data-ttu-id="77d11-130">Всего по Закупкам</span><span class="sxs-lookup"><span data-stu-id="77d11-130">Total purchase</span></span>
- <span data-ttu-id="77d11-131">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="77d11-131">YOY purchase growth</span></span>
- <span data-ttu-id="77d11-132">Общее число поставщиков</span><span class="sxs-lookup"><span data-stu-id="77d11-132">Total # vendors</span></span>
- <span data-ttu-id="77d11-133">Общее число активных поставщиков</span><span class="sxs-lookup"><span data-stu-id="77d11-133">Total # of active vendors</span></span>

<span data-ttu-id="77d11-134">**Пример**</span><span class="sxs-lookup"><span data-stu-id="77d11-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="77d11-135">Страница отчета "Покупки по продуктам"</span><span class="sxs-lookup"><span data-stu-id="77d11-135">Purchase by product report page</span></span>

<span data-ttu-id="77d11-136">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="77d11-136">**Charts**</span></span>
- <span data-ttu-id="77d11-137">Покупка по категориям закупаемой продукции/названиям продуктов (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="77d11-138">Общие покупки по категориям закупаемой продукции/названиям продуктов (круговая диаграмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="77d11-139">10 продуктов с наибольшими закупкам (линейчатая диаграмма с накоплением)</span><span class="sxs-lookup"><span data-stu-id="77d11-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="77d11-140">**Плитки**</span><span class="sxs-lookup"><span data-stu-id="77d11-140">**Tiles**</span></span>
- <span data-ttu-id="77d11-141">Общее число продуктов</span><span class="sxs-lookup"><span data-stu-id="77d11-141">Total # of products</span></span></li>
- <span data-ttu-id="77d11-142">Общий процент активных продуктов от общего числа продуктов</span><span class="sxs-lookup"><span data-stu-id="77d11-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="77d11-143">Число продуктов, на которые приходится 80% покупок</span><span class="sxs-lookup"><span data-stu-id="77d11-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="77d11-144">**Пример**</span><span class="sxs-lookup"><span data-stu-id="77d11-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="77d11-145">Страница отчета "Покупки по периодам"</span><span class="sxs-lookup"><span data-stu-id="77d11-145">Purchase by period report page</span></span>
<span data-ttu-id="77d11-146">На этой странице отображаются покупки за этот год и прошлый год, а также рост по категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="77d11-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="77d11-147">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="77d11-147">**Charts**</span></span> 
- <span data-ttu-id="77d11-148">Покупки по месяцам/дням (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="77d11-149">Накопительное отклонение покупок по годам (каскадная диаграмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="77d11-150">Рост общей суммы покупки по годам (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="77d11-151">Отчет о закупаемой продукции (матрица)</span><span class="sxs-lookup"><span data-stu-id="77d11-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="77d11-152">**Плитки**</span><span class="sxs-lookup"><span data-stu-id="77d11-152">**Tiles**</span></span>
- <span data-ttu-id="77d11-153">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="77d11-153">YOY purchase growth</span></span>
- <span data-ttu-id="77d11-154">Рост покупок по годам, %</span><span class="sxs-lookup"><span data-stu-id="77d11-154">YOY purchase growth %</span></span>

<span data-ttu-id="77d11-155">**Пример**</span><span class="sxs-lookup"><span data-stu-id="77d11-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="77d11-156">Страница отчета "Покупки по местонахождению поставщиков"</span><span class="sxs-lookup"><span data-stu-id="77d11-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="77d11-157">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="77d11-157">**Charts**</span></span>
- <span data-ttu-id="77d11-158">Покупки по городам</span><span class="sxs-lookup"><span data-stu-id="77d11-158">Purchase by city</span></span>
- <span data-ttu-id="77d11-159">Рост покупок по годам, %</span><span class="sxs-lookup"><span data-stu-id="77d11-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="77d11-160">Покупки по странам</span><span class="sxs-lookup"><span data-stu-id="77d11-160">Purchase by country</span></span>

<span data-ttu-id="77d11-161">**Пример**</span><span class="sxs-lookup"><span data-stu-id="77d11-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="77d11-162">Страница отчета "Анализ расходов на закупку по времени"</span><span class="sxs-lookup"><span data-stu-id="77d11-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="77d11-163">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="77d11-163">**Charts**</span></span> 
- <span data-ttu-id="77d11-164">Покупки за текущий год по месяцам/дням (график)</span><span class="sxs-lookup"><span data-stu-id="77d11-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="77d11-165">Покупки за текущий год и последний год (график и гистограмма)</span><span class="sxs-lookup"><span data-stu-id="77d11-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="77d11-166">**Пример**</span><span class="sxs-lookup"><span data-stu-id="77d11-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="77d11-167">Страница отчета "Анализ расходов на закупку по поставщикам"</span><span class="sxs-lookup"><span data-stu-id="77d11-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="77d11-168">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="77d11-168">**Charts**</span></span> 
- <span data-ttu-id="77d11-169">Первые 10 поставщиков, покупки в % от покупок (воронка)</span><span class="sxs-lookup"><span data-stu-id="77d11-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="77d11-170">Первые 10 поставщиков с увеличившимися расходами по годам</span><span class="sxs-lookup"><span data-stu-id="77d11-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="77d11-171">Первые 10 поставщиков с уменьшившимися расходами по годам</span><span class="sxs-lookup"><span data-stu-id="77d11-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="77d11-172">**Пример** 
</span><span class="sxs-lookup"><span data-stu-id="77d11-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="77d11-173">Модель данных и объекты</span><span class="sxs-lookup"><span data-stu-id="77d11-173">Data model and entities</span></span>
<span data-ttu-id="77d11-174">Следующие данные используются для заполнения страниц отчета в содержимом Power BI **Анализ расходов на закупку**.</span><span class="sxs-lookup"><span data-stu-id="77d11-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="77d11-175">Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="77d11-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="77d11-176">Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики.</span><span class="sxs-lookup"><span data-stu-id="77d11-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="77d11-177">Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="77d11-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="77d11-178">Сводные измерения в этом содержимом являются подмножеством сводных измерений, которые были доступны в кубе закупок в Microsoft Dynamics AX 2012 и Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="77d11-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="77d11-179">Для временного размещения агрегированных измерений куба в хранилище объектов необходимо сделать их развертываемыми.</span><span class="sxs-lookup"><span data-stu-id="77d11-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="77d11-180">Дополнительные сведения см. в процедуре временного размещения агрегированных измерений в хранилище объектов в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="77d11-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="77d11-181">Следующие ключевые агрегированные измерения доступны непосредственно из объекта "Строки накладной" и используются в качестве основы для содержимого.</span><span class="sxs-lookup"><span data-stu-id="77d11-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="77d11-182">Объект</span><span class="sxs-lookup"><span data-stu-id="77d11-182">Entity</span></span>        | <span data-ttu-id="77d11-183">Ключевые сводные измерения</span><span class="sxs-lookup"><span data-stu-id="77d11-183">Key aggregate measurements</span></span> | <span data-ttu-id="77d11-184">Иcточник данных</span><span class="sxs-lookup"><span data-stu-id="77d11-184">Data source</span></span>                                 | <span data-ttu-id="77d11-185">Поле</span><span class="sxs-lookup"><span data-stu-id="77d11-185">Field</span></span>              | <span data-ttu-id="77d11-186">описание</span><span class="sxs-lookup"><span data-stu-id="77d11-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="77d11-187">Строки накладной</span><span class="sxs-lookup"><span data-stu-id="77d11-187">Invoice lines</span></span> | <span data-ttu-id="77d11-188">Покупка</span><span class="sxs-lookup"><span data-stu-id="77d11-188">Purchase</span></span>                   | <span data-ttu-id="77d11-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="77d11-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="77d11-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="77d11-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="77d11-191">Сумма в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="77d11-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="77d11-192">В следующей таблице приведены ключевые измерения, которые рассчитываются из объекта "Строки накладной".</span><span class="sxs-lookup"><span data-stu-id="77d11-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="77d11-193">Мера</span><span class="sxs-lookup"><span data-stu-id="77d11-193">Measure</span></span>               | <span data-ttu-id="77d11-194">Расчет</span><span class="sxs-lookup"><span data-stu-id="77d11-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d11-195">Покупки за текущий год</span><span class="sxs-lookup"><span data-stu-id="77d11-195">Purchase current year</span></span> | <span data-ttu-id="77d11-196">Покупки за текущий год = SUM('Строки накладной'\[Покупка\])</span><span class="sxs-lookup"><span data-stu-id="77d11-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="77d11-197">Покупки за прошлый год</span><span class="sxs-lookup"><span data-stu-id="77d11-197">Purchase last year</span></span>    | <span data-ttu-id="77d11-198">Покупки за прошлый год = CALCULATE(SUM('Строки накладной'\[Покупка\]), SAMEPERIODLASTYEAR(Даты\[Дата\]))</span><span class="sxs-lookup"><span data-stu-id="77d11-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="77d11-199">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="77d11-199">YOY purchase growth</span></span>   | <span data-ttu-id="77d11-200">Рост покупок по годам = \[Покупки за текущий год\] – \[Покупки за прошлый год\]</span><span class="sxs-lookup"><span data-stu-id="77d11-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="77d11-201">Следующие ключевые измерения в содержимом используются в качестве фильтров для разделения агрегированных измерений, чтобы можно было достичь большей детализации и получить более глубокое аналитическое представление.</span><span class="sxs-lookup"><span data-stu-id="77d11-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="77d11-202">Объект</span><span class="sxs-lookup"><span data-stu-id="77d11-202">Entity</span></span>                 | <span data-ttu-id="77d11-203">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="77d11-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="77d11-204">Поставщики</span><span class="sxs-lookup"><span data-stu-id="77d11-204">Vendors</span></span>                | <span data-ttu-id="77d11-205">Группы поставщиков, Страна или регионы поставщика, Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="77d11-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="77d11-206">Товары</span><span class="sxs-lookup"><span data-stu-id="77d11-206">Products</span></span>               | <span data-ttu-id="77d11-207">Номер продукта, Название продукта, Название групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="77d11-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="77d11-208">Категории закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="77d11-208">Procurement categories</span></span> | <span data-ttu-id="77d11-209">Категория закупаемой продукции, Названия категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="77d11-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="77d11-210">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="77d11-210">Legal entities</span></span>         | <span data-ttu-id="77d11-211">Имя информации о компании</span><span class="sxs-lookup"><span data-stu-id="77d11-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="77d11-212">Даты</span><span class="sxs-lookup"><span data-stu-id="77d11-212">Dates</span></span>                  | <span data-ttu-id="77d11-213">Даты, Смещение по году</span><span class="sxs-lookup"><span data-stu-id="77d11-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="77d11-214">По умолчанию содержимое отображает дату для текущего календарного года.</span><span class="sxs-lookup"><span data-stu-id="77d11-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="77d11-215">Однако можно изменить фильтр дат в разделе фильтров отчета.</span><span class="sxs-lookup"><span data-stu-id="77d11-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="77d11-216">Можно также изменить фильтр компаний.</span><span class="sxs-lookup"><span data-stu-id="77d11-216">You can also change the company filter.</span></span>
