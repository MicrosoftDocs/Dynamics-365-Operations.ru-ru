---
title: Таблицы Dataverse
description: Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114038"
---
# <a name="dataverse-tables"></a><span data-ttu-id="d3f8b-103">Таблицы Dataverse</span><span class="sxs-lookup"><span data-stu-id="d3f8b-103">Dataverse tables</span></span>

<span data-ttu-id="d3f8b-104">Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.</span><span class="sxs-lookup"><span data-stu-id="d3f8b-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="d3f8b-105">Сущности Human Resources соответствуют таблицам Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3f8b-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="d3f8b-106">Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="d3f8b-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="d3f8b-107">Доступны следующие таблицы Dataverse на основе сущностей Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3f8b-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="d3f8b-108">Таблицы льгот</span><span class="sxs-lookup"><span data-stu-id="d3f8b-108">Benefit tables</span></span>

| <span data-ttu-id="d3f8b-109">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-109">Name</span></span> | <span data-ttu-id="d3f8b-110">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-111">Частота расчета льгот</span><span class="sxs-lookup"><span data-stu-id="d3f8b-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="d3f8b-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="d3f8b-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="d3f8b-113">Частоты расчета для платежного периода для льгот</span><span class="sxs-lookup"><span data-stu-id="d3f8b-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="d3f8b-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="d3f8b-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="d3f8b-115">Ставка расчета льгот</span><span class="sxs-lookup"><span data-stu-id="d3f8b-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="d3f8b-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="d3f8b-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="d3f8b-117">Сведения о ставке расчета льгот</span><span class="sxs-lookup"><span data-stu-id="d3f8b-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="d3f8b-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="d3f8b-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="d3f8b-119">Параметр льготы</span><span class="sxs-lookup"><span data-stu-id="d3f8b-119">Benefit Option</span></span> | <span data-ttu-id="d3f8b-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="d3f8b-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="d3f8b-121">План льготы</span><span class="sxs-lookup"><span data-stu-id="d3f8b-121">Benefit Plan</span></span> | <span data-ttu-id="d3f8b-122">cdm_benefitplan (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="d3f8b-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="d3f8b-123">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="d3f8b-123">Benefit Type</span></span> | <span data-ttu-id="d3f8b-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="d3f8b-125">Таблицы задач бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="d3f8b-125">Business process tasks tables</span></span>

| <span data-ttu-id="d3f8b-126">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-126">Name</span></span> | <span data-ttu-id="d3f8b-127">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-128">Календарь бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="d3f8b-128">Business Process Calendar</span></span> | <span data-ttu-id="d3f8b-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="d3f8b-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="d3f8b-130">Назначение группы бизнес-процессу</span><span class="sxs-lookup"><span data-stu-id="d3f8b-130">Business Process Group Assignment</span></span> | <span data-ttu-id="d3f8b-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="d3f8b-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="d3f8b-132">Группа задач библиотеки бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="d3f8b-132">Business Process Library Task Group</span></span> | <span data-ttu-id="d3f8b-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="d3f8b-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="d3f8b-134">Стадия бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="d3f8b-134">Business Process Stage</span></span> | <span data-ttu-id="d3f8b-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="d3f8b-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="d3f8b-136">Заголовок шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="d3f8b-136">Checklist Template Header</span></span> | <span data-ttu-id="d3f8b-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="d3f8b-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="d3f8b-138">Задача шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="d3f8b-138">Checklist Template Task</span></span> | <span data-ttu-id="d3f8b-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="d3f8b-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="d3f8b-140">Таблицы компенсаций</span><span class="sxs-lookup"><span data-stu-id="d3f8b-140">Compensation tables</span></span>

| <span data-ttu-id="d3f8b-141">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-141">Name</span></span> | <span data-ttu-id="d3f8b-142">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-143">Фиксированный план компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="d3f8b-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="d3f8b-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="d3f8b-145">Сетка компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-145">Compensation Grid</span></span> | <span data-ttu-id="d3f8b-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="d3f8b-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="d3f8b-147">Уровень компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-147">Compensation Level</span></span> | <span data-ttu-id="d3f8b-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="d3f8b-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="d3f8b-149">Частота компенсационных выплат</span><span class="sxs-lookup"><span data-stu-id="d3f8b-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="d3f8b-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="d3f8b-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="d3f8b-151">Настройка опорной точки компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="d3f8b-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="d3f8b-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="d3f8b-153">Линия настройки опорных точки компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="d3f8b-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="d3f8b-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="d3f8b-155">Регион компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-155">Compensation Region</span></span> | <span data-ttu-id="d3f8b-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="d3f8b-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="d3f8b-157">Структура компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-157">Compensation Structure</span></span> | <span data-ttu-id="d3f8b-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="d3f8b-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="d3f8b-159">План переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-159">Compensation Variable Plan</span></span> | <span data-ttu-id="d3f8b-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="d3f8b-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="d3f8b-161">Уровень плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="d3f8b-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="d3f8b-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="d3f8b-163">Тип плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="d3f8b-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="d3f8b-165">Мероприятие фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="d3f8b-165">Fixed Compensation Event</span></span> | <span data-ttu-id="d3f8b-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="d3f8b-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="d3f8b-167">Положение о передаче прав на льготы</span><span class="sxs-lookup"><span data-stu-id="d3f8b-167">Vesting Rule</span></span> | <span data-ttu-id="d3f8b-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="d3f8b-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="d3f8b-169">Фиксированная компенсация работника</span><span class="sxs-lookup"><span data-stu-id="d3f8b-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="d3f8b-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="d3f8b-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="d3f8b-171">Таблицы организаций</span><span class="sxs-lookup"><span data-stu-id="d3f8b-171">Organization tables</span></span>

| <span data-ttu-id="d3f8b-172">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-172">Name</span></span> | <span data-ttu-id="d3f8b-173">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-174">Отдел</span><span class="sxs-lookup"><span data-stu-id="d3f8b-174">Department</span></span> | <span data-ttu-id="d3f8b-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="d3f8b-175">cdm_department</span></span> |
| <span data-ttu-id="d3f8b-176">Занятость</span><span class="sxs-lookup"><span data-stu-id="d3f8b-176">Employment</span></span> | <span data-ttu-id="d3f8b-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="d3f8b-177">cdm_employment</span></span> |
| <span data-ttu-id="d3f8b-178">Организация</span><span class="sxs-lookup"><span data-stu-id="d3f8b-178">Company</span></span> | <span data-ttu-id="d3f8b-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="d3f8b-179">cdm_company</span></span> |
| <span data-ttu-id="d3f8b-180">Должность</span><span class="sxs-lookup"><span data-stu-id="d3f8b-180">Job</span></span> | <span data-ttu-id="d3f8b-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="d3f8b-181">cdm_job</span></span> |
| <span data-ttu-id="d3f8b-182">Функциональные обязанности</span><span class="sxs-lookup"><span data-stu-id="d3f8b-182">Job Function</span></span> | <span data-ttu-id="d3f8b-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="d3f8b-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="d3f8b-184">Должность</span><span class="sxs-lookup"><span data-stu-id="d3f8b-184">Job Position</span></span> | <span data-ttu-id="d3f8b-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="d3f8b-185">cdm_jobposition</span></span> |
| <span data-ttu-id="d3f8b-186">Тип позиции</span><span class="sxs-lookup"><span data-stu-id="d3f8b-186">Position Type</span></span> | <span data-ttu-id="d3f8b-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-187">cdm_positiontype</span></span> |
| <span data-ttu-id="d3f8b-188">Назначение работника на должность</span><span class="sxs-lookup"><span data-stu-id="d3f8b-188">Position Worker Assignment</span></span> | <span data-ttu-id="d3f8b-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="d3f8b-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="d3f8b-190">Аналитика должности</span><span class="sxs-lookup"><span data-stu-id="d3f8b-190">Job Position Dimension</span></span> | <span data-ttu-id="d3f8b-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="d3f8b-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="d3f8b-192">Тип вакансии</span><span class="sxs-lookup"><span data-stu-id="d3f8b-192">Job Type</span></span> | <span data-ttu-id="d3f8b-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-193">cdm_jobtype</span></span> |
| <span data-ttu-id="d3f8b-194">Язык</span><span class="sxs-lookup"><span data-stu-id="d3f8b-194">Language</span></span> | <span data-ttu-id="d3f8b-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="d3f8b-195">cdm_language</span></span> |
| <span data-ttu-id="d3f8b-196">Должность</span><span class="sxs-lookup"><span data-stu-id="d3f8b-196">Title</span></span> | <span data-ttu-id="d3f8b-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="d3f8b-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="d3f8b-198">Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3f8b-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="d3f8b-199">Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Dataverse в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3f8b-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="d3f8b-200">Таблицы отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="d3f8b-200">Leave and absence tables</span></span>

| <span data-ttu-id="d3f8b-201">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-201">Name</span></span> | <span data-ttu-id="d3f8b-202">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-203">Банковская проводка отпуска</span><span class="sxs-lookup"><span data-stu-id="d3f8b-203">Leave Bank Transaction</span></span> | <span data-ttu-id="d3f8b-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="d3f8b-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="d3f8b-205">Регистрация отпуска</span><span class="sxs-lookup"><span data-stu-id="d3f8b-205">Leave Enrollment</span></span> | <span data-ttu-id="d3f8b-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="d3f8b-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="d3f8b-207">План отпусков</span><span class="sxs-lookup"><span data-stu-id="d3f8b-207">Leave Plan</span></span> | <span data-ttu-id="d3f8b-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="d3f8b-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="d3f8b-209">Запрос на отпуск</span><span class="sxs-lookup"><span data-stu-id="d3f8b-209">Leave Request</span></span> | <span data-ttu-id="d3f8b-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="d3f8b-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="d3f8b-211">Сведения запроса отпуска</span><span class="sxs-lookup"><span data-stu-id="d3f8b-211">Leave Request Detail</span></span> | <span data-ttu-id="d3f8b-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="d3f8b-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="d3f8b-213">Тип отпуска</span><span class="sxs-lookup"><span data-stu-id="d3f8b-213">Leave Type</span></span> | <span data-ttu-id="d3f8b-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-214">cdm_leavetype</span></span> |
| <span data-ttu-id="d3f8b-215">Код основания типа отпуска</span><span class="sxs-lookup"><span data-stu-id="d3f8b-215">Leave Type Reason Code</span></span> | <span data-ttu-id="d3f8b-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="d3f8b-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="d3f8b-217">Таблицы зарплаты</span><span class="sxs-lookup"><span data-stu-id="d3f8b-217">Payroll tables</span></span>

| <span data-ttu-id="d3f8b-218">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-218">Name</span></span> | <span data-ttu-id="d3f8b-219">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-220">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="d3f8b-220">Pay Cycle</span></span> | <span data-ttu-id="d3f8b-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="d3f8b-221">cdm_paycycle</span></span> |
| <span data-ttu-id="d3f8b-222">Платежный период</span><span class="sxs-lookup"><span data-stu-id="d3f8b-222">Pay Period</span></span> | <span data-ttu-id="d3f8b-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="d3f8b-223">cdm_payperiod</span></span> |
| <span data-ttu-id="d3f8b-224">Код дохода по зарплате</span><span class="sxs-lookup"><span data-stu-id="d3f8b-224">Payroll Earning Code</span></span> | <span data-ttu-id="d3f8b-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="d3f8b-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="d3f8b-226">Выплаты по банковскому счету</span><span class="sxs-lookup"><span data-stu-id="d3f8b-226">Bank Account Disbursement</span></span> | <span data-ttu-id="d3f8b-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="d3f8b-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="d3f8b-228">Налоговый регион</span><span class="sxs-lookup"><span data-stu-id="d3f8b-228">Tax Region</span></span> | <span data-ttu-id="d3f8b-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="d3f8b-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="d3f8b-230">Таблицы работников</span><span class="sxs-lookup"><span data-stu-id="d3f8b-230">Worker tables</span></span>

| <span data-ttu-id="d3f8b-231">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-231">Name</span></span> | <span data-ttu-id="d3f8b-232">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-233">Рабочий</span><span class="sxs-lookup"><span data-stu-id="d3f8b-233">Worker</span></span> | <span data-ttu-id="d3f8b-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="d3f8b-234">cdm_worker</span></span> |
| <span data-ttu-id="d3f8b-235">Адрес работника</span><span class="sxs-lookup"><span data-stu-id="d3f8b-235">Worker Address</span></span> | <span data-ttu-id="d3f8b-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="d3f8b-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="d3f8b-237">Личные данные работника</span><span class="sxs-lookup"><span data-stu-id="d3f8b-237">Worker Personal Detail</span></span> | <span data-ttu-id="d3f8b-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="d3f8b-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="d3f8b-239">Идентификационный код работника</span><span class="sxs-lookup"><span data-stu-id="d3f8b-239">Worker Person Identification Number</span></span> | <span data-ttu-id="d3f8b-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="d3f8b-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="d3f8b-241">Идентификационный тип работника</span><span class="sxs-lookup"><span data-stu-id="d3f8b-241">Worker Person Identification Type</span></span> | <span data-ttu-id="d3f8b-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="d3f8b-243">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="d3f8b-243">Work Calendar</span></span> | <span data-ttu-id="d3f8b-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="d3f8b-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="d3f8b-245">Календарный день работы</span><span class="sxs-lookup"><span data-stu-id="d3f8b-245">Work Calendar Day</span></span> | <span data-ttu-id="d3f8b-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="d3f8b-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="d3f8b-247">Праздничный день в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="d3f8b-247">Work Calendar Holiday</span></span> |<span data-ttu-id="d3f8b-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="d3f8b-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="d3f8b-249">Строка праздничного дня в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="d3f8b-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="d3f8b-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="d3f8b-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="d3f8b-251">Интервал рабочего времени</span><span class="sxs-lookup"><span data-stu-id="d3f8b-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="d3f8b-252">cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="d3f8b-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="d3f8b-253">Банковский счет работника</span><span class="sxs-lookup"><span data-stu-id="d3f8b-253">Worker Bank Account</span></span> | <span data-ttu-id="d3f8b-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="d3f8b-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="d3f8b-255">Таблицы настройки работников</span><span class="sxs-lookup"><span data-stu-id="d3f8b-255">Worker setup tables</span></span>

| <span data-ttu-id="d3f8b-256">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-256">Name</span></span> | <span data-ttu-id="d3f8b-257">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-258">Статус ветерана</span><span class="sxs-lookup"><span data-stu-id="d3f8b-258">Veteran Status</span></span> | <span data-ttu-id="d3f8b-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="d3f8b-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="d3f8b-260">Этническое происхождение</span><span class="sxs-lookup"><span data-stu-id="d3f8b-260">Ethnic Origin</span></span> | <span data-ttu-id="d3f8b-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="d3f8b-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="d3f8b-262">Код основания</span><span class="sxs-lookup"><span data-stu-id="d3f8b-262">Reason Code</span></span> | <span data-ttu-id="d3f8b-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="d3f8b-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="d3f8b-264">Агентство, выпускающее средства идентификации пользователей</span><span class="sxs-lookup"><span data-stu-id="d3f8b-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="d3f8b-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="d3f8b-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="d3f8b-266">Таблицы компетенции</span><span class="sxs-lookup"><span data-stu-id="d3f8b-266">Competency tables</span></span>

| <span data-ttu-id="d3f8b-267">ФИО</span><span class="sxs-lookup"><span data-stu-id="d3f8b-267">Name</span></span> | <span data-ttu-id="d3f8b-268">Таблица</span><span class="sxs-lookup"><span data-stu-id="d3f8b-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="d3f8b-269">Тип навыка</span><span class="sxs-lookup"><span data-stu-id="d3f8b-269">Skill Type</span></span> | <span data-ttu-id="d3f8b-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="d3f8b-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="d3f8b-271">Модели связи таблиц</span><span class="sxs-lookup"><span data-stu-id="d3f8b-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="d3f8b-272">Рабочий</span><span class="sxs-lookup"><span data-stu-id="d3f8b-272">Worker</span></span>

![Рабочий](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="d3f8b-274">Работа и должность</span><span class="sxs-lookup"><span data-stu-id="d3f8b-274">Job and Job Position</span></span>

![Работа и должность](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="d3f8b-276">Льготы</span><span class="sxs-lookup"><span data-stu-id="d3f8b-276">Benefits</span></span>

![Льготы](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="d3f8b-278">Компенсация</span><span class="sxs-lookup"><span data-stu-id="d3f8b-278">Compensation</span></span>

![Компенсация](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="d3f8b-280">Отпуск</span><span class="sxs-lookup"><span data-stu-id="d3f8b-280">Leave</span></span>

![Отпуск](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="d3f8b-282">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="d3f8b-282">Work Calendar</span></span>

![Рабочий календарь](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="d3f8b-284">См. также</span><span class="sxs-lookup"><span data-stu-id="d3f8b-284">See also</span></span>

[<span data-ttu-id="d3f8b-285">Выбор технологии интеграции данных</span><span class="sxs-lookup"><span data-stu-id="d3f8b-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="d3f8b-286">Настройка интеграции Dataverse</span><span class="sxs-lookup"><span data-stu-id="d3f8b-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="d3f8b-287">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="d3f8b-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="d3f8b-288">Вопросы и ответы по виртуальным таблицам Human Resources</span><span class="sxs-lookup"><span data-stu-id="d3f8b-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="d3f8b-289">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="d3f8b-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="d3f8b-290">Обновления терминологии</span><span class="sxs-lookup"><span data-stu-id="d3f8b-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
