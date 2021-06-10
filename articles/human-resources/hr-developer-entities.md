---
title: Таблицы Dataverse
description: Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054364"
---
# <a name="dataverse-tables"></a><span data-ttu-id="0c876-103">Таблицы Dataverse</span><span class="sxs-lookup"><span data-stu-id="0c876-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0c876-104">Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.</span><span class="sxs-lookup"><span data-stu-id="0c876-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="0c876-105">Сущности Human Resources соответствуют таблицам Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0c876-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="0c876-106">Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="0c876-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="0c876-107">Доступны следующие таблицы Dataverse на основе сущностей Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c876-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="0c876-108">Таблицы льгот</span><span class="sxs-lookup"><span data-stu-id="0c876-108">Benefit tables</span></span>

| <span data-ttu-id="0c876-109">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-109">Name</span></span> | <span data-ttu-id="0c876-110">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-111">Частота расчета льгот</span><span class="sxs-lookup"><span data-stu-id="0c876-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="0c876-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="0c876-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="0c876-113">Частоты расчета для платежного периода для льгот</span><span class="sxs-lookup"><span data-stu-id="0c876-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="0c876-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="0c876-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="0c876-115">Ставка расчета льгот</span><span class="sxs-lookup"><span data-stu-id="0c876-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="0c876-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="0c876-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="0c876-117">Сведения о ставке расчета льгот</span><span class="sxs-lookup"><span data-stu-id="0c876-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="0c876-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="0c876-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="0c876-119">Параметр льготы</span><span class="sxs-lookup"><span data-stu-id="0c876-119">Benefit Option</span></span> | <span data-ttu-id="0c876-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="0c876-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="0c876-121">План льготы</span><span class="sxs-lookup"><span data-stu-id="0c876-121">Benefit Plan</span></span> | <span data-ttu-id="0c876-122">cdm_benefitplan (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="0c876-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="0c876-123">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="0c876-123">Benefit Type</span></span> | <span data-ttu-id="0c876-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="0c876-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="0c876-125">Таблицы задач бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="0c876-125">Business process tasks tables</span></span>

| <span data-ttu-id="0c876-126">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-126">Name</span></span> | <span data-ttu-id="0c876-127">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-128">Календарь бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="0c876-128">Business Process Calendar</span></span> | <span data-ttu-id="0c876-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="0c876-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="0c876-130">Назначение группы бизнес-процессу</span><span class="sxs-lookup"><span data-stu-id="0c876-130">Business Process Group Assignment</span></span> | <span data-ttu-id="0c876-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="0c876-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="0c876-132">Группа задач библиотеки бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="0c876-132">Business Process Library Task Group</span></span> | <span data-ttu-id="0c876-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="0c876-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="0c876-134">Стадия бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="0c876-134">Business Process Stage</span></span> | <span data-ttu-id="0c876-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="0c876-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="0c876-136">Заголовок шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="0c876-136">Checklist Template Header</span></span> | <span data-ttu-id="0c876-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="0c876-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="0c876-138">Задача шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="0c876-138">Checklist Template Task</span></span> | <span data-ttu-id="0c876-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="0c876-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="0c876-140">Таблицы компенсаций</span><span class="sxs-lookup"><span data-stu-id="0c876-140">Compensation tables</span></span>

| <span data-ttu-id="0c876-141">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-141">Name</span></span> | <span data-ttu-id="0c876-142">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-143">Фиксированный план компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="0c876-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="0c876-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="0c876-145">Сетка компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-145">Compensation Grid</span></span> | <span data-ttu-id="0c876-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="0c876-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="0c876-147">Уровень компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-147">Compensation Level</span></span> | <span data-ttu-id="0c876-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="0c876-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="0c876-149">Частота компенсационных выплат</span><span class="sxs-lookup"><span data-stu-id="0c876-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="0c876-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="0c876-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="0c876-151">Настройка опорной точки компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="0c876-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="0c876-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="0c876-153">Линия настройки опорных точки компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="0c876-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="0c876-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="0c876-155">Регион компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-155">Compensation Region</span></span> | <span data-ttu-id="0c876-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="0c876-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="0c876-157">Структура компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-157">Compensation Structure</span></span> | <span data-ttu-id="0c876-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="0c876-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="0c876-159">План переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-159">Compensation Variable Plan</span></span> | <span data-ttu-id="0c876-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="0c876-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="0c876-161">Уровень плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="0c876-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="0c876-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="0c876-163">Тип плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="0c876-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="0c876-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="0c876-165">Мероприятие фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="0c876-165">Fixed Compensation Event</span></span> | <span data-ttu-id="0c876-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="0c876-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="0c876-167">Положение о передаче прав на льготы</span><span class="sxs-lookup"><span data-stu-id="0c876-167">Vesting Rule</span></span> | <span data-ttu-id="0c876-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="0c876-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="0c876-169">Фиксированная компенсация работника</span><span class="sxs-lookup"><span data-stu-id="0c876-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="0c876-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="0c876-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="0c876-171">Таблицы организаций</span><span class="sxs-lookup"><span data-stu-id="0c876-171">Organization tables</span></span>

| <span data-ttu-id="0c876-172">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-172">Name</span></span> | <span data-ttu-id="0c876-173">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-174">Отдел</span><span class="sxs-lookup"><span data-stu-id="0c876-174">Department</span></span> | <span data-ttu-id="0c876-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="0c876-175">cdm_department</span></span> |
| <span data-ttu-id="0c876-176">Занятость</span><span class="sxs-lookup"><span data-stu-id="0c876-176">Employment</span></span> | <span data-ttu-id="0c876-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="0c876-177">cdm_employment</span></span> |
| <span data-ttu-id="0c876-178">Организация</span><span class="sxs-lookup"><span data-stu-id="0c876-178">Company</span></span> | <span data-ttu-id="0c876-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="0c876-179">cdm_company</span></span> |
| <span data-ttu-id="0c876-180">Должность</span><span class="sxs-lookup"><span data-stu-id="0c876-180">Job</span></span> | <span data-ttu-id="0c876-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="0c876-181">cdm_job</span></span> |
| <span data-ttu-id="0c876-182">Функциональные обязанности</span><span class="sxs-lookup"><span data-stu-id="0c876-182">Job Function</span></span> | <span data-ttu-id="0c876-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="0c876-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="0c876-184">Должность</span><span class="sxs-lookup"><span data-stu-id="0c876-184">Job Position</span></span> | <span data-ttu-id="0c876-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="0c876-185">cdm_jobposition</span></span> |
| <span data-ttu-id="0c876-186">Тип позиции</span><span class="sxs-lookup"><span data-stu-id="0c876-186">Position Type</span></span> | <span data-ttu-id="0c876-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="0c876-187">cdm_positiontype</span></span> |
| <span data-ttu-id="0c876-188">Назначение работника на должность</span><span class="sxs-lookup"><span data-stu-id="0c876-188">Position Worker Assignment</span></span> | <span data-ttu-id="0c876-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="0c876-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="0c876-190">Аналитика должности</span><span class="sxs-lookup"><span data-stu-id="0c876-190">Job Position Dimension</span></span> | <span data-ttu-id="0c876-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="0c876-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="0c876-192">Тип вакансии</span><span class="sxs-lookup"><span data-stu-id="0c876-192">Job Type</span></span> | <span data-ttu-id="0c876-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="0c876-193">cdm_jobtype</span></span> |
| <span data-ttu-id="0c876-194">Язык</span><span class="sxs-lookup"><span data-stu-id="0c876-194">Language</span></span> | <span data-ttu-id="0c876-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="0c876-195">cdm_language</span></span> |
| <span data-ttu-id="0c876-196">Должность</span><span class="sxs-lookup"><span data-stu-id="0c876-196">Title</span></span> | <span data-ttu-id="0c876-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="0c876-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="0c876-198">Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0c876-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="0c876-199">Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Dataverse в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0c876-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="0c876-200">Таблицы отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="0c876-200">Leave and absence tables</span></span>

| <span data-ttu-id="0c876-201">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-201">Name</span></span> | <span data-ttu-id="0c876-202">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-203">Банковская проводка отпуска</span><span class="sxs-lookup"><span data-stu-id="0c876-203">Leave Bank Transaction</span></span> | <span data-ttu-id="0c876-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="0c876-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="0c876-205">Регистрация отпуска</span><span class="sxs-lookup"><span data-stu-id="0c876-205">Leave Enrollment</span></span> | <span data-ttu-id="0c876-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="0c876-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="0c876-207">План отпусков</span><span class="sxs-lookup"><span data-stu-id="0c876-207">Leave Plan</span></span> | <span data-ttu-id="0c876-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="0c876-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="0c876-209">Запрос на отпуск</span><span class="sxs-lookup"><span data-stu-id="0c876-209">Leave Request</span></span> | <span data-ttu-id="0c876-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="0c876-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="0c876-211">Сведения запроса отпуска</span><span class="sxs-lookup"><span data-stu-id="0c876-211">Leave Request Detail</span></span> | <span data-ttu-id="0c876-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="0c876-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="0c876-213">Тип отпуска</span><span class="sxs-lookup"><span data-stu-id="0c876-213">Leave Type</span></span> | <span data-ttu-id="0c876-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="0c876-214">cdm_leavetype</span></span> |
| <span data-ttu-id="0c876-215">Код основания типа отпуска</span><span class="sxs-lookup"><span data-stu-id="0c876-215">Leave Type Reason Code</span></span> | <span data-ttu-id="0c876-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="0c876-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="0c876-217">Таблицы зарплаты</span><span class="sxs-lookup"><span data-stu-id="0c876-217">Payroll tables</span></span>

| <span data-ttu-id="0c876-218">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-218">Name</span></span> | <span data-ttu-id="0c876-219">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-220">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="0c876-220">Pay Cycle</span></span> | <span data-ttu-id="0c876-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="0c876-221">cdm_paycycle</span></span> |
| <span data-ttu-id="0c876-222">Платежный период</span><span class="sxs-lookup"><span data-stu-id="0c876-222">Pay Period</span></span> | <span data-ttu-id="0c876-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="0c876-223">cdm_payperiod</span></span> |
| <span data-ttu-id="0c876-224">Код дохода по зарплате</span><span class="sxs-lookup"><span data-stu-id="0c876-224">Payroll Earning Code</span></span> | <span data-ttu-id="0c876-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="0c876-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="0c876-226">Выплаты по банковскому счету</span><span class="sxs-lookup"><span data-stu-id="0c876-226">Bank Account Disbursement</span></span> | <span data-ttu-id="0c876-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="0c876-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="0c876-228">Налоговый регион</span><span class="sxs-lookup"><span data-stu-id="0c876-228">Tax Region</span></span> | <span data-ttu-id="0c876-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="0c876-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="0c876-230">Таблицы работников</span><span class="sxs-lookup"><span data-stu-id="0c876-230">Worker tables</span></span>

| <span data-ttu-id="0c876-231">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-231">Name</span></span> | <span data-ttu-id="0c876-232">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-233">Рабочий</span><span class="sxs-lookup"><span data-stu-id="0c876-233">Worker</span></span> | <span data-ttu-id="0c876-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="0c876-234">cdm_worker</span></span> |
| <span data-ttu-id="0c876-235">Адрес работника</span><span class="sxs-lookup"><span data-stu-id="0c876-235">Worker Address</span></span> | <span data-ttu-id="0c876-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="0c876-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="0c876-237">Личные данные работника</span><span class="sxs-lookup"><span data-stu-id="0c876-237">Worker Personal Detail</span></span> | <span data-ttu-id="0c876-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="0c876-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="0c876-239">Идентификационный код работника</span><span class="sxs-lookup"><span data-stu-id="0c876-239">Worker Person Identification Number</span></span> | <span data-ttu-id="0c876-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="0c876-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="0c876-241">Идентификационный тип работника</span><span class="sxs-lookup"><span data-stu-id="0c876-241">Worker Person Identification Type</span></span> | <span data-ttu-id="0c876-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="0c876-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="0c876-243">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="0c876-243">Work Calendar</span></span> | <span data-ttu-id="0c876-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="0c876-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="0c876-245">Календарный день работы</span><span class="sxs-lookup"><span data-stu-id="0c876-245">Work Calendar Day</span></span> | <span data-ttu-id="0c876-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="0c876-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="0c876-247">Праздничный день в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="0c876-247">Work Calendar Holiday</span></span> |<span data-ttu-id="0c876-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="0c876-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="0c876-249">Строка праздничного дня в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="0c876-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="0c876-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="0c876-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="0c876-251">Интервал рабочего времени</span><span class="sxs-lookup"><span data-stu-id="0c876-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="0c876-252">cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="0c876-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="0c876-253">Банковский счет работника</span><span class="sxs-lookup"><span data-stu-id="0c876-253">Worker Bank Account</span></span> | <span data-ttu-id="0c876-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="0c876-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="0c876-255">Таблицы настройки работников</span><span class="sxs-lookup"><span data-stu-id="0c876-255">Worker setup tables</span></span>

| <span data-ttu-id="0c876-256">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-256">Name</span></span> | <span data-ttu-id="0c876-257">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-258">Статус ветерана</span><span class="sxs-lookup"><span data-stu-id="0c876-258">Veteran Status</span></span> | <span data-ttu-id="0c876-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="0c876-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="0c876-260">Этническое происхождение</span><span class="sxs-lookup"><span data-stu-id="0c876-260">Ethnic Origin</span></span> | <span data-ttu-id="0c876-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="0c876-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="0c876-262">Код основания</span><span class="sxs-lookup"><span data-stu-id="0c876-262">Reason Code</span></span> | <span data-ttu-id="0c876-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="0c876-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="0c876-264">Агентство, выпускающее средства идентификации пользователей</span><span class="sxs-lookup"><span data-stu-id="0c876-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="0c876-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="0c876-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="0c876-266">Таблицы компетенции</span><span class="sxs-lookup"><span data-stu-id="0c876-266">Competency tables</span></span>

| <span data-ttu-id="0c876-267">ФИО</span><span class="sxs-lookup"><span data-stu-id="0c876-267">Name</span></span> | <span data-ttu-id="0c876-268">Таблица</span><span class="sxs-lookup"><span data-stu-id="0c876-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="0c876-269">Тип навыка</span><span class="sxs-lookup"><span data-stu-id="0c876-269">Skill Type</span></span> | <span data-ttu-id="0c876-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="0c876-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="0c876-271">Модели связи таблиц</span><span class="sxs-lookup"><span data-stu-id="0c876-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="0c876-272">Рабочий</span><span class="sxs-lookup"><span data-stu-id="0c876-272">Worker</span></span>

![Рабочий](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="0c876-274">Работа и должность</span><span class="sxs-lookup"><span data-stu-id="0c876-274">Job and Job Position</span></span>

![Работа и должность](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="0c876-276">Льготы</span><span class="sxs-lookup"><span data-stu-id="0c876-276">Benefits</span></span>

![Льготы](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="0c876-278">Компенсация</span><span class="sxs-lookup"><span data-stu-id="0c876-278">Compensation</span></span>

![Компенсация](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="0c876-280">Отпуск</span><span class="sxs-lookup"><span data-stu-id="0c876-280">Leave</span></span>

![Отпуск](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="0c876-282">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="0c876-282">Work Calendar</span></span>

![Рабочий календарь](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="0c876-284">См. также</span><span class="sxs-lookup"><span data-stu-id="0c876-284">See also</span></span>

[<span data-ttu-id="0c876-285">Выбор технологии интеграции данных</span><span class="sxs-lookup"><span data-stu-id="0c876-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="0c876-286">Настройка интеграции Dataverse</span><span class="sxs-lookup"><span data-stu-id="0c876-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="0c876-287">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="0c876-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="0c876-288">Вопросы и ответы по виртуальным таблицам Human Resources</span><span class="sxs-lookup"><span data-stu-id="0c876-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="0c876-289">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="0c876-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="0c876-290">Обновления терминологии</span><span class="sxs-lookup"><span data-stu-id="0c876-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]