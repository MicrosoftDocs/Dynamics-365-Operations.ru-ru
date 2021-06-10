---
title: Создание отчетов по закону США о доступном медицинском обслуживании (ACA)
description: Отчетность по закону США о доступном медицинском обслуживании (ACA) создает формы 1095-B и 1095-C в поддержку части **Мандат работодателя** закона США о доступном медицинском обслуживании.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053209"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="6c174-103">Создание отчетов ACA</span><span class="sxs-lookup"><span data-stu-id="6c174-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6c174-104">Отчетность по закону США о доступном медицинском обслуживании (ACA) создает формы 1095-B и 1095-C в поддержку части **Мандат работодателя** закона США о доступном медицинском обслуживании.</span><span class="sxs-lookup"><span data-stu-id="6c174-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="6c174-105">Отчетность ACA включена только для юридических лиц в Соединенных Штатах Америки.</span><span class="sxs-lookup"><span data-stu-id="6c174-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="6c174-106">Начало работы</span><span class="sxs-lookup"><span data-stu-id="6c174-106">Getting started</span></span>

<span data-ttu-id="6c174-107">Чтобы отследить информацию для форм 1095-B и 1095-C, сначала необходимо создать одну или несколько групп покрытия в соответствии с законом США о доступном медицинском обслуживании.</span><span class="sxs-lookup"><span data-stu-id="6c174-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="6c174-108">Группы покрытия по закону США о доступном медицинском обслуживании указывают:</span><span class="sxs-lookup"><span data-stu-id="6c174-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="6c174-109">Предложение покрытия для сотрудника</span><span class="sxs-lookup"><span data-stu-id="6c174-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="6c174-110">Доля сотрудника от минимального ежемесячного вознаграждения, если затраты превышают федеральный уровень бедности</span><span class="sxs-lookup"><span data-stu-id="6c174-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="6c174-111">Параметры Safe Harbor, которые используются работодателем, если применимо</span><span class="sxs-lookup"><span data-stu-id="6c174-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="6c174-112">С помощью групп покрытия Affordable Care можно управлять информацией для этих полей без изменения записей каждого сотрудника, если условия одинаковые.</span><span class="sxs-lookup"><span data-stu-id="6c174-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="6c174-113">Группы покрытия Affordable Care можно легко назначить одному или нескольким сотрудникам с помощью параметра **Массовое назначение** на странице.</span><span class="sxs-lookup"><span data-stu-id="6c174-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="6c174-114">Поддержка нескольких версий группы покрытия</span><span class="sxs-lookup"><span data-stu-id="6c174-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="6c174-115">Можно поддерживать нескольких версий любой группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="6c174-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="6c174-116">Эта функция позволяет вносить изменения без создания новой группы и повторного назначения сотрудников ей.</span><span class="sxs-lookup"><span data-stu-id="6c174-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="6c174-117">После создания групп покрытия ACA можно выполнить массовое назначение групп сотрудникам, используя параметр **Массовое назначение**.</span><span class="sxs-lookup"><span data-stu-id="6c174-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="6c174-118">Можно также отдельно указать, следует ли отслеживать и сообщать информацию ACA и назначать сотрудника группе покрытия Affordable Care.</span><span class="sxs-lookup"><span data-stu-id="6c174-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="6c174-119">Нет необходимости отслеживать некоторую информацию ACA, например, для сотрудников с частичной занятостью.</span><span class="sxs-lookup"><span data-stu-id="6c174-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="6c174-120">В этом случае установите в поле **Сообщать о покрытии** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="6c174-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="6c174-121">Хотя необходимо назначить каждого сотрудника с отслеживаемой информацией ACA группу покрытия Affordable Care, все равно можно изменить следующие параметры для месяцев с другими значениями:</span><span class="sxs-lookup"><span data-stu-id="6c174-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="6c174-122">**Предложение покрытия**</span><span class="sxs-lookup"><span data-stu-id="6c174-122">**Offer of coverage**</span></span>
- <span data-ttu-id="6c174-123">**Доля затрат сотрудника**</span><span class="sxs-lookup"><span data-stu-id="6c174-123">**Employee share of cost**</span></span>
- <span data-ttu-id="6c174-124">**Директива Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="6c174-124">**Safe Harbor**</span></span>

<span data-ttu-id="6c174-125">Для ввода исключений для значений группы покрытия Affordable Care выберите ссылку **Покрытие Affordable Care** на странице **Сведения о работнике**, под разделом **Дополнительная информация** на вкладке **Занятость**.</span><span class="sxs-lookup"><span data-stu-id="6c174-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="6c174-126">Отчетность по покрытию здравоохранения</span><span class="sxs-lookup"><span data-stu-id="6c174-126">Reporting health care coverage</span></span>

