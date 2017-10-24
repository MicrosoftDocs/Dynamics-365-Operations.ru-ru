---
title: "Содержимое Power BI \"Менеджер по методикам\""
description: "В этом разделе описывается, что входит в содержимое Power BI \"Менеджер по методикам\". В нем описывается порядок доступа к отчетам, входящим в содержимое, и предоставляется информация о модели данных и объектах, используемых для построения содержимого."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 99e5b5087cc72c01ff3e92d0b2b3a6279385eb19
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="practice-manager-power-bi-content"></a><span data-ttu-id="0f5f6-104">Содержимое Power BI "Менеджер по методикам"</span><span class="sxs-lookup"><span data-stu-id="0f5f6-104">Practice manager Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f5f6-105">В этом разделе описывается, что входит в содержимое Microsoft Power BI **Менеджер по методикам**.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-105">This topic describes what is included in the **Practice manager** Microsoft Power BI content.</span></span> <span data-ttu-id="0f5f6-106">В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="0f5f6-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="0f5f6-107">Overview</span></span>

<span data-ttu-id="0f5f6-108">Содержимое Power BI **Менеджер по методикам** создано для менеджеров по методикам и менеджеров проектов.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-108">The **Practice manager** Power BI content was created for practice managers and project managers.</span></span> <span data-ttu-id="0f5f6-109">Оно предоставляет ключевые показатели, связанные с проектами, над которыми работает организация.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-109">It provides key metrics that are related to the projects that the organization is working on.</span></span> <span data-ttu-id="0f5f6-110">Панель мониторинга содержит общие сведения о проектах и связанных с ними клиентах.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-110">The dashboard gives an overview of the projects and related customers.</span></span> <span data-ttu-id="0f5f6-111">Фильтр уровня отчета можно использовать для получения отчета для конкретных юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-111">A report-level filter can be used to report for specific legal entities.</span></span> <span data-ttu-id="0f5f6-112">Это содержимое Power BI подтягивает данные из агрегированных измерений учета по проекту.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-112">This Power BI content pulls data from the project accounting aggregate measurements.</span></span>

<span data-ttu-id="0f5f6-113">Содержимое Power BI **Менеджер по методикам** содержит пять страниц отчетов: одна обзорная страница и четыре страницы, которые предоставляют подробные сведения о затратах по проекту, доходах, управлением вырученной стоимостью и почасовым показателям, которые разбиты по различным измерениям.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-113">The **Practice manager** Power BI content contains five report pages: one overview page, and four pages that provide details about project costs, revenues, earned value management, and hour metrics that are broken down across various dimensions.</span></span>

<span data-ttu-id="0f5f6-114">Все суммы в содержимом отображаются в системной валюте.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-114">All the amounts in the content are shown in the system currency.</span></span> <span data-ttu-id="0f5f6-115">Системную валюту можно задать на странице **Системные параметры**.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-115">You can set the system currency on the **System parameters** page.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="0f5f6-116">Доступ к содержимому Power BI</span><span class="sxs-lookup"><span data-stu-id="0f5f6-116">Accessing the Power BI content</span></span>
<span data-ttu-id="0f5f6-117">При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.), содержимое Power BI **Менеджер по методикам** отображается в рабочей области **Управление проектами**.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-117">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Practice manager** Power BI content is shown in the **Project management** workspace.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="0f5f6-118">Отчеты, которые включены в содержимое Power BI</span><span class="sxs-lookup"><span data-stu-id="0f5f6-118">Reports that are included in the Power BI content</span></span>

<span data-ttu-id="0f5f6-119">В следующей таблице приводятся подробные сведения о показателях, которые находятся на каждой странице отчета, в содержимом Power BI **Менеджер по методикам**.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-119">The following table provides details about the metrics that are found on each report page in the **Practice manager** Power BI content.</span></span>

