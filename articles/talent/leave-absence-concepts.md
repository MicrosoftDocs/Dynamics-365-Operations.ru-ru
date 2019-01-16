---
title: "Концепции отпусков и отсутствия на работе"
description: "В этой теме описываются концепции отпусков и отсутствия на работе, а также способ определения сальдо отгулов."
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a388e0efe6c19a3aabe04e7fff039ce11ae023c4
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.contentlocale: ru-ru
ms.lasthandoff: 01/07/2019

---

# <a name="leave-and-absence-concepts"></a><span data-ttu-id="487d0-103">Концепции отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="487d0-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="487d0-104">Понятия и термины, которые описаны в этом разделе, помогут определить, как сотрудникам начисляется время отгулов и как рассчитываются сальдо отгулов для сотрудников.</span><span class="sxs-lookup"><span data-stu-id="487d0-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="487d0-105">Дополнительные сведения об управлении отпусками и отгулами см. в разделе [Управление отпусками и отгулами](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="487d0-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="487d0-106">Сведения плана отпусков</span><span class="sxs-lookup"><span data-stu-id="487d0-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="487d0-107">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="487d0-107">Start date</span></span>

<span data-ttu-id="487d0-108">Дата начала — это дата начала обработки начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="487d0-109">Начальная дата также служит датой юбилея, которая используется для расчета переносимых сумм.</span><span class="sxs-lookup"><span data-stu-id="487d0-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="487d0-110">Начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-110">Accruals</span></span>

<span data-ttu-id="487d0-111">Начисления определяют, когда и как часто сотрудникам начисляется время отгулов.</span><span class="sxs-lookup"><span data-stu-id="487d0-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="487d0-112">Политики относительно времени начисления и политики пропорций определяются в разделе **Начисления** при настройте плана отпусков и отгулов.</span><span class="sxs-lookup"><span data-stu-id="487d0-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="487d0-113">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-113">Accrual frequency</span></span>

<span data-ttu-id="487d0-114">Частота начисления определяет, как часто начисляется или предоставляется отпуск.</span><span class="sxs-lookup"><span data-stu-id="487d0-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="487d0-115">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="487d0-115">The following options are available:</span></span>

- <span data-ttu-id="487d0-116">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="487d0-116">Daily</span></span>
- <span data-ttu-id="487d0-117">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="487d0-117">Weekly</span></span>
- <span data-ttu-id="487d0-118">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="487d0-118">Biweekly</span></span>
- <span data-ttu-id="487d0-119">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-119">Semimonthly</span></span>
- <span data-ttu-id="487d0-120">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="487d0-120">Monthly</span></span>
- <span data-ttu-id="487d0-121">Ежеквартально</span><span class="sxs-lookup"><span data-stu-id="487d0-121">Quarterly</span></span>
- <span data-ttu-id="487d0-122">Раз в полгода</span><span class="sxs-lookup"><span data-stu-id="487d0-122">Semiannually</span></span>
- <span data-ttu-id="487d0-123">Ежегодно</span><span class="sxs-lookup"><span data-stu-id="487d0-123">Annually</span></span>
- <span data-ttu-id="487d0-124">Не допускается</span><span class="sxs-lookup"><span data-stu-id="487d0-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="487d0-125">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-125">Accrual period basis</span></span>

<span data-ttu-id="487d0-126">Базис периода начисления определяет дату, которая используется для расчета периодов начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="487d0-127">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="487d0-127">The following options are available:</span></span>

- <span data-ttu-id="487d0-128">**Дата начала плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-128">**Plan start date**</span></span>
- <span data-ttu-id="487d0-129">**Дата конкретного сотрудника** — если этот параметр выбран, значение определяет источник значения начальной даты, используемый для расчета периодов начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="487d0-130">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="487d0-130">The following options are available:</span></span>

    - <span data-ttu-id="487d0-131">Произвольная</span><span class="sxs-lookup"><span data-stu-id="487d0-131">Custom</span></span>
    - <span data-ttu-id="487d0-132">Дата юбилея</span><span class="sxs-lookup"><span data-stu-id="487d0-132">Anniversary date</span></span>
    - <span data-ttu-id="487d0-133">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="487d0-133">Original hire date</span></span>
    - <span data-ttu-id="487d0-134">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="487d0-134">Seniority date</span></span>
    - <span data-ttu-id="487d0-135">Скорректированная дата приема работника на работу</span><span class="sxs-lookup"><span data-stu-id="487d0-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="487d0-136">Дата приема работника на работу</span><span class="sxs-lookup"><span data-stu-id="487d0-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="487d0-137">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-137">Accrual award date</span></span>

<span data-ttu-id="487d0-138">Дата начисления определяет, когда сотруднику начисляется время отгулов.</span><span class="sxs-lookup"><span data-stu-id="487d0-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="487d0-139">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="487d0-139">The following options are available:</span></span>

