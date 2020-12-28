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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530014"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="60c1b-103">Объекты Common Data Service</span><span class="sxs-lookup"><span data-stu-id="60c1b-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="60c1b-104">Microsoft Dynamics 365 Human Resources использует Common Data Service для включения сценариев расширяемости и интеграции.</span><span class="sxs-lookup"><span data-stu-id="60c1b-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="60c1b-105">Дополнительные сведения о Common Data Service см. в разделе [Что такое Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="60c1b-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="60c1b-106">Доступны следующие объекты Управление персоналом в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="60c1b-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="60c1b-107">Объекты льгот</span><span class="sxs-lookup"><span data-stu-id="60c1b-107">Benefit entities</span></span>

| <span data-ttu-id="60c1b-108">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-108">Name</span></span> | <span data-ttu-id="60c1b-109">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-110">Частота расчета льгот</span><span class="sxs-lookup"><span data-stu-id="60c1b-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="60c1b-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="60c1b-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="60c1b-112">Частоты расчета для платежного периода для льгот</span><span class="sxs-lookup"><span data-stu-id="60c1b-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="60c1b-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="60c1b-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="60c1b-114">Ставка расчета льгот</span><span class="sxs-lookup"><span data-stu-id="60c1b-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="60c1b-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="60c1b-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="60c1b-116">Сведения о ставке расчета льгот</span><span class="sxs-lookup"><span data-stu-id="60c1b-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="60c1b-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="60c1b-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="60c1b-118">Параметр льготы</span><span class="sxs-lookup"><span data-stu-id="60c1b-118">Benefit Option</span></span> | <span data-ttu-id="60c1b-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="60c1b-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="60c1b-120">План льготы</span><span class="sxs-lookup"><span data-stu-id="60c1b-120">Benefit Plan</span></span> | <span data-ttu-id="60c1b-121">cdm_benefitplan (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="60c1b-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="60c1b-122">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="60c1b-122">Benefit Type</span></span> | <span data-ttu-id="60c1b-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="60c1b-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="60c1b-124">Объекты задач бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="60c1b-124">Business process tasks entities</span></span>

| <span data-ttu-id="60c1b-125">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-125">Name</span></span> | <span data-ttu-id="60c1b-126">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-127">Календарь бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="60c1b-127">Business Process Calendar</span></span> | <span data-ttu-id="60c1b-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="60c1b-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="60c1b-129">Назначение группы бизнес-процессу</span><span class="sxs-lookup"><span data-stu-id="60c1b-129">Business Process Group Assignment</span></span> | <span data-ttu-id="60c1b-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="60c1b-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="60c1b-131">Группа задач библиотеки бизнес-процессов</span><span class="sxs-lookup"><span data-stu-id="60c1b-131">Business Process Library Task Group</span></span> | <span data-ttu-id="60c1b-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="60c1b-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="60c1b-133">Стадия бизнес-процесса</span><span class="sxs-lookup"><span data-stu-id="60c1b-133">Business Process Stage</span></span> | <span data-ttu-id="60c1b-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="60c1b-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="60c1b-135">Заголовок шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="60c1b-135">Checklist Template Header</span></span> | <span data-ttu-id="60c1b-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="60c1b-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="60c1b-137">Задача шаблона контрольного списка</span><span class="sxs-lookup"><span data-stu-id="60c1b-137">Checklist Template Task</span></span> | <span data-ttu-id="60c1b-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="60c1b-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="60c1b-139">Объекты компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-139">Compensation entities</span></span>

| <span data-ttu-id="60c1b-140">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-140">Name</span></span> | <span data-ttu-id="60c1b-141">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-142">План фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="60c1b-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="60c1b-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="60c1b-144">Сетка компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-144">Compensation Grid</span></span> | <span data-ttu-id="60c1b-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="60c1b-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="60c1b-146">Уровень компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-146">Compensation Level</span></span> | <span data-ttu-id="60c1b-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="60c1b-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="60c1b-148">Частота компенсационных выплат</span><span class="sxs-lookup"><span data-stu-id="60c1b-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="60c1b-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="60c1b-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="60c1b-150">Настройка опорной точки компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="60c1b-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="60c1b-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="60c1b-152">Линия настройки опорных точки компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="60c1b-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="60c1b-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="60c1b-154">Регион компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-154">Compensation Region</span></span> | <span data-ttu-id="60c1b-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="60c1b-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="60c1b-156">Структура компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-156">Compensation Structure</span></span> | <span data-ttu-id="60c1b-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="60c1b-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="60c1b-158">План переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-158">Compensation Variable Plan</span></span> | <span data-ttu-id="60c1b-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="60c1b-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="60c1b-160">Уровень плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="60c1b-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="60c1b-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="60c1b-162">Тип плана переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="60c1b-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="60c1b-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="60c1b-164">Мероприятие фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="60c1b-164">Fixed Compensation Event</span></span> | <span data-ttu-id="60c1b-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="60c1b-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="60c1b-166">Положение о передаче прав на льготы</span><span class="sxs-lookup"><span data-stu-id="60c1b-166">Vesting Rule</span></span> | <span data-ttu-id="60c1b-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="60c1b-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="60c1b-168">Фиксированная компенсация для работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="60c1b-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="60c1b-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="60c1b-170">Объекты организации</span><span class="sxs-lookup"><span data-stu-id="60c1b-170">Organization entities</span></span>

| <span data-ttu-id="60c1b-171">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-171">Name</span></span> | <span data-ttu-id="60c1b-172">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-173">Отдел</span><span class="sxs-lookup"><span data-stu-id="60c1b-173">Department</span></span> | <span data-ttu-id="60c1b-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="60c1b-174">cdm_department</span></span> |
| <span data-ttu-id="60c1b-175">Занятость</span><span class="sxs-lookup"><span data-stu-id="60c1b-175">Employment</span></span> | <span data-ttu-id="60c1b-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="60c1b-176">cdm_employment</span></span> |
| <span data-ttu-id="60c1b-177">Организация</span><span class="sxs-lookup"><span data-stu-id="60c1b-177">Company</span></span> | <span data-ttu-id="60c1b-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="60c1b-178">cdm_company</span></span> |
| <span data-ttu-id="60c1b-179">Должность</span><span class="sxs-lookup"><span data-stu-id="60c1b-179">Job</span></span> | <span data-ttu-id="60c1b-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="60c1b-180">cdm_job</span></span> |
| <span data-ttu-id="60c1b-181">Функциональные обязанности</span><span class="sxs-lookup"><span data-stu-id="60c1b-181">Job Function</span></span> | <span data-ttu-id="60c1b-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="60c1b-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="60c1b-183">Должность</span><span class="sxs-lookup"><span data-stu-id="60c1b-183">Job Position</span></span> | <span data-ttu-id="60c1b-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="60c1b-184">cdm_jobposition</span></span> |
| <span data-ttu-id="60c1b-185">Тип позиции</span><span class="sxs-lookup"><span data-stu-id="60c1b-185">Position Type</span></span> | <span data-ttu-id="60c1b-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="60c1b-186">cdm_positiontype</span></span> |
| <span data-ttu-id="60c1b-187">Назначение работника на должность</span><span class="sxs-lookup"><span data-stu-id="60c1b-187">Position Worker Assignment</span></span> | <span data-ttu-id="60c1b-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="60c1b-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="60c1b-189">Аналитика должности</span><span class="sxs-lookup"><span data-stu-id="60c1b-189">Job Position Dimension</span></span> | <span data-ttu-id="60c1b-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="60c1b-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="60c1b-191">Тип вакансии</span><span class="sxs-lookup"><span data-stu-id="60c1b-191">Job Type</span></span> | <span data-ttu-id="60c1b-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="60c1b-192">cdm_jobtype</span></span> |
| <span data-ttu-id="60c1b-193">Язык</span><span class="sxs-lookup"><span data-stu-id="60c1b-193">Language</span></span> | <span data-ttu-id="60c1b-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="60c1b-194">cdm_language</span></span> |
| <span data-ttu-id="60c1b-195">Должность</span><span class="sxs-lookup"><span data-stu-id="60c1b-195">Title</span></span> | <span data-ttu-id="60c1b-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="60c1b-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="60c1b-197">Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="60c1b-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="60c1b-198">Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Common Data Service в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="60c1b-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="60c1b-199">Объекты отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="60c1b-199">Leave and absence entities</span></span>

| <span data-ttu-id="60c1b-200">Наименование</span><span class="sxs-lookup"><span data-stu-id="60c1b-200">Name</span></span> | <span data-ttu-id="60c1b-201">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-202">Банковская проводка отпуска</span><span class="sxs-lookup"><span data-stu-id="60c1b-202">Leave Bank Transaction</span></span> | <span data-ttu-id="60c1b-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="60c1b-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="60c1b-204">Регистрация отпуска</span><span class="sxs-lookup"><span data-stu-id="60c1b-204">Leave Enrollment</span></span> | <span data-ttu-id="60c1b-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="60c1b-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="60c1b-206">План отпусков</span><span class="sxs-lookup"><span data-stu-id="60c1b-206">Leave Plan</span></span> | <span data-ttu-id="60c1b-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="60c1b-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="60c1b-208">Запрос на отпуск</span><span class="sxs-lookup"><span data-stu-id="60c1b-208">Leave Request</span></span> | <span data-ttu-id="60c1b-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="60c1b-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="60c1b-210">Сведения запроса отпуска</span><span class="sxs-lookup"><span data-stu-id="60c1b-210">Leave Request Detail</span></span> | <span data-ttu-id="60c1b-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="60c1b-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="60c1b-212">Тип отпуска</span><span class="sxs-lookup"><span data-stu-id="60c1b-212">Leave Type</span></span> | <span data-ttu-id="60c1b-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="60c1b-213">cdm_leavetype</span></span> |
| <span data-ttu-id="60c1b-214">Код основания типа отпуска</span><span class="sxs-lookup"><span data-stu-id="60c1b-214">Leave Type Reason Code</span></span> | <span data-ttu-id="60c1b-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="60c1b-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="60c1b-216">Объекты заработной платы</span><span class="sxs-lookup"><span data-stu-id="60c1b-216">Payroll entities</span></span>

| <span data-ttu-id="60c1b-217">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-217">Name</span></span> | <span data-ttu-id="60c1b-218">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-219">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="60c1b-219">Pay Cycle</span></span> | <span data-ttu-id="60c1b-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="60c1b-220">cdm_paycycle</span></span> |
| <span data-ttu-id="60c1b-221">Платежный период</span><span class="sxs-lookup"><span data-stu-id="60c1b-221">Pay Period</span></span> | <span data-ttu-id="60c1b-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="60c1b-222">cdm_payperiod</span></span> |
| <span data-ttu-id="60c1b-223">Код дохода в зарплате</span><span class="sxs-lookup"><span data-stu-id="60c1b-223">Payroll Earning Code</span></span> | <span data-ttu-id="60c1b-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="60c1b-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="60c1b-225">Выплаты по банковскому счету</span><span class="sxs-lookup"><span data-stu-id="60c1b-225">Bank Account Disbursement</span></span> | <span data-ttu-id="60c1b-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="60c1b-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="60c1b-227">Налоговый регион</span><span class="sxs-lookup"><span data-stu-id="60c1b-227">Tax Region</span></span> | <span data-ttu-id="60c1b-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="60c1b-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="60c1b-229">Объекты работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-229">Worker entities</span></span>

| <span data-ttu-id="60c1b-230">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-230">Name</span></span> | <span data-ttu-id="60c1b-231">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-232">Рабочий</span><span class="sxs-lookup"><span data-stu-id="60c1b-232">Worker</span></span> | <span data-ttu-id="60c1b-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="60c1b-233">cdm_worker</span></span> |
| <span data-ttu-id="60c1b-234">Адрес работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-234">Worker Address</span></span> | <span data-ttu-id="60c1b-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="60c1b-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="60c1b-236">Личные данные работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-236">Worker Personal Detail</span></span> | <span data-ttu-id="60c1b-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="60c1b-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="60c1b-238">Идентификационный код работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-238">Worker Person Identification Number</span></span> | <span data-ttu-id="60c1b-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="60c1b-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="60c1b-240">Идентификационный тип работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-240">Worker Person Identification Type</span></span> | <span data-ttu-id="60c1b-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="60c1b-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="60c1b-242">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="60c1b-242">Work Calendar</span></span> | <span data-ttu-id="60c1b-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="60c1b-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="60c1b-244">Календарный день работы</span><span class="sxs-lookup"><span data-stu-id="60c1b-244">Work Calendar Day</span></span> | <span data-ttu-id="60c1b-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="60c1b-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="60c1b-246">Праздничный день в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="60c1b-246">Work Calendar Holiday</span></span> |<span data-ttu-id="60c1b-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="60c1b-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="60c1b-248">Строка праздничного дня в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="60c1b-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="60c1b-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="60c1b-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="60c1b-250">Интервал рабочего времени</span><span class="sxs-lookup"><span data-stu-id="60c1b-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="60c1b-251">cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей)</span><span class="sxs-lookup"><span data-stu-id="60c1b-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="60c1b-252">Банковский счет работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-252">Worker Bank Account</span></span> | <span data-ttu-id="60c1b-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="60c1b-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="60c1b-254">Объекты настройки работника</span><span class="sxs-lookup"><span data-stu-id="60c1b-254">Worker setup entities</span></span>

