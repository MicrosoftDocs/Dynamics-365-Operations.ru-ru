---
title: Содержимое Power BI "Анализ расходов на закупку"
description: В этой теме описывается, что входит в содержимое Power BI "Анализ расходов на закупку".
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
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5914abaafab509e278d7a85441928feddb0b5164
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093450"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="0985d-103">Содержимое Power BI "Анализ расходов на закупку"</span><span class="sxs-lookup"><span data-stu-id="0985d-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0985d-104">В этой теме описывается, что входит в содержимое Power BI **Анализ расходов на закупку**.</span><span class="sxs-lookup"><span data-stu-id="0985d-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="0985d-105">В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые используются для построения пакета содержимого.</span><span class="sxs-lookup"><span data-stu-id="0985d-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="0985d-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="0985d-106">Overview</span></span>

<span data-ttu-id="0985d-107">Содержимое **Анализ расходов на закупку** Power BI было создано, чтобы помочь менеджерам по закупкам и менеджерам, которые отвечают за бюджеты, отслеживать расходы на закупки.</span><span class="sxs-lookup"><span data-stu-id="0985d-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="0985d-108">Менеджеры могут анализировать расходы на закупки следующими способами:</span><span class="sxs-lookup"><span data-stu-id="0985d-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="0985d-109">Покупки с начала года (по группам поставщиков и отдельным поставщикам, категориям закупок и отдельным продуктам и местонахождению поставщиков)</span><span class="sxs-lookup"><span data-stu-id="0985d-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="0985d-110">Изменение закупок по годам (по группам поставщиков и категориям закупок)</span><span class="sxs-lookup"><span data-stu-id="0985d-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="0985d-111">В содержимом используются данные проводок по закупкам для формирования как агрегированного представления показателей закупок по всей компании, так и разбивки затрат на закупки по поставщикам и продуктам.</span><span class="sxs-lookup"><span data-stu-id="0985d-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="0985d-112">В отчете выделены изменения расходов на покупку со временем.</span><span class="sxs-lookup"><span data-stu-id="0985d-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="0985d-113">Поэтому отчеты можно использовать для оповещения менеджеров о положительных и отрицательных тенденциях расходов по отдельным поставщикам и продуктам.</span><span class="sxs-lookup"><span data-stu-id="0985d-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="0985d-114">Кроме того, диаграммы иллюстрируют расходы на закупку по различным категориям закупок и группам поставщиков.</span><span class="sxs-lookup"><span data-stu-id="0985d-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="0985d-115">Категорийные и региональные менеджеры могут использовать эти диаграммы для выявления изменений в поведении расходов.</span><span class="sxs-lookup"><span data-stu-id="0985d-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="0985d-116">Доступ к содержимому Power BI</span><span class="sxs-lookup"><span data-stu-id="0985d-116">Accessing the Power BI content</span></span>
<span data-ttu-id="0985d-117">Содержимое Power BI **Анализ расходов на покупки** отображается на странице **Анализ покупок и расходов** (**Закупки и источники** \> **Запросы и отчеты** \> **Анализ производительности покупок** \> **Анализ покупок и расходов**).</span><span class="sxs-lookup"><span data-stu-id="0985d-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="0985d-118">Показатели, включенные в пакет содержимого Power BI</span><span class="sxs-lookup"><span data-stu-id="0985d-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="0985d-119">Пакет содержимого Power BI **Анализ расходов на закупку** включает отчет, состоящий из набора показателей.</span><span class="sxs-lookup"><span data-stu-id="0985d-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="0985d-120">Эти показатели отображаются в виде диаграмм, плиток и таблиц.</span><span class="sxs-lookup"><span data-stu-id="0985d-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="0985d-121">В следующем разделе приведен обзор визуализаций.</span><span class="sxs-lookup"><span data-stu-id="0985d-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="0985d-122">Страница отчета "Покупки по поставщикам"</span><span class="sxs-lookup"><span data-stu-id="0985d-122">Purchase by vendor report page</span></span>
<span data-ttu-id="0985d-123">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="0985d-123">**Charts**</span></span>
- <span data-ttu-id="0985d-124">10 лучших поставщиков по закупкам (линейчатая диаграмма с накоплением)</span><span class="sxs-lookup"><span data-stu-id="0985d-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="0985d-125">Итоговая сумма закупок по группам поставщиков/странам/наименованиям (круговая диаграмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="0985d-126">Покупки по группам поставщиков/странам/наименованиям (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="0985d-127">Средние покупки по группам поставщиков/странам/наименованиям (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="0985d-128">**Плитки**</span><span class="sxs-lookup"><span data-stu-id="0985d-128">**Tiles**</span></span>
- <span data-ttu-id="0985d-129">Всего по Закупкам</span><span class="sxs-lookup"><span data-stu-id="0985d-129">Total purchase</span></span>
- <span data-ttu-id="0985d-130">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="0985d-130">YOY purchase growth</span></span>
- <span data-ttu-id="0985d-131">Общее число поставщиков</span><span class="sxs-lookup"><span data-stu-id="0985d-131">Total # vendors</span></span>
- <span data-ttu-id="0985d-132">Общее число активных поставщиков</span><span class="sxs-lookup"><span data-stu-id="0985d-132">Total # of active vendors</span></span>