- <span data-ttu-id="487d0-140">**Дата окончания периода начисления** — сотруднику начисляется время отгула в последний день периода вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="487d0-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="487d0-141">Для начисления правильной суммы процесс начисления должен включать весь период.</span><span class="sxs-lookup"><span data-stu-id="487d0-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="487d0-142">Например, период начисления с 1 января 2018 по 31 января 2018.</span><span class="sxs-lookup"><span data-stu-id="487d0-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="487d0-143">В этом случае для включения января необходимо выполнить начисление для 1 февраля 2018.</span><span class="sxs-lookup"><span data-stu-id="487d0-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="487d0-144">**Дата начала периода начисления** — сотруднику начисляется время отгула в первый день периода вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="487d0-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="487d0-145">Политика начисления по заявке</span><span class="sxs-lookup"><span data-stu-id="487d0-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="487d0-146">Эта политика начисления по заявке определяет способ расчета начисления, когда сотрудник зарегистрирован в середине периода начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="487d0-147">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="487d0-147">The following options are available:</span></span>

- <span data-ttu-id="487d0-148">**Пропорционально** — диапазон дат между датой регистрации и датой начала используется для определения разницы в днях.</span><span class="sxs-lookup"><span data-stu-id="487d0-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="487d0-149">Эта разница учитывается при обработке начислений.</span><span class="sxs-lookup"><span data-stu-id="487d0-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="487d0-150">**Полное начисления** — полное начисления суммы в зависимости от уровня производится во время обработки первого начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="487d0-151">**Без начисления** — до следующего периода начисления никакие начисления не производятся.</span><span class="sxs-lookup"><span data-stu-id="487d0-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="487d0-152">Политика начисления при отмене регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="487d0-153">Эта политика начисления по отмене регистрации определяет способ расчета начисления, когда регистрация сотрудника отменена в середине периода начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="487d0-154">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="487d0-154">The following options are available:</span></span>

- <span data-ttu-id="487d0-155">**Пропорционально** — диапазон дат между датой регистрации и датой начала используется для определения разницы в днях.</span><span class="sxs-lookup"><span data-stu-id="487d0-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="487d0-156">Эта разница учитывается при обработке начислений.</span><span class="sxs-lookup"><span data-stu-id="487d0-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="487d0-157">**Полное начисления** — полное начисления суммы в зависимости от уровня производится во время обработки первого начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="487d0-158">**Без начисления** — до следующего периода начисления никакие начисления не производятся.</span><span class="sxs-lookup"><span data-stu-id="487d0-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="487d0-159">График начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-159">Accrual schedule</span></span>

<span data-ttu-id="487d0-160">График начисления определяет способ начисления сотрудникам времени отгулов, а также какие суммы будут начислены сотруднику и перенесены на будущее.</span><span class="sxs-lookup"><span data-stu-id="487d0-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="487d0-161">Уровни могут создаваться таким образом, чтобы отгулы начислялись на основе различных уровней.</span><span class="sxs-lookup"><span data-stu-id="487d0-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="487d0-162">Месяцы службы</span><span class="sxs-lookup"><span data-stu-id="487d0-162">Months of service</span></span>

<span data-ttu-id="487d0-163">Значение **Месяцы службы** определяет минимальное количество месяцев, которые сотрудники должны отработать для получения права на начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="487d0-164">Если для сотрудников нет минимального срока, задайте значение **0**.</span><span class="sxs-lookup"><span data-stu-id="487d0-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="487d0-165">Отработанные часы</span><span class="sxs-lookup"><span data-stu-id="487d0-165">Hours worked</span></span>

<span data-ttu-id="487d0-166">Значение **Отработанные часы** определяет минимальное количество часов, которые сотрудники должны отработать за период начисления для получения права на начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="487d0-167">Если для сотрудников нет минимального срока, задайте значение **0**.</span><span class="sxs-lookup"><span data-stu-id="487d0-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="487d0-168">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-168">Accrual amount</span></span>

<span data-ttu-id="487d0-169">Сумма начисления — это число часов или дней, которые будут начисляться сотрудникам за период.</span><span class="sxs-lookup"><span data-stu-id="487d0-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="487d0-170">Период основан на частоте начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="487d0-171">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-171">Minimum balance</span></span>

<span data-ttu-id="487d0-172">Отрицательное значение может использоваться для минимального сальдо, если сотрудники могут запрашивать больше отпуска, чем им доступно на данный момент.</span><span class="sxs-lookup"><span data-stu-id="487d0-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="487d0-173">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-173">Maximum carry-forward</span></span>

