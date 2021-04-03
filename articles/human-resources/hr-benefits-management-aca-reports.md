---
title: Создание отчетов по закону США о доступном медицинском обслуживании в управлении льготами
description: В этом разделе описывается, каким образом управление льготами помогает отслеживать информацию, о которой сообщается в форме 1095-B и форме 1095-C для мандата работодателя по закону США о доступном медицинском обслуживании (ACA).
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 24df18f428e4ca14859bc34048a6bda5e03d1b2f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464382"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="646de-103">Создание отчетов ACA в управлении льготами</span><span class="sxs-lookup"><span data-stu-id="646de-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="646de-104">Управление льготами помогает отслеживать информацию, о которой сообщается в форме 1095-B и форме 1095-C для мандата работодателя по закону США о доступном медицинском обслуживании (ACA).</span><span class="sxs-lookup"><span data-stu-id="646de-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="646de-105">Подобно возможности отчетности ACA в старой рабочей области **Льготы**, эта функция применяется только к юридическим лицам в Соединенных Штатах Америки.</span><span class="sxs-lookup"><span data-stu-id="646de-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="646de-106">Чтобы использовать эту функцию, необходимо сначала включить **Расширенное управление льготами**.</span><span class="sxs-lookup"><span data-stu-id="646de-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="646de-107">Дополнительные сведения, включая важные пояснения относительно управления льготами, см. в разделе [Включение или отключение модуля "Управление льготами"](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="646de-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="646de-108">Отчетность ACA можно использовать только в рабочей области **Управление льготами** или в старой рабочей области **Льготы**, но не в обоих областях.</span><span class="sxs-lookup"><span data-stu-id="646de-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="646de-109">Например, если вы переключились на управление льготами, отчетность ACA доступна только в рабочей области **Управление льготами**, но не в старой рабочей области **Льготы**.</span><span class="sxs-lookup"><span data-stu-id="646de-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="646de-110">При переключении на управление льготами в середине года регистрации, необходимо правильно настроить данные о сотруднике для всего года в управлении льготами.</span><span class="sxs-lookup"><span data-stu-id="646de-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="646de-111">Таким образом вы обеспечите, что вы получите точную отчетную информацию для всего года.</span><span class="sxs-lookup"><span data-stu-id="646de-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="646de-112">Начало работы</span><span class="sxs-lookup"><span data-stu-id="646de-112">Getting started</span></span>