| <span data-ttu-id="0f5f6-120">Страница отчета</span><span class="sxs-lookup"><span data-stu-id="0f5f6-120">Report page</span></span>       | <span data-ttu-id="0f5f6-121">Показатели</span><span class="sxs-lookup"><span data-stu-id="0f5f6-121">Metrics</span></span> |
|-------------------|---------|
| <span data-ttu-id="0f5f6-122">Обзор проектов</span><span class="sxs-lookup"><span data-stu-id="0f5f6-122">Projects overview</span></span> | <ul><li><span data-ttu-id="0f5f6-123">Созданные проекты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-123">Created projects</span></span></li><li><span data-ttu-id="0f5f6-124">Оцененные проекты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-124">Estimated projects</span></span></li><li><span data-ttu-id="0f5f6-125">Выполняющиеся проекты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-125">In-process projects</span></span></li><li><span data-ttu-id="0f5f6-126">Число проектов по этапам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-126">Number of projects by stage</span></span></li><li><span data-ttu-id="0f5f6-127">Число проектов по городам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-127">Number of projects by city</span></span></li><li><span data-ttu-id="0f5f6-128">Фактическая выручка по клиентам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-128">Actual revenue by customer</span></span></li><li><span data-ttu-id="0f5f6-129">Бюджетная валовая прибыль по проектам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-129">Budget gross margin by project</span></span></li><li><span data-ttu-id="0f5f6-130">Обзор управления вырученной стоимостью</span><span class="sxs-lookup"><span data-stu-id="0f5f6-130">Earned value management overview</span></span></li></ul> |
| <span data-ttu-id="0f5f6-131">Затраты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-131">Cost</span></span>              | <ul><li><span data-ttu-id="0f5f6-132">Фактические и бюджетные затраты по месяцам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-132">Actual vs. budget cost by month</span></span></li><li><span data-ttu-id="0f5f6-133">Фактические и бюджетные затраты по годам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-133">Actual vs. budget cost by year</span></span></li><li><span data-ttu-id="0f5f6-134">Фактические и бюджетные затраты по категориям</span><span class="sxs-lookup"><span data-stu-id="0f5f6-134">Actual vs. budget cost by category</span></span></li><li><span data-ttu-id="0f5f6-135">Фактические затраты по типам проводки</span><span class="sxs-lookup"><span data-stu-id="0f5f6-135">Actual cost by transaction type</span></span></li></ul> |
| <span data-ttu-id="0f5f6-136">Реализация</span><span class="sxs-lookup"><span data-stu-id="0f5f6-136">Revenue</span></span>           | <ul><li><span data-ttu-id="0f5f6-137">Фактическая выручка по месяцам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-137">Actual revenue by month</span></span></li><li><span data-ttu-id="0f5f6-138">Фактическая выручка по почтовому индексу</span><span class="sxs-lookup"><span data-stu-id="0f5f6-138">Actual revenue by postal code</span></span></li><li><span data-ttu-id="0f5f6-139">Фактическая и бюджетная выручка по категориям</span><span class="sxs-lookup"><span data-stu-id="0f5f6-139">Actual vs. budget revenue by category</span></span></li><li><span data-ttu-id="0f5f6-140">Фактическая выручка по отрасли клиента</span><span class="sxs-lookup"><span data-stu-id="0f5f6-140">Actual revenue by customer industry</span></span></li></ul> |
| <span data-ttu-id="0f5f6-141">EVM</span><span class="sxs-lookup"><span data-stu-id="0f5f6-141">EVM</span></span>               | <span data-ttu-id="0f5f6-142">Затраты и индекс выполнения графика по проектам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-142">Cost and schedule performance index by project</span></span> |
| <span data-ttu-id="0f5f6-143">Часы</span><span class="sxs-lookup"><span data-stu-id="0f5f6-143">Hours</span></span>             | <ul><li><span data-ttu-id="0f5f6-144">Фактические оплачиваемые использованные часы, фактические оплачиваемые часы по накладным расходам и бюджетные часы</span><span class="sxs-lookup"><span data-stu-id="0f5f6-144">Actual billable utilized hours vs. actual billable burden hours vs. budget hours</span></span></li><li><span data-ttu-id="0f5f6-145">Фактические оплачиваемые использованные часы и фактические оплачиваемые часы по накладным расходам по проектам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-145">Actual billable utilized hours vs. actual billable burden hours by project</span></span></li><li><span data-ttu-id="0f5f6-146">Фактические оплачиваемые использованные часы и фактические оплачиваемые часы по накладным расходам по ресурсам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-146">Actual billable utilized hours vs. actual billable burden hours by resource</span></span></li><li><span data-ttu-id="0f5f6-147">Отношение фактически оплачиваемых часов по проектам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-147">Actual billable hours ratio by project</span></span></li><li><span data-ttu-id="0f5f6-148">Отношение фактически оплачиваемых часов по ресурсам</span><span class="sxs-lookup"><span data-stu-id="0f5f6-148">Actual billable hours ratio by resource</span></span></li></ul> |