<span data-ttu-id="487d0-174">Процесс начисления настроит сальдо отпуска, которое превышающих максимальное сальдо переноса на день годовщины даты начала.</span><span class="sxs-lookup"><span data-stu-id="487d0-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="487d0-175">Предоставляемая сумма</span><span class="sxs-lookup"><span data-stu-id="487d0-175">Grant amount</span></span>

<span data-ttu-id="487d0-176">Предоставляемая сумма — это начальное количество часов или дней, которое предоставляется сотрудникам при начальной регистрации в плане отпусков.</span><span class="sxs-lookup"><span data-stu-id="487d0-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="487d0-177">Эта сумма не начисляется за каждый период начисления.</span><span class="sxs-lookup"><span data-stu-id="487d0-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="487d0-178">Регистрации и сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="487d0-179">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-179">Enrollment date</span></span>

<span data-ttu-id="487d0-180">Дата регистрации определяет, когда сотрудник может начинать начисление времени отпуска.</span><span class="sxs-lookup"><span data-stu-id="487d0-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="487d0-181">Например, если сотрудник зарегистрирован в плане отпуска 15 июня 2018, она не может начислять никакое время отпуска до 15 июня 2018.</span><span class="sxs-lookup"><span data-stu-id="487d0-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="487d0-182">Текущее сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-182">Current balance</span></span>

<span data-ttu-id="487d0-183">Текущее сальдо — это количество, доступное для запросов отгулов.</span><span class="sxs-lookup"><span data-stu-id="487d0-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="487d0-184">Эта сумма включает в себя начисления, одобренные запросы и корректировки до текущей даты.</span><span class="sxs-lookup"><span data-stu-id="487d0-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="487d0-185">Примеры текущего сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="487d0-186">Годовой план</span><span class="sxs-lookup"><span data-stu-id="487d0-186">Annual plan</span></span>

<span data-ttu-id="487d0-187">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-187">**Plan setup**</span></span>

| <span data-ttu-id="487d0-188">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-188">Plan start date</span></span> | <span data-ttu-id="487d0-189">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-189">Enrollment date</span></span> | <span data-ttu-id="487d0-190">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-190">Accrual frequency</span></span> | <span data-ttu-id="487d0-191">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-191">Accrual period basis</span></span> | <span data-ttu-id="487d0-192">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="487d0-193">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-193">1/1/2018</span></span>        | <span data-ttu-id="487d0-194">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-194">1/1/2018</span></span>        | <span data-ttu-id="487d0-195">Ежегодный</span><span class="sxs-lookup"><span data-stu-id="487d0-195">Annual</span></span>            | <span data-ttu-id="487d0-196">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-196">Plan start date</span></span>      | <span data-ttu-id="487d0-197">Конец периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-197">End of accrual period</span></span> |

<span data-ttu-id="487d0-198">Начисления обрабатываются на 1 января 2019 (01.01.2019), чтобы весь период был добавлен.</span><span class="sxs-lookup"><span data-stu-id="487d0-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="487d0-199">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-199">**Results**</span></span>

| <span data-ttu-id="487d0-200">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-200">Accrual amount</span></span> | <span data-ttu-id="487d0-201">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-201">Minimum balance</span></span> | <span data-ttu-id="487d0-202">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-202">Maximum carry-forward</span></span> | <span data-ttu-id="487d0-203">Сумма запроса</span><span class="sxs-lookup"><span data-stu-id="487d0-203">Request amount</span></span> | <span data-ttu-id="487d0-204">Текущее сальдо (на 01.01.2019)</span><span class="sxs-lookup"><span data-stu-id="487d0-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="487d0-205">200</span><span class="sxs-lookup"><span data-stu-id="487d0-205">200</span></span>            | <span data-ttu-id="487d0-206">0</span><span class="sxs-lookup"><span data-stu-id="487d0-206">0</span></span>               | <span data-ttu-id="487d0-207">120</span><span class="sxs-lookup"><span data-stu-id="487d0-207">120</span></span>                   | <span data-ttu-id="487d0-208">40</span><span class="sxs-lookup"><span data-stu-id="487d0-208">40</span></span>             | <span data-ttu-id="487d0-209">160</span><span class="sxs-lookup"><span data-stu-id="487d0-209">160</span></span>                              |

<span data-ttu-id="487d0-210">Текущее сальдо (160) = Сумма начислений (200) — Сумма запроса (40)</span><span class="sxs-lookup"><span data-stu-id="487d0-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="487d0-211">План два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-211">Semimonthly plan</span></span>

<span data-ttu-id="487d0-212">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-212">**Plan setup**</span></span>

