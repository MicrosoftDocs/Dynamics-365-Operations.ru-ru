---
title: Что нового и что изменилось в Dynamics 365 Human Resources (25 июня 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa02cf10b2b4fe08440d3641472e83dfe58169c9
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614394"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="e2585-103">Что нового и что изменилось в Dynamics 365 Human Resources (23 июня 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="e2585-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

<span data-ttu-id="e2585-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e2585-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e2585-105">Изменения применяются для номера сборки 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="e2585-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="e2585-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="e2585-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="e2585-107">Когда истекает срок регистрации для уволенного сотрудника, в форме регистрация отпуска (444867) удаляются тип отпуска, сальдо и сумма.</span><span class="sxs-lookup"><span data-stu-id="e2585-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="e2585-108">Значения в поле **Тип отпуска**, **Сальдо** и **Сумма** в данный момент поддерживаются, а не удаляются при выполнении этого выбора.</span><span class="sxs-lookup"><span data-stu-id="e2585-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="e2585-109">Неправильное прогнозируемое сальдо, если новая функция (Начисление отпуска для одной компании или единого плана) включена (456553)</span><span class="sxs-lookup"><span data-stu-id="e2585-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="e2585-110">Правильное прогнозируемое сальдо теперь отображается, если функция начисления отпуска для одной компании или единого плана включена.</span><span class="sxs-lookup"><span data-stu-id="e2585-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="e2585-111">Сущности с отношениями, которые приводят к дублированными свойствами навигации (456486)</span><span class="sxs-lookup"><span data-stu-id="e2585-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="e2585-112">В этом выпуске исправлена проблема со свойствами навигации (отношениями) нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="e2585-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="e2585-113">Обнаружены повторяющиеся отношения.</span><span class="sxs-lookup"><span data-stu-id="e2585-113">Duplicate relations are detected.</span></span> <span data-ttu-id="e2585-114">Эти сценарии все были исправлены.</span><span class="sxs-lookup"><span data-stu-id="e2585-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="e2585-115">Комментарии между компаниями при обзоре производительности (455536)</span><span class="sxs-lookup"><span data-stu-id="e2585-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="e2585-116">В этом исправлении отображаются межфирменные комментарии в ходе рассмотрения производительности.</span><span class="sxs-lookup"><span data-stu-id="e2585-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="e2585-117">Это изменение исправляет представление примечаний рецензента, которые были введены в разных компаниях для одного обзора производительности.</span><span class="sxs-lookup"><span data-stu-id="e2585-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="e2585-118">Несогласованность при отображении данных управления компенсациями (432562)</span><span class="sxs-lookup"><span data-stu-id="e2585-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="e2585-119">Согласованное представление данных компенсации теперь поддерживается в службе самообслуживания менеджера.</span><span class="sxs-lookup"><span data-stu-id="e2585-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="e2585-120">В зависимости от способа перехода к **сведениям о компенсации** работника, данные компенсации теперь согласованно отображаются для руководителей.</span><span class="sxs-lookup"><span data-stu-id="e2585-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="e2585-121">Дата вступления в силу плана фиксированной компенсации по умолчанию равна сегодняшней дате (411994)</span><span class="sxs-lookup"><span data-stu-id="e2585-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="e2585-122">Дата начала компенсации теперь основана на начальной дате должности, назначенной сотруднику.</span><span class="sxs-lookup"><span data-stu-id="e2585-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="e2585-123">В форме отпуска и отсутствие включение определения половины дня отключено при открытии формы (452607)</span><span class="sxs-lookup"><span data-stu-id="e2585-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="e2585-124">При этом изменении **Включить определение половины дня** будет включено до тех пор, пока существуют новые проводки отпуска.</span><span class="sxs-lookup"><span data-stu-id="e2585-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="e2585-125">Невозможно выполнить публикацию в HcmDiscussionEntity через Excel; ошибка в поле TotalRatingScore (453899)</span><span class="sxs-lookup"><span data-stu-id="e2585-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="e2585-126">Теперь можно обновить поле **TotalRatingScore**, используя **HCMDiscussionEntity** в конструкторе книг Excel.</span><span class="sxs-lookup"><span data-stu-id="e2585-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e2585-127">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="e2585-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="e2585-128">Регистрация базы данных</span><span class="sxs-lookup"><span data-stu-id="e2585-128">Database logging</span></span>

<span data-ttu-id="e2585-129">Ведение журнала базы данных позволяет определить, какие таблицы и какие поля следует отслеживать.</span><span class="sxs-lookup"><span data-stu-id="e2585-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="e2585-130">Она также позволяет определить события, которые должны вызывать отслеживание изменений.</span><span class="sxs-lookup"><span data-stu-id="e2585-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="e2585-131">Для просмотра этих изменений со временем используются средства ведения журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="e2585-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="e2585-132">Дополнительные сведения см. в разделе [Настройка ведения журнала базы данных и управление этим журналом](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="e2585-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="e2585-133">Обязательные поля</span><span class="sxs-lookup"><span data-stu-id="e2585-133">Mandatory fields</span></span> 

<span data-ttu-id="e2585-134">Теперь можно сделать поля обязательными, используя возможности персонализации в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e2585-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="e2585-135">Для этой функции требуются **сохраненные представления**.</span><span class="sxs-lookup"><span data-stu-id="e2585-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="e2585-136">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="e2585-136">Human Resources application in Teams</span></span>

<span data-ttu-id="e2585-137">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e2585-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="e2585-138">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="e2585-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="e2585-139">Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="e2585-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="e2585-140">Объекты платформы управления данными (ДМФ) для управления льготами</span><span class="sxs-lookup"><span data-stu-id="e2585-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="e2585-141">Объекты управления льготами выпускаются.</span><span class="sxs-lookup"><span data-stu-id="e2585-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="e2585-142">Объекты DMF позволяют импортировать и экспортировать данные для упрощения настройки управления льготами.</span><span class="sxs-lookup"><span data-stu-id="e2585-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="e2585-143">Будет доступен шаблон управления льготами для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="e2585-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="e2585-144">Шаблон экспортирует и импортирует данные последовательно для учета зависимостей данных.</span><span class="sxs-lookup"><span data-stu-id="e2585-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="e2585-145">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="e2585-145">Buy and sell leave</span></span> 

<span data-ttu-id="e2585-146">Некоторые организации предоставляют льготу, позволяющую сотрудникам покупать или продавать отпуск.</span><span class="sxs-lookup"><span data-stu-id="e2585-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="e2585-147">Этот процесс часто управляется вручную.</span><span class="sxs-lookup"><span data-stu-id="e2585-147">This process is often managed manually.</span></span> <span data-ttu-id="e2585-148">Эта функция автоматизирует управление политиками и запросами для отдела кадров.</span><span class="sxs-lookup"><span data-stu-id="e2585-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="e2585-149">Она упрощает процесс управления отпусками и помогает исключить ошибки.</span><span class="sxs-lookup"><span data-stu-id="e2585-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="e2585-150">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="e2585-150">For more information, see:</span></span>

- [<span data-ttu-id="e2585-151">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="e2585-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="e2585-152">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="e2585-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="e2585-153">Начисление отпуска для одной компании или одного плана</span><span class="sxs-lookup"><span data-stu-id="e2585-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="e2585-154">Клиенты могут обрабатывать начисления для одной компании или для одного плана отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="e2585-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="e2585-155">Эта возможность обеспечивает ясность процесса начисления для клиентов с различными политиками лет отпусков или начисления отпусков.</span><span class="sxs-lookup"><span data-stu-id="e2585-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="e2585-156">Дополнительные сведения см. в разделе [Начисление отпуска по компаниям или по плану отпуска](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="e2585-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="e2585-157">Добавление вложений в запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="e2585-157">Add attachments to time off requests</span></span>

<span data-ttu-id="e2585-158">Возможность добавлять вложения к утвержденным запросам отпусков является критической в текущей среде COVID-19.</span><span class="sxs-lookup"><span data-stu-id="e2585-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="e2585-159">Сотрудники теперь смогут добавлять эти вложения.</span><span class="sxs-lookup"><span data-stu-id="e2585-159">Employees can now add these attachments.</span></span> <span data-ttu-id="e2585-160">Они также имеют более глубокое представление о том, как выполняются запросы на отпуск.</span><span class="sxs-lookup"><span data-stu-id="e2585-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="e2585-161">Дополнительные сведения см. в разделе [Добавление вложений к существующему запросу](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="e2585-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="e2585-162">Добавление кода основания к приостановке начисления</span><span class="sxs-lookup"><span data-stu-id="e2585-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="e2585-163">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="e2585-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="e2585-164">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="e2585-164">Carry forward rules</span></span> 

<span data-ttu-id="e2585-165">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="e2585-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="e2585-166">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="e2585-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="e2585-167">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="e2585-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="e2585-168">Приостановка начисления отпуска для указанных типов отпусков</span><span class="sxs-lookup"><span data-stu-id="e2585-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="e2585-169">Вы можете создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="e2585-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="e2585-170">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="e2585-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="e2585-171">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="e2585-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="e2585-172">Объект DMF доступен для приостановки начисления</span><span class="sxs-lookup"><span data-stu-id="e2585-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="e2585-173">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="e2585-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e2585-174">Скоро</span><span class="sxs-lookup"><span data-stu-id="e2585-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="e2585-175">Настройка имени самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="e2585-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="e2585-176">Новый параметр будет доступен в **параметрах Human Resources**, чтобы обновить имя рабочей области самообслуживания сотрудников на самообслуживание.</span><span class="sxs-lookup"><span data-stu-id="e2585-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="e2585-177">Сущности контрольного списка, включенные в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e2585-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="e2585-178">Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e2585-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2585-179">См. также</span><span class="sxs-lookup"><span data-stu-id="e2585-179">See also</span></span>

[<span data-ttu-id="e2585-180">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="e2585-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e2585-181">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="e2585-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e2585-182">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="e2585-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e2585-183">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="e2585-183">Manage features</span></span>](hr-admin-manage-features.md)