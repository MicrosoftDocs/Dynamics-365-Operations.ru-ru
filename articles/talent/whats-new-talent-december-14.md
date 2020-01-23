---
title: Что нового и что изменилось в Dynamics 365 Talent — Core HR (14 декабря 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad677d1c36ac5159111afdcb5c31aed215d7b0a1
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897749"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a><span data-ttu-id="2d2fc-103">Что нового и что изменилось в Dynamics 365 Talent — Core HR (14 декабря 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-103">What's new or changed in Dynamics 365 Talent - Core HR (December 14, 2018)</span></span>

<span data-ttu-id="2d2fc-104">**Сборка 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="2d2fc-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="2d2fc-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="2d2fc-106">Изменения</span><span class="sxs-lookup"><span data-stu-id="2d2fc-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="2d2fc-107">США — Поддержка ACA (закон Affordable Care) для форм 1095-B и 1095-C для налогового года 2018</span><span class="sxs-lookup"><span data-stu-id="2d2fc-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="2d2fc-108">Каждый год соответствующие крупные работодатели (ALE) должны предоставить каждому сотруднику с полной занятостью форму 1095-C.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="2d2fc-109">Кроме того, если работодатель предоставляет самостоятельное покрытие, он обязан предоставить формы 1095-C (если он является крупным работодателем (ALE)) и 1095-B (если он является небольшим работодателем) для любого сотрудника, с полной или частичной занятостью, застрахованного в соответствии с одним из предложенных планов медицинского страхования.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="2d2fc-110">Эта функциональная возможность обеспечивает печатные варианты форм 1095-C и 1095-B.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="2d2fc-111">Во время импорта поле SubmittedByPersonId в HcmPerfJournalEntity игнорируется</span><span class="sxs-lookup"><span data-stu-id="2d2fc-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="2d2fc-112">При импорте или экспорте записей журнала производительности поле **Кем отправлено** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="2d2fc-113">В результате этого изменения значение **импортировано/экспортировано** будет отражать значение в таблице во время экспорта, при импорте система обновляется со значением, указанным в файле импорта.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="2d2fc-114">На вкладке аналитики в рабочей области "Отпуск и отсутствие" отображается ошибка "OpenConnectionError" для ролей, отличных от администратора</span><span class="sxs-lookup"><span data-stu-id="2d2fc-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="2d2fc-115">В этом обновлении никакие ошибки не отображаются при открытии вкладки **Аналитика** в рабочей области **Отпуск и отсутствие**.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="2d2fc-116">Детализация самообслуживания сотрудников, иерархия штатных единиц, из плитки не получает родительский узел</span><span class="sxs-lookup"><span data-stu-id="2d2fc-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="2d2fc-117">Внесено изменение для исправления ошибки "Не удалось получить родительский узел", когда иерархия штатных единиц настраивается для отображения в существующей рабочей области и выбирается должность в иерархии.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="2d2fc-118">Для просмотра вкладки заработной платы на странице должностей необходимо быть системным администратором</span><span class="sxs-lookup"><span data-stu-id="2d2fc-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="2d2fc-119">Был внесено изменение для включения правильных элементов безопасности в существующую привилегию: "Вести сведения о работнике на зарплате и его должности".</span><span class="sxs-lookup"><span data-stu-id="2d2fc-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="2d2fc-120">После этого изменения по умолчанию администратор заработной платы будут иметь доступ к полям заработной платы на странице должности.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="2d2fc-121">Ошибка, когда при отправке оценки производительности руководителю используется заполнитель %Reviews.PerfPeriod% в инструкциях по отправке</span><span class="sxs-lookup"><span data-stu-id="2d2fc-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="2d2fc-122">Внесено изменение, которое исправляет ошибку "Пустая ссылка" при использовании заполнителя %Reviews.PerfPeriod% в инструкциях по отправке.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="2d2fc-123">В отчете Power BI о трудовых ресурсах отображается ошибка, когда дата начала трудового стажа работника приходится на високосный день</span><span class="sxs-lookup"><span data-stu-id="2d2fc-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="2d2fc-124">После этого изменения високосные дни теперь поддерживаются в Power BI.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="2d2fc-125">Интеграцию между модулями Core HR и Attract</span><span class="sxs-lookup"><span data-stu-id="2d2fc-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="2d2fc-126">Внесено изменение для обновления интеграции между модулями Core HR и Attract, связанной с кандидатами для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="2d2fc-127">Чтобы кандидаты для приема на работу отображались в рабочей области **Управление персоналом**, используются следующие сущности Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="2d2fc-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="2d2fc-128">Заявление о приеме на работу</span><span class="sxs-lookup"><span data-stu-id="2d2fc-128">Job Application</span></span>
- <span data-ttu-id="2d2fc-129">Для причины состояния необходимо задать значение "Предложение принято"</span><span class="sxs-lookup"><span data-stu-id="2d2fc-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="2d2fc-130">Предоставляет кандидата и вакансию</span><span class="sxs-lookup"><span data-stu-id="2d2fc-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="2d2fc-131">Кандидат</span><span class="sxs-lookup"><span data-stu-id="2d2fc-131">Candidate</span></span>
-   <span data-ttu-id="2d2fc-132">Представляет сведения о кандидате</span><span class="sxs-lookup"><span data-stu-id="2d2fc-132">Provides Candidate information</span></span>

<span data-ttu-id="2d2fc-133">Вакансия</span><span class="sxs-lookup"><span data-stu-id="2d2fc-133">Job Opening</span></span>
-   <span data-ttu-id="2d2fc-134">Предоставляет идентификатор вакансии и участников на вакансию</span><span class="sxs-lookup"><span data-stu-id="2d2fc-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="2d2fc-135">Участники на вакансию</span><span class="sxs-lookup"><span data-stu-id="2d2fc-135">Job Opening Participants</span></span>
-   <span data-ttu-id="2d2fc-136">Представляет специалиста по комплектации штата</span><span class="sxs-lookup"><span data-stu-id="2d2fc-136">Provides Hiring Manager</span></span>

<span data-ttu-id="2d2fc-137">При добавлении кандидата в модуль "Управление персоналом" кандидата теперь также можно отклонить с помощью нового параметра, доступного на карточке кандидата.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2d2fc-138">Скоро</span><span class="sxs-lookup"><span data-stu-id="2d2fc-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="2d2fc-139">Отпуск и отсутствие: будущий отпуск и прогноз сальдо отпуска</span><span class="sxs-lookup"><span data-stu-id="2d2fc-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="2d2fc-140">С изменениями, вносимыми, чтобы сотрудники могли прогнозировать отгулы и подавать запросы на будущие отгулы, не влияя на текущее сальдо отгулов, также изменяется способ отображения сальдо отгулов.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="2d2fc-141">Отображаемое в настоящее время доступное сальдо — это время отгула, доступное для запроса, включая начисления за сегодняшний день и все утвержденные отпуска до конца времен.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="2d2fc-142">Когда возможность прогноза будет выпущена, отображаемое сальдо изменится на текущий баланс отгулов, включая начисления до сегодняшнего дня и запросы на сегодня.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="2d2fc-143">Сотрудники и менеджеры увидит эти обновленные сальдо в службе самообслуживания сотрудников и менеджера на карте **Отгулы** и в окне **Сальдо отгулов**.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="2d2fc-144">Менеджеры отдела кадров увидят эти обновленные сальдо в рабочей области **Люди** и в окне **Назначенные планы отпусков** сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="2d2fc-145">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="2d2fc-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance"></a><span data-ttu-id="2d2fc-146">Ошибки сопоставления в интеграции с Finance</span><span class="sxs-lookup"><span data-stu-id="2d2fc-146">Mapping errors in the integration with Finance</span></span>

<span data-ttu-id="2d2fc-147">Следующие проблемы были выявлены в текущем шаблоне для интеграции Talent с Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 Finance.</span></span> <span data-ttu-id="2d2fc-148">Новый шаблон будет опубликован в ближайшее время и будет применяться ко всем новым создаваемым проектам интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="2d2fc-149">Для существующих проектов интеграции сопоставления задач можно обновить.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="2d2fc-150">Обновленные сопоставления см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="2d2fc-151">Задача назначения должностей для родительских должностей не интегрирует данные.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="2d2fc-152">Это ошибка, которая в настоящее время исследуется.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="2d2fc-153">Не имеет временного решения в текущем сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="2d2fc-154">В задаче сопоставления отделов с операционными единицами должны быть обновлены следующие сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="2d2fc-155">Существующее поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-155">Existing source field</span></span>          | <span data-ttu-id="2d2fc-156">Новое поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="2d2fc-157">cdm_description (Описание)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-157">cdm_description (Description)</span></span>  | <span data-ttu-id="2d2fc-158">cdm_name (Имя)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="2d2fc-159">Также необходимо добавить дополнительные сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="2d2fc-160">Выберите последнее поле **Нет**, чтобы добавить следующее сопоставление.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="2d2fc-161">Поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-161">Source field</span></span>                   | <span data-ttu-id="2d2fc-162">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="2d2fc-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="2d2fc-163">cdm_description (Описание)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-163">cdm_description (Description)</span></span>  | <span data-ttu-id="2d2fc-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="2d2fc-165">Обновленные сопоставления должна выглядеть, как на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-165">The updated mappings should look like the following image.</span></span>

![Задача сопоставления подразделений с операционными единицами](./media/DepartmentMapping.png)


<span data-ttu-id="2d2fc-167">В задаче сопоставления должностей со сведения о должности должны быть обновлены следующие сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="2d2fc-168">Существующее поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-168">Existing source field</span></span>          | <span data-ttu-id="2d2fc-169">Новое поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="2d2fc-170">cdm_name (Имя)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-170">cdm_name (Name)</span></span>                | <span data-ttu-id="2d2fc-171">cdm_description (Описание)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="2d2fc-172">cdm_name (Описание)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-172">cdm_name (Description)</span></span>         | <span data-ttu-id="2d2fc-173">cdm_jobdescription(Описание должности)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="2d2fc-174">Обновленные сопоставления должна выглядеть, как на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-174">The updated mappings should look like the image below.</span></span>

![Задача сопоставления должностей со сведения о должности](./media/JobMapping.png)

<span data-ttu-id="2d2fc-176">В задаче сопоставления сотрудников с должностными обязанностями должны быть обновлены следующие сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="2d2fc-177">Существующее поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-177">Existing source field</span></span>                 | <span data-ttu-id="2d2fc-178">Новое поле источника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="2d2fc-179">cdm_emailaddress1 (Адрес электронной почты 1)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="2d2fc-180">cdm_primaryemailaddress (Основной адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="2d2fc-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="2d2fc-181">cdm_telephone1 (Телефон 1)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="2d2fc-182">cdm_primarytelephone (Основной телефон)</span><span class="sxs-lookup"><span data-stu-id="2d2fc-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="2d2fc-183">Также необходимо обновить преобразование поля "Пол".</span><span class="sxs-lookup"><span data-stu-id="2d2fc-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="2d2fc-184">Выберите тип сопоставления **fn** (функция) для поля "Пол" и обновите следующие сопоставления значений.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="2d2fc-185">Значение Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2d2fc-185">Common Data Service value</span></span>                   | <span data-ttu-id="2d2fc-186">Значение в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d2fc-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="2d2fc-187">75440000</span><span class="sxs-lookup"><span data-stu-id="2d2fc-187">75440000</span></span>                    | <span data-ttu-id="2d2fc-188">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="2d2fc-188">Male</span></span>                                             |
| <span data-ttu-id="2d2fc-189">75440001</span><span class="sxs-lookup"><span data-stu-id="2d2fc-189">75440001</span></span>                    | <span data-ttu-id="2d2fc-190">Женский</span><span class="sxs-lookup"><span data-stu-id="2d2fc-190">Female</span></span>                                           |
| <span data-ttu-id="2d2fc-191">75440002</span><span class="sxs-lookup"><span data-stu-id="2d2fc-191">75440002</span></span>                    | <span data-ttu-id="2d2fc-192">Не допускается</span><span class="sxs-lookup"><span data-stu-id="2d2fc-192">None</span></span>                                             | 
| <span data-ttu-id="2d2fc-193">75440003</span><span class="sxs-lookup"><span data-stu-id="2d2fc-193">75440003</span></span>                    | <span data-ttu-id="2d2fc-194">Не указан</span><span class="sxs-lookup"><span data-stu-id="2d2fc-194">NonSpecific</span></span>                                      |

<span data-ttu-id="2d2fc-195">Обновленные сопоставления должна выглядеть, как на следующих рисунках.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-195">The updated mappings should look like the following images.</span></span>

![Задача сопоставления работников с работником](./media/WorkerMapping.png)

![Преобразование поля "Пол"](./media/WorkerTransform.png)