| <span data-ttu-id="487d0-213">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-213">Plan start date</span></span> | <span data-ttu-id="487d0-214">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-214">Enrollment date</span></span> | <span data-ttu-id="487d0-215">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-215">Accrual frequency</span></span> | <span data-ttu-id="487d0-216">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-216">Accrual period basis</span></span> | <span data-ttu-id="487d0-217">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="487d0-218">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-218">1/1/2018</span></span>        | <span data-ttu-id="487d0-219">01.02.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-219">2/1/2018</span></span>        | <span data-ttu-id="487d0-220">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-220">Semimonthly</span></span>       | <span data-ttu-id="487d0-221">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-221">Plan start date</span></span>      | <span data-ttu-id="487d0-222">Конец периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-222">End of accrual period</span></span> |

<span data-ttu-id="487d0-223">Начисления обрабатываются на 1 мая 2018 (01.05.2018), чтобы весь период был добавлен.</span><span class="sxs-lookup"><span data-stu-id="487d0-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="487d0-224">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-224">**Results**</span></span>

| <span data-ttu-id="487d0-225">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-225">Accrual amount</span></span> | <span data-ttu-id="487d0-226">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-226">Minimum balance</span></span> | <span data-ttu-id="487d0-227">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-227">Maximum carry-forward</span></span> | <span data-ttu-id="487d0-228">Сумма запроса</span><span class="sxs-lookup"><span data-stu-id="487d0-228">Request amount</span></span> | <span data-ttu-id="487d0-229">Текущее сальдо (на 01.01.2019)</span><span class="sxs-lookup"><span data-stu-id="487d0-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="487d0-230">5</span><span class="sxs-lookup"><span data-stu-id="487d0-230">5</span></span>              | <span data-ttu-id="487d0-231">0</span><span class="sxs-lookup"><span data-stu-id="487d0-231">0</span></span>               | <span data-ttu-id="487d0-232">120</span><span class="sxs-lookup"><span data-stu-id="487d0-232">120</span></span>                   | <span data-ttu-id="487d0-233">8</span><span class="sxs-lookup"><span data-stu-id="487d0-233">8</span></span>              | <span data-ttu-id="487d0-234">22</span><span class="sxs-lookup"><span data-stu-id="487d0-234">22</span></span>                               |

<span data-ttu-id="487d0-235">Текущее сальдо (22) = Сумма начислений (5 × 6) — Сумма запроса (8)</span><span class="sxs-lookup"><span data-stu-id="487d0-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="487d0-236">Месячный план</span><span class="sxs-lookup"><span data-stu-id="487d0-236">Monthly plan</span></span>

<span data-ttu-id="487d0-237">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-237">**Plan setup**</span></span>

| <span data-ttu-id="487d0-238">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-238">Plan start date</span></span> | <span data-ttu-id="487d0-239">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-239">Enrollment date</span></span> | <span data-ttu-id="487d0-240">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-240">Accrual frequency</span></span> | <span data-ttu-id="487d0-241">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-241">Accrual period basis</span></span> | <span data-ttu-id="487d0-242">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="487d0-243">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-243">1/1/2018</span></span>        | <span data-ttu-id="487d0-244">01.02.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-244">2/1/2018</span></span>        | <span data-ttu-id="487d0-245">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-245">Semimonthly</span></span>       | <span data-ttu-id="487d0-246">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-246">Plan start date</span></span>      | <span data-ttu-id="487d0-247">Конец периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-247">End of accrual period</span></span> |

<span data-ttu-id="487d0-248">Начисления обрабатываются на 1 мая 2018 (01.05.2018), чтобы весь период был добавлен.</span><span class="sxs-lookup"><span data-stu-id="487d0-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="487d0-249">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-249">**Results**</span></span>

| <span data-ttu-id="487d0-250">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-250">Accrual amount</span></span> | <span data-ttu-id="487d0-251">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-251">Minimum balance</span></span> | <span data-ttu-id="487d0-252">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-252">Maximum carry-forward</span></span> | <span data-ttu-id="487d0-253">Сумма запроса</span><span class="sxs-lookup"><span data-stu-id="487d0-253">Request amount</span></span> | <span data-ttu-id="487d0-254">Текущее сальдо (на 01.01.2019)</span><span class="sxs-lookup"><span data-stu-id="487d0-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="487d0-255">5</span><span class="sxs-lookup"><span data-stu-id="487d0-255">5</span></span>              | <span data-ttu-id="487d0-256">0</span><span class="sxs-lookup"><span data-stu-id="487d0-256">0</span></span>               | <span data-ttu-id="487d0-257">120</span><span class="sxs-lookup"><span data-stu-id="487d0-257">120</span></span>                   | <span data-ttu-id="487d0-258">8</span><span class="sxs-lookup"><span data-stu-id="487d0-258">8</span></span>              | <span data-ttu-id="487d0-259">7</span><span class="sxs-lookup"><span data-stu-id="487d0-259">7</span></span>                                |

<span data-ttu-id="487d0-260">Текущее сальдо (7) = Сумма начислений (5 × 3) — Сумма запроса (8)</span><span class="sxs-lookup"><span data-stu-id="487d0-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="487d0-261">Прогнозируемое сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-261">Forecasted balance</span></span>