| <span data-ttu-id="60c1b-255">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-255">Name</span></span> | <span data-ttu-id="60c1b-256">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-257">Статус ветерана</span><span class="sxs-lookup"><span data-stu-id="60c1b-257">Veteran Status</span></span> | <span data-ttu-id="60c1b-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="60c1b-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="60c1b-259">Этническое происхождение</span><span class="sxs-lookup"><span data-stu-id="60c1b-259">Ethnic Origin</span></span> | <span data-ttu-id="60c1b-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="60c1b-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="60c1b-261">Код основания</span><span class="sxs-lookup"><span data-stu-id="60c1b-261">Reason Code</span></span> | <span data-ttu-id="60c1b-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="60c1b-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="60c1b-263">Выпускающее агентство по идентификации лиц</span><span class="sxs-lookup"><span data-stu-id="60c1b-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="60c1b-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="60c1b-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="60c1b-265">Объекты компетенции</span><span class="sxs-lookup"><span data-stu-id="60c1b-265">Competency entities</span></span>

| <span data-ttu-id="60c1b-266">Название</span><span class="sxs-lookup"><span data-stu-id="60c1b-266">Name</span></span> | <span data-ttu-id="60c1b-267">Объект</span><span class="sxs-lookup"><span data-stu-id="60c1b-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="60c1b-268">Тип навыка</span><span class="sxs-lookup"><span data-stu-id="60c1b-268">Skill Type</span></span> | <span data-ttu-id="60c1b-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="60c1b-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="60c1b-270">Модели связи объектов</span><span class="sxs-lookup"><span data-stu-id="60c1b-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="60c1b-271">Рабочий</span><span class="sxs-lookup"><span data-stu-id="60c1b-271">Worker</span></span>

![Рабочий](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="60c1b-273">Работа и должность</span><span class="sxs-lookup"><span data-stu-id="60c1b-273">Job and Job Position</span></span>

![Работа и должность](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="60c1b-275">Льготы</span><span class="sxs-lookup"><span data-stu-id="60c1b-275">Benefits</span></span>

![Льготы](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="60c1b-277">Компенсация</span><span class="sxs-lookup"><span data-stu-id="60c1b-277">Compensation</span></span>

![Компенсация](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="60c1b-279">Отпуск</span><span class="sxs-lookup"><span data-stu-id="60c1b-279">Leave</span></span>

![Отпуск](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="60c1b-281">Рабочий календарь</span><span class="sxs-lookup"><span data-stu-id="60c1b-281">Work Calendar</span></span>

![Рабочий календарь](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="60c1b-283">См. также</span><span class="sxs-lookup"><span data-stu-id="60c1b-283">See also</span></span>

[<span data-ttu-id="60c1b-284">Выбор технологии интеграции данных</span><span class="sxs-lookup"><span data-stu-id="60c1b-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="60c1b-285">Настройка интеграции Common Data Service</span><span class="sxs-lookup"><span data-stu-id="60c1b-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
