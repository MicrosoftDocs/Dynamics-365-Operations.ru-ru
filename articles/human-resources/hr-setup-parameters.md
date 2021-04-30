---
title: Настройка параметров Human Resources
description: В этой теме описывается, как настроить параметры модуля, относящиеся к конкретной компании, в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889940"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="b2677-103">Настройка параметров Human Resources</span><span class="sxs-lookup"><span data-stu-id="b2677-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b2677-104">Настройки некоторых параметров управления персоналом используются совместно несколькими компаниями, в то время как настройки других параметров относятся только к конкретной компании.</span><span class="sxs-lookup"><span data-stu-id="b2677-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="b2677-105">В этой теме описывается, как настроить параметры управления персоналом, относящиеся к конкретной компании.</span><span class="sxs-lookup"><span data-stu-id="b2677-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="b2677-106">Для задания параметров управления персоналом используются две страницы.</span><span class="sxs-lookup"><span data-stu-id="b2677-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="b2677-107">Для параметров, которые являются общими для различных компаний, используется страница **Совместно используемые параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="b2677-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="b2677-108">Для параметров конкретной компании (иными словами, параметров, относящихся к одной компании) используется страница **Параметры Управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="b2677-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Перейдите к параметрам управления персоналом](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="b2677-110">На странице **Параметры Управления персоналом** страницы разделены на шесть вкладок:</span><span class="sxs-lookup"><span data-stu-id="b2677-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="b2677-111">**Общие сведения**</span><span class="sxs-lookup"><span data-stu-id="b2677-111">**General**</span></span>
- <span data-ttu-id="b2677-112">**Набор сотрудников** (эта вкладка не входит в Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="b2677-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="b2677-113">**Компенсация**</span><span class="sxs-lookup"><span data-stu-id="b2677-113">**Compensation**</span></span>
- <span data-ttu-id="b2677-114">**Номерные серии**</span><span class="sxs-lookup"><span data-stu-id="b2677-114">**Number sequences**</span></span>
- <span data-ttu-id="b2677-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="b2677-115">**FMLA**</span></span>
- <span data-ttu-id="b2677-116">**Портал самообслуживания сотрудников**</span><span class="sxs-lookup"><span data-stu-id="b2677-116">**Employee self service**</span></span>
- <span data-ttu-id="b2677-117">**Портал самообслуживания менеджеров**</span><span class="sxs-lookup"><span data-stu-id="b2677-117">**Manager self service**</span></span>
- <span data-ttu-id="b2677-118">**Управление льготами**</span><span class="sxs-lookup"><span data-stu-id="b2677-118">**Benefits management**</span></span>
- <span data-ttu-id="b2677-119">**Отпуск и отсутствие**</span><span class="sxs-lookup"><span data-stu-id="b2677-119">**Leave and absence**</span></span>
- <span data-ttu-id="b2677-120">**Способы оплаты**</span><span class="sxs-lookup"><span data-stu-id="b2677-120">**Payment methods**</span></span>

<span data-ttu-id="b2677-121">Каждая вкладка содержит информацию, относящуюся к одной компании.</span><span class="sxs-lookup"><span data-stu-id="b2677-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="b2677-122">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b2677-122">General</span></span>

<span data-ttu-id="b2677-123">Настройки на вкладке **Общее** определяют внешний вид информации об отсутствия, травмах и заболеваниях, а также новых работниках.</span><span class="sxs-lookup"><span data-stu-id="b2677-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="b2677-124">Настройки на этой вкладке также определяют некоторые значения по умолчанию, предлагаемые вам в ходе работы.</span><span class="sxs-lookup"><span data-stu-id="b2677-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="b2677-125">В частности, эта вкладка позволяет:</span><span class="sxs-lookup"><span data-stu-id="b2677-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="b2677-126">Выбрать цвет, который будет применяться к открытым проводкам отсутствия</span><span class="sxs-lookup"><span data-stu-id="b2677-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="b2677-127">Задать таблицу стилей для использования в отчетах</span><span class="sxs-lookup"><span data-stu-id="b2677-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="b2677-128">Включить интеграцию между курсами обучения и регистрацией отсутствия</span><span class="sxs-lookup"><span data-stu-id="b2677-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="b2677-129">Выбрать код отсутствия, который используется для управления этой интеграцией.</span><span class="sxs-lookup"><span data-stu-id="b2677-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="b2677-130">Указать длительность хранения случаев травм и заболеваний.</span><span class="sxs-lookup"><span data-stu-id="b2677-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="b2677-131">Задавать идентификационный номер по умолчанию, отображаемый при найме нового работника.</span><span class="sxs-lookup"><span data-stu-id="b2677-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Вкладка "Общие"](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="b2677-133">Набор сотрудников</span><span class="sxs-lookup"><span data-stu-id="b2677-133">Recruitment</span></span>

<span data-ttu-id="b2677-134">Настройки на вкладке **Набор сотрудников** определяют типы документов, используемые для корреспонденции, автоматически отправляемой кандидатам.</span><span class="sxs-lookup"><span data-stu-id="b2677-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="b2677-135">Можно также указать проект по набору сотрудников, используемый для незапрошенных заявлений.</span><span class="sxs-lookup"><span data-stu-id="b2677-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="b2677-136">Период, заданный для распределения по срокам проектов по набору сотрудников, определяет, какие проекты по набору сотрудников включаются на плитку **Распределение по срокам проектов** в рабочей области **Управление набором сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="b2677-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="b2677-137">Период, заданный для предупреждения о крайнем сроке подачи заявлений, используется для отображения проектов по набору сотрудников, которые приближаются к крайнему сроку, на плитке **Приближается крайний срок подачи заявления** в рабочей области **Набор сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="b2677-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="b2677-138">Дополнительные сведения о наборе сотрудников см. в разделе [Наем кандидатов на должность](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="b2677-139">Компенсация</span><span class="sxs-lookup"><span data-stu-id="b2677-139">Compensation</span></span>

<span data-ttu-id="b2677-140">В Dynamics 365 Finance настройки на вкладке **Компенсация** определяют, должны ли пользователи подтверждать, что они хотят сохранить информацию для плана фиксированной или переменной компенсации.</span><span class="sxs-lookup"><span data-stu-id="b2677-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="b2677-141">Если выбрать **Включить сохранение подтверждения**, когда пользователь закрывает связанную с компенсациями страницу, он будет получать сообщение с вопросом о том, хочет ли он сохранить запись.</span><span class="sxs-lookup"><span data-stu-id="b2677-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="b2677-142">Некоторые страницы управления компенсациями не позволяют пользователям удалять информацию.</span><span class="sxs-lookup"><span data-stu-id="b2677-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="b2677-143">Предлагая пользователям подтвердить, что они хотят сохранить информацию, вы сможете ограничить объем информации, которая сохраняется, но впоследствии не может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="b2677-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="b2677-144">Если удалить **Включить сохранение подтверждения**, записи сохраняются сразу же, возможно, когда пользователь к этому еще не готов.</span><span class="sxs-lookup"><span data-stu-id="b2677-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="b2677-145">Если вы используете управление производительностью, вкладка **Компенсация** также позволяет выбрать модель рейтинга для использования вместо модели, назначаемой планам компенсационных выплат при оценке производительности.</span><span class="sxs-lookup"><span data-stu-id="b2677-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="b2677-146">В управлении персоналом можно использовать вкладку **Компенсация**, чтобы ограничить доступ к планам компенсаций и задать валюту по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2677-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="b2677-147">Дополнительные сведения о планах компенсации см. в разделе [Обзор планов компенсационных выплат](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Вкладка "Компенсация"](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="b2677-149">Номерные серии</span><span class="sxs-lookup"><span data-stu-id="b2677-149">Number sequences</span></span>

<span data-ttu-id="b2677-150">Настройки на вкладке **Номерные серии** определяют последовательности, используемые для автоматического присвоения кодов номенклатурам в управлении персоналом, например:</span><span class="sxs-lookup"><span data-stu-id="b2677-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="b2677-151">Приложения</span><span class="sxs-lookup"><span data-stu-id="b2677-151">Applications</span></span>
- <span data-ttu-id="b2677-152">Регистрация отсутствия</span><span class="sxs-lookup"><span data-stu-id="b2677-152">Absence registrations</span></span>
- <span data-ttu-id="b2677-153">Результаты процесса компенсации</span><span class="sxs-lookup"><span data-stu-id="b2677-153">Compensation process results</span></span>
- <span data-ttu-id="b2677-154">Номера вариантов</span><span class="sxs-lookup"><span data-stu-id="b2677-154">Case numbers</span></span>
- <span data-ttu-id="b2677-155">Курсы</span><span class="sxs-lookup"><span data-stu-id="b2677-155">Courses</span></span>
- <span data-ttu-id="b2677-156">Планы курса</span><span class="sxs-lookup"><span data-stu-id="b2677-156">Course agendas</span></span>

<span data-ttu-id="b2677-157">Для ведения ссылок и кодов номерных серий используется страница списка **Номерные серии** (выберите **Управление организацией > Номерные серии > Номерные серии**).</span><span class="sxs-lookup"><span data-stu-id="b2677-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="b2677-158">Дополнительные сведения см. в разделе [Обзор номерных серий](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="b2677-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="b2677-159">Количество отработанных часов не может превышать 1250, а длительность трудоустройства не может превышать 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="b2677-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="b2677-160">Эти максимальные значения соответствуют федеральному законодательству США.</span><span class="sxs-lookup"><span data-stu-id="b2677-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Вкладка "Номерные серии"](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="b2677-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="b2677-162">FMLA</span></span>

<span data-ttu-id="b2677-163">На вкладке FMLA настройте требования к доступности FMLA и трудозатраты FMLA.</span><span class="sxs-lookup"><span data-stu-id="b2677-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="b2677-164">Дополнительные сведения см. в разделе [Настройка параметров отпусков и отгулов](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![Вкладка FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="b2677-166">Самообслуживание сотрудника</span><span class="sxs-lookup"><span data-stu-id="b2677-166">Employee self service</span></span>

<span data-ttu-id="b2677-167">Настройки на вкладке **Самообслуживание сотрудника** влияют на то, как cамообслуживание сотрудника отображается для сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b2677-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="b2677-168">На этой вкладке можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b2677-168">On this tab, you can:</span></span>

- <span data-ttu-id="b2677-169">Введите имя рабочей области самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="b2677-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="b2677-170">Выбор сведений, которые руководитель может ввести для сотрудников</span><span class="sxs-lookup"><span data-stu-id="b2677-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="b2677-171">Добавление полезных ссылок для сотрудников</span><span class="sxs-lookup"><span data-stu-id="b2677-171">Add useful links for employees</span></span>
- <span data-ttu-id="b2677-172">Ограничение сотрудникам добавления или изменения сведений о бизнес-контактах.</span><span class="sxs-lookup"><span data-stu-id="b2677-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="b2677-173">Дополнительные сведения см. в разделе [Ограничение редактирования личных данных](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="b2677-174">Дополнительные сведения о настройке самообслуживания сотрудников см. в разделе [Обзор самообслуживания сотрудников и менеджеров](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Вкладка самообслуживания сотрудников](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="b2677-176">Портал самообслуживания менеджеров</span><span class="sxs-lookup"><span data-stu-id="b2677-176">Manager self service</span></span>

<span data-ttu-id="b2677-177">Настройки на вкладке **Самообслуживание менеджеров** влияют на то, что видят менеджеры в самообслуживании менеджеров.</span><span class="sxs-lookup"><span data-stu-id="b2677-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="b2677-178">На этой вкладке можно настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b2677-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="b2677-179">Диапазон записей с истекающим сроком действия</span><span class="sxs-lookup"><span data-stu-id="b2677-179">The range for expiring records</span></span>
- <span data-ttu-id="b2677-180">Менеджеры по информационным данным могут просматривать записи с истекающим сроком действия</span><span class="sxs-lookup"><span data-stu-id="b2677-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="b2677-181">Могут ли менеджеры просматривать открытые должности для расширенных отчетов</span><span class="sxs-lookup"><span data-stu-id="b2677-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="b2677-182">Представления существующих работников</span><span class="sxs-lookup"><span data-stu-id="b2677-182">Views of exiting workers</span></span>
- <span data-ttu-id="b2677-183">Полезные ссылки для менеджеров</span><span class="sxs-lookup"><span data-stu-id="b2677-183">Useful links for managers</span></span>

<span data-ttu-id="b2677-184">Дополнительные сведения о настройке самообслуживания менеджеров см. в разделе [Обзор самообслуживания сотрудников и менеджеров](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Вкладка самообслуживания менеджеров](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="b2677-186">Управление льготами</span><span class="sxs-lookup"><span data-stu-id="b2677-186">Benefits management</span></span>

<span data-ttu-id="b2677-187">На вкладке управления льготами можно настроить параметры электронной почты для управления льготами.</span><span class="sxs-lookup"><span data-stu-id="b2677-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="b2677-188">Дополнительные сведения о настройке и использовании управления льготами см. в разделе [Обзор управления льготами](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Вкладка управления льготами](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="b2677-190">Отпуск и отсутствие</span><span class="sxs-lookup"><span data-stu-id="b2677-190">Leave and absence</span></span>

<span data-ttu-id="b2677-191">Дополнительные сведения о настройке и использовании отпусков и отгулов см. в разделе [Обзор отпусков и отгулов](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="b2677-192">Способы оплаты</span><span class="sxs-lookup"><span data-stu-id="b2677-192">Payment methods</span></span>

<span data-ttu-id="b2677-193">На вкладке **Методы оплаты** можно выбрать методы оплаты, поддерживаемые вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="b2677-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="b2677-194">Дополнительные сведения о настройке компенсации см. в разделе [Обзор планов компенсационных выплат](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2677-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Вкладка методов оплаты](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]