<span data-ttu-id="487d0-262">*Прогнозируемое сальдо* равно сумме отпуска, которая доступна на будущую дату.</span><span class="sxs-lookup"><span data-stu-id="487d0-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="487d0-263">Начисления и корректировки переноса прогнозируются до этой даты.</span><span class="sxs-lookup"><span data-stu-id="487d0-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="487d0-264">Используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="487d0-264">The following formula is used:</span></span>

<span data-ttu-id="487d0-265">Прогнозируемое сальдо на понедельник = Текущее сальдо — Запросы + Начисления — Корректировки переноса</span><span class="sxs-lookup"><span data-stu-id="487d0-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="487d0-266">Примеры прогнозируемого сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="487d0-267">Годовой план</span><span class="sxs-lookup"><span data-stu-id="487d0-267">Annual plan</span></span>

<span data-ttu-id="487d0-268">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-268">**Plan setup**</span></span>

| <span data-ttu-id="487d0-269">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-269">Plan start date</span></span> | <span data-ttu-id="487d0-270">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-270">Enrollment date</span></span> | <span data-ttu-id="487d0-271">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-271">Accrual frequency</span></span> | <span data-ttu-id="487d0-272">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-272">Accrual period basis</span></span> | <span data-ttu-id="487d0-273">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="487d0-274">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-274">1/1/2018</span></span>        | <span data-ttu-id="487d0-275">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-275">1/1/2018</span></span>        | <span data-ttu-id="487d0-276">Ежегодный</span><span class="sxs-lookup"><span data-stu-id="487d0-276">Annual</span></span>            | <span data-ttu-id="487d0-277">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-277">Plan start date</span></span>      | <span data-ttu-id="487d0-278">Конец периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-278">End of accrual period</span></span> |

<span data-ttu-id="487d0-279">Начисления обрабатываются на 15 февраля 2019 (15.02.2019), чтобы весь период был добавлен.</span><span class="sxs-lookup"><span data-stu-id="487d0-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="487d0-280">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-280">**Results**</span></span>

| <span data-ttu-id="487d0-281">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-281">Accrual amount</span></span> | <span data-ttu-id="487d0-282">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-282">Minimum balance</span></span> | <span data-ttu-id="487d0-283">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-283">Maximum carry-forward</span></span> | <span data-ttu-id="487d0-284">Текущее сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-284">Current balance</span></span> | <span data-ttu-id="487d0-285">Прогнозируемое сальдо (на 15.02.2019)</span><span class="sxs-lookup"><span data-stu-id="487d0-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="487d0-286">20</span><span class="sxs-lookup"><span data-stu-id="487d0-286">20</span></span>             | <span data-ttu-id="487d0-287">0</span><span class="sxs-lookup"><span data-stu-id="487d0-287">0</span></span>               | <span data-ttu-id="487d0-288">20</span><span class="sxs-lookup"><span data-stu-id="487d0-288">20</span></span>                    | <span data-ttu-id="487d0-289">40</span><span class="sxs-lookup"><span data-stu-id="487d0-289">40</span></span>              | <span data-ttu-id="487d0-290">40</span><span class="sxs-lookup"><span data-stu-id="487d0-290">40</span></span>                                   |

<span data-ttu-id="487d0-291">Прогнозируемое сальдо (40) = Сумма начислений (20) + Текущее сальдо (40) — Корректировка переноса (20)</span><span class="sxs-lookup"><span data-stu-id="487d0-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="487d0-292">План два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-292">Semimonthly plan</span></span>

<span data-ttu-id="487d0-293">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-293">**Plan setup**</span></span>

| <span data-ttu-id="487d0-294">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-294">Plan start date</span></span> | <span data-ttu-id="487d0-295">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-295">Enrollment date</span></span> | <span data-ttu-id="487d0-296">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-296">Accrual frequency</span></span> | <span data-ttu-id="487d0-297">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-297">Accrual period basis</span></span> | <span data-ttu-id="487d0-298">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="487d0-299">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-299">1/1/2018</span></span>        | <span data-ttu-id="487d0-300">01.02.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-300">2/1/2018</span></span>        | <span data-ttu-id="487d0-301">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-301">Semimonthly</span></span>       | <span data-ttu-id="487d0-302">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-302">Plan start date</span></span>      | <span data-ttu-id="487d0-303">Конец периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-303">End of accrual period</span></span> |

<span data-ttu-id="487d0-304">Начисления обрабатываются на 15 февраля 2019 (15.02.2019), чтобы весь период был добавлен.</span><span class="sxs-lookup"><span data-stu-id="487d0-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="487d0-305">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-305">**Results**</span></span>

