---
title: "Содержимое Power BI фактическое в сравнении с бюджетом"
description: "В этой теме описывается содержимое Power BI \"Факт/Бюджет\". В нем описывается порядок доступа к отчетам, входящим в содержимое, и предоставляется информация о модели данных и объектах, которые использовались для построения содержимого."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: afa8e07505283531c97663f35b208d82d69d2b42
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="149f9-104">Содержимое Power BI фактическое в сравнении с бюджетом</span><span class="sxs-lookup"><span data-stu-id="149f9-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="149f9-105">В этой теме описывается содержимое Microsoft Power BI **Факт/Бюджет**.</span><span class="sxs-lookup"><span data-stu-id="149f9-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="149f9-106">В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.</span><span class="sxs-lookup"><span data-stu-id="149f9-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="149f9-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="149f9-107">Overview</span></span>

<span data-ttu-id="149f9-108">Содержимое Power BI **Факт/бюджет** было создан по отдельным лицам, ответственным за мониторинг фактических показателей в сравнении с бюджетными в своей организации.</span><span class="sxs-lookup"><span data-stu-id="149f9-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="149f9-109">Содержимое Power BI **Факт/бюджет** обеспечивает видимость расхождений бюджета.</span><span class="sxs-lookup"><span data-stu-id="149f9-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="149f9-110">Можно проанализировать бюджет за текущий года по категории счета, коду бюджета, счету ГК, описаниям счета ГК или финансовому периоду, чтобы лучше понять причину любых расхождений.</span><span class="sxs-lookup"><span data-stu-id="149f9-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="149f9-111">Доступ к содержимому Power BI</span><span class="sxs-lookup"><span data-stu-id="149f9-111">Accessing the Power BI content</span></span>
<span data-ttu-id="149f9-112">При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) отчеты содержимого Power BI **Факт/Бюджет** отображаются в рабочих областях **Бюджет ГК и прогнозы** и **CFO**.</span><span class="sxs-lookup"><span data-stu-id="149f9-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="149f9-113">Отчеты, которые включены в содержимое Power BI</span><span class="sxs-lookup"><span data-stu-id="149f9-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="149f9-114">В следующей таблице приводятся подробные сведения о показателях, которые находятся на каждой странице отчета, в содержимом Power BI **Факт/Бюджет**.</span><span class="sxs-lookup"><span data-stu-id="149f9-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="149f9-115">Отчет</span><span class="sxs-lookup"><span data-stu-id="149f9-115">Report</span></span>                      | <span data-ttu-id="149f9-116">Показатели</span><span class="sxs-lookup"><span data-stu-id="149f9-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="149f9-117">Расходы — фактические и бюджетные</span><span class="sxs-lookup"><span data-stu-id="149f9-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="149f9-118">Итоговые расходы за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-118">Total expenses this year</span></span></li><li><span data-ttu-id="149f9-119">Итоговые расходы по бюджету за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="149f9-120">Выручка — фактическая и бюджетная</span><span class="sxs-lookup"><span data-stu-id="149f9-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="149f9-121">Итоговая выручка за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-121">Total revenue this year</span></span></li><li><span data-ttu-id="149f9-122">Итоговая выручка по бюджету за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="149f9-123">Расход</span><span class="sxs-lookup"><span data-stu-id="149f9-123">Expense</span></span>                     | <ul><li><span data-ttu-id="149f9-124">Итоговые расходы за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-124">Total expenses this year</span></span></li><li><span data-ttu-id="149f9-125">Цель для расходов в зависимости от бюджета</span><span class="sxs-lookup"><span data-stu-id="149f9-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="149f9-126">Реализация</span><span class="sxs-lookup"><span data-stu-id="149f9-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="149f9-127">Итоговая выручка за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-127">Total revenue this year</span></span></li><li><span data-ttu-id="149f9-128">Цель для выручки в зависимости от бюджета</span><span class="sxs-lookup"><span data-stu-id="149f9-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="149f9-129">Чистый доход</span><span class="sxs-lookup"><span data-stu-id="149f9-129">Net income</span></span>                  | <ul><li><span data-ttu-id="149f9-130">Чистый доход за этот год</span><span class="sxs-lookup"><span data-stu-id="149f9-130">Net income this year</span></span></li><li><span data-ttu-id="149f9-131">Цель для чистого дохода в зависимости от бюджета</span><span class="sxs-lookup"><span data-stu-id="149f9-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="149f9-132">Расширение содержимого Power BI</span><span class="sxs-lookup"><span data-stu-id="149f9-132">Extending the Power BI content</span></span>
<span data-ttu-id="149f9-133">С помощью пакетов содержимого, доступных в Microsoft Dynamics Lifecycle Services (LCS), можно повысить эффективность аналитики для тех, кто не использует Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="149f9-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="149f9-134">Эти пакеты содержимого можно изменить, чтобы они включали других отчеты или визуальные элементы, и затем опубликовать пакеты содержимого для владельца Power BI.com для анализа.</span><span class="sxs-lookup"><span data-stu-id="149f9-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="149f9-135">Содержимое Power BI **Факт/Бюджет** можно найти в библиотеке общих ресурсов в LCS.</span><span class="sxs-lookup"><span data-stu-id="149f9-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="149f9-136">Дополнительные сведения о том, как загрузить содержимое и реализовать его в вашей организации, см. в разделе [Содержимое Power BI в LCS от Майкрософт и ваших партнеров](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="149f9-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="149f9-137">Чтобы просмотреть демонстрацию, которая показывает, как реализовать содержимое Power BI, см. [Содержимое Power BI от Майкрософт и ваших партнеров в службах Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office mix).</span><span class="sxs-lookup"><span data-stu-id="149f9-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="149f9-138">Понимание модели данных и объектов</span><span class="sxs-lookup"><span data-stu-id="149f9-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="149f9-139">Объект</span><span class="sxs-lookup"><span data-stu-id="149f9-139">Entity</span></span>                    | <span data-ttu-id="149f9-140">Содержание</span><span class="sxs-lookup"><span data-stu-id="149f9-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="149f9-141">Действия ГК</span><span class="sxs-lookup"><span data-stu-id="149f9-141">General Ledger Activities</span></span> | <span data-ttu-id="149f9-142">Сумма проводки по КГ</span><span class="sxs-lookup"><span data-stu-id="149f9-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="149f9-143">Действия бюджета</span><span class="sxs-lookup"><span data-stu-id="149f9-143">Budget Activities</span></span>         | <span data-ttu-id="149f9-144">Суммы проводок для регистра бюджета</span><span class="sxs-lookup"><span data-stu-id="149f9-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="149f9-145">Счета ГК</span><span class="sxs-lookup"><span data-stu-id="149f9-145">Main Accounts</span></span>             | <span data-ttu-id="149f9-146">Счета ГК для фильтрации отчетов</span><span class="sxs-lookup"><span data-stu-id="149f9-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="149f9-147">Финансовые календари</span><span class="sxs-lookup"><span data-stu-id="149f9-147">Fiscal Calendars</span></span>          | <span data-ttu-id="149f9-148">Финансовые календари для фильтрации отчетов</span><span class="sxs-lookup"><span data-stu-id="149f9-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="149f9-149">Главные книги</span><span class="sxs-lookup"><span data-stu-id="149f9-149">Ledgers</span></span>                   | <span data-ttu-id="149f9-150">Книги, которые могут использоваться для фильтрации отчета по текущей книге</span><span class="sxs-lookup"><span data-stu-id="149f9-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="149f9-151">Коды бюджета</span><span class="sxs-lookup"><span data-stu-id="149f9-151">Budget Codes</span></span>              | <span data-ttu-id="149f9-152">Коды бюджета, по которым требуется фильтровать отчеты</span><span class="sxs-lookup"><span data-stu-id="149f9-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="149f9-153">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="149f9-153">Legal Entities</span></span>            | <span data-ttu-id="149f9-154">Юридические лица, которые могут использоваться для фильтрации отчета по текущему юридическому лицу</span><span class="sxs-lookup"><span data-stu-id="149f9-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |
