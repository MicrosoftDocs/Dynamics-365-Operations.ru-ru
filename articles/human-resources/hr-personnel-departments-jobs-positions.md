---
title: Организация трудовых ресурсов с помощью подразделений, должностей и штатных единиц
description: Подразделения, задания и должности — организационные элементы, которые поддерживаются в модуле « управление персоналом «. Эта статья содержит общие сведения об этих элементах.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e1dace0dc6477e259d1004440c4cda8060bf90e3
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130237"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="4fbd7-104">Организация трудовых ресурсов с использованием подразделений, должностей и штатных единиц</span><span class="sxs-lookup"><span data-stu-id="4fbd7-104">Organize your workforce by using departments, jobs, and positions</span></span>

<span data-ttu-id="4fbd7-105">Подразделения, задания и должности — организационные элементы, которые поддерживаются в модуле « управление персоналом «.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="4fbd7-106">Эта статья содержит общие сведения об этих элементах.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-106">This article describes conceptual information about these elements.</span></span> 

<span data-ttu-id="4fbd7-107">Следующий пример использован для того, чтобы проиллюстрировать концепции, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-107">The following example is used to illustrate the concepts described in this article.</span></span>

|<span data-ttu-id="4fbd7-108">**Отдел**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-108">**Department**</span></span>|<span data-ttu-id="4fbd7-109">**Занимаемая должность**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-109">**Position**</span></span>|<span data-ttu-id="4fbd7-110">**Задание**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="4fbd7-111">**Прод.**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-111">**Sales**</span></span>|<span data-ttu-id="4fbd7-112">Менеджер по продажам (восток)</span><span class="sxs-lookup"><span data-stu-id="4fbd7-112">Sales manager (East)</span></span>|<span data-ttu-id="4fbd7-113">Менеджер по продажам</span><span class="sxs-lookup"><span data-stu-id="4fbd7-113">Sales manager</span></span>|
|<span data-ttu-id="4fbd7-114">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-114">**Sales**</span></span>|<span data-ttu-id="4fbd7-115">Менеджер по продажам (запад)</span><span class="sxs-lookup"><span data-stu-id="4fbd7-115">Sales manager (West)</span></span>|<span data-ttu-id="4fbd7-116">Менеджер по продажам</span><span class="sxs-lookup"><span data-stu-id="4fbd7-116">Sales manager</span></span>|
|<span data-ttu-id="4fbd7-117">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-117">**Sales**</span></span>|<span data-ttu-id="4fbd7-118">Менеджер по продажам (центр)</span><span class="sxs-lookup"><span data-stu-id="4fbd7-118">Sales manager (Central)</span></span>|<span data-ttu-id="4fbd7-119">Менеджер по продажам</span><span class="sxs-lookup"><span data-stu-id="4fbd7-119">Sales manager</span></span>|
|<span data-ttu-id="4fbd7-120">**Учет**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-120">**Accounting**</span></span>|<span data-ttu-id="4fbd7-121">Супервизор по учету</span><span class="sxs-lookup"><span data-stu-id="4fbd7-121">Accounting supervisor</span></span>|<span data-ttu-id="4fbd7-122">Главный бухгалтер</span><span class="sxs-lookup"><span data-stu-id="4fbd7-122">Accounting manager</span></span>|
|<span data-ttu-id="4fbd7-123">**Учет**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-123">**Accounting**</span></span>|<span data-ttu-id="4fbd7-124">Учет-A</span><span class="sxs-lookup"><span data-stu-id="4fbd7-124">Accounting-A</span></span>|<span data-ttu-id="4fbd7-125">Бухгалтер</span><span class="sxs-lookup"><span data-stu-id="4fbd7-125">Accountant</span></span>|
|<span data-ttu-id="4fbd7-126">**Управление персоналом**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-126">**Human resources**</span></span>|<span data-ttu-id="4fbd7-127">Менеджер по персоналу (восток)</span><span class="sxs-lookup"><span data-stu-id="4fbd7-127">HR manager (East)</span></span>|<span data-ttu-id="4fbd7-128">Менеджер по персоналу</span><span class="sxs-lookup"><span data-stu-id="4fbd7-128">HR manager</span></span>|
|<span data-ttu-id="4fbd7-129">**Управление персоналом**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-129">**Human resources**</span></span>|<span data-ttu-id="4fbd7-130">Менеджер по персоналу (запад)</span><span class="sxs-lookup"><span data-stu-id="4fbd7-130">HR manager (West)</span></span>|<span data-ttu-id="4fbd7-131">Менеджер по персоналу</span><span class="sxs-lookup"><span data-stu-id="4fbd7-131">HR manager</span></span>|
|<span data-ttu-id="4fbd7-132">**Управление персоналом**</span><span class="sxs-lookup"><span data-stu-id="4fbd7-132">**Human resources**</span></span>|<span data-ttu-id="4fbd7-133">Менеджер по персоналу (центр)</span><span class="sxs-lookup"><span data-stu-id="4fbd7-133">HR manager (Central)</span></span>|<span data-ttu-id="4fbd7-134">Менеджер по персоналу</span><span class="sxs-lookup"><span data-stu-id="4fbd7-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="4fbd7-135">Отделы</span><span class="sxs-lookup"><span data-stu-id="4fbd7-135">Departments</span></span>
------------

<span data-ttu-id="4fbd7-136">Подразделение — операционная единица, которая представляет собой категорию или функциональную зону организации, ответственную за конкретную область организации, например за продажи или учет.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="4fbd7-137">Подразделение используется для создания отчетов по функциональным областям и может иметь ответственность за прибыль и убытки.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="4fbd7-138">Кроме того, Подразделение может включать группу центров затрат.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="4fbd7-139">Продажи, учет, и управление персоналом — некоторые примеры подразделений в организации.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="4fbd7-140">Задания и должности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-140">Jobs and positions</span></span>
<span data-ttu-id="4fbd7-141">Задание — это набор задач и обязанностей, которые возлагаются на занимающее эту задание лицо.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="4fbd7-142">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="4fbd7-143">Области ответственности, задачи по заданию, функциональные обязанности, навыки, сведения об образовании, и сертификаты, которые требуются для задания, также необходимы для должностей, связанных с заданием.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="4fbd7-144">Задачи задания</span><span class="sxs-lookup"><span data-stu-id="4fbd7-144">Job tasks</span></span>

<span data-ttu-id="4fbd7-145">Можно создать задачи задания, которые описывают основные задачи, которые работник в должности этого задания должен выполнять.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="4fbd7-146">Одну и ту же задачи по заданию можно добавить к нескольким заданиям, и должности для этих заданий унаследуют эти задачи по заданию.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="4fbd7-147">Примеры задач заданий приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4fbd7-148">Задание</span><span class="sxs-lookup"><span data-stu-id="4fbd7-148">Job</span></span></th>
<th><span data-ttu-id="4fbd7-149">Задача задания</span><span class="sxs-lookup"><span data-stu-id="4fbd7-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fbd7-150">Менеджер по продажам</span><span class="sxs-lookup"><span data-stu-id="4fbd7-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="4fbd7-151"><span class="input">Обзор производительности</span> – обзор производительности задания каждого продавца.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="4fbd7-152"><span class="input">Обзор отсутствия</span> – утверждение или отклонение запросов или регистраций отсутствий каждого продавца.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fbd7-153">Бухгалтер</span><span class="sxs-lookup"><span data-stu-id="4fbd7-153">Accountant</span></span></td>
<td><span data-ttu-id="4fbd7-154"><span class="input">Фин. отчет</span> – представить недельные финансовых отчеты главному финансовому директору.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="4fbd7-155">Должностные функции</span><span class="sxs-lookup"><span data-stu-id="4fbd7-155">Job functions</span></span>

<span data-ttu-id="4fbd7-156">функциональные обязанности — как задачи по заданию.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-156">Job functions are like job tasks.</span></span> <span data-ttu-id="4fbd7-157">Функциональная обязанность описывает одну или несколько задач, обязанностей или ответственностей, которые присваиваются заданию.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="4fbd7-158">Функциональные обязанности можно назначить к заданиям и использовать для настройки и реализации правил приемлемости для Планов компенсационных выплат.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="4fbd7-159">Примеры функциональных обязанностей приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="4fbd7-160">Задание</span><span class="sxs-lookup"><span data-stu-id="4fbd7-160">Job</span></span>           | <span data-ttu-id="4fbd7-161">Должностные функции</span><span class="sxs-lookup"><span data-stu-id="4fbd7-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="4fbd7-162">Менеджер по продажам</span><span class="sxs-lookup"><span data-stu-id="4fbd7-162">Sales manager</span></span> | <span data-ttu-id="4fbd7-163">Упр. люди – управление людьми, которые подчиняются вам.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="4fbd7-164">Бухгалтер</span><span class="sxs-lookup"><span data-stu-id="4fbd7-164">Accountant</span></span>    | <span data-ttu-id="4fbd7-165">Фин. обзор – управление финансовыми данными для набора счетов.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="4fbd7-166">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="4fbd7-166">Job types</span></span>

<span data-ttu-id="4fbd7-167">Используйте типы заданий для классификации похожих заданий в категории.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="4fbd7-168">Типы задания, как и функциональные обязанности, можно назначить к заданиям и использовать для настройки и реализации правил приемлемости для Планов компенсационных выплат.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="4fbd7-169">В следующем списке содержатся некоторые примеры типов заданий.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="4fbd7-170">полная занятость</span><span class="sxs-lookup"><span data-stu-id="4fbd7-170">Full-time</span></span>
-   <span data-ttu-id="4fbd7-171">частичная занятость</span><span class="sxs-lookup"><span data-stu-id="4fbd7-171">Part-time</span></span>
-   <span data-ttu-id="4fbd7-172">Зарплата</span><span class="sxs-lookup"><span data-stu-id="4fbd7-172">Salary</span></span>
-   <span data-ttu-id="4fbd7-173">Почасовая оплата</span><span class="sxs-lookup"><span data-stu-id="4fbd7-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="4fbd7-174">Области ответственности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-174">Areas of responsibility</span></span>

<span data-ttu-id="4fbd7-175">Используйте области ответственности, чтобы показать рабочие роли, процессы и продукты, за которые сотрудник в должности по этому заданию является ответственным.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="4fbd7-176">Пример области ответственности для задания «Бухгалтер» может быть «Финансовая отчетность по продукту А».</span><span class="sxs-lookup"><span data-stu-id="4fbd7-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="4fbd7-177">Должности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-177">Positions</span></span>
----------

<span data-ttu-id="4fbd7-178">Должности являются важным элементом нижнего уровня организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="4fbd7-179">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="4fbd7-180">Например, должность «Менеджер по продажам (восток)» — это одна из должностей, связанных с общей должностью, «Менеджер по продажам».</span><span class="sxs-lookup"><span data-stu-id="4fbd7-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="4fbd7-181">Должности существуют в подразделениях и назначены работникам.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="4fbd7-182">Создание и обслуживание должностей</span><span class="sxs-lookup"><span data-stu-id="4fbd7-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="4fbd7-183">Можно просмотреть историю системных изменений, связанных с должностью, на удобной странице списка.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="4fbd7-184">Можно создать коды причин, которые пользователи могут выбирать при создании или изменении должности.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="4fbd7-185">Можно создать типы действий персонала и назначить номерную серию к действиям сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="4fbd7-186">Можно настроить workflow-процесс, чтобы добавления и изменения должностей требовали утверждения.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="4fbd7-187">Период должности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-187">Position duration</span></span>

<span data-ttu-id="4fbd7-188">Каждое должность имеет период времени, в течение которого должность эффективна.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="4fbd7-189">Этот период времени называется Продолжительность.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="4fbd7-190">Например, летние должности могут иметь длительность с 1 мая 2015 до 31 августа 2015.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="4fbd7-191">Назначения работников</span><span class="sxs-lookup"><span data-stu-id="4fbd7-191">Worker assignments</span></span>

<span data-ttu-id="4fbd7-192">При назначении работника на должность, вы заполняете эту должность.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="4fbd7-193">Можно назначить работников по нескольким должностям, но только один работник может быть назначен на одну должность одновременно.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="4fbd7-194">Отношения отчетности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-194">Reporting relationships</span></span>

<span data-ttu-id="4fbd7-195">Должности являются важными элементами нижнего уровня организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="4fbd7-196">В форме "Должность" можно определить должность, относительно которой должность является подотчетной.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="4fbd7-197">При назначении работника на должность, подотчетную другой должности, создается отчетная связь между работниками, назначенными на две должности.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="4fbd7-198">Например, должность «Бухгалтер А» отчитывается должности «Супервизор по учету».</span><span class="sxs-lookup"><span data-stu-id="4fbd7-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="4fbd7-199">Ким Акерс назначен на должность «Супервизор по учету» и Сергей Пател назначен на должность «Бухгалтер А».</span><span class="sxs-lookup"><span data-stu-id="4fbd7-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="4fbd7-200">Это означает, что Сергей Пател является подотчетной по отношению к Ким Акерс.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="4fbd7-201">Если ваша организация использует матричную иерархию или другую специальную иерархию, можно настроить типы иерархии должностей и затем добавить отношения подотчетности для должностей для каждого настроенного типа иерархии.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="4fbd7-202">Например, Лори Пенор — генеральный менеджер в Adventure Works и назначен на должность «Генеральный менеджер».</span><span class="sxs-lookup"><span data-stu-id="4fbd7-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="4fbd7-203">Лори управляет развитием продукта, который используется, чтобы чистить устройства.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="4fbd7-204">Лори требуется бухгалтер, который помогает ему с финансами для разработки продукта.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-204">Lori requires an accountant to help her with the finances for developing the product.</span></span> <span data-ttu-id="4fbd7-205">Поэтому он нанимает Сергея Пател, в качестве его бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-205">Therefore, she has recruited Sanjay Patel to be her accountant.</span></span> <span data-ttu-id="4fbd7-206">Сергей отчитывается непосредственно Киму Акерсу, но также работает с Лори Пенор по поводу финансов для разработки очистителя устройств.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="4fbd7-207">Для предыдущего примера, нужно выполнить следующие задачи для настройки рабочих отношений между Сергеем Пател и Лори Пенор:</span><span class="sxs-lookup"><span data-stu-id="4fbd7-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="4fbd7-208">Создать настраиваемый тип иерархии должностей «Устройство», чтобы создать иерархию, которая включает должности ответственные за работу по продукту очистителя устройств.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="4fbd7-209">Назначить должность генерального менеджера на должность, которой отчитывается должность Бухгалтер А в иерархии «Устройство».</span><span class="sxs-lookup"><span data-stu-id="4fbd7-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="4fbd7-210">Используйте иерархию должностей для просмотра структуры подотчетности должностей.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="4fbd7-211">Если имеется несколько иерархией должностей, можно просмотреть иерархию для каждого типа иерархии в иерархии должностей.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="4fbd7-212">Также можно найти должности по коду должности или по имени работника, который назначен на должность.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="4fbd7-213">Иерархия должностей — это организационная иерархия.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="4fbd7-214">Записи дат вступления в силу</span><span class="sxs-lookup"><span data-stu-id="4fbd7-214">Date effective records</span></span>
<span data-ttu-id="4fbd7-215">Для некоторых записей, можно указать будущие изменения в запись.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="4fbd7-216">Для Следующей информации действует дата.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4fbd7-217">Записи</span><span class="sxs-lookup"><span data-stu-id="4fbd7-217">Records</span></span></th>
<th><span data-ttu-id="4fbd7-218">Сведения о дате вступления в силу</span><span class="sxs-lookup"><span data-stu-id="4fbd7-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fbd7-219">Задания</span><span class="sxs-lookup"><span data-stu-id="4fbd7-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="4fbd7-220">Некоторые подробные сведения о задании</span><span class="sxs-lookup"><span data-stu-id="4fbd7-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="4fbd7-221">Сведения о классификации заданий</span><span class="sxs-lookup"><span data-stu-id="4fbd7-221">Job classification information</span></span></li>
<li><span data-ttu-id="4fbd7-222">Информация о компенсации</span><span class="sxs-lookup"><span data-stu-id="4fbd7-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fbd7-223">Должности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="4fbd7-224">Некоторые подробные сведения о должности</span><span class="sxs-lookup"><span data-stu-id="4fbd7-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="4fbd7-225">Назначения работников</span><span class="sxs-lookup"><span data-stu-id="4fbd7-225">Worker assignments</span></span></li>
<li><span data-ttu-id="4fbd7-226">Периоды должностей</span><span class="sxs-lookup"><span data-stu-id="4fbd7-226">Position durations</span></span></li>
<li><span data-ttu-id="4fbd7-227">Иерархия должностей</span><span class="sxs-lookup"><span data-stu-id="4fbd7-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4fbd7-228">Можно изменять информацию, указанную в предыдущей таблице, для должности или задания, и указать дату, когда изменения должности или задания должны вступить в силу.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="4fbd7-229">Например, должность может быть назначена только одному работнику, но Сергей Пател, которому назначена должность Бухгалтер А, уходит через 2 недели.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="4fbd7-230">Джо Хили заменит Сергея Патела когда он уйдет.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-230">Joe Healy will replace Sanjay Patel when he leaves.</span></span> <span data-ttu-id="4fbd7-231">Даже если Сергей все еще назначен для его должности, можно назначить Джо Хили на эту же должность так, что назначение будет действовать только после последнего дня Сергея.</span><span class="sxs-lookup"><span data-stu-id="4fbd7-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>





