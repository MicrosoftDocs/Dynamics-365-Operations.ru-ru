---
title: "Планы компенсации"
description: "Менеджеры по компенсациям и льготам могут использовать управление компенсациями для ведения и для обработки планов фиксированной и переменной компенсации для сотрудников организации."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e80b3ebc9c374073ff5a2dfc8c2acf1d7f6c6287
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="compensation-plans"></a><span data-ttu-id="17fbc-103">Планы компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-103">Compensation plans</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17fbc-104">Менеджеры по компенсациям и льготам могут использовать управление компенсациями для ведения и для обработки планов фиксированной и переменной компенсации для сотрудников организации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="17fbc-105">Введение</span><span class="sxs-lookup"><span data-stu-id="17fbc-105">Introduction</span></span>

<span data-ttu-id="17fbc-106">Управление компенсациями используется для управления предоставлением базовой оплаты и вознаграждений.</span><span class="sxs-lookup"><span data-stu-id="17fbc-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="17fbc-107">Тарифные ставки и единовременные надбавки контролируются с помощью планов фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="17fbc-108">Поощрительные выплаты, такие как премии, вознаграждения за производительность, опционы на покупку акций и гранты, а также одноразовые компенсации, контролируются с помощью планов переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="17fbc-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="17fbc-109">Сотрудники могут участвовать в одном или нескольких планах обоих типов.</span><span class="sxs-lookup"><span data-stu-id="17fbc-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="17fbc-110">Сотрудник должен отвечать следующим требованиям, чтобы иметь право на регистрацию в плане компенсации:</span><span class="sxs-lookup"><span data-stu-id="17fbc-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="17fbc-111">Сотрудник должен иметь назначение активной позиции.</span><span class="sxs-lookup"><span data-stu-id="17fbc-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="17fbc-112">Сотрудник должен удовлетворять критериям, которые определяются правилами соответствия для плана компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="17fbc-113">Настройка компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-113">Compensation setup</span></span>
<span data-ttu-id="17fbc-114">В следующей таблице перечислены компоненты процесса компенсации, которые можно использовать для настройки планов компенсации вашей компании.</span><span class="sxs-lookup"><span data-stu-id="17fbc-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="17fbc-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="17fbc-115">Component</span></span></th>
<th><span data-ttu-id="17fbc-116">Дополнительные сведения...</span><span class="sxs-lookup"><span data-stu-id="17fbc-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17fbc-117">Действия по постоянному вознаграждению.</span><span class="sxs-lookup"><span data-stu-id="17fbc-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="17fbc-118">Действия по фиксированной компенсации имеют две цели:</span><span class="sxs-lookup"><span data-stu-id="17fbc-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="17fbc-119">Действия могут определять вид информации, которая должна быть зарегистрирована при изменении компенсации сотрудника.</span><span class="sxs-lookup"><span data-stu-id="17fbc-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="17fbc-120">Например, вы можете требовать, чтобы была записана причина изменения, например повышение или понижение в должности.</span><span class="sxs-lookup"><span data-stu-id="17fbc-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="17fbc-121">Действия могут обеспечить, чтобы вычисление применялось при обработке фиксированных планов компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="17fbc-122">Например, действия типа "Справедливость" сравнивают оплату сотрудников с минимальной контрольной точкой для уровня сотрудников и обеспечивают, что сотрудник получает по крайней мере минимальную оплату.</span><span class="sxs-lookup"><span data-stu-id="17fbc-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-123">Уровни</span><span class="sxs-lookup"><span data-stu-id="17fbc-123">Levels</span></span></td>
<td><span data-ttu-id="17fbc-124">Уровни связаны с заданиями и любыми позициями, связанными со ссылкой на задание.</span><span class="sxs-lookup"><span data-stu-id="17fbc-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="17fbc-125">Можно создать отдельные уровни для трех типов планов компенсации: "Уровень", "Полоса" и "Шаг".</span><span class="sxs-lookup"><span data-stu-id="17fbc-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-126">Матрица диапазона утилизации</span><span class="sxs-lookup"><span data-stu-id="17fbc-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="17fbc-127">Матрица использования диапазона позволяет переводить сотрудников на контрольную точку для соответствующих заданий.</span><span class="sxs-lookup"><span data-stu-id="17fbc-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="17fbc-128">Использование диапазона применяется также для управления собственным капиталом ставки зарплаты в компании, независимо от производительности отдельного сотрудника или всей компании.</span><span class="sxs-lookup"><span data-stu-id="17fbc-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="17fbc-129">Например, сотрудники, получающие оплату меньше в своем диапазоне, получают больший процент повышения чем сотрудники, получающие более высокую оплату в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="17fbc-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="17fbc-130">Таким образом, можно систематически компенсировать разницу собственного капитала.</span><span class="sxs-lookup"><span data-stu-id="17fbc-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="17fbc-131">Использование диапазона вычисляется следующим образом: (Фиксированная ставка зарплаты - минимум диапазона) ÷ (максимум диапазона - минимум диапазона).</span><span class="sxs-lookup"><span data-stu-id="17fbc-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-132">Настройки точек отсчета</span><span class="sxs-lookup"><span data-stu-id="17fbc-132">Reference point setups</span></span></td>
<td><span data-ttu-id="17fbc-133">Настройка точки отсчета включает набор точек отсчета, представляющих в матрице диапазоны.</span><span class="sxs-lookup"><span data-stu-id="17fbc-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="17fbc-134">Каждый диапазон может быть связан со ставкой оплаты.</span><span class="sxs-lookup"><span data-stu-id="17fbc-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="17fbc-135">Например, планы типа "Уровень" часто будут иметь контрольные точки минимума, средней точки и максимума.</span><span class="sxs-lookup"><span data-stu-id="17fbc-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-136">Матрица компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="17fbc-137">Матрица компенсации — это набор опорных точек и уровней, которые используются для создания структуры компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-138">Структура компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-138">Compensation structure</span></span></td>
<td><span data-ttu-id="17fbc-139">Структура компенсации — это матрица компенсации, которая имеет ставки зарплаты, связанные с контрольными точками для каждого уровня.</span><span class="sxs-lookup"><span data-stu-id="17fbc-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-140">Правила приемлемости</span><span class="sxs-lookup"><span data-stu-id="17fbc-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="17fbc-141">Правила проверки годности используются для выявления сотрудников на конкретных должностях, функциональных обязанностях, типах работ, подразделениях, профсоюзах и регионах компенсации, покрываемых конкретными планами компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="17fbc-142">Вы должны создать правила применимости как для переменных, так и для фиксированных планов компенсации, чтобы зарегистрировать сотрудников в плане.</span><span class="sxs-lookup"><span data-stu-id="17fbc-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="17fbc-143">После определения правил применимости для плана компенсаций можно определить множество уровней, которые должны применяться к работам, охватываемым данным планом.</span><span class="sxs-lookup"><span data-stu-id="17fbc-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-144">Частота платежей</span><span class="sxs-lookup"><span data-stu-id="17fbc-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="17fbc-145">Периодичность оплаты используется, чтобы определить период времени, для которого указана компенсация.</span><span class="sxs-lookup"><span data-stu-id="17fbc-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="17fbc-146">Например, частота оплаты помогает понять, указана ли сумма компенсации как годовая заработная плата или как часовая ставка.</span><span class="sxs-lookup"><span data-stu-id="17fbc-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="17fbc-147">Периодичность оплаты также используется для настройки коэффициентов пересчета сумм, чтобы преобразовать компенсацию из ежемесячной, еженедельной, двухнедельной и почасовой оплаты в годовую оплату.</span><span class="sxs-lookup"><span data-stu-id="17fbc-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-148">Регионы компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-148">Compensation regions</span></span></td>
<td><span data-ttu-id="17fbc-149">Регионы компенсации используются, чтобы определить компенсацию сотрудника с учетом расположения рабочего места.</span><span class="sxs-lookup"><span data-stu-id="17fbc-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-150">Контрольная точка</span><span class="sxs-lookup"><span data-stu-id="17fbc-150">Control point</span></span></td>
<td><span data-ttu-id="17fbc-151">Контрольная точка определяет, что считается идеальной ставкой зарплаты для всех сотрудников на уровне компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="17fbc-152">Для ступенчатых структур планов контрольные точки являются обычно средней точкой диапазона.</span><span class="sxs-lookup"><span data-stu-id="17fbc-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="17fbc-153">Лентообразные структуры редко используют контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="17fbc-153">Band structures rarely use control points.</span></span> <span data-ttu-id="17fbc-154">Можно определить контрольную точку для плана фиксированной компенсации в форме "Планы постоянного вознаграждения".</span><span class="sxs-lookup"><span data-stu-id="17fbc-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-155">Должностные функции</span><span class="sxs-lookup"><span data-stu-id="17fbc-155">Job functions</span></span></td>
<td><span data-ttu-id="17fbc-156">Должностные функции используются для классификации и фильтрации планов компенсации для конкретных должностей.</span><span class="sxs-lookup"><span data-stu-id="17fbc-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-157">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="17fbc-157">Job types</span></span></td>
<td><span data-ttu-id="17fbc-158">Типы должностей используются для классификации и фильтрации планов компенсации для конкретных должностей.</span><span class="sxs-lookup"><span data-stu-id="17fbc-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-159">Типы дополнительного вознаграждения</span><span class="sxs-lookup"><span data-stu-id="17fbc-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="17fbc-160">Типы переменных компенсаций, такие как компенсация в виде ценных бумаг или премия в виде денежного вознаграждения, настраиваются в планах переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="17fbc-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-161">Сетка компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-161">Compensation grids</span></span></td>
<td><span data-ttu-id="17fbc-162">Сетка компенсаций содержит структуру компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="17fbc-163">Сетки компенсаций могут использоваться в одном или нескольких планах компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17fbc-164">Планы производительности</span><span class="sxs-lookup"><span data-stu-id="17fbc-164">Performance plans</span></span></td>
<td><span data-ttu-id="17fbc-165">Планы производительности используются для связи производительности с матрицей распределения, чтобы можно было использовать план в стратегии оплаты по производительности.</span><span class="sxs-lookup"><span data-stu-id="17fbc-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17fbc-166">Оценки производительности</span><span class="sxs-lookup"><span data-stu-id="17fbc-166">Performance ratings</span></span></td>
<td><span data-ttu-id="17fbc-167">Рейтинги производительности используются в планах производительности, чтобы определить сумму вознаграждения за заслуги или вознаграждения за производительность.</span><span class="sxs-lookup"><span data-stu-id="17fbc-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="17fbc-168">События процесса</span><span class="sxs-lookup"><span data-stu-id="17fbc-168">Process events</span></span>
<span data-ttu-id="17fbc-169">Событие процесса рассчитывает данные компенсации для конкретного периода для всех сотрудников, которые зарегистрированы для одного или нескольких планов фиксированных или переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="17fbc-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="17fbc-170">Событие процесса можно запускать неоднократно, например, чтобы проверить или обновить результаты компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="17fbc-171">События компенсации</span><span class="sxs-lookup"><span data-stu-id="17fbc-171">Compensation events</span></span>
-------------------

<span data-ttu-id="17fbc-172">При каждом запуске события процесса создается событие компенсации.</span><span class="sxs-lookup"><span data-stu-id="17fbc-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="17fbc-173">События компенсации содержат результаты процесса компенсации для каждого сотрудника, включенного в это событие процесса.</span><span class="sxs-lookup"><span data-stu-id="17fbc-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="17fbc-174">Если расчеты правильны, можно загрузить событие компенсации, чтобы обновить записи компенсации для сотрудников, на которых повлияло событие процесса.</span><span class="sxs-lookup"><span data-stu-id="17fbc-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="17fbc-175">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="17fbc-175">Recommendations</span></span>
<span data-ttu-id="17fbc-176">После выполнения события процесса можно рекомендовать корректировки к надбавке к зарплате за успешную работу или сумме вознаграждения сотрудника на основе расчетных инструкций события процесса.</span><span class="sxs-lookup"><span data-stu-id="17fbc-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="17fbc-177">Для создания рекомендаций для сотрудников необходимо включить рекомендаций при настройке планов компенсации настройки или при настройке события процесса.</span><span class="sxs-lookup"><span data-stu-id="17fbc-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




