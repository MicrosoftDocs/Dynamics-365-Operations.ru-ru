---
title: Объекты Common Data Service
description: Microsoft Dynamics 365 Human Resources использует Common Data Service для включения сценариев расширяемости и интеграции.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087354"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="2e626-103">Объекты Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2e626-103">Common Data Service entities</span></span>

<span data-ttu-id="2e626-104">Microsoft Dynamics 365 Human Resources использует Common Data Service для включения сценариев расширяемости и интеграции.</span><span class="sxs-lookup"><span data-stu-id="2e626-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="2e626-105">Дополнительные сведения о Common Data Service см. в разделе [Что такое Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="2e626-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="2e626-106">Доступны следующие объекты Управление персоналом в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2e626-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="2e626-107">Объекты льгот</span><span class="sxs-lookup"><span data-stu-id="2e626-107">Benefit entities</span></span>

| <span data-ttu-id="2e626-108">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-108">Name</span></span> | <span data-ttu-id="2e626-109">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-110">Частота расчета льгот</span><span class="sxs-lookup"><span data-stu-id="2e626-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="2e626-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="2e626-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="2e626-112">Частоты расчета для платежного периода для льгот</span><span class="sxs-lookup"><span data-stu-id="2e626-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="2e626-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="2e626-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="2e626-114">Ставка расчета льгот</span><span class="sxs-lookup"><span data-stu-id="2e626-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="2e626-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="2e626-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="2e626-116">Сведения о ставке расчета льгот</span><span class="sxs-lookup"><span data-stu-id="2e626-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="2e626-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="2e626-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="2e626-118">Параметр льготы</span><span class="sxs-lookup"><span data-stu-id="2e626-118">Benefit Option</span></span> | <span data-ttu-id="2e626-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="2e626-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="2e626-120">План льготы</span><span class="sxs-lookup"><span data-stu-id="2e626-120">Benefit Plan</span></span> | <span data-ttu-id="2e626-121">cdm_benefitplan (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="2e626-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="2e626-122">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="2e626-122">Benefit Type</span></span> | <span data-ttu-id="2e626-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="2e626-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="2e626-124">Объекты задач бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="2e626-124">Business process tasks entities</span></span>

| <span data-ttu-id="2e626-125">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-125">Name</span></span> | <span data-ttu-id="2e626-126">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-127">Календарь бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="2e626-127">Business Process Calendar</span></span> | <span data-ttu-id="2e626-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="2e626-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="2e626-129">Назначение группы бизнес-процессу</span><span class="sxs-lookup"><span data-stu-id="2e626-129">Business Process Group Assignment</span></span> | <span data-ttu-id="2e626-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="2e626-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="2e626-131">Группа задач библиотеки бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="2e626-131">Business Process Library Task Group</span></span> | <span data-ttu-id="2e626-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="2e626-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="2e626-133">Стадия бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="2e626-133">Business Process Stage</span></span> | <span data-ttu-id="2e626-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="2e626-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="2e626-135">Заголовок шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="2e626-135">Checklist Template Header</span></span> | <span data-ttu-id="2e626-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="2e626-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="2e626-137">Задача шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="2e626-137">Checklist Template Task</span></span> | <span data-ttu-id="2e626-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="2e626-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="2e626-139">Объекты компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-139">Compensation entities</span></span>

| <span data-ttu-id="2e626-140">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-140">Name</span></span> | <span data-ttu-id="2e626-141">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-142">План фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="2e626-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="2e626-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="2e626-144">Сетка компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-144">Compensation Grid</span></span> | <span data-ttu-id="2e626-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="2e626-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="2e626-146">Уровень компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-146">Compensation Level</span></span> | <span data-ttu-id="2e626-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="2e626-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="2e626-148">Частота компенсационных выплат</span><span class="sxs-lookup"><span data-stu-id="2e626-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="2e626-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="2e626-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="2e626-150">Настройка опорной точки компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="2e626-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="2e626-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="2e626-152">Линия настройки опорных точки компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="2e626-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="2e626-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="2e626-154">Регион компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-154">Compensation Region</span></span> | <span data-ttu-id="2e626-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="2e626-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="2e626-156">Структура компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-156">Compensation Structure</span></span> | <span data-ttu-id="2e626-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="2e626-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="2e626-158">План переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-158">Compensation Variable Plan</span></span> | <span data-ttu-id="2e626-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="2e626-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="2e626-160">Уровень плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="2e626-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="2e626-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="2e626-162">Тип плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="2e626-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="2e626-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="2e626-164">Мероприятие фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="2e626-164">Fixed Compensation Event</span></span> | <span data-ttu-id="2e626-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="2e626-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="2e626-166">Положение о передаче прав на льготы</span><span class="sxs-lookup"><span data-stu-id="2e626-166">Vesting Rule</span></span> | <span data-ttu-id="2e626-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="2e626-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="2e626-168">Фиксированная компенсация для работника</span><span class="sxs-lookup"><span data-stu-id="2e626-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="2e626-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="2e626-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="2e626-170">Объекты организации</span><span class="sxs-lookup"><span data-stu-id="2e626-170">Organization entities</span></span>

| <span data-ttu-id="2e626-171">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-171">Name</span></span> | <span data-ttu-id="2e626-172">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-173">Отдел</span><span class="sxs-lookup"><span data-stu-id="2e626-173">Department</span></span> | <span data-ttu-id="2e626-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="2e626-174">cdm_department</span></span> |
| <span data-ttu-id="2e626-175">Занятость</span><span class="sxs-lookup"><span data-stu-id="2e626-175">Employment</span></span> | <span data-ttu-id="2e626-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="2e626-176">cdm_employment</span></span> |
| <span data-ttu-id="2e626-177">Организация</span><span class="sxs-lookup"><span data-stu-id="2e626-177">Company</span></span> | <span data-ttu-id="2e626-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="2e626-178">cdm_company</span></span> |
| <span data-ttu-id="2e626-179">Должность</span><span class="sxs-lookup"><span data-stu-id="2e626-179">Job</span></span> | <span data-ttu-id="2e626-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="2e626-180">cdm_job</span></span> |
| <span data-ttu-id="2e626-181">Функциональные обязанности</span><span class="sxs-lookup"><span data-stu-id="2e626-181">Job Function</span></span> | <span data-ttu-id="2e626-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="2e626-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="2e626-183">Должность</span><span class="sxs-lookup"><span data-stu-id="2e626-183">Job Position</span></span> | <span data-ttu-id="2e626-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="2e626-184">cdm_jobposition</span></span> |
| <span data-ttu-id="2e626-185">Тип позиции</span><span class="sxs-lookup"><span data-stu-id="2e626-185">Position Type</span></span> | <span data-ttu-id="2e626-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="2e626-186">cdm_positiontype</span></span> |
| <span data-ttu-id="2e626-187">Назначение работника на позицию</span><span class="sxs-lookup"><span data-stu-id="2e626-187">Position Worker Assignment</span></span> | <span data-ttu-id="2e626-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="2e626-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="2e626-189">Тип должности</span><span class="sxs-lookup"><span data-stu-id="2e626-189">Job Type</span></span> | <span data-ttu-id="2e626-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="2e626-190">cdm_jobtype</span></span> |
| <span data-ttu-id="2e626-191">Язык</span><span class="sxs-lookup"><span data-stu-id="2e626-191">Language</span></span> | <span data-ttu-id="2e626-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="2e626-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="2e626-193">Объекты отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="2e626-193">Leave and absence entities</span></span>

| <span data-ttu-id="2e626-194">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-194">Name</span></span> | <span data-ttu-id="2e626-195">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-196">Банковская проводка отпуска</span><span class="sxs-lookup"><span data-stu-id="2e626-196">Leave Bank Transaction</span></span> | <span data-ttu-id="2e626-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="2e626-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="2e626-198">Регистрация отпуска</span><span class="sxs-lookup"><span data-stu-id="2e626-198">Leave Enrollment</span></span> | <span data-ttu-id="2e626-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="2e626-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="2e626-200">План отпусков</span><span class="sxs-lookup"><span data-stu-id="2e626-200">Leave Plan</span></span> | <span data-ttu-id="2e626-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="2e626-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="2e626-202">Запрос на отпуск</span><span class="sxs-lookup"><span data-stu-id="2e626-202">Leave Request</span></span> | <span data-ttu-id="2e626-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="2e626-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="2e626-204">Сведения запроса отпуска</span><span class="sxs-lookup"><span data-stu-id="2e626-204">Leave Request Detail</span></span> | <span data-ttu-id="2e626-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="2e626-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="2e626-206">Тип отпуска</span><span class="sxs-lookup"><span data-stu-id="2e626-206">Leave Type</span></span> | <span data-ttu-id="2e626-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="2e626-207">cdm_leavetype</span></span> |
| <span data-ttu-id="2e626-208">Код основания типа отпуска</span><span class="sxs-lookup"><span data-stu-id="2e626-208">Leave Type Reason Code</span></span> | <span data-ttu-id="2e626-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="2e626-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="2e626-210">Объекты заработной платы</span><span class="sxs-lookup"><span data-stu-id="2e626-210">Payroll entities</span></span>

| <span data-ttu-id="2e626-211">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-211">Name</span></span> | <span data-ttu-id="2e626-212">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-213">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="2e626-213">Pay Cycle</span></span> | <span data-ttu-id="2e626-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="2e626-214">cdm_paycycle</span></span> |
| <span data-ttu-id="2e626-215">Платежный период</span><span class="sxs-lookup"><span data-stu-id="2e626-215">Pay Period</span></span> | <span data-ttu-id="2e626-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="2e626-216">cdm_payperiod</span></span> |
| <span data-ttu-id="2e626-217">Код дохода в зарплате</span><span class="sxs-lookup"><span data-stu-id="2e626-217">Payroll Earning Code</span></span> | <span data-ttu-id="2e626-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="2e626-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="2e626-219">Выплаты по банковскому счету</span><span class="sxs-lookup"><span data-stu-id="2e626-219">Bank Account Disbursement</span></span> | <span data-ttu-id="2e626-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="2e626-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="2e626-221">Налоговый регион</span><span class="sxs-lookup"><span data-stu-id="2e626-221">Tax Region</span></span> | <span data-ttu-id="2e626-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="2e626-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="2e626-223">Объекты работника</span><span class="sxs-lookup"><span data-stu-id="2e626-223">Worker entities</span></span>

| <span data-ttu-id="2e626-224">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-224">Name</span></span> | <span data-ttu-id="2e626-225">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-226">Рабочий</span><span class="sxs-lookup"><span data-stu-id="2e626-226">Worker</span></span> | <span data-ttu-id="2e626-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="2e626-227">cdm_worker</span></span> |
| <span data-ttu-id="2e626-228">Адрес работника</span><span class="sxs-lookup"><span data-stu-id="2e626-228">Worker Address</span></span> | <span data-ttu-id="2e626-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="2e626-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="2e626-230">Личные данные работника</span><span class="sxs-lookup"><span data-stu-id="2e626-230">Worker Personal Detail</span></span> | <span data-ttu-id="2e626-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="2e626-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="2e626-232">Идентификационный код работника</span><span class="sxs-lookup"><span data-stu-id="2e626-232">Worker Person Identification Number</span></span> | <span data-ttu-id="2e626-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="2e626-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="2e626-234">Идентификационный тип работника</span><span class="sxs-lookup"><span data-stu-id="2e626-234">Worker Person Identification Type</span></span> | <span data-ttu-id="2e626-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="2e626-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="2e626-236">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="2e626-236">Work Calendar</span></span> | <span data-ttu-id="2e626-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="2e626-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="2e626-238">Календарный день работы</span><span class="sxs-lookup"><span data-stu-id="2e626-238">Work Calendar Day</span></span> | <span data-ttu-id="2e626-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="2e626-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="2e626-240">Праздничный день в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="2e626-240">Work Calendar Holiday</span></span> |<span data-ttu-id="2e626-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="2e626-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="2e626-242">Строка праздничного дня в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="2e626-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="2e626-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="2e626-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="2e626-244">Интервал рабочего времени</span><span class="sxs-lookup"><span data-stu-id="2e626-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="2e626-245">cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="2e626-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="2e626-246">Банковский счет работника</span><span class="sxs-lookup"><span data-stu-id="2e626-246">Worker Bank Account</span></span> | <span data-ttu-id="2e626-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="2e626-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="2e626-248">Объекты настройки работника</span><span class="sxs-lookup"><span data-stu-id="2e626-248">Worker setup entities</span></span>

| <span data-ttu-id="2e626-249">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-249">Name</span></span> | <span data-ttu-id="2e626-250">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-251">Статус ветерана</span><span class="sxs-lookup"><span data-stu-id="2e626-251">Veteran Status</span></span> | <span data-ttu-id="2e626-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="2e626-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="2e626-253">Этническое происхождение</span><span class="sxs-lookup"><span data-stu-id="2e626-253">Ethnic Origin</span></span> | <span data-ttu-id="2e626-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="2e626-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="2e626-255">Код основания</span><span class="sxs-lookup"><span data-stu-id="2e626-255">Reason Code</span></span> | <span data-ttu-id="2e626-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="2e626-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="2e626-257">Выпускающее агентство по идентификации лиц</span><span class="sxs-lookup"><span data-stu-id="2e626-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="2e626-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="2e626-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="2e626-259">Объекты компетенции</span><span class="sxs-lookup"><span data-stu-id="2e626-259">Competency entities</span></span>

| <span data-ttu-id="2e626-260">Название</span><span class="sxs-lookup"><span data-stu-id="2e626-260">Name</span></span> | <span data-ttu-id="2e626-261">Объект</span><span class="sxs-lookup"><span data-stu-id="2e626-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2e626-262">Тип навыка</span><span class="sxs-lookup"><span data-stu-id="2e626-262">Skill Type</span></span> | <span data-ttu-id="2e626-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="2e626-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="2e626-264">Модели связи объектов</span><span class="sxs-lookup"><span data-stu-id="2e626-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="2e626-265">Рабочий</span><span class="sxs-lookup"><span data-stu-id="2e626-265">Worker</span></span>

![Рабочий](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="2e626-267">Работа и должность</span><span class="sxs-lookup"><span data-stu-id="2e626-267">Job and Job Position</span></span>

![Работа и должность](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="2e626-269">Льготы</span><span class="sxs-lookup"><span data-stu-id="2e626-269">Benefits</span></span>

![Льготы](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="2e626-271">Компенсация</span><span class="sxs-lookup"><span data-stu-id="2e626-271">Compensation</span></span>

![Компенсация](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="2e626-273">Отпуск</span><span class="sxs-lookup"><span data-stu-id="2e626-273">Leave</span></span>

![Отпуск](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="2e626-275">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="2e626-275">Work Calendar</span></span>

![Рабочий календарь](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="2e626-277">См. также</span><span class="sxs-lookup"><span data-stu-id="2e626-277">See also</span></span>

[<span data-ttu-id="2e626-278">Выбор технологии интеграции данных</span><span class="sxs-lookup"><span data-stu-id="2e626-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="2e626-279">Настройка интеграции Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2e626-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)