<span data-ttu-id="0f5f6-149">Диаграммы и плитки во всех этих отчетах можно отфильтровать и закрепить на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-149">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="0f5f6-150">Дополнительные сведения о том, как отфильтровать и закрепить элементы в Power BI, см. в разделе [Создание и настройка панели мониторинга](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/).</span><span class="sxs-lookup"><span data-stu-id="0f5f6-150">For more information about how to filter and pin in Power BI, see [Create and configure a dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/).</span></span> <span data-ttu-id="0f5f6-151">Можно также использовать функцию экспорта базовых данных для экспорта базовых данных, сводка которых отображается в визуализации.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-151">You can also use the Export underlying data functionality to export the underlying data that is summarized in a visualization.</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="0f5f6-152">Расширение содержимого Power BI</span><span class="sxs-lookup"><span data-stu-id="0f5f6-152">Extending the Power BI content</span></span>
<span data-ttu-id="0f5f6-153">С помощью пакетов содержимого, доступных в Microsoft Dynamics Lifecycle Services (LCS), можно повысить эффективность аналитики для тех, кто не использует Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-153">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="0f5f6-154">Эти пакеты содержимого можно изменить, включив в них другие отчеты или визуальные элементы, и затем опубликовать пакеты для вашего владельца Power BI.com для анализа.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-154">You can modify these content packs so that they include other reports or visuals, and then publish them to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="0f5f6-155">Содержимое Power BI **Менеджер по методикам** можно найти в библиотеке общих ресурсов в LCS.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-155">You can find the **Practice manager** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="0f5f6-156">Дополнительные сведения о том, как загрузить содержимое и реализовать его в вашей организации, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="0f5f6-156">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="0f5f6-157">Чтобы просмотреть демонстрацию, которая показывает, как реализовать содержимое Power BI, см. [Содержимое Power BI от Майкрософт и ваших партнеров в службах Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office mix).</span><span class="sxs-lookup"><span data-stu-id="0f5f6-157">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="0f5f6-158">Следите за тем, чтобы загружаемое содержимое Power BI **Менеджер по методикам** соответствовало версии Dynamics 365, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-158">Be sure to download the **Practice manager** content that applies to the version of Dynamics 365 that you're using.</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="0f5f6-159">Понимание модели данных и объектов</span><span class="sxs-lookup"><span data-stu-id="0f5f6-159">Understanding the data model and entities</span></span>

<span data-ttu-id="0f5f6-160">Следующие данные используются для заполнения страниц отчета в содержимом Power BI **Менеджер по методикам**.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-160">The following data is used to fill the report pages in the **Practice manager** Power BI content.</span></span> <span data-ttu-id="0f5f6-161">Эти данные представлены как общие измерения, которые помещаются на временное хранение в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-161">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="0f5f6-162">Хранилище объектов является базой данных Microsoft SQL Server, оптимизированной для аналитики.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-162">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="0f5f6-163">Дополнительные сведения см. в разделе [Обзор интеграции Power BI с хранилищем объектов](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="0f5f6-163">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="0f5f6-164">В следующих разделах описываются агрегированные измерения, используемые в каждом объекте.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-164">The following sections describe the aggregate measurements that are used in each entity.</span></span>

