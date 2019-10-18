---
title: Использование аналитических отчетов в Microsoft Dynamics 365 Talent - Attract
description: В этой теме описываются аналитические отчеты для анализа процесса найма в Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010023"
---
# <a name="use-analytic-reports"></a><span data-ttu-id="457d2-103">Использование аналитических отчетов</span><span class="sxs-lookup"><span data-stu-id="457d2-103">Use analytic reports</span></span>

<span data-ttu-id="457d2-104">Аналитические отчеты в Microsoft Dynamics 365 Talent: Attract предоставляют готовое решение для получения аналитической информации о приеме на работу.</span><span class="sxs-lookup"><span data-stu-id="457d2-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="457d2-105">К доступным функциям относятся:</span><span class="sxs-lookup"><span data-stu-id="457d2-105">Availabe features include:</span></span>

- <span data-ttu-id="457d2-106">**Аналитики должности:** нажмите вкладку **Аналитика** в должности для показателей по кандидату на должность.</span><span class="sxs-lookup"><span data-stu-id="457d2-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="457d2-107">**Центр аналитики:** щелкните **Аналитика** в левой области навигации для суммарных показателей по должностям.</span><span class="sxs-lookup"><span data-stu-id="457d2-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="457d2-108">**Безопасность на уровне пользователей:** доступ к отчетам управляется [ролью](security-attract.md) Attract и ролью участника должности.</span><span class="sxs-lookup"><span data-stu-id="457d2-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="457d2-109">**Перекрестная фильтрация:** щелкните визуальные элементы в отчете для просмотра других показателей, отфильтрованных по выбранным данным.</span><span class="sxs-lookup"><span data-stu-id="457d2-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="457d2-110">Эта функция в данный момент находится в режиме [предварительного просмотра](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="457d2-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="457d2-111">Чтобы попробовать ее, необходимо иметь [**надстройку Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="457d2-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="457d2-112">Все отчеты открытой предварительной версии выводятся на английском языке.</span><span class="sxs-lookup"><span data-stu-id="457d2-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="457d2-113">Отчеты обновляются каждые 3 часа.</span><span class="sxs-lookup"><span data-stu-id="457d2-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="457d2-114">Время последнего обновления (в местном часовом поясе) находится в верхней части отчета.</span><span class="sxs-lookup"><span data-stu-id="457d2-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="457d2-115">Время обновления является приблизительным и может меняться в зависимости от объема данных и загрузки ресурсов в вашем регионе.</span><span class="sxs-lookup"><span data-stu-id="457d2-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="457d2-116">Аналитика должности</span><span class="sxs-lookup"><span data-stu-id="457d2-116">Job Analytics</span></span>

<span data-ttu-id="457d2-117">Отчеты аналитики должностей являются моментальным снимком процесса найма на работу.</span><span class="sxs-lookup"><span data-stu-id="457d2-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="457d2-118">Основные метрики включают:</span><span class="sxs-lookup"><span data-stu-id="457d2-118">Key metrics include:</span></span>

- <span data-ttu-id="457d2-119">Активные кандидаты по этапам</span><span class="sxs-lookup"><span data-stu-id="457d2-119">Active applicants by stage</span></span>
- <span data-ttu-id="457d2-120">Источник кандидата</span><span class="sxs-lookup"><span data-stu-id="457d2-120">Applicant source</span></span>
- <span data-ttu-id="457d2-121">Тип кандидата (внутренний или внешний)</span><span class="sxs-lookup"><span data-stu-id="457d2-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="457d2-122">Центр аналитики</span><span class="sxs-lookup"><span data-stu-id="457d2-122">Analytics Hub</span></span>

<span data-ttu-id="457d2-123">Центр аналитики сообщает сводные данные о должностях, чтобы выявить тенденции в процессе найма.</span><span class="sxs-lookup"><span data-stu-id="457d2-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="457d2-124">Attract включает два готовых отчета: сводка по процессу и анализ последовательностей.</span><span class="sxs-lookup"><span data-stu-id="457d2-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="457d2-125">Сводка по процессу продаж</span><span class="sxs-lookup"><span data-stu-id="457d2-125">Pipeline Summary</span></span>

<span data-ttu-id="457d2-126">Сводный отчет по процессу объединяет данные для открытых должностей.</span><span class="sxs-lookup"><span data-stu-id="457d2-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="457d2-127">Основные метрики включают:</span><span class="sxs-lookup"><span data-stu-id="457d2-127">Key metrics include:</span></span>

- <span data-ttu-id="457d2-128">Кандидаты среди всех должностей по этапам</span><span class="sxs-lookup"><span data-stu-id="457d2-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="457d2-129">Источник кандидата</span><span class="sxs-lookup"><span data-stu-id="457d2-129">Applicant source</span></span>
- <span data-ttu-id="457d2-130">Открытые вакансии по уровню трудового стажа</span><span class="sxs-lookup"><span data-stu-id="457d2-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="457d2-131">Анализ последовательностей</span><span class="sxs-lookup"><span data-stu-id="457d2-131">Funnel Analysis</span></span>

<span data-ttu-id="457d2-132">Отчет анализа последовательностей объединяет данные для вакансий, которые были закрыты как заполненные.</span><span class="sxs-lookup"><span data-stu-id="457d2-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="457d2-133">Основные метрики включают:</span><span class="sxs-lookup"><span data-stu-id="457d2-133">Key metrics include:</span></span>

- <span data-ttu-id="457d2-134">Время до найма</span><span class="sxs-lookup"><span data-stu-id="457d2-134">Time to hire</span></span>
- <span data-ttu-id="457d2-135">Метрики преобразования (при наведении)</span><span class="sxs-lookup"><span data-stu-id="457d2-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="457d2-136">Коэффициент принятия предложений</span><span class="sxs-lookup"><span data-stu-id="457d2-136">Offer acceptance rate</span></span>

<span data-ttu-id="457d2-137">Примечание. Для наиболее точной отчетности о времени до найма рекомендуется использовать [Управление предложениями](offer-setup.md) — функцию, доступную в рамках надстройки Comprehensive Hiring Add-On.</span><span class="sxs-lookup"><span data-stu-id="457d2-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="457d2-138">Попробуйте навести курсор на визуальные элементы для получения дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="457d2-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="457d2-139">Например, при наведении указателя на визуальные элементы **Активные кандидаты** будет отображено среднее число дней на этапе.</span><span class="sxs-lookup"><span data-stu-id="457d2-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="457d2-140">Анализ этой информации позволяет получить ценные сведения, необходимые для сокращения времени найма, и позволяющие сотрудникам по найму сосредоточиться на способах уменьшения времени, потраченного на каждый этап.</span><span class="sxs-lookup"><span data-stu-id="457d2-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="457d2-141">Безопасность на уровне пользователей</span><span class="sxs-lookup"><span data-stu-id="457d2-141">User-specific security</span></span>

<span data-ttu-id="457d2-142">Отчеты Attract доступны для [ролей](security-attract.md) администратора, чтение всего, сотрудник по найму и менеджер по найму.</span><span class="sxs-lookup"><span data-stu-id="457d2-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="457d2-143">Неназначенные пользователи не имеют доступа к страницам аналитических отчетов (аналитика должностей или центр аналитики).</span><span class="sxs-lookup"><span data-stu-id="457d2-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="457d2-144">Отчеты "Аналитика должности" показывают данные для выбранной должности.</span><span class="sxs-lookup"><span data-stu-id="457d2-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="457d2-145">Отчет "Центр аналитики" отображает сводные данные по всем должностям, которые пользователь может просмотреть.</span><span class="sxs-lookup"><span data-stu-id="457d2-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="457d2-146">Пользователи, которые могут просматривать как "Мои должности", так и "Все должности" на странице "Должности", имеют те же представления, которые доступны в Центре аналитики.</span><span class="sxs-lookup"><span data-stu-id="457d2-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="457d2-147">Перекрестный фильтр</span><span class="sxs-lookup"><span data-stu-id="457d2-147">Cross-filter</span></span>

<span data-ttu-id="457d2-148">Одной из замечательных функций Power BI — это способ, которым взаимосвязаны все визуальные элементы на странице отчета.</span><span class="sxs-lookup"><span data-stu-id="457d2-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="457d2-149">Если выбрать точку данных на одном из визуальных элементов, все остальные визуальные элементы на странице, содержащие это изменение данных, будут выделены на основе выбранного значения.</span><span class="sxs-lookup"><span data-stu-id="457d2-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="457d2-150">Дополнительные сведения и пример см. в разделе [Как визуальные элементы реализуют перекрестную фильтрацию в отчете Power BI](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="457d2-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="457d2-151">Экспорт в Excel</span><span class="sxs-lookup"><span data-stu-id="457d2-151">Export to Excel</span></span>

<span data-ttu-id="457d2-152">Для просмотра данных отчета в Excel можно щелкнуть меню параметров (три точки) на визуальном элементе и выбрать **Экспорт базовых данных**</span><span class="sxs-lookup"><span data-stu-id="457d2-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="457d2-153">Экспортированные данные экспортируются как отфильтрованные с учетом разрешений пользователя в Attract.</span><span class="sxs-lookup"><span data-stu-id="457d2-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="457d2-154">Дополнительные сведения см. в разделе [Экспорт данных из визуальных элементов](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="457d2-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
