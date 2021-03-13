---
title: Что нового и что изменилось в Dynamics 365 Human Resources (20 августа 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 20 августа 2020 года.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b3654617b0e8bc4b586e969913d5dc355b60b882
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130067"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="7c2e8-103">Что нового и что изменилось в Dynamics 365 Human Resources (20 августа 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7c2e8-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7c2e8-105">Изменения применяются для номера сборки 8.1.3478.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="7c2e8-106">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="7c2e8-107">Отображение сведений о предстоящих и ожидающих отпусках на карточках в рабочей области пользователей</span><span class="sxs-lookup"><span data-stu-id="7c2e8-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="7c2e8-108">В карточках отпусков и отсутствий в рабочем пространстве **Сотрудники** теперь доступны параметры запроса ожидающих и предстоящих отпусков.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="7c2e8-109">Поле "Частный" не имеет значение "Да" по умолчанию для роли сотрудника в модуле самообслуживания сотрудника (477106)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="7c2e8-110">Поле **Частный** теперь по умолчанию равно **Да**, когда сотрудники добавляют новые записи адресов через страницу **Личные данные** в службе самообслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="7c2e8-111">Кандидаты для найма на экспресс-вкладке в модуле "Управление персоналом" показывают неверное количество кандидатов (470110)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="7c2e8-112">Страница **Управление персоналом** теперь будет точно отображать число кандидатов для найма.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="7c2e8-113">Невозможно ввести отсутствие по болезни для уволенного сотрудника, когда для начисления установлено значение ноль (446195)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="7c2e8-114">Проводки отпусков теперь разрешены для сотрудников, которые были уволены в будущем, и для начисления установлено значение ноль.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="7c2e8-115">Проводки отпусков можно ввести до даты увольнения сотрудника.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="7c2e8-116">Добавление настраиваемых полей в новую форму сотрудника отключает поля в панели операций для управления отпуском (473314)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="7c2e8-117">Параметры области действий в новой форме **Сотрудник** в модуле **Управление отпусками** больше не будут отключаться, если в новую форму **Сотрудник** добавлены настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="7c2e8-118">Если сделать поле комментария к отпуску обязательным, то запрос отпуска можно отправить при отсутствии введенного комментария (473543)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="7c2e8-119">Поля комментариев теперь могут быть обязательными, а запросы отпусков учитывают эту настройку.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="7c2e8-120">Обязательные поля являются предварительной версией функции.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="7c2e8-121">Объект DMF доступен для приостановки начисления</span><span class="sxs-lookup"><span data-stu-id="7c2e8-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="7c2e8-122">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7c2e8-123">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="7c2e8-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="7c2e8-124">Обязательные поля</span><span class="sxs-lookup"><span data-stu-id="7c2e8-124">Mandatory fields</span></span>

<span data-ttu-id="7c2e8-125">Можно сделать поля обязательными, используя возможности персонализации в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="7c2e8-126">Для этой функции требуются **сохраненные представления**.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="7c2e8-127">Дополнительные сведения о сохраненных представлениях см. в:</span><span class="sxs-lookup"><span data-stu-id="7c2e8-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="7c2e8-128">[Сохраненные представления — общая доступность](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) в плане выпуска Dynamics 365 волны 2 за 2020 год</span><span class="sxs-lookup"><span data-stu-id="7c2e8-128">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="7c2e8-129">Создание форм, использующих сохраненные представления</span><span class="sxs-lookup"><span data-stu-id="7c2e8-129">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="7c2e8-130">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="7c2e8-130">Human Resources application in Teams</span></span>

<span data-ttu-id="7c2e8-131">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="7c2e8-132">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="7c2e8-133">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-133">For more information, see:</span></span>

- <span data-ttu-id="7c2e8-134">[Отпуск сотрудника и опыт отсутствия в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 1 за 2020 год</span><span class="sxs-lookup"><span data-stu-id="7c2e8-134">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="7c2e8-135">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="7c2e8-135">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a><span data-ttu-id="7c2e8-136">Скоро</span><span class="sxs-lookup"><span data-stu-id="7c2e8-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="7c2e8-137">Предварительные версии функций приложения Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="7c2e8-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="7c2e8-138">**Уведомления**: отправители и утверждающие запросы отпусков получают уведомления в приложении Human Resources в Teams.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="7c2e8-139">Утверждающие смогут утверждать или отклонять запросы отпусков, и отправители будут получать уведомление, если запрос был утвержден или отклонен.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="7c2e8-140">**Календарь отпусков руководителя**: руководители смогут просматривать утвержденные и ожидающие отпуска для их непосредственных подчиненных в представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="7c2e8-141">Это представление упрощает понимание того, когда члены рабочей группы не находятся на рабочем месте.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="7c2e8-142">Сущности контрольного списка, включенные в Dataverse</span><span class="sxs-lookup"><span data-stu-id="7c2e8-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="7c2e8-143">Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="7c2e8-144">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="7c2e8-144">Known issues</span></span>

<span data-ttu-id="7c2e8-145">В рабочей области **управления функциями** могут отображаться функции, которые отключены в качестве предварительных функций предварительного просмотра, когда они обычно доступны.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="7c2e8-146">Далее приведен список общедоступных функций, которые показывают неправильный статус.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="7c2e8-147">Управление льготами</span><span class="sxs-lookup"><span data-stu-id="7c2e8-147">Benefits management</span></span>
- <span data-ttu-id="7c2e8-148">Управление обращениями</span><span class="sxs-lookup"><span data-stu-id="7c2e8-148">Case management</span></span>
- <span data-ttu-id="7c2e8-149">Ведение журнала базы данных (аудит)</span><span class="sxs-lookup"><span data-stu-id="7c2e8-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="7c2e8-150">Начисление отпуска для одной компании или одного плана</span><span class="sxs-lookup"><span data-stu-id="7c2e8-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="7c2e8-151">Приостановка начисления отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="7c2e8-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="7c2e8-152">Код основания корректировки сальдо и комментарий</span><span class="sxs-lookup"><span data-stu-id="7c2e8-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="7c2e8-153">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="7c2e8-153">Buy and sell leave</span></span>
- <span data-ttu-id="7c2e8-154">Календарь отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="7c2e8-154">Leave and absence calendar</span></span>
- <span data-ttu-id="7c2e8-155">Правила переноса отпуска</span><span class="sxs-lookup"><span data-stu-id="7c2e8-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="7c2e8-156">Аудит начисления отпуска</span><span class="sxs-lookup"><span data-stu-id="7c2e8-156">Leave accrual auditing</span></span>
- <span data-ttu-id="7c2e8-157">Удаление начисления отпуска</span><span class="sxs-lookup"><span data-stu-id="7c2e8-157">Leave accrual deletion</span></span>
- <span data-ttu-id="7c2e8-158">Округление начислений отпусков</span><span class="sxs-lookup"><span data-stu-id="7c2e8-158">Leave accrual rounding</span></span>
- <span data-ttu-id="7c2e8-159">Настройка нескольких типов отпусков в одном плане отпусков</span><span class="sxs-lookup"><span data-stu-id="7c2e8-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="7c2e8-160">Улучшения обновления отгулов</span><span class="sxs-lookup"><span data-stu-id="7c2e8-160">Update time-off enhancements</span></span>
- <span data-ttu-id="7c2e8-161">Использовать FTE сотрудника для начислений</span><span class="sxs-lookup"><span data-stu-id="7c2e8-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="7c2e8-162">Представление межфирменной компенсации</span><span class="sxs-lookup"><span data-stu-id="7c2e8-162">Cross company compensation view</span></span>
- <span data-ttu-id="7c2e8-163">Печать оценок производительности</span><span class="sxs-lookup"><span data-stu-id="7c2e8-163">Print performance reviews</span></span>
- <span data-ttu-id="7c2e8-164">Корректировки праздников при начислении отпуска</span><span class="sxs-lookup"><span data-stu-id="7c2e8-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="7c2e8-165">Сущность плана льгот сотрудников</span><span class="sxs-lookup"><span data-stu-id="7c2e8-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="7c2e8-166">Недавно мы обнаружили две ошибки, связанные с сущностью **BenefitsPlanEmployee**.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="7c2e8-167">При импорте регистраций работников **Код покрытия** и **Код типа плана** устанавливаются неправильно.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="7c2e8-168">Эта проблема приводит к неправильному отображению планов льгот сотрудников в форме **План льгот работников** и в форме **Открытие регистрации** в службе самообслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="7c2e8-169">Эта проблема также может повлиять на способность сотрудника выбирать планы в службе самообслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="7c2e8-170">В настоящее время нет обходного пути.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="7c2e8-171">Мы рассматриваем это как исправление высокого приоритета, и исправление будет развернуто в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="7c2e8-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c2e8-172">См. также</span><span class="sxs-lookup"><span data-stu-id="7c2e8-172">See also</span></span>

[<span data-ttu-id="7c2e8-173">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="7c2e8-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7c2e8-174">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="7c2e8-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7c2e8-175">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="7c2e8-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7c2e8-176">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="7c2e8-176">Manage features</span></span>](hr-admin-manage-features.md)