### <a name="entity-projectaccountingcubeactualhourutilization"></a><span data-ttu-id="0f5f6-165">Объект: ProjectAccountingCube_ActualHourUtilization</span><span class="sxs-lookup"><span data-stu-id="0f5f6-165">Entity: ProjectAccountingCube_ActualHourUtilization</span></span>
<span data-ttu-id="0f5f6-166">**Источник данных:** ProjEmplTrans</span><span class="sxs-lookup"><span data-stu-id="0f5f6-166">**Data source:** ProjEmplTrans</span></span>

| <span data-ttu-id="0f5f6-167">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-167">Key aggregate measurement</span></span>      | <span data-ttu-id="0f5f6-168">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-168">Field</span></span>                              | <span data-ttu-id="0f5f6-169">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-169">Description</span></span> | 
|--------------------------------|------------------------------------|-------------|
| <span data-ttu-id="0f5f6-170">Фактические оплачиваемые использованные часы</span><span class="sxs-lookup"><span data-stu-id="0f5f6-170">Actual billable utilized hours</span></span> | <span data-ttu-id="0f5f6-171">Sum(ActualUtilizationBillableRate)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-171">Sum(ActualUtilizationBillableRate)</span></span> | <span data-ttu-id="0f5f6-172">Общее количество фактически оплачиваемых использованных часов.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-172">The total of actual billable utilized hours.</span></span> |
| <span data-ttu-id="0f5f6-173">Фактические оплачиваемые не учитываемые в начислении часы</span><span class="sxs-lookup"><span data-stu-id="0f5f6-173">Actual billable burden hours</span></span>   | <span data-ttu-id="0f5f6-174">Sum(ActualBurdenBillableRate)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-174">Sum(ActualBurdenBillableRate)</span></span>      | <span data-ttu-id="0f5f6-175">Общий коэффициент фактических накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-175">The total of the actual burden rate.</span></span> |

### <a name="entity-projectaccountingcubeactuals"></a><span data-ttu-id="0f5f6-176">Объект: ProjectAccountingCube_Actuals</span><span class="sxs-lookup"><span data-stu-id="0f5f6-176">Entity: ProjectAccountingCube_Actuals</span></span>
<span data-ttu-id="0f5f6-177">**Источник данных:** ProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="0f5f6-177">**Data source:** ProjTransPosting</span></span>

| <span data-ttu-id="0f5f6-178">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-178">Key aggregate measurement</span></span> | <span data-ttu-id="0f5f6-179">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-179">Field</span></span>              | <span data-ttu-id="0f5f6-180">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-180">Description</span></span> | 
|---------------------------|--------------------|-------------|
| <span data-ttu-id="0f5f6-181">Фактическая выручка</span><span class="sxs-lookup"><span data-stu-id="0f5f6-181">Actual revenue</span></span>            | <span data-ttu-id="0f5f6-182">Sum(ActualRevenue)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-182">Sum(ActualRevenue)</span></span> | <span data-ttu-id="0f5f6-183">Общая сумма разнесенной выручки для всех проводок.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-183">The total of posted revenue for all transactions.</span></span> |   
| <span data-ttu-id="0f5f6-184">Фактические затраты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-184">Actual cost</span></span>               | <span data-ttu-id="0f5f6-185">Sum(ActualCost)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-185">Sum(ActualCost)</span></span>    | <span data-ttu-id="0f5f6-186">Общая сумма разнесенных затрат для всех типов проводок.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-186">The total of posted cost for all transaction types.</span></span> |