| <span data-ttu-id="487d0-306">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-306">Accrual amount</span></span> | <span data-ttu-id="487d0-307">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-307">Minimum balance</span></span> | <span data-ttu-id="487d0-308">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-308">Maximum carry-forward</span></span> | <span data-ttu-id="487d0-309">Текущее сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-309">Current balance</span></span> | <span data-ttu-id="487d0-310">Прогнозируемое сальдо (на 15.02.2019)</span><span class="sxs-lookup"><span data-stu-id="487d0-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="487d0-311">5</span><span class="sxs-lookup"><span data-stu-id="487d0-311">5</span></span>              | <span data-ttu-id="487d0-312">0</span><span class="sxs-lookup"><span data-stu-id="487d0-312">0</span></span>               | <span data-ttu-id="487d0-313">20</span><span class="sxs-lookup"><span data-stu-id="487d0-313">20</span></span>                    | <span data-ttu-id="487d0-314">40</span><span class="sxs-lookup"><span data-stu-id="487d0-314">40</span></span>              | <span data-ttu-id="487d0-315">35</span><span class="sxs-lookup"><span data-stu-id="487d0-315">35</span></span>                                   |

<span data-ttu-id="487d0-316">Прогнозируемое сальдо (35) = Сумма начислений (5 × 3) + Текущее сальдо (40) — Корректировка переноса (20)</span><span class="sxs-lookup"><span data-stu-id="487d0-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="487d0-317">Месячный план</span><span class="sxs-lookup"><span data-stu-id="487d0-317">Monthly plan</span></span>

<span data-ttu-id="487d0-318">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-318">**Plan setup**</span></span>

| <span data-ttu-id="487d0-319">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-319">Plan start date</span></span> | <span data-ttu-id="487d0-320">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-320">Enrollment date</span></span> | <span data-ttu-id="487d0-321">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-321">Accrual frequency</span></span> | <span data-ttu-id="487d0-322">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-322">Accrual period basis</span></span> | <span data-ttu-id="487d0-323">Дата вознаграждения начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="487d0-324">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-324">1/1/2018</span></span>        | <span data-ttu-id="487d0-325">01.02.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-325">2/1/2018</span></span>        | <span data-ttu-id="487d0-326">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="487d0-326">Semimonthly</span></span>       | <span data-ttu-id="487d0-327">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-327">Plan start date</span></span>      | <span data-ttu-id="487d0-328">Конец периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-328">End of accrual period</span></span> |

<span data-ttu-id="487d0-329">Начисления обрабатываются на 15 февраля 2019 (15.02.2019), чтобы весь период был добавлен.</span><span class="sxs-lookup"><span data-stu-id="487d0-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="487d0-330">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-330">**Results**</span></span>

| <span data-ttu-id="487d0-331">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-331">Accrual amount</span></span> | <span data-ttu-id="487d0-332">Минимальное сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-332">Minimum balance</span></span> | <span data-ttu-id="487d0-333">Максимальный перенос</span><span class="sxs-lookup"><span data-stu-id="487d0-333">Maximum carry-forward</span></span> | <span data-ttu-id="487d0-334">Текущее сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-334">Current balance</span></span> | <span data-ttu-id="487d0-335">Прогнозируемое сальдо (на 15.02.2019)</span><span class="sxs-lookup"><span data-stu-id="487d0-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="487d0-336">10</span><span class="sxs-lookup"><span data-stu-id="487d0-336">10</span></span>             | <span data-ttu-id="487d0-337">0</span><span class="sxs-lookup"><span data-stu-id="487d0-337">0</span></span>               | <span data-ttu-id="487d0-338">20</span><span class="sxs-lookup"><span data-stu-id="487d0-338">20</span></span>                    | <span data-ttu-id="487d0-339">40</span><span class="sxs-lookup"><span data-stu-id="487d0-339">40</span></span>              | <span data-ttu-id="487d0-340">30</span><span class="sxs-lookup"><span data-stu-id="487d0-340">30</span></span>                                   |

<span data-ttu-id="487d0-341">Прогнозируемое сальдо (30) = Сумма начислений (10 × 1) + Текущее сальдо (40) — Корректировка переноса (20)</span><span class="sxs-lookup"><span data-stu-id="487d0-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="487d0-342">Примеры пропорционального сальдо</span><span class="sxs-lookup"><span data-stu-id="487d0-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="487d0-343">Пропорциональный ежемесячный план</span><span class="sxs-lookup"><span data-stu-id="487d0-343">Prorated monthly plan</span></span>

<span data-ttu-id="487d0-344">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-344">**Plan setup**</span></span>

| <span data-ttu-id="487d0-345">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-345">Plan start date</span></span> | <span data-ttu-id="487d0-346">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-346">Accrual frequency</span></span> | <span data-ttu-id="487d0-347">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="487d0-348">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-348">1/1/2018</span></span>        | <span data-ttu-id="487d0-349">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="487d0-349">Monthly</span></span>           | <span data-ttu-id="487d0-350">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-350">Plan start date</span></span>      |