<span data-ttu-id="646de-113">Чтобы отследить информацию для форм 1095, сначала создайте одну или несколько групп покрытия в соответствии с законом США о доступном медицинском обслуживании.</span><span class="sxs-lookup"><span data-stu-id="646de-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="646de-114">Эти группы указывают следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="646de-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="646de-115">Предложение покрытия, предоставленное сотруднику</span><span class="sxs-lookup"><span data-stu-id="646de-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="646de-116">Доля сотрудника от минимального ежемесячного вознаграждения, если затраты превышают федеральный уровень бедности</span><span class="sxs-lookup"><span data-stu-id="646de-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="646de-117">Зона безопасности Safe Harbor, которая используется работодателем, если применимо</span><span class="sxs-lookup"><span data-stu-id="646de-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="646de-118">Группы покрытия по закону США о доступном медицинском обслуживании помогают управлять этими сведениями для нескольких записей сотрудников, имеющих одинаковые условия.</span><span class="sxs-lookup"><span data-stu-id="646de-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="646de-119">Можно легко назначать группы одному или нескольким сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="646de-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="646de-120">Создание или редактирование группы покрытия по закону США о доступном медицинском обслуживании</span><span class="sxs-lookup"><span data-stu-id="646de-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="646de-121">В рабочей области **Управление льготами** выберите **Группа покрытия по закону США о доступном медицинском обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="646de-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Выбор группы покрытия по закону США о доступном медицинском обслуживании](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="646de-123">Выберите **Создать**, чтобы создать новую группу по закону США о доступном медицинском обслуживании, или **Редактировать**, чтобы изменить существующую группу.</span><span class="sxs-lookup"><span data-stu-id="646de-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Выбор создания или редактирования](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="646de-125">Задайте следующие поля.</span><span class="sxs-lookup"><span data-stu-id="646de-125">Set the following fields.</span></span>

    | <span data-ttu-id="646de-126">Поле</span><span class="sxs-lookup"><span data-stu-id="646de-126">Field</span></span> | <span data-ttu-id="646de-127">описание</span><span class="sxs-lookup"><span data-stu-id="646de-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="646de-128">ФИО</span><span class="sxs-lookup"><span data-stu-id="646de-128">Name</span></span> | <span data-ttu-id="646de-129">Ввод наименования для группы.</span><span class="sxs-lookup"><span data-stu-id="646de-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="646de-130">описание</span><span class="sxs-lookup"><span data-stu-id="646de-130">Description</span></span> | <span data-ttu-id="646de-131">Введите описание группы.</span><span class="sxs-lookup"><span data-stu-id="646de-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="646de-132">Предложение покрытия</span><span class="sxs-lookup"><span data-stu-id="646de-132">Offer of coverage</span></span> | <span data-ttu-id="646de-133">Покрытие, предлагаемое сотрудникам, их супругам или партнерам, и их иждивенцам.</span><span class="sxs-lookup"><span data-stu-id="646de-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="646de-134">Доля затрат сотрудника</span><span class="sxs-lookup"><span data-stu-id="646de-134">Employee share of cost</span></span> | <span data-ttu-id="646de-135">Сумма, за которую отвечает сотрудник.</span><span class="sxs-lookup"><span data-stu-id="646de-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="646de-136">Применимый раздел 4980H (директива Safe Harbor)</span><span class="sxs-lookup"><span data-stu-id="646de-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="646de-137">4980H Safe Harbor или код облегчения перехода.</span><span class="sxs-lookup"><span data-stu-id="646de-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="646de-138">Месяц начала плана</span><span class="sxs-lookup"><span data-stu-id="646de-138">Plan start month</span></span> | <span data-ttu-id="646de-139">Выберите календарный месяц, когда начинается год плана льгот.</span><span class="sxs-lookup"><span data-stu-id="646de-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="646de-140">Группа действительна с</span><span class="sxs-lookup"><span data-stu-id="646de-140">Group valid from</span></span> | <span data-ttu-id="646de-141">Первая дата, когда эта запись является действительной.</span><span class="sxs-lookup"><span data-stu-id="646de-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="646de-142">Группа действительна по</span><span class="sxs-lookup"><span data-stu-id="646de-142">Group valid through</span></span> | <span data-ttu-id="646de-143">Последняя дата, когда эта запись является действительной.</span><span class="sxs-lookup"><span data-stu-id="646de-143">The last date when this record is valid.</span></span> <span data-ttu-id="646de-144">Если срок окончания действия отсутствует, введите **Никогда**.</span><span class="sxs-lookup"><span data-stu-id="646de-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Создание группы покрытия](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="646de-146">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="646de-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="646de-147">Назначение нескольким сотрудникам группы покрытия по закону США о доступном медицинском обслуживании</span><span class="sxs-lookup"><span data-stu-id="646de-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="646de-148">В рабочей области **Управление льготами** выберите **Группа покрытия по закону США о доступном медицинском обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="646de-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="646de-149">Выберите группу, которой требуется назначить сотрудников.</span><span class="sxs-lookup"><span data-stu-id="646de-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="646de-150">Выберите **Массовое назначение**.</span><span class="sxs-lookup"><span data-stu-id="646de-150">Select **Mass assignment**.</span></span>

    ![Выбор массового назначения](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="646de-152">Выберите сотрудников в списке, затем выберите **Назначить**.</span><span class="sxs-lookup"><span data-stu-id="646de-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Назначение выбранных сотрудников в группу](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="646de-154">Поддержка нескольких версий вариантов покрытия</span><span class="sxs-lookup"><span data-stu-id="646de-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="646de-155">Можно поддерживать нескольких версий любой группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="646de-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="646de-156">При внесении изменений в организацию или предлагаемые льготы можно сохранить актуальность сведений о группе без необходимости создания новой группы и переназначения в нее сотрудников.</span><span class="sxs-lookup"><span data-stu-id="646de-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="646de-157">После создания групп покрытия по закону США о доступном медицинском обслуживании можно выполнить массовое назначение сотрудников.</span><span class="sxs-lookup"><span data-stu-id="646de-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="646de-158">Можно также отдельно назначить сотрудников группам и указать, будут ли данные по закону США о доступном медицинском обслуживании отслеживаться и сообщаться.</span><span class="sxs-lookup"><span data-stu-id="646de-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="646de-159">Если нет необходимости отслеживать и сообщать информацию по закону США о доступном медицинском обслуживании для сотрудника, можно установить для параметра **Сообщать о покрытии** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="646de-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="646de-160">Например, у вас могут быть сотрудники с частичной занятостью, для которых не требуется отчетность ACA.</span><span class="sxs-lookup"><span data-stu-id="646de-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="646de-161">Переопределение значений по умолчанию для сотрудника</span><span class="sxs-lookup"><span data-stu-id="646de-161">Override default values for an employee</span></span>

<span data-ttu-id="646de-162">Для сотрудников, назначенных для группы покрытия по закону США о доступном медицинском обслуживании, можно изменить следующие параметры для любых месяцев, для которых требуются другие значения:</span><span class="sxs-lookup"><span data-stu-id="646de-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="646de-163">Предложение покрытия</span><span class="sxs-lookup"><span data-stu-id="646de-163">Offer of coverage</span></span>
- <span data-ttu-id="646de-164">Доля затрат сотрудника</span><span class="sxs-lookup"><span data-stu-id="646de-164">Employee share of cost</span></span>
- <span data-ttu-id="646de-165">Применимый раздел 4980H (директива Safe Harbor)</span><span class="sxs-lookup"><span data-stu-id="646de-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="646de-166">Для отчетов ACA 2020 необходимо сообщать как рабочие, так и домашние почтовые индексы в форме 1095-C.</span><span class="sxs-lookup"><span data-stu-id="646de-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="646de-167">Значения заполняются автоматически на основе текущих активных местоположений.</span><span class="sxs-lookup"><span data-stu-id="646de-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="646de-168">Если в какой-либо части года какое-либо местоположение было другим, необходимо переопределить значение.</span><span class="sxs-lookup"><span data-stu-id="646de-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="646de-169">Поле **Почтовый индекс** (строка 17) в отчете 1095-C заполняется только в том случае , если код **Предложение покрытия** содержит **1L** через **1Q**, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="646de-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="646de-170">**1L, 1M или 1N:** основной почтовый индекс проживания</span><span class="sxs-lookup"><span data-stu-id="646de-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="646de-171">**1O, 1P, 1Q:** основной почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="646de-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="646de-172">Для ввода исключений для любых значений группы покрытия по закону США о доступном медицинском обслуживании, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="646de-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="646de-173">В рабочей области **Управление персоналом** выберите **ссылки**, а затем выберите **работники**.</span><span class="sxs-lookup"><span data-stu-id="646de-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="646de-174">Выберите сотрудника в списке.</span><span class="sxs-lookup"><span data-stu-id="646de-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="646de-175">На вкладке **Занятость** в разделе **Дополнительная информация** выберите **Покрытие по закону США о доступном медицинском обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="646de-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Изменение параметров для одного сотрудника](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="646de-177">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="646de-177">Select **Edit**.</span></span>
5. <span data-ttu-id="646de-178">Для каждого месяца, требующего изменений, установите флажок **Переопределить значение по умолчанию**, затем измените другие значения, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="646de-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Переопределение значений по умолчанию](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="646de-180">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="646de-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="646de-181">Отчетность по покрытию здравоохранения</span><span class="sxs-lookup"><span data-stu-id="646de-181">Report health care coverage</span></span>

<span data-ttu-id="646de-182">Необходимо отслеживать все финансируемое работодателем самостоятельно застрахованное покрытие здравоохранения для сотрудников с полной занятостью и частичной занятостью.</span><span class="sxs-lookup"><span data-stu-id="646de-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="646de-183">Включите каждого сотрудника вместе с их иждивенцами в отчет 1095-C для месяцев, когда они покрывались.</span><span class="sxs-lookup"><span data-stu-id="646de-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="646de-184">Чтобы указать, следует ли включать в отчет план льгот, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="646de-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="646de-185">В рабочей области **Управления льготами** выберите **Планы льгот**.</span><span class="sxs-lookup"><span data-stu-id="646de-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="646de-186">Выберите план льгот для отчета.</span><span class="sxs-lookup"><span data-stu-id="646de-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="646de-187">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="646de-187">Select **Edit**.</span></span>
4. <span data-ttu-id="646de-188">Установите для параметра **Отчетность по закону США о доступном медицинском обслуживании** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="646de-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Отчетность по покрытию здравоохранения](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="646de-190">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="646de-190">Select **Save**.</span></span>

<span data-ttu-id="646de-191">Если сотрудник выбирает покрытие здравоохранения для иждивенца, период покрытия иждивенца определяется датой, в которую иждивенец был зарегистрирован или удален.</span><span class="sxs-lookup"><span data-stu-id="646de-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="646de-192">Даты покрытия для иждивенцев автоматически рассчитываются на основе периода, в течение которого иждивенец был подходящим и активным в плане в течение года регистрации.</span><span class="sxs-lookup"><span data-stu-id="646de-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="646de-193">Создание форм 1095-B и 1095-C</span><span class="sxs-lookup"><span data-stu-id="646de-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="646de-194">Можно также создать формы ACA 1095-B и 1095-C и затем распределять их по каждому сотруднику.</span><span class="sxs-lookup"><span data-stu-id="646de-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="646de-195">Можно также создать форму 1095-C и соответствующие файлы 1094-C в электронном виде для отправки в налоговое ведомство (IRS).</span><span class="sxs-lookup"><span data-stu-id="646de-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="646de-196">В рабочей области **Управление льготами** выберите **Форма ACA 1095-B** или **Форма ACA 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="646de-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="646de-197">Внесите требуемые изменения в параметры, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="646de-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="646de-198">При печати форм 1095-C для более чем 500 сотрудников вы получите несколько файлов PDF.</span><span class="sxs-lookup"><span data-stu-id="646de-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="646de-199">Рекомендуется увеличить значение поля **Максимальный размер файла в мегабайтах** на странице **Параметры управления документами** на **150**.</span><span class="sxs-lookup"><span data-stu-id="646de-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="646de-200">(Чтобы быстро открыть эту страницу, можно использовать поле поиска на панели переходов.)</span><span class="sxs-lookup"><span data-stu-id="646de-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Изменение максимального размера файла](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="646de-202">Чтобы проверить состояние отчетов и просмотреть их, используйте поле поиска на панели переходов, чтобы открыть страницу **Задания электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="646de-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Поиск страницы заданий электронной отчетности](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="646de-204">Выберите отчет для просмотра, затем выберите команду **Показать файлы**.</span><span class="sxs-lookup"><span data-stu-id="646de-204">Select the report to view, and then select **Show files**.</span></span>

    ![Отображение файлов](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="646de-206">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="646de-206">Select **Open**.</span></span>

    ![Открытие файла](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="646de-208">На панели уведомлений, которая отображается в нижней части окна браузера, откройте ZIP-файл, затем выберите отчет.</span><span class="sxs-lookup"><span data-stu-id="646de-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="646de-209">Можно просмотреть или напечатать PDF-файл.</span><span class="sxs-lookup"><span data-stu-id="646de-209">You can view or print the PDF file.</span></span>

    ![Образец формы 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="646de-211">Просмотр информации о покрытии ACA</span><span class="sxs-lookup"><span data-stu-id="646de-211">View ACA coverage information</span></span>

<span data-ttu-id="646de-212">На странице **Покрытие сотрудников по закону США о доступном медицинском обслуживании** отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="646de-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="646de-213">Сотрудники, назначенные для каждой группы покрытия</span><span class="sxs-lookup"><span data-stu-id="646de-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="646de-214">Сотрудники, которые не обязательно должны быть включены в отчет</span><span class="sxs-lookup"><span data-stu-id="646de-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="646de-215">Неназначенные сотрудники</span><span class="sxs-lookup"><span data-stu-id="646de-215">Unassigned employees</span></span>

<span data-ttu-id="646de-216">Для просмотра этой информации выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="646de-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="646de-217">В рабочей области **Управление льготами** выберите **Покрытие сотрудников по закону США о доступном медицинском обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="646de-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="646de-218">В поле **Имя группы** выберите группу.</span><span class="sxs-lookup"><span data-stu-id="646de-218">In the **Group name** field, select a group.</span></span>

    ![Просмотр покрытия ACA](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="646de-220">Если какие-либо значения по умолчанию для группы покрытия Affordable Care были переопределены, рядом со значением, которое было изменено, появляется звездочка.</span><span class="sxs-lookup"><span data-stu-id="646de-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="646de-221">Если значения для всех 12 месяцев одинаковы и не были переопределены, значение указывается в столбце **Все 12 месяцев**.</span><span class="sxs-lookup"><span data-stu-id="646de-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="646de-222">Можно просмотреть сотрудников, которые помечены как не подлежащие отчетности ACA, и которым не требуется форма 1095-C.</span><span class="sxs-lookup"><span data-stu-id="646de-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="646de-223">В поле **Фильтр по** выберите **Не подлежат отчетности по ACA**.</span><span class="sxs-lookup"><span data-stu-id="646de-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="646de-224">Можно просмотреть сотрудников, которые не назначены группе или которые назначены группе с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="646de-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="646de-225">В поле **Фильтр по** выберите **Неназначенная или просроченная группа**.</span><span class="sxs-lookup"><span data-stu-id="646de-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="646de-226">Экспорт в Excel</span><span class="sxs-lookup"><span data-stu-id="646de-226">Export to Excel</span></span>

<span data-ttu-id="646de-227">Чтобы экспортировать какие-либо списки в Microsoft Excel, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="646de-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="646de-228">Нажмите кнопку **Открыть в Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="646de-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="646de-229">Выберите **временную таблицу HCM управления персоналом для внутреннего использования**.</span><span class="sxs-lookup"><span data-stu-id="646de-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="646de-230">Выберите **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="646de-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="646de-231">Просмотр иждивенцев, подлежащих отчетности ACA</span><span class="sxs-lookup"><span data-stu-id="646de-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="646de-232">Если необходимо сообщить о покрытых лицах, поскольку вы предоставляете покрытие с самостоятельным страхованием, вы можете просматривать иждивенцев, которые покрываются в планах льгот, помеченных как **Подлежащие отчетности ACA**.</span><span class="sxs-lookup"><span data-stu-id="646de-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="646de-233">В области действий выберите **Просмотреть покрытие по иждивенцам**.</span><span class="sxs-lookup"><span data-stu-id="646de-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Просмотр покрытия иждивенцев](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="646de-235">Отображаются сведения о покрытии для иждивенцев сотрудника.</span><span class="sxs-lookup"><span data-stu-id="646de-235">Coverage information for the employee's dependents is shown.</span></span>

![Покрытие иждивенца](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="646de-237">На этой странице отображаются только те планы льгот, которые помечены как **Подлежащие отчетности по ACA**.</span><span class="sxs-lookup"><span data-stu-id="646de-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]