### <a name="entity-projectaccountingcubecustomer"></a><span data-ttu-id="0f5f6-187">Объект: ProjectAccountingCube_Customer</span><span class="sxs-lookup"><span data-stu-id="0f5f6-187">Entity: ProjectAccountingCube_Customer</span></span>
<span data-ttu-id="0f5f6-188">**Источник данных:** CustTable</span><span class="sxs-lookup"><span data-stu-id="0f5f6-188">**Data source:** CustTable</span></span>

| <span data-ttu-id="0f5f6-189">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-189">Key aggregate measurement</span></span> | <span data-ttu-id="0f5f6-190">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-190">Field</span></span>                                            | <span data-ttu-id="0f5f6-191">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-191">Description</span></span> | 
|---------------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="0f5f6-192">Число проектов</span><span class="sxs-lookup"><span data-stu-id="0f5f6-192">Number of projects</span></span>        | <span data-ttu-id="0f5f6-193">COUNTA(ProjectAccountingCube_Projects[PROJECTS])</span><span class="sxs-lookup"><span data-stu-id="0f5f6-193">COUNTA(ProjectAccountingCube_Projects[PROJECTS])</span></span> | <span data-ttu-id="0f5f6-194">Число доступных проектов.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-194">The count of available projects.</span></span> |


### <a name="entity-projectaccountingcubeforecasts"></a><span data-ttu-id="0f5f6-195">Объект: ProjectAccountingCube_Forecasts</span><span class="sxs-lookup"><span data-stu-id="0f5f6-195">Entity: ProjectAccountingCube_Forecasts</span></span>
<span data-ttu-id="0f5f6-196">**Источник данных:** ProjTransBudget</span><span class="sxs-lookup"><span data-stu-id="0f5f6-196">**Data source:** ProjTransBudget</span></span>

| <span data-ttu-id="0f5f6-197">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-197">Key aggregate measurement</span></span> | <span data-ttu-id="0f5f6-198">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-198">Field</span></span>                  | <span data-ttu-id="0f5f6-199">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-199">Description</span></span> | 
|---------------------------|------------------------|-------------|
| <span data-ttu-id="0f5f6-200">Бюджетные затраты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-200">Budget cost</span></span>               | <span data-ttu-id="0f5f6-201">Sum(BudgetCost)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-201">Sum(BudgetCost)</span></span>        | <span data-ttu-id="0f5f6-202">Общая сумма прогнозируемых затрат для всех типов проводок.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-202">The total of forecast cost for all transaction types.</span></span> |
| <span data-ttu-id="0f5f6-203">Бюджетный доход</span><span class="sxs-lookup"><span data-stu-id="0f5f6-203">Budget revenue</span></span>            | <span data-ttu-id="0f5f6-204">Sum(BudgetRevenue)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-204">Sum(BudgetRevenue)</span></span>     | <span data-ttu-id="0f5f6-205">Общая сумма прогнозируемой начисленной выручки/выручки по выставленным накладным.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-205">The total of forecast accrued/invoiced revenue.</span></span>  |
| <span data-ttu-id="0f5f6-206">Бюджетная валовая прибыль</span><span class="sxs-lookup"><span data-stu-id="0f5f6-206">Budget gross margin</span></span>       | <span data-ttu-id="0f5f6-207">Sum(BudgetGrossMargin)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-207">Sum(BudgetGrossMargin)</span></span> | <span data-ttu-id="0f5f6-208">Разница между суммой общей прогнозируемой выручки и суммой общих прогнозируемых затрат.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-208">The difference between the sum of total forecast revenue and the sum of total forecast cost.</span></span> |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a><span data-ttu-id="0f5f6-209">Объект: ProjectAccountingCube_ProjectPlanCostsView</span><span class="sxs-lookup"><span data-stu-id="0f5f6-209">Entity: ProjectAccountingCube_ProjectPlanCostsView</span></span>
<span data-ttu-id="0f5f6-210">**Источник данных:** Project</span><span class="sxs-lookup"><span data-stu-id="0f5f6-210">**Data source:** Project</span></span>