<span data-ttu-id="6c174-127">Помимо отслеживания того, распространяется ли медицинская страховка на сотрудников с полной занятостью, если работодатель предлагает спонсируемую работодателем самостоятельную страховку, на которую зарегистрирован сотрудник (независимо от способа занятости, полная или частичная), необходимо внести дополнительную информацию в 1095-C.</span><span class="sxs-lookup"><span data-stu-id="6c174-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="6c174-128">Каждый работник (в том числе иждивенец), на которого распространяются планы льгот, должен быть включен в отчет за месяцы, которые были покрыты.</span><span class="sxs-lookup"><span data-stu-id="6c174-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="6c174-129">Можно указать, должен ли план льгот вносится в отчетность, установив флажок **Для отчета ACA**.</span><span class="sxs-lookup"><span data-stu-id="6c174-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="6c174-130">Кроме того, если у сотрудника есть иждивенцы, которые подпадают под льготы, можно указать даты покрытия для каждого сотрудника на странице **Ведение льгот**.</span><span class="sxs-lookup"><span data-stu-id="6c174-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="6c174-131">Для указания того, что на иждивенца распространяются льготы, выберите кнопку **Редактировать** в области действий на экспресс-вкладке **Иждивенцы**.</span><span class="sxs-lookup"><span data-stu-id="6c174-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="6c174-132">На странице **Диспетчер дат покрытия для иждивенцев** можно указать даты, когда на иждивенца распространялись льготы.</span><span class="sxs-lookup"><span data-stu-id="6c174-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="6c174-133">При вводе дат на этой странице автоматически будет поставлен флажок **Охвачено** на странице **Ведение льгот**.</span><span class="sxs-lookup"><span data-stu-id="6c174-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="6c174-134">Создание форм 1095-B и 1095-C</span><span class="sxs-lookup"><span data-stu-id="6c174-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="6c174-135">Можно также создать формы 1095-B и 1095-C из продукта и распределить их по каждому сотруднику.</span><span class="sxs-lookup"><span data-stu-id="6c174-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="6c174-136">Кроме того, система может создавать формы 1095-C и файлы передачи IRS 1094-C в электронном виде.</span><span class="sxs-lookup"><span data-stu-id="6c174-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="6c174-137">При создании формы 1095-C введите соответствующий налоговый год и укажите, должны ли скрываться номера социального страхования.</span><span class="sxs-lookup"><span data-stu-id="6c174-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="6c174-138">При печати форм 1095-C для более чем 500 сотрудников вы получите несколько файлов PDF.</span><span class="sxs-lookup"><span data-stu-id="6c174-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="6c174-139">Рекомендуется увеличить значение параметра **Максимальный размер файла** в окне **Параметры управления документами** до 150 МБ.</span><span class="sxs-lookup"><span data-stu-id="6c174-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="6c174-140">Просмотр сведений</span><span class="sxs-lookup"><span data-stu-id="6c174-140">Viewing information</span></span>

<span data-ttu-id="6c174-141">Можно использовать страницу **Покрытие по закону Affordable Care работника** для просмотра сотрудников, для которых были назначены группы покрытия, где сотрудники не должны включаться в отчетность, и какие сотрудники не назначены.</span><span class="sxs-lookup"><span data-stu-id="6c174-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="6c174-142">Если какие-либо значения по умолчанию для группы покрытия Affordable Care были переопределены, рядом со значением, которое было изменено, появится звездочка.</span><span class="sxs-lookup"><span data-stu-id="6c174-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="6c174-143">Если значения для всех 12 месяцев одинаковы и не были переопределены, значение будет указано в столбце **Все 12 месяцев**.</span><span class="sxs-lookup"><span data-stu-id="6c174-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="6c174-144">Окно запроса можно также использовать для определения того, какие сотрудники были помечены как не включаемые в отчеты ACA.</span><span class="sxs-lookup"><span data-stu-id="6c174-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="6c174-145">Нет необходимости отслеживать, было ли предложено им покрытие, и не нужно выпускать форму 1095-C для них в конце года.</span><span class="sxs-lookup"><span data-stu-id="6c174-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="6c174-146">Выберите **Не подлежат отчетности по ACA** в поле **Фильтр по** для создания списка всех сотрудников, которые не будут получать форму 1095-C.</span><span class="sxs-lookup"><span data-stu-id="6c174-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="6c174-147">Кроме того, можно также просмотреть сотрудников, не назначенных (поле **Покрытие отчетов ACA** пустое) или назначенных для группы покрытия Affordable Care, срок действия которой истек за год, выбранный в поле **Год**.</span><span class="sxs-lookup"><span data-stu-id="6c174-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="6c174-148">Можно экспортировать списки сотрудников, которые были созданы с одним из параметров фильтрации в Excel.</span><span class="sxs-lookup"><span data-stu-id="6c174-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="6c174-149">Если необходимо сообщить о покрытых лицах, поскольку вы предоставляете покрытие с самостоятельным страхованием, вы можете просматривать любых иждивенцев, которые покрываются в планах льгот, помеченных как **Подлежащие отчетности ACA**.</span><span class="sxs-lookup"><span data-stu-id="6c174-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="6c174-150">Выберите **Просмотреть покрытие по иждивенцам** в области действий.</span><span class="sxs-lookup"><span data-stu-id="6c174-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="6c174-151">В окне запроса отображаются только планы льгот, помеченные как **Подлежащие отчетности по ACA**.</span><span class="sxs-lookup"><span data-stu-id="6c174-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]