<span data-ttu-id="487d0-351">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-351">**Results**</span></span>

| <span data-ttu-id="487d0-352">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="487d0-352">Employee</span></span>            | <span data-ttu-id="487d0-353">Месяцы службы</span><span class="sxs-lookup"><span data-stu-id="487d0-353">Months of service</span></span> | <span data-ttu-id="487d0-354">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-354">Enrollment date</span></span> | <span data-ttu-id="487d0-355">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="487d0-355">Start date</span></span> | <span data-ttu-id="487d0-356">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-356">Accrual amount</span></span> | <span data-ttu-id="487d0-357">Обработка начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-357">Process accrual</span></span> | <span data-ttu-id="487d0-358">Баланс</span><span class="sxs-lookup"><span data-stu-id="487d0-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="487d0-359">Jeannette Nicholson (Джанет Никольсон)</span><span class="sxs-lookup"><span data-stu-id="487d0-359">Jeannette Nicholson</span></span> | <span data-ttu-id="487d0-360">0,00</span><span class="sxs-lookup"><span data-stu-id="487d0-360">0.00</span></span>              | <span data-ttu-id="487d0-361">01.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-361">6/1/2018</span></span>        | <span data-ttu-id="487d0-362">01.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-362">6/1/2018</span></span>   | <span data-ttu-id="487d0-363">1.00</span><span class="sxs-lookup"><span data-stu-id="487d0-363">1.00</span></span>           | <span data-ttu-id="487d0-364">01.09.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-364">9/1/2018</span></span>        | <span data-ttu-id="487d0-365">3,00</span><span class="sxs-lookup"><span data-stu-id="487d0-365">3.00</span></span>    |
| <span data-ttu-id="487d0-366">Jay Norman (Джей Норман)</span><span class="sxs-lookup"><span data-stu-id="487d0-366">Jay Norman</span></span>          | <span data-ttu-id="487d0-367">0,00</span><span class="sxs-lookup"><span data-stu-id="487d0-367">0.00</span></span>              | <span data-ttu-id="487d0-368">15.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-368">6/15/2018</span></span>       | <span data-ttu-id="487d0-369">15.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-369">6/15/2018</span></span>  | <span data-ttu-id="487d0-370">1.00</span><span class="sxs-lookup"><span data-stu-id="487d0-370">1.00</span></span>           | <span data-ttu-id="487d0-371">01.09.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-371">9/1/2018</span></span>        | <span data-ttu-id="487d0-372">2.53</span><span class="sxs-lookup"><span data-stu-id="487d0-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="487d0-373">Ежемесячный план с полным начислением</span><span class="sxs-lookup"><span data-stu-id="487d0-373">Full accrual monthly plan</span></span>

<span data-ttu-id="487d0-374">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-374">**Plan setup**</span></span>

| <span data-ttu-id="487d0-375">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-375">Plan start date</span></span> | <span data-ttu-id="487d0-376">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-376">Accrual frequency</span></span> | <span data-ttu-id="487d0-377">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="487d0-378">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-378">1/1/2018</span></span>        | <span data-ttu-id="487d0-379">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="487d0-379">Monthly</span></span>           | <span data-ttu-id="487d0-380">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-380">Plan start date</span></span>      |

<span data-ttu-id="487d0-381">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-381">**Results**</span></span>

| <span data-ttu-id="487d0-382">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="487d0-382">Employee</span></span>            | <span data-ttu-id="487d0-383">Месяцы службы</span><span class="sxs-lookup"><span data-stu-id="487d0-383">Months of service</span></span> | <span data-ttu-id="487d0-384">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-384">Enrollment date</span></span> | <span data-ttu-id="487d0-385">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="487d0-385">Start date</span></span> | <span data-ttu-id="487d0-386">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-386">Accrual amount</span></span> | <span data-ttu-id="487d0-387">Обработка начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-387">Process accrual</span></span> | <span data-ttu-id="487d0-388">Баланс</span><span class="sxs-lookup"><span data-stu-id="487d0-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="487d0-389">Jeannette Nicholson (Джанет Никольсон)</span><span class="sxs-lookup"><span data-stu-id="487d0-389">Jeannette Nicholson</span></span> | <span data-ttu-id="487d0-390">0,00</span><span class="sxs-lookup"><span data-stu-id="487d0-390">0.00</span></span>              | <span data-ttu-id="487d0-391">01.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-391">6/1/2018</span></span>        | <span data-ttu-id="487d0-392">01.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-392">6/1/2018</span></span>   | <span data-ttu-id="487d0-393">1.00</span><span class="sxs-lookup"><span data-stu-id="487d0-393">1.00</span></span>           | <span data-ttu-id="487d0-394">01.09.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-394">9/1/2018</span></span>        | <span data-ttu-id="487d0-395">3,00</span><span class="sxs-lookup"><span data-stu-id="487d0-395">3.00</span></span>    |
| <span data-ttu-id="487d0-396">Jay Norman (Джей Норман)</span><span class="sxs-lookup"><span data-stu-id="487d0-396">Jay Norman</span></span>          | <span data-ttu-id="487d0-397">0,00</span><span class="sxs-lookup"><span data-stu-id="487d0-397">0.00</span></span>              | <span data-ttu-id="487d0-398">15.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-398">6/15/2018</span></span>       | <span data-ttu-id="487d0-399">15.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-399">6/15/2018</span></span>  | <span data-ttu-id="487d0-400">1.00</span><span class="sxs-lookup"><span data-stu-id="487d0-400">1.00</span></span>           | <span data-ttu-id="487d0-401">01.09.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-401">9/1/2018</span></span>        | <span data-ttu-id="487d0-402">3,00</span><span class="sxs-lookup"><span data-stu-id="487d0-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="487d0-403">Ежемесячный план без начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-403">No accrual monthly plan</span></span>