| <span data-ttu-id="0f5f6-211">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-211">Key aggregate measurement</span></span> | <span data-ttu-id="0f5f6-212">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-212">Field</span></span>                    | <span data-ttu-id="0f5f6-213">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-213">Description</span></span> | 
|---------------------------|--------------------------|-------------|
| <span data-ttu-id="0f5f6-214">Плановые затраты</span><span class="sxs-lookup"><span data-stu-id="0f5f6-214">Planned cost</span></span>              | <span data-ttu-id="0f5f6-215">Sum(SumOfTotalCostPrice)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-215">Sum(SumOfTotalCostPrice)</span></span> | <span data-ttu-id="0f5f6-216">Общая себестоимость в оценках для всех типов проводок проекта с запланированными задачами.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-216">The total cost price in estimates for all project transaction types that have planned tasks.</span></span> |

### <a name="entity-projectaccountingcubeprojects"></a><span data-ttu-id="0f5f6-217">Объект: ProjectAccountingCube_Projects</span><span class="sxs-lookup"><span data-stu-id="0f5f6-217">Entity: ProjectAccountingCube_Projects</span></span>
<span data-ttu-id="0f5f6-218">**Источник данных:** Project</span><span class="sxs-lookup"><span data-stu-id="0f5f6-218">**Data source:** Project</span></span>

