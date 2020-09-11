---
title: Что нового и что изменилось в Dynamics 365 Human Resources (08 июля 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 8 июля 2020 года.
author: Darinkramer
manager: AnnBe
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2f542195693e825391b85efc4a7e91fdfea3944
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711900"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="c7d16-103">Что нового и что изменилось в Dynamics 365 Human Resources (8 июля 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="c7d16-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="c7d16-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c7d16-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c7d16-105">Изменения применяются для номера сборки 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="c7d16-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="c7d16-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="c7d16-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="c7d16-107">Регистрация базы данных</span><span class="sxs-lookup"><span data-stu-id="c7d16-107">Database logging</span></span>

<span data-ttu-id="c7d16-108">Ведение журнала базы данных позволяет определить, какие таблицы и какие поля следует отслеживать.</span><span class="sxs-lookup"><span data-stu-id="c7d16-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="c7d16-109">Она также позволяет определить события, которые должны вызывать отслеживание изменений.</span><span class="sxs-lookup"><span data-stu-id="c7d16-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="c7d16-110">Для просмотра этих изменений со временем используются средства ведения журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="c7d16-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="c7d16-111">Дополнительные сведения см. в разделе [Настройка ведения журнала базы данных и управление этим журналом](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="c7d16-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="c7d16-112">Настройка имени самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="c7d16-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="c7d16-113">В разделе **Параметры Human Resources** теперь можно изменить имя рабочей области **Самообслуживание сотрудников** на **Самообслуживание**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="c7d16-114">Дополнительные сведения см. в разделе [Изменение имени рабочей области самообслуживания сотрудников](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="c7d16-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="c7d16-115">Управление льготами открывает доступ к регистрации вне периода</span><span class="sxs-lookup"><span data-stu-id="c7d16-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="c7d16-116">В этой версии исправляется ошибка, из-за которой сотрудники могут получить доступ к льготам с открытой регистрацией вне периода регистрации или без события в жизни.</span><span class="sxs-lookup"><span data-stu-id="c7d16-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="c7d16-117">В результате, если требуется демонстрационная с открытой регистрацией в службе самообслуживания сотрудников, следует откорректировать открытые даты регистрации до текущих (или более ранних), чтобы сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="c7d16-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="c7d16-118">Этот параметр можно изменить в разделе **Управление льготами > Периоды правил и параметров**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="c7d16-119">Подтверждение регистрации сотрудника по электронной почте</span><span class="sxs-lookup"><span data-stu-id="c7d16-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="c7d16-120">Теперь можно отправлять сообщения электронной почты сотрудникам после того, как они завершили выбор льгот.</span><span class="sxs-lookup"><span data-stu-id="c7d16-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="c7d16-121">Можно либо отправить сообщение по умолчанию, либо использовать шаблон сообщений электронной почты организации.</span><span class="sxs-lookup"><span data-stu-id="c7d16-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="c7d16-122">Эти параметры находятся в разделе **Параметры управления персоналом > Управление льготами**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="c7d16-123">Отмененный отпуск по-прежнему отображается в предстоящих отпусках в рабочей области пользователей (441358)</span><span class="sxs-lookup"><span data-stu-id="c7d16-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="c7d16-124">Отмененный отпуск больше не будет отображаться как предстоящий отпуск в карточках отпусков в рабочей области **Люди**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="c7d16-125">Невозможно использовать свойство сущности подразделения в сущности PositionV2 (456486)</span><span class="sxs-lookup"><span data-stu-id="c7d16-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="c7d16-126">Теперь можно добавить отдел без создания дубликата отношения.</span><span class="sxs-lookup"><span data-stu-id="c7d16-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="c7d16-127">В PayrollWorkerEnrolledBenefitDetailEntity следует использовать только вычисляемое поле для пенсионных программ (459779)</span><span class="sxs-lookup"><span data-stu-id="c7d16-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="c7d16-128">При экспорте сущности **PayrollWorkerEnrolledBenefitDetailEntity** экспорт определяет, следует ли использовать вычисляемое поле на основе таблицы норм или использовать поле **ContributionAmountCur** в резервной таблице.</span><span class="sxs-lookup"><span data-stu-id="c7d16-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="c7d16-129">Логика, используемая сущностью данных, использует таблицу норм в ситуациях, когда приложение обычно не использует ее.</span><span class="sxs-lookup"><span data-stu-id="c7d16-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="c7d16-130">Эта логика приводит к тому, что экспортируемые сущности будут возвращать нулевое значение для этого столбца, поскольку отсутствует таблица норм расчета, и продукт не позволяет клиенту указать ее.</span><span class="sxs-lookup"><span data-stu-id="c7d16-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="c7d16-131">Путаница с переводами на чешском языке в модуле управления персоналом и самообслуживании сотрудников (400276)</span><span class="sxs-lookup"><span data-stu-id="c7d16-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="c7d16-132">В этом выпуске исправляется перевод для терминов **Каталог компании**, **Следующий зарегистрированный курс**, **Задание** и **Должность**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="c7d16-133">В таблице WorkCalendarEmployment не включены созданные и измененные системные поля (460171)</span><span class="sxs-lookup"><span data-stu-id="c7d16-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="c7d16-134">Созданные и измененные системные поля теперь включены в таблице **WorkCalendarEmployment** в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c7d16-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="c7d16-135">Исключение ссылки null для приема на работу и добавление сведений для будущего сотрудника (455475)</span><span class="sxs-lookup"><span data-stu-id="c7d16-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="c7d16-136">В этом выпуске исправляется ошибка (ссылка null) в оптимизированной записи сотрудника при найме сотрудника с использованием параметра **Прием на работу и добавление сведений**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="c7d16-137">Изменения, внесенные в сущность работника Common Data Service, не отражается в Human Resources (455652)</span><span class="sxs-lookup"><span data-stu-id="c7d16-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="c7d16-138">Изменения, внесенные в следующие поля в сущности **Работник** в Common Data Service, будут теперь отображаться в модуле Human Resources:</span><span class="sxs-lookup"><span data-stu-id="c7d16-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="c7d16-139">**Работает из дома**</span><span class="sxs-lookup"><span data-stu-id="c7d16-139">**Works from home**</span></span>
- <span data-ttu-id="c7d16-140">**Дата начала стажа**</span><span class="sxs-lookup"><span data-stu-id="c7d16-140">**Seniority date**</span></span>
- <span data-ttu-id="c7d16-141">**Дата годовщины**</span><span class="sxs-lookup"><span data-stu-id="c7d16-141">**Anniversary date**</span></span>
- <span data-ttu-id="c7d16-142">**Дата первоначального приема на работу**</span><span class="sxs-lookup"><span data-stu-id="c7d16-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="c7d16-143">Правильный уровень компенсации не устанавливается по умолчанию на основе задания, назначенного для данной должности (394136)</span><span class="sxs-lookup"><span data-stu-id="c7d16-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="c7d16-144">При этом изменении правильный уровень компенсаций устанавливается по умолчанию на основе записей **Дата вступления в силу** для параметров **Сведения о должности** и **Начальная дата** в разделе **Назначение плана компенсаций**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="c7d16-145">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="c7d16-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="c7d16-146">Обязательные поля</span><span class="sxs-lookup"><span data-stu-id="c7d16-146">Mandatory fields</span></span> 

<span data-ttu-id="c7d16-147">Теперь можно сделать поля обязательными, используя возможности персонализации в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c7d16-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="c7d16-148">Для этой функции требуются **сохраненные представления**.</span><span class="sxs-lookup"><span data-stu-id="c7d16-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="c7d16-149">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="c7d16-149">Human Resources application in Teams</span></span>

<span data-ttu-id="c7d16-150">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c7d16-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="c7d16-151">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="c7d16-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="c7d16-152">Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="c7d16-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="c7d16-153">Объекты платформы управления данными (ДМФ) для управления льготами</span><span class="sxs-lookup"><span data-stu-id="c7d16-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="c7d16-154">Объекты управления льготами выпускаются.</span><span class="sxs-lookup"><span data-stu-id="c7d16-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="c7d16-155">Объекты DMF позволяют импортировать и экспортировать данные для упрощения настройки управления льготами.</span><span class="sxs-lookup"><span data-stu-id="c7d16-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="c7d16-156">Будет доступен шаблон управления льготами для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="c7d16-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="c7d16-157">Шаблон экспортирует и импортирует данные последовательно для учета зависимостей данных.</span><span class="sxs-lookup"><span data-stu-id="c7d16-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="c7d16-158">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="c7d16-158">Buy and sell leave</span></span> 

<span data-ttu-id="c7d16-159">Некоторые организации предоставляют льготу, позволяющую сотрудникам покупать или продавать отпуск.</span><span class="sxs-lookup"><span data-stu-id="c7d16-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="c7d16-160">Этот процесс часто управляется вручную.</span><span class="sxs-lookup"><span data-stu-id="c7d16-160">This process is often managed manually.</span></span> <span data-ttu-id="c7d16-161">Эта функция автоматизирует управление политиками и запросами для отдела кадров.</span><span class="sxs-lookup"><span data-stu-id="c7d16-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="c7d16-162">Она упрощает процесс управления отпусками и помогает исключить ошибки.</span><span class="sxs-lookup"><span data-stu-id="c7d16-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="c7d16-163">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="c7d16-163">For more information, see:</span></span>

- [<span data-ttu-id="c7d16-164">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="c7d16-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="c7d16-165">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="c7d16-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="c7d16-166">Начисление отпуска для одной компании или одного плана</span><span class="sxs-lookup"><span data-stu-id="c7d16-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="c7d16-167">Клиенты могут обрабатывать начисления для одной компании или для одного плана отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="c7d16-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="c7d16-168">Эта возможность обеспечивает ясность для процесса начисления для клиентов с различными политиками лет отпусков или начисления отпусков.</span><span class="sxs-lookup"><span data-stu-id="c7d16-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="c7d16-169">Дополнительные сведения см. в разделе [Начисление отпуска по компаниям или по плану отпуска](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="c7d16-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="c7d16-170">Добавление вложений в запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="c7d16-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="c7d16-171">Возможность добавлять вложения к утвержденным запросам отпусков является критической в текущей среде COVID-19.</span><span class="sxs-lookup"><span data-stu-id="c7d16-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="c7d16-172">Сотрудники теперь смогут добавлять эти вложения.</span><span class="sxs-lookup"><span data-stu-id="c7d16-172">Employees can now add these attachments.</span></span> <span data-ttu-id="c7d16-173">Они также имеют более глубокое представление о том, как выполняются запросы на отпуск.</span><span class="sxs-lookup"><span data-stu-id="c7d16-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="c7d16-174">Дополнительные сведения см. в разделе [Добавление вложений к существующему запросу](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="c7d16-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="c7d16-175">Добавление кода основания к приостановке начисления</span><span class="sxs-lookup"><span data-stu-id="c7d16-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="c7d16-176">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="c7d16-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="c7d16-177">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="c7d16-177">Carry forward rules</span></span> 

<span data-ttu-id="c7d16-178">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="c7d16-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="c7d16-179">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="c7d16-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="c7d16-180">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="c7d16-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="c7d16-181">Приостановка начисления отпуска для указанных типов отпусков</span><span class="sxs-lookup"><span data-stu-id="c7d16-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="c7d16-182">Вы можете создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="c7d16-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="c7d16-183">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="c7d16-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="c7d16-184">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="c7d16-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="c7d16-185">Объект DMF доступен для приостановки начисления</span><span class="sxs-lookup"><span data-stu-id="c7d16-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="c7d16-186">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="c7d16-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c7d16-187">Скоро</span><span class="sxs-lookup"><span data-stu-id="c7d16-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="c7d16-188">Сущности контрольного списка, включенные в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c7d16-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="c7d16-189">Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c7d16-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7d16-190">См. также</span><span class="sxs-lookup"><span data-stu-id="c7d16-190">See also</span></span>

[<span data-ttu-id="c7d16-191">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="c7d16-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c7d16-192">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="c7d16-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c7d16-193">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="c7d16-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c7d16-194">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="c7d16-194">Manage features</span></span>](hr-admin-manage-features.md)
