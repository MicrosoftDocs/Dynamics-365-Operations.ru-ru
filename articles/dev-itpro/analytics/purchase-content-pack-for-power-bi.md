---
title: "Содержимое Power BI \"Анализ расходов на закупку\""
description: "В этой теме описывается, что входит в содержимое Power BI \"Анализ расходов на закупку\". В нем описывается порядок доступа к отчетам, входящим в содержимое, и предоставляется информация о модели данных и объектах, используемых для построения содержимого."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3e42746329b1194c0ce0e2fb5c476742259a5b43
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="18417-104">Содержимое Power BI "Анализ расходов на закупку"</span><span class="sxs-lookup"><span data-stu-id="18417-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="18417-105">В этой теме описывается, что входит в содержимое Microsoft Power BI **Анализ расходов на закупку**.</span><span class="sxs-lookup"><span data-stu-id="18417-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="18417-106">В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.</span><span class="sxs-lookup"><span data-stu-id="18417-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="18417-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="18417-107">Overview</span></span>

<span data-ttu-id="18417-108">Содержимое **Анализ расходов на закупку** Power BI было создано, чтобы помочь менеджерам по закупкам и менеджерам, которые отвечают за бюджеты, контролировать расходы на закупки.</span><span class="sxs-lookup"><span data-stu-id="18417-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="18417-109">Менеджеры могут анализировать расходы на закупки следующими способами:</span><span class="sxs-lookup"><span data-stu-id="18417-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="18417-110">Покупки с начала года (по группам поставщиков и отдельным поставщикам, категориям закупок и отдельным продуктам и местонахождению поставщиков)</span><span class="sxs-lookup"><span data-stu-id="18417-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="18417-111">Изменение закупок по годам (по группам поставщиков и категориям закупок)</span><span class="sxs-lookup"><span data-stu-id="18417-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="18417-112">В содержимом используются данные проводок по закупкам для формирования как агрегированного представления показателей закупок по всей компании, так и разбивки затрат на закупки по поставщикам и продуктам.</span><span class="sxs-lookup"><span data-stu-id="18417-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="18417-113">В отчете выделены изменения расходов на покупку со временем.</span><span class="sxs-lookup"><span data-stu-id="18417-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="18417-114">Поэтому отчеты можно использовать для оповещения менеджеров о положительных и отрицательных тенденциях расходов по отдельным поставщикам и продуктам.</span><span class="sxs-lookup"><span data-stu-id="18417-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="18417-115">Кроме того, диаграммы иллюстрируют расходы на закупку по различным категориям закупок и группам поставщиков.</span><span class="sxs-lookup"><span data-stu-id="18417-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="18417-116">Категорийные и региональные менеджеры могут использовать эти диаграммы для выявления изменений в поведении расходов.</span><span class="sxs-lookup"><span data-stu-id="18417-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="18417-117">Доступ к содержимому Power BI</span><span class="sxs-lookup"><span data-stu-id="18417-117">Accessing the Power BI content</span></span>
<span data-ttu-id="18417-118">При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) содержимое Power BI **Анализ расходов на закупку** отображается на странице **Анализ покупок и расходов** (**Закупки и источники** > **Запросы и отчеты** > **Анализ производительности покупок** > **Анализ покупок и расходов**).</span><span class="sxs-lookup"><span data-stu-id="18417-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="18417-119">Показатели, которые включены в содержимое Power BI</span><span class="sxs-lookup"><span data-stu-id="18417-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="18417-120">Содержимое Power BI **Анализ расходов на закупку** включает отчет, состоящий из набора показателей.</span><span class="sxs-lookup"><span data-stu-id="18417-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="18417-121">Эти показатели отображаются в виде диаграмм, плиток и таблиц.</span><span class="sxs-lookup"><span data-stu-id="18417-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="18417-122">В следующей таблице приведен обзор визуализаций.</span><span class="sxs-lookup"><span data-stu-id="18417-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18417-123">Страница отчета</span><span class="sxs-lookup"><span data-stu-id="18417-123">Report page</span></span></th>
<th><span data-ttu-id="18417-124">Диаграммы</span><span class="sxs-lookup"><span data-stu-id="18417-124">Charts</span></span></th>
<th><span data-ttu-id="18417-125">Плитки</span><span class="sxs-lookup"><span data-stu-id="18417-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18417-126">Покупки по поставщикам</span><span class="sxs-lookup"><span data-stu-id="18417-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="18417-127">10 лучших поставщиков по закупкам (линейчатая диаграмма с накоплением)</span><span class="sxs-lookup"><span data-stu-id="18417-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="18417-128">Итоговая сумма закупок по группам поставщиков/странам/наименованиям (круговая диаграмма)</span><span class="sxs-lookup"><span data-stu-id="18417-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="18417-129">Покупки по группам поставщиков/странам/наименованиям (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="18417-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="18417-130">Средние покупки по группам поставщиков/странам/наименованиям (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="18417-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="18417-131">Всего по Закупкам</span><span class="sxs-lookup"><span data-stu-id="18417-131">Total purchase</span></span></li>
<li><span data-ttu-id="18417-132">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="18417-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="18417-133">Общее число поставщиков</span><span class="sxs-lookup"><span data-stu-id="18417-133">Total # vendors</span></span></li>
<li><span data-ttu-id="18417-134">Общее число активных поставщиков</span><span class="sxs-lookup"><span data-stu-id="18417-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18417-135">Покупки по продуктам</span><span class="sxs-lookup"><span data-stu-id="18417-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="18417-136">Покупка по категориям закупаемой продукции/названиям продуктов (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="18417-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="18417-137">Общие покупки по категориям закупаемой продукции/названиям продуктов (круговая диаграмма)</span><span class="sxs-lookup"><span data-stu-id="18417-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="18417-138">10 продуктов с наибольшими закупкам (линейчатая диаграмма с накоплением)</span><span class="sxs-lookup"><span data-stu-id="18417-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="18417-139">Общее число продуктов</span><span class="sxs-lookup"><span data-stu-id="18417-139">Total # of products</span></span></li>
<li><span data-ttu-id="18417-140">Общий процент активных продуктов от общего числа продуктов</span><span class="sxs-lookup"><span data-stu-id="18417-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="18417-141">Число продуктов, на которые приходится 80% покупок</span><span class="sxs-lookup"><span data-stu-id="18417-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18417-142">Покупки по периодам*</span><span class="sxs-lookup"><span data-stu-id="18417-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="18417-143">Покупки по месяцам/дням (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="18417-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="18417-144">Накопительное отклонение покупок по годам (каскадная диаграмма)</span><span class="sxs-lookup"><span data-stu-id="18417-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="18417-145">Рост общей суммы покупки по годам (гистограмма)</span><span class="sxs-lookup"><span data-stu-id="18417-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="18417-146">Отчет о закупаемой продукции (матрица)</span><span class="sxs-lookup"><span data-stu-id="18417-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="18417-147">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="18417-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="18417-148">Рост покупок по годам, %</span><span class="sxs-lookup"><span data-stu-id="18417-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18417-149">Покупки по местонахождению поставщиков</span><span class="sxs-lookup"><span data-stu-id="18417-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="18417-150">Покупки по городам</span><span class="sxs-lookup"><span data-stu-id="18417-150">Purchase by city</span></span></li>
<li><span data-ttu-id="18417-151">Рост покупок по годам, %</span><span class="sxs-lookup"><span data-stu-id="18417-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="18417-152">Покупки по странам</span><span class="sxs-lookup"><span data-stu-id="18417-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18417-153">Анализ расходов на закупку по времени</span><span class="sxs-lookup"><span data-stu-id="18417-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="18417-154">Покупки за текущий год по месяцам/дням (график)</span><span class="sxs-lookup"><span data-stu-id="18417-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="18417-155">Покупки за текущий год и последний год (график и гистограмма)</span><span class="sxs-lookup"><span data-stu-id="18417-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18417-156">Анализ расходов на закупку по поставщикам</span><span class="sxs-lookup"><span data-stu-id="18417-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="18417-157">Первые 10 поставщиков, покупки в % от покупок (воронка)</span><span class="sxs-lookup"><span data-stu-id="18417-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="18417-158">Первые 10 поставщиков с увеличившимися расходами по годам</span><span class="sxs-lookup"><span data-stu-id="18417-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="18417-159">Первые 10 поставщиков с уменьшившимися расходами по годам</span><span class="sxs-lookup"><span data-stu-id="18417-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="18417-160">\* Покупки за этот год и прошлый год, а также рост по категориям закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="18417-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="18417-161">Расширение содержимого Power BI</span><span class="sxs-lookup"><span data-stu-id="18417-161">Extending the Power BI content</span></span>
<span data-ttu-id="18417-162">С помощью пакетов содержимого, доступных в Microsoft Dynamics Lifecycle Services (LCS), можно повысить эффективность аналитики для тех, кто не использует Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="18417-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="18417-163">Эти пакеты содержимого можно изменить, чтобы они включали других отчеты или визуальные элементы, и затем опубликовать пакеты содержимого для владельца Power BI.com для анализа.</span><span class="sxs-lookup"><span data-stu-id="18417-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="18417-164">Содержимое Power BI **Анализ расходов на закупку** можно найти в библиотеке общих ресурсов в LCS.</span><span class="sxs-lookup"><span data-stu-id="18417-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="18417-165">Дополнительные сведения о том, как загрузить содержимое и реализовать его в вашей организации, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="18417-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="18417-166">Чтобы просмотреть демонстрацию, которая показывает, как реализовать содержимое Power BI, см. [Содержимое Power BI от Майкрософт и ваших партнеров в службах Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office mix).</span><span class="sxs-lookup"><span data-stu-id="18417-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="18417-167">Следите за тем, чтобы загружаемое Power BI **Анализ расходов на закупку** соответствовало версии Dynamics 365, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="18417-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="18417-168">При использовании Microsoft Dynamics 365 for Finance and Operations версии 1611 необходимым условием для использования этого содержимого Power BI является реализация KB 4011327.</span><span class="sxs-lookup"><span data-stu-id="18417-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="18417-169">После входа в LCS этот KB можно найти здесь: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="18417-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="18417-170">Модель данных и объекты</span><span class="sxs-lookup"><span data-stu-id="18417-170">Data model and entities</span></span>
<span data-ttu-id="18417-171">Следующие данные используются для заполнения страниц отчета в содержимом Power BI **Анализ расходов на закупку**.</span><span class="sxs-lookup"><span data-stu-id="18417-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="18417-172">Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="18417-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="18417-173">Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики.</span><span class="sxs-lookup"><span data-stu-id="18417-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="18417-174">Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="18417-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="18417-175">Агрегированные измерения в этом содержимом являются подмножеством агрегированных измерений, которые были доступны в кубе Purchase в Microsoft Dynamics AX 2012 и Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="18417-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="18417-176">Для временного размещения сводных измерений куба в хранилище объектов необходимо сделать их развертываемыми.</span><span class="sxs-lookup"><span data-stu-id="18417-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="18417-177">Дополнительные сведения см. в процедуре временного размещения агрегированных измерений в хранилище объектов в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="18417-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="18417-178">Следующие ключевые агрегированные измерения доступны непосредственно из объекта "Строки накладной" и используются в качестве основы для содержимого.</span><span class="sxs-lookup"><span data-stu-id="18417-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="18417-179">Объект</span><span class="sxs-lookup"><span data-stu-id="18417-179">Entity</span></span>        | <span data-ttu-id="18417-180">Ключевые сводные измерения</span><span class="sxs-lookup"><span data-stu-id="18417-180">Key aggregate measurements</span></span> | <span data-ttu-id="18417-181">Иcточник данных</span><span class="sxs-lookup"><span data-stu-id="18417-181">Data source</span></span>                                 | <span data-ttu-id="18417-182">Поле</span><span class="sxs-lookup"><span data-stu-id="18417-182">Field</span></span>              | <span data-ttu-id="18417-183">описание</span><span class="sxs-lookup"><span data-stu-id="18417-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="18417-184">Строки накладной</span><span class="sxs-lookup"><span data-stu-id="18417-184">Invoice lines</span></span> | <span data-ttu-id="18417-185">Покупка</span><span class="sxs-lookup"><span data-stu-id="18417-185">Purchase</span></span>                   | <span data-ttu-id="18417-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="18417-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="18417-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="18417-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="18417-188">Сумма в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="18417-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="18417-189">В следующей таблице приведены ключевые измерения, которые рассчитываются из объекта "Строки накладной".</span><span class="sxs-lookup"><span data-stu-id="18417-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="18417-190">Мера</span><span class="sxs-lookup"><span data-stu-id="18417-190">Measure</span></span>               | <span data-ttu-id="18417-191">Расчет</span><span class="sxs-lookup"><span data-stu-id="18417-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18417-192">Покупки за текущий год</span><span class="sxs-lookup"><span data-stu-id="18417-192">Purchase current year</span></span> | <span data-ttu-id="18417-193">Покупки за текущий год = SUM('Строки накладной'\[Покупка\])</span><span class="sxs-lookup"><span data-stu-id="18417-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="18417-194">Покупки за прошлый год</span><span class="sxs-lookup"><span data-stu-id="18417-194">Purchase last year</span></span>    | <span data-ttu-id="18417-195">Покупки за прошлый год = CALCULATE(SUM('Строки накладной'\[Покупка\]), SAMEPERIODLASTYEAR(Даты\[Дата\]))</span><span class="sxs-lookup"><span data-stu-id="18417-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="18417-196">Рост покупок по годам</span><span class="sxs-lookup"><span data-stu-id="18417-196">YOY purchase growth</span></span>   | <span data-ttu-id="18417-197">Рост покупок по годам = \[Покупки за текущий год\] – \[Покупки за прошлый год\]</span><span class="sxs-lookup"><span data-stu-id="18417-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="18417-198">Следующие ключевые измерения в содержимом используются в качестве фильтров для разделения агрегированных измерений, чтобы можно было достичь большей детализации и получить более глубокое аналитическое представление.</span><span class="sxs-lookup"><span data-stu-id="18417-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="18417-199">Объект</span><span class="sxs-lookup"><span data-stu-id="18417-199">Entity</span></span>                 | <span data-ttu-id="18417-200">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="18417-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="18417-201">Поставщики</span><span class="sxs-lookup"><span data-stu-id="18417-201">Vendors</span></span>                | <span data-ttu-id="18417-202">Группы поставщиков, Страна или регионы поставщика, Имя поставщика</span><span class="sxs-lookup"><span data-stu-id="18417-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="18417-203">Товары</span><span class="sxs-lookup"><span data-stu-id="18417-203">Products</span></span>               | <span data-ttu-id="18417-204">Номер продукта, Название продукта, Название групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="18417-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="18417-205">Категории закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="18417-205">Procurement categories</span></span> | <span data-ttu-id="18417-206">Категория закупаемой продукции, Названия категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="18417-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="18417-207">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="18417-207">Legal entities</span></span>         | <span data-ttu-id="18417-208">Имя информации о компании</span><span class="sxs-lookup"><span data-stu-id="18417-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="18417-209">Даты</span><span class="sxs-lookup"><span data-stu-id="18417-209">Dates</span></span>                  | <span data-ttu-id="18417-210">Даты, Смещение по году</span><span class="sxs-lookup"><span data-stu-id="18417-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="18417-211">По умолчанию содержимое отображает дату для текущего календарного года.</span><span class="sxs-lookup"><span data-stu-id="18417-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="18417-212">Однако можно изменить фильтр дат в разделе фильтров отчета.</span><span class="sxs-lookup"><span data-stu-id="18417-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="18417-213">Можно также изменить фильтр компаний.</span><span class="sxs-lookup"><span data-stu-id="18417-213">You can also change the company filter.</span></span>