| <span data-ttu-id="0f5f6-219">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-219">Key aggregate measurement</span></span>    | <span data-ttu-id="0f5f6-220">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-220">Field</span></span> | <span data-ttu-id="0f5f6-221">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-221">Description</span></span> | 
|------------------------------|-------|-------------|
| <span data-ttu-id="0f5f6-222">Индекс показателей затрат</span><span class="sxs-lookup"><span data-stu-id="0f5f6-222">Cost performance index</span></span>       | <span data-ttu-id="0f5f6-223">ProjectAccountingCube_Projects[Вырученная стоимость] / ProjectAccountingCube_Projects[Общие фактические затраты на выполненные задачи]</span><span class="sxs-lookup"><span data-stu-id="0f5f6-223">ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total actual cost of completed tasks]</span></span> | <span data-ttu-id="0f5f6-224">Расчет общей вырученной стоимости, деленной на общие фактические затраты.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-224">The calculation of the total earned value divided by the total actual cost.</span></span> |
| <span data-ttu-id="0f5f6-225">Индекс выполнения графика</span><span class="sxs-lookup"><span data-stu-id="0f5f6-225">Schedule performance index</span></span>   | <span data-ttu-id="0f5f6-226">ProjectAccountingCube_Projects[Вырученная стоимость] / ProjectAccountingCube_Projects[Общие плановые затраты на выполненные задачи]</span><span class="sxs-lookup"><span data-stu-id="0f5f6-226">ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total planned cost of completed tasks]</span></span> | <span data-ttu-id="0f5f6-227">Расчет общей вырученной стоимости, деленной на общие плановые затраты.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-227">The calculation of the total earned value divided by the total planned cost.</span></span> |
| <span data-ttu-id="0f5f6-228">Процент завершения работы</span><span class="sxs-lookup"><span data-stu-id="0f5f6-228">Percentage of work completed</span></span> | <span data-ttu-id="0f5f6-229">Процент завершения работы = ProjectAccountingCube_Projects[Общие фактические затраты на выполненные задачи] / (ProjectAccountingCube_Projects[Общие фактические затраты на выполненные задачи] + ProjectAccountingCube_Projects[Общие плановые затраты на проект] - ProjectAccountingCube_Projects[Общие плановые затраты на выполненные задачи])</span><span class="sxs-lookup"><span data-stu-id="0f5f6-229">Percentage of work completed = ProjectAccountingCube_Projects[Total actual cost of completed tasks] / (ProjectAccountingCube_Projects[Total actual cost of completed tasks] + ProjectAccountingCube_Projects[Total planned cost of project] - ProjectAccountingCube_Projects[Total planned cost of completed tasks])</span></span> | <span data-ttu-id="0f5f6-230">Общий процент выполненной работы на основе общих фактических затрат на выполненные задачи и плановых затрат для проекта.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-230">The total percentage of completed work, based on the total actual cost of completed tasks and the planned cost of the project.</span></span> |
| <span data-ttu-id="0f5f6-231">Относительный показатель фактически оплачиваемых часов</span><span class="sxs-lookup"><span data-stu-id="0f5f6-231">Actual billable hours ratio</span></span>  | <span data-ttu-id="0f5f6-232">ProjectAccountingCube_Projects[Общие фактические оплачиваемые использованные часы по проекту] / (ProjectAccountingCube_Projects[Общие фактические оплачиваемые использованные часы по проекту] + ProjectAccountingCube_Projects[Общие фактические оплачиваемые часы по накладным расходам по проекту])</span><span class="sxs-lookup"><span data-stu-id="0f5f6-232">ProjectAccountingCube_Projects[Project total actual billable utilized hours] / (ProjectAccountingCube_Projects[Project total actual billable utilized hours] + ProjectAccountingCube_Projects[Project total actual billable burden hours])</span></span> | <span data-ttu-id="0f5f6-233">Общие фактически оплачиваемые часы на основе использованных часов и часов по накладным расходам.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-233">The total actual billable hours, based on the utilized hours and the burden hours.</span></span> |
| <span data-ttu-id="0f5f6-234">Вырученная стоимость</span><span class="sxs-lookup"><span data-stu-id="0f5f6-234">Earned value</span></span>                 | <span data-ttu-id="0f5f6-235">ProjectAccountingCube_Projects[Общие плановые затраты на проект] * ProjectAccountingCube_Projects[Процент выполненных работ]</span><span class="sxs-lookup"><span data-stu-id="0f5f6-235">ProjectAccountingCube_Projects[Total planned cost of project] * ProjectAccountingCube_Projects[Percentage of work completed]</span></span> | <span data-ttu-id="0f5f6-236">Общие плановые затраты, умноженные на процент выполненных работ.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-236">The total planned cost multiplied by the percentage of completed work.</span></span> |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a><span data-ttu-id="0f5f6-237">Объект: ProjectAccountingCube_TotalEstimatedCosts</span><span class="sxs-lookup"><span data-stu-id="0f5f6-237">Entity: ProjectAccountingCube_TotalEstimatedCosts</span></span> 
<span data-ttu-id="0f5f6-238">**Источник данных:** ProjTable</span><span class="sxs-lookup"><span data-stu-id="0f5f6-238">**Data source:** ProjTable</span></span>

| <span data-ttu-id="0f5f6-239">Ключевое агрегированное измерение</span><span class="sxs-lookup"><span data-stu-id="0f5f6-239">Key aggregate measurement</span></span>       | <span data-ttu-id="0f5f6-240">Поле</span><span class="sxs-lookup"><span data-stu-id="0f5f6-240">Field</span></span>               | <span data-ttu-id="0f5f6-241">описание</span><span class="sxs-lookup"><span data-stu-id="0f5f6-241">Description</span></span> | 
|---------------------------------|---------------------|-------------|
| <span data-ttu-id="0f5f6-242">Плановые затраты по выполненным действиям</span><span class="sxs-lookup"><span data-stu-id="0f5f6-242">Completed activity planned cost</span></span> | <span data-ttu-id="0f5f6-243">Sum(TotalCostPrice)</span><span class="sxs-lookup"><span data-stu-id="0f5f6-243">Sum(TotalCostPrice)</span></span> | <span data-ttu-id="0f5f6-244">Общая себестоимость в оценках для всех типов проводок проекта с выполненными задачами.</span><span class="sxs-lookup"><span data-stu-id="0f5f6-244">The total cost price in estimates for all project transaction types that have completed tasks.</span></span> |