<span data-ttu-id="0985d-133">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0985d-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="0985d-134">Страница отчета "Покупки по продуктам"</span><span class="sxs-lookup"><span data-stu-id="0985d-134">Purchase by product report page</span></span>

<span data-ttu-id="0985d-135">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="0985d-135">**Charts**</span></span>
- <span data-ttu-id="0985d-136">Покупка по категориям закупаемой продукции/названиям продуктов (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="0985d-137">Общие покупки по категориям закупаемой продукции/названиям продуктов (круговая диаграмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="0985d-138">10 продуктов с наибольшими закупкам (линейчатая диаграмма с накоплением)</span><span class="sxs-lookup"><span data-stu-id="0985d-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="0985d-139">**Плитки**</span><span class="sxs-lookup"><span data-stu-id="0985d-139">**Tiles**</span></span>
- <span data-ttu-id="0985d-140">Общее число продуктов</span><span class="sxs-lookup"><span data-stu-id="0985d-140">Total # of products</span></span></li>
- <span data-ttu-id="0985d-141">Общий процент активных продуктов от общего числа продуктов</span><span class="sxs-lookup"><span data-stu-id="0985d-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="0985d-142">Число продуктов, на которые приходится 80% покупок</span><span class="sxs-lookup"><span data-stu-id="0985d-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="0985d-143">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0985d-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="0985d-144">Страница отчета "Покупки по периодам"</span><span class="sxs-lookup"><span data-stu-id="0985d-144">Purchase by period report page</span></span>
<span data-ttu-id="0985d-145">На этой странице отображаются покупки за этот год и прошлый год, а также рост по категориям закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="0985d-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="0985d-146">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="0985d-146">**Charts**</span></span> 
- <span data-ttu-id="0985d-147">Покупки по месяцам/дням (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="0985d-148">Накопительное отклонение покупок по годам (каскадная диаграмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="0985d-149">Рост общей суммы покупки по годам (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="0985d-150">Отчет о закупаемой продукции (матрица)</span><span class="sxs-lookup"><span data-stu-id="0985d-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="0985d-151">**Плитки**</span><span class="sxs-lookup"><span data-stu-id="0985d-151">**Tiles**</span></span>
- <span data-ttu-id="0985d-152">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="0985d-152">YOY purchase growth</span></span>
- <span data-ttu-id="0985d-153">Рост покупок по годам, %</span><span class="sxs-lookup"><span data-stu-id="0985d-153">YOY purchase growth %</span></span>

<span data-ttu-id="0985d-154">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0985d-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="0985d-155">Страница отчета "Покупки по местонахождению поставщиков"</span><span class="sxs-lookup"><span data-stu-id="0985d-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="0985d-156">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="0985d-156">**Charts**</span></span>
- <span data-ttu-id="0985d-157">Покупки по городам</span><span class="sxs-lookup"><span data-stu-id="0985d-157">Purchase by city</span></span>
- <span data-ttu-id="0985d-158">Рост покупок по годам, %</span><span class="sxs-lookup"><span data-stu-id="0985d-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="0985d-159">Покупки по странам</span><span class="sxs-lookup"><span data-stu-id="0985d-159">Purchase by country</span></span>

<span data-ttu-id="0985d-160">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0985d-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="0985d-161">Страница отчета "Анализ расходов на закупку по времени"</span><span class="sxs-lookup"><span data-stu-id="0985d-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="0985d-162">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="0985d-162">**Charts**</span></span> 
- <span data-ttu-id="0985d-163">Покупки за текущий год по месяцам/дням (график)</span><span class="sxs-lookup"><span data-stu-id="0985d-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="0985d-164">Покупки за текущий год и последний год (график и гистограмма)</span><span class="sxs-lookup"><span data-stu-id="0985d-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="0985d-165">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0985d-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="0985d-166">Страница отчета "Анализ расходов на закупку по поставщикам"</span><span class="sxs-lookup"><span data-stu-id="0985d-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="0985d-167">**Диаграммы**</span><span class="sxs-lookup"><span data-stu-id="0985d-167">**Charts**</span></span> 
- <span data-ttu-id="0985d-168">Первые 10 поставщиков, покупки в % от покупок (воронка)</span><span class="sxs-lookup"><span data-stu-id="0985d-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="0985d-169">Первые 10 поставщиков с увеличившимися расходами по годам</span><span class="sxs-lookup"><span data-stu-id="0985d-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="0985d-170">Первые 10 поставщиков с уменьшившимися расходами по годам</span><span class="sxs-lookup"><span data-stu-id="0985d-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="0985d-171">**Пример** 
</span><span class="sxs-lookup"><span data-stu-id="0985d-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="0985d-172">Модель данных и объекты</span><span class="sxs-lookup"><span data-stu-id="0985d-172">Data model and entities</span></span>
<span data-ttu-id="0985d-173">Следующие данные используются для заполнения страниц отчета в содержимом Power BI **Анализ расходов на закупку**.</span><span class="sxs-lookup"><span data-stu-id="0985d-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="0985d-174">Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="0985d-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="0985d-175">Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики.</span><span class="sxs-lookup"><span data-stu-id="0985d-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="0985d-176">Дополнительные сведения см. в разделе [Интеграция Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="0985d-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="0985d-177">Сводные измерения в этом содержимом являются подмножеством сводных измерений, которые были доступны в кубе закупок в Microsoft Dynamics AX 2012 и Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="0985d-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="0985d-178">Для временного размещения агрегированных измерений куба в хранилище объектов необходимо сделать их развертываемыми.</span><span class="sxs-lookup"><span data-stu-id="0985d-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="0985d-179">Дополнительные сведения см. в процедуре временного размещения агрегированных измерений в хранилище объектов в разделе [Интеграция Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="0985d-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="0985d-180">Следующие ключевые агрегированные измерения доступны непосредственно из объекта "Строки накладной" и используются в качестве основы для содержимого.</span><span class="sxs-lookup"><span data-stu-id="0985d-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="0985d-181">Объект</span><span class="sxs-lookup"><span data-stu-id="0985d-181">Entity</span></span>        | <span data-ttu-id="0985d-182">Ключевые сводные измерения</span><span class="sxs-lookup"><span data-stu-id="0985d-182">Key aggregate measurements</span></span> | <span data-ttu-id="0985d-183">Иcточник данных</span><span class="sxs-lookup"><span data-stu-id="0985d-183">Data source</span></span>                                 | <span data-ttu-id="0985d-184">Поле</span><span class="sxs-lookup"><span data-stu-id="0985d-184">Field</span></span>              | <span data-ttu-id="0985d-185">описание</span><span class="sxs-lookup"><span data-stu-id="0985d-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="0985d-186">Строки накладной</span><span class="sxs-lookup"><span data-stu-id="0985d-186">Invoice lines</span></span> | <span data-ttu-id="0985d-187">Покупка</span><span class="sxs-lookup"><span data-stu-id="0985d-187">Purchase</span></span>                   | <span data-ttu-id="0985d-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="0985d-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="0985d-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="0985d-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="0985d-190">Сумма в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="0985d-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="0985d-191">В следующей таблице приведены ключевые измерения, которые рассчитываются из объекта "Строки накладной".</span><span class="sxs-lookup"><span data-stu-id="0985d-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="0985d-192">Мера</span><span class="sxs-lookup"><span data-stu-id="0985d-192">Measure</span></span>               | <span data-ttu-id="0985d-193">Расчет</span><span class="sxs-lookup"><span data-stu-id="0985d-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0985d-194">Покупки за текущий год</span><span class="sxs-lookup"><span data-stu-id="0985d-194">Purchase current year</span></span> | <span data-ttu-id="0985d-195">Покупки за текущий год = SUM('Строки накладной'\[Покупка\])</span><span class="sxs-lookup"><span data-stu-id="0985d-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="0985d-196">Покупки за прошлый год</span><span class="sxs-lookup"><span data-stu-id="0985d-196">Purchase last year</span></span>    | <span data-ttu-id="0985d-197">Покупки за прошлый год = CALCULATE(SUM('Строки накладной'\[Покупка\]), SAMEPERIODLASTYEAR(Даты\[Дата\]))</span><span class="sxs-lookup"><span data-stu-id="0985d-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="0985d-198">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="0985d-198">YOY purchase growth</span></span>   | <span data-ttu-id="0985d-199">Рост покупок по годам = \[Покупки за текущий год\] – \[Покупки за прошлый год\]</span><span class="sxs-lookup"><span data-stu-id="0985d-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="0985d-200">Следующие ключевые измерения в содержимом используются в качестве фильтров для разделения агрегированных измерений, чтобы можно было достичь большей детализации и получить более глубокое аналитическое представление.</span><span class="sxs-lookup"><span data-stu-id="0985d-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="0985d-201">Объект</span><span class="sxs-lookup"><span data-stu-id="0985d-201">Entity</span></span>                 | <span data-ttu-id="0985d-202">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="0985d-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="0985d-203">Поставщики</span><span class="sxs-lookup"><span data-stu-id="0985d-203">Vendors</span></span>                | <span data-ttu-id="0985d-204">Группы поставщиков, Страна или регионы поставщика, Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="0985d-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="0985d-205">Товары</span><span class="sxs-lookup"><span data-stu-id="0985d-205">Products</span></span>               | <span data-ttu-id="0985d-206">Номер продукта, Название продукта, Название групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="0985d-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="0985d-207">Категории закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="0985d-207">Procurement categories</span></span> | <span data-ttu-id="0985d-208">Категория закупаемой продукции, Названия категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="0985d-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="0985d-209">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="0985d-209">Legal entities</span></span>         | <span data-ttu-id="0985d-210">Имя информации о компании</span><span class="sxs-lookup"><span data-stu-id="0985d-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="0985d-211">Даты</span><span class="sxs-lookup"><span data-stu-id="0985d-211">Dates</span></span>                  | <span data-ttu-id="0985d-212">Даты, Смещение по году</span><span class="sxs-lookup"><span data-stu-id="0985d-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="0985d-213">По умолчанию содержимое отображает дату для текущего календарного года.</span><span class="sxs-lookup"><span data-stu-id="0985d-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="0985d-214">Однако можно изменить фильтр дат в разделе фильтров отчета.</span><span class="sxs-lookup"><span data-stu-id="0985d-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="0985d-215">Можно также изменить фильтр компаний.</span><span class="sxs-lookup"><span data-stu-id="0985d-215">You can also change the company filter.</span></span>