<span data-ttu-id="487d0-404">**Настройка плана**</span><span class="sxs-lookup"><span data-stu-id="487d0-404">**Plan setup**</span></span>

| <span data-ttu-id="487d0-405">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-405">Plan start date</span></span> | <span data-ttu-id="487d0-406">Частота начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-406">Accrual frequency</span></span> | <span data-ttu-id="487d0-407">Базис периода начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="487d0-408">01.01.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-408">1/1/2018</span></span>        | <span data-ttu-id="487d0-409">ежемесячно</span><span class="sxs-lookup"><span data-stu-id="487d0-409">Monthly</span></span>           | <span data-ttu-id="487d0-410">Дата начала плана</span><span class="sxs-lookup"><span data-stu-id="487d0-410">Plan start date</span></span>      |

<span data-ttu-id="487d0-411">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="487d0-411">**Results**</span></span>

| <span data-ttu-id="487d0-412">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="487d0-412">Employee</span></span>            | <span data-ttu-id="487d0-413">Месяцы службы</span><span class="sxs-lookup"><span data-stu-id="487d0-413">Months of service</span></span> | <span data-ttu-id="487d0-414">Дата регистрации</span><span class="sxs-lookup"><span data-stu-id="487d0-414">Enrollment date</span></span> | <span data-ttu-id="487d0-415">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="487d0-415">Start date</span></span> | <span data-ttu-id="487d0-416">Сумма начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-416">Accrual amount</span></span> | <span data-ttu-id="487d0-417">Обработка начисления</span><span class="sxs-lookup"><span data-stu-id="487d0-417">Process accrual</span></span> | <span data-ttu-id="487d0-418">Баланс</span><span class="sxs-lookup"><span data-stu-id="487d0-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="487d0-419">Jeannette Nicholson (Джанет Никольсон)</span><span class="sxs-lookup"><span data-stu-id="487d0-419">Jeannette Nicholson</span></span> | <span data-ttu-id="487d0-420">0,00</span><span class="sxs-lookup"><span data-stu-id="487d0-420">0.00</span></span>              | <span data-ttu-id="487d0-421">01.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-421">6/1/2018</span></span>        | <span data-ttu-id="487d0-422">01.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-422">6/1/2018</span></span>   | <span data-ttu-id="487d0-423">1.00</span><span class="sxs-lookup"><span data-stu-id="487d0-423">1.00</span></span>           | <span data-ttu-id="487d0-424">01.09.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-424">9/1/2018</span></span>        | <span data-ttu-id="487d0-425">3,00</span><span class="sxs-lookup"><span data-stu-id="487d0-425">3.00</span></span>    |
| <span data-ttu-id="487d0-426">Jay Norman (Джей Норман)</span><span class="sxs-lookup"><span data-stu-id="487d0-426">Jay Norman</span></span>          | <span data-ttu-id="487d0-427">0,00</span><span class="sxs-lookup"><span data-stu-id="487d0-427">0.00</span></span>              | <span data-ttu-id="487d0-428">15.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-428">6/15/2018</span></span>       | <span data-ttu-id="487d0-429">15.06.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-429">6/15/2018</span></span>  | <span data-ttu-id="487d0-430">1.00</span><span class="sxs-lookup"><span data-stu-id="487d0-430">1.00</span></span>           | <span data-ttu-id="487d0-431">01.09.2018</span><span class="sxs-lookup"><span data-stu-id="487d0-431">9/1/2018</span></span>        | <span data-ttu-id="487d0-432">2.00</span><span class="sxs-lookup"><span data-stu-id="487d0-432">2.00</span></span>    |

