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
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465230"
---
# <a name="dataverse-tables"></a><span data-ttu-id="19d50-103">Таблицы Dataverse</span><span class="sxs-lookup"><span data-stu-id="19d50-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="19d50-104">Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.</span><span class="sxs-lookup"><span data-stu-id="19d50-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="19d50-105">Сущности Human Resources соответствуют таблицам Dataverse.</span><span class="sxs-lookup"><span data-stu-id="19d50-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="19d50-106">Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="19d50-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="19d50-107">Доступны следующие таблицы Dataverse на основе сущностей Human Resources.</span><span class="sxs-lookup"><span data-stu-id="19d50-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="19d50-108">Таблицы льгот</span><span class="sxs-lookup"><span data-stu-id="19d50-108">Benefit tables</span></span>

| <span data-ttu-id="19d50-109">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-109">Name</span></span> | <span data-ttu-id="19d50-110">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-111">Частота расчета льгот</span><span class="sxs-lookup"><span data-stu-id="19d50-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="19d50-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="19d50-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="19d50-113">Частоты расчета для платежного периода для льгот</span><span class="sxs-lookup"><span data-stu-id="19d50-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="19d50-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="19d50-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="19d50-115">Ставка расчета льгот</span><span class="sxs-lookup"><span data-stu-id="19d50-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="19d50-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="19d50-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="19d50-117">Сведения о ставке расчета льгот</span><span class="sxs-lookup"><span data-stu-id="19d50-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="19d50-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="19d50-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="19d50-119">Параметр льготы</span><span class="sxs-lookup"><span data-stu-id="19d50-119">Benefit Option</span></span> | <span data-ttu-id="19d50-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="19d50-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="19d50-121">План льготы</span><span class="sxs-lookup"><span data-stu-id="19d50-121">Benefit Plan</span></span> | <span data-ttu-id="19d50-122">cdm_benefitplan (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="19d50-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="19d50-123">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="19d50-123">Benefit Type</span></span> | <span data-ttu-id="19d50-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="19d50-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="19d50-125">Таблицы задач бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="19d50-125">Business process tasks tables</span></span>

| <span data-ttu-id="19d50-126">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-126">Name</span></span> | <span data-ttu-id="19d50-127">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-128">Календарь бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="19d50-128">Business Process Calendar</span></span> | <span data-ttu-id="19d50-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="19d50-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="19d50-130">Назначение группы бизнес-процессу</span><span class="sxs-lookup"><span data-stu-id="19d50-130">Business Process Group Assignment</span></span> | <span data-ttu-id="19d50-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="19d50-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="19d50-132">Группа задач библиотеки бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="19d50-132">Business Process Library Task Group</span></span> | <span data-ttu-id="19d50-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="19d50-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="19d50-134">Стадия бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="19d50-134">Business Process Stage</span></span> | <span data-ttu-id="19d50-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="19d50-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="19d50-136">Заголовок шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="19d50-136">Checklist Template Header</span></span> | <span data-ttu-id="19d50-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="19d50-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="19d50-138">Задача шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="19d50-138">Checklist Template Task</span></span> | <span data-ttu-id="19d50-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="19d50-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="19d50-140">Таблицы компенсаций</span><span class="sxs-lookup"><span data-stu-id="19d50-140">Compensation tables</span></span>

| <span data-ttu-id="19d50-141">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-141">Name</span></span> | <span data-ttu-id="19d50-142">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-143">Фиксированный план компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="19d50-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="19d50-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="19d50-145">Сетка компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-145">Compensation Grid</span></span> | <span data-ttu-id="19d50-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="19d50-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="19d50-147">Уровень компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-147">Compensation Level</span></span> | <span data-ttu-id="19d50-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="19d50-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="19d50-149">Частота компенсационных выплат</span><span class="sxs-lookup"><span data-stu-id="19d50-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="19d50-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="19d50-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="19d50-151">Настройка опорной точки компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="19d50-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="19d50-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="19d50-153">Линия настройки опорных точки компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="19d50-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="19d50-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="19d50-155">Регион компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-155">Compensation Region</span></span> | <span data-ttu-id="19d50-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="19d50-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="19d50-157">Структура компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-157">Compensation Structure</span></span> | <span data-ttu-id="19d50-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="19d50-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="19d50-159">План переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-159">Compensation Variable Plan</span></span> | <span data-ttu-id="19d50-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="19d50-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="19d50-161">Уровень плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="19d50-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="19d50-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="19d50-163">Тип плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="19d50-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="19d50-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="19d50-165">Мероприятие фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="19d50-165">Fixed Compensation Event</span></span> | <span data-ttu-id="19d50-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="19d50-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="19d50-167">Положение о передаче прав на льготы</span><span class="sxs-lookup"><span data-stu-id="19d50-167">Vesting Rule</span></span> | <span data-ttu-id="19d50-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="19d50-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="19d50-169">Фиксированная компенсация работника</span><span class="sxs-lookup"><span data-stu-id="19d50-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="19d50-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="19d50-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="19d50-171">Таблицы организаций</span><span class="sxs-lookup"><span data-stu-id="19d50-171">Organization tables</span></span>

| <span data-ttu-id="19d50-172">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-172">Name</span></span> | <span data-ttu-id="19d50-173">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-174">Отдел</span><span class="sxs-lookup"><span data-stu-id="19d50-174">Department</span></span> | <span data-ttu-id="19d50-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="19d50-175">cdm_department</span></span> |
| <span data-ttu-id="19d50-176">Занятость</span><span class="sxs-lookup"><span data-stu-id="19d50-176">Employment</span></span> | <span data-ttu-id="19d50-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="19d50-177">cdm_employment</span></span> |
| <span data-ttu-id="19d50-178">Организация</span><span class="sxs-lookup"><span data-stu-id="19d50-178">Company</span></span> | <span data-ttu-id="19d50-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="19d50-179">cdm_company</span></span> |
| <span data-ttu-id="19d50-180">Должность</span><span class="sxs-lookup"><span data-stu-id="19d50-180">Job</span></span> | <span data-ttu-id="19d50-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="19d50-181">cdm_job</span></span> |
| <span data-ttu-id="19d50-182">Функциональные обязанности</span><span class="sxs-lookup"><span data-stu-id="19d50-182">Job Function</span></span> | <span data-ttu-id="19d50-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="19d50-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="19d50-184">Должность</span><span class="sxs-lookup"><span data-stu-id="19d50-184">Job Position</span></span> | <span data-ttu-id="19d50-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="19d50-185">cdm_jobposition</span></span> |
| <span data-ttu-id="19d50-186">Тип позиции</span><span class="sxs-lookup"><span data-stu-id="19d50-186">Position Type</span></span> | <span data-ttu-id="19d50-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="19d50-187">cdm_positiontype</span></span> |
| <span data-ttu-id="19d50-188">Назначение работника на должность</span><span class="sxs-lookup"><span data-stu-id="19d50-188">Position Worker Assignment</span></span> | <span data-ttu-id="19d50-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="19d50-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="19d50-190">Аналитика должности</span><span class="sxs-lookup"><span data-stu-id="19d50-190">Job Position Dimension</span></span> | <span data-ttu-id="19d50-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="19d50-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="19d50-192">Тип вакансии</span><span class="sxs-lookup"><span data-stu-id="19d50-192">Job Type</span></span> | <span data-ttu-id="19d50-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="19d50-193">cdm_jobtype</span></span> |
| <span data-ttu-id="19d50-194">Язык</span><span class="sxs-lookup"><span data-stu-id="19d50-194">Language</span></span> | <span data-ttu-id="19d50-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="19d50-195">cdm_language</span></span> |
| <span data-ttu-id="19d50-196">Должность</span><span class="sxs-lookup"><span data-stu-id="19d50-196">Title</span></span> | <span data-ttu-id="19d50-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="19d50-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="19d50-198">Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Dataverse.</span><span class="sxs-lookup"><span data-stu-id="19d50-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="19d50-199">Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Dataverse в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="19d50-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="19d50-200">Таблицы отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="19d50-200">Leave and absence tables</span></span>

| <span data-ttu-id="19d50-201">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-201">Name</span></span> | <span data-ttu-id="19d50-202">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-203">Банковская проводка отпуска</span><span class="sxs-lookup"><span data-stu-id="19d50-203">Leave Bank Transaction</span></span> | <span data-ttu-id="19d50-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="19d50-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="19d50-205">Регистрация отпуска</span><span class="sxs-lookup"><span data-stu-id="19d50-205">Leave Enrollment</span></span> | <span data-ttu-id="19d50-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="19d50-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="19d50-207">План отпусков</span><span class="sxs-lookup"><span data-stu-id="19d50-207">Leave Plan</span></span> | <span data-ttu-id="19d50-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="19d50-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="19d50-209">Запрос на отпуск</span><span class="sxs-lookup"><span data-stu-id="19d50-209">Leave Request</span></span> | <span data-ttu-id="19d50-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="19d50-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="19d50-211">Сведения запроса отпуска</span><span class="sxs-lookup"><span data-stu-id="19d50-211">Leave Request Detail</span></span> | <span data-ttu-id="19d50-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="19d50-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="19d50-213">Тип отпуска</span><span class="sxs-lookup"><span data-stu-id="19d50-213">Leave Type</span></span> | <span data-ttu-id="19d50-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="19d50-214">cdm_leavetype</span></span> |
| <span data-ttu-id="19d50-215">Код основания типа отпуска</span><span class="sxs-lookup"><span data-stu-id="19d50-215">Leave Type Reason Code</span></span> | <span data-ttu-id="19d50-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="19d50-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="19d50-217">Таблицы зарплаты</span><span class="sxs-lookup"><span data-stu-id="19d50-217">Payroll tables</span></span>

| <span data-ttu-id="19d50-218">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-218">Name</span></span> | <span data-ttu-id="19d50-219">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-220">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="19d50-220">Pay Cycle</span></span> | <span data-ttu-id="19d50-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="19d50-221">cdm_paycycle</span></span> |
| <span data-ttu-id="19d50-222">Платежный период</span><span class="sxs-lookup"><span data-stu-id="19d50-222">Pay Period</span></span> | <span data-ttu-id="19d50-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="19d50-223">cdm_payperiod</span></span> |
| <span data-ttu-id="19d50-224">Код дохода по зарплате</span><span class="sxs-lookup"><span data-stu-id="19d50-224">Payroll Earning Code</span></span> | <span data-ttu-id="19d50-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="19d50-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="19d50-226">Выплаты по банковскому счету</span><span class="sxs-lookup"><span data-stu-id="19d50-226">Bank Account Disbursement</span></span> | <span data-ttu-id="19d50-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="19d50-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="19d50-228">Налоговый регион</span><span class="sxs-lookup"><span data-stu-id="19d50-228">Tax Region</span></span> | <span data-ttu-id="19d50-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="19d50-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="19d50-230">Таблицы работников</span><span class="sxs-lookup"><span data-stu-id="19d50-230">Worker tables</span></span>

| <span data-ttu-id="19d50-231">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-231">Name</span></span> | <span data-ttu-id="19d50-232">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-233">Рабочий</span><span class="sxs-lookup"><span data-stu-id="19d50-233">Worker</span></span> | <span data-ttu-id="19d50-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="19d50-234">cdm_worker</span></span> |
| <span data-ttu-id="19d50-235">Адрес работника</span><span class="sxs-lookup"><span data-stu-id="19d50-235">Worker Address</span></span> | <span data-ttu-id="19d50-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="19d50-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="19d50-237">Личные данные работника</span><span class="sxs-lookup"><span data-stu-id="19d50-237">Worker Personal Detail</span></span> | <span data-ttu-id="19d50-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="19d50-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="19d50-239">Идентификационный код работника</span><span class="sxs-lookup"><span data-stu-id="19d50-239">Worker Person Identification Number</span></span> | <span data-ttu-id="19d50-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="19d50-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="19d50-241">Идентификационный тип работника</span><span class="sxs-lookup"><span data-stu-id="19d50-241">Worker Person Identification Type</span></span> | <span data-ttu-id="19d50-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="19d50-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="19d50-243">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="19d50-243">Work Calendar</span></span> | <span data-ttu-id="19d50-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="19d50-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="19d50-245">Календарный день работы</span><span class="sxs-lookup"><span data-stu-id="19d50-245">Work Calendar Day</span></span> | <span data-ttu-id="19d50-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="19d50-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="19d50-247">Праздничный день в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="19d50-247">Work Calendar Holiday</span></span> |<span data-ttu-id="19d50-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="19d50-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="19d50-249">Строка праздничного дня в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="19d50-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="19d50-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="19d50-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="19d50-251">Интервал рабочего времени</span><span class="sxs-lookup"><span data-stu-id="19d50-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="19d50-252">cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="19d50-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="19d50-253">Банковский счет работника</span><span class="sxs-lookup"><span data-stu-id="19d50-253">Worker Bank Account</span></span> | <span data-ttu-id="19d50-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="19d50-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="19d50-255">Таблицы настройки работников</span><span class="sxs-lookup"><span data-stu-id="19d50-255">Worker setup tables</span></span>

| <span data-ttu-id="19d50-256">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-256">Name</span></span> | <span data-ttu-id="19d50-257">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-258">Статус ветерана</span><span class="sxs-lookup"><span data-stu-id="19d50-258">Veteran Status</span></span> | <span data-ttu-id="19d50-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="19d50-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="19d50-260">Этническое происхождение</span><span class="sxs-lookup"><span data-stu-id="19d50-260">Ethnic Origin</span></span> | <span data-ttu-id="19d50-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="19d50-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="19d50-262">Код основания</span><span class="sxs-lookup"><span data-stu-id="19d50-262">Reason Code</span></span> | <span data-ttu-id="19d50-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="19d50-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="19d50-264">Агентство, выпускающее средства идентификации пользователей</span><span class="sxs-lookup"><span data-stu-id="19d50-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="19d50-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="19d50-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="19d50-266">Таблицы компетенции</span><span class="sxs-lookup"><span data-stu-id="19d50-266">Competency tables</span></span>

| <span data-ttu-id="19d50-267">ФИО</span><span class="sxs-lookup"><span data-stu-id="19d50-267">Name</span></span> | <span data-ttu-id="19d50-268">Таблица</span><span class="sxs-lookup"><span data-stu-id="19d50-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="19d50-269">Тип навыка</span><span class="sxs-lookup"><span data-stu-id="19d50-269">Skill Type</span></span> | <span data-ttu-id="19d50-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="19d50-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="19d50-271">Модели связи таблиц</span><span class="sxs-lookup"><span data-stu-id="19d50-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="19d50-272">Рабочий</span><span class="sxs-lookup"><span data-stu-id="19d50-272">Worker</span></span>

![Рабочий](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="19d50-274">Работа и должность</span><span class="sxs-lookup"><span data-stu-id="19d50-274">Job and Job Position</span></span>

![Работа и должность](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="19d50-276">Льготы</span><span class="sxs-lookup"><span data-stu-id="19d50-276">Benefits</span></span>

![Льготы](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="19d50-278">Компенсация</span><span class="sxs-lookup"><span data-stu-id="19d50-278">Compensation</span></span>

![Компенсация](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="19d50-280">Отпуск</span><span class="sxs-lookup"><span data-stu-id="19d50-280">Leave</span></span>

![Отпуск](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="19d50-282">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="19d50-282">Work Calendar</span></span>

![Рабочий календарь](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="19d50-284">См. также</span><span class="sxs-lookup"><span data-stu-id="19d50-284">See also</span></span>

[<span data-ttu-id="19d50-285">Выбор технологии интеграции данных</span><span class="sxs-lookup"><span data-stu-id="19d50-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="19d50-286">Настройка интеграции Dataverse</span><span class="sxs-lookup"><span data-stu-id="19d50-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="19d50-287">Настройка виртуальных таблиц Dataverse</span><span class="sxs-lookup"><span data-stu-id="19d50-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="19d50-288">Вопросы и ответы по виртуальным таблицам Human Resources</span><span class="sxs-lookup"><span data-stu-id="19d50-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="19d50-289">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="19d50-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="19d50-290">Обновления терминологии</span><span class="sxs-lookup"><span data-stu-id="19d50-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]