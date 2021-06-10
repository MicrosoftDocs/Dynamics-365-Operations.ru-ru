---
title: Что нового и что изменилось в Dynamics 365 Human Resources (16 сентября 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 16 сентября 2020 года.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fe3ac2393e66a00e070d8cb6862c29625d39b53
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057172"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="79b24-103">Что нового и что изменилось в Dynamics 365 Human Resources (16 сентября 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="79b24-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="79b24-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="79b24-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="79b24-105">Изменения применяются для номера сборки 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="79b24-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="79b24-106">Числа в скобках рядом с некоторыми функциями относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.</span><span class="sxs-lookup"><span data-stu-id="79b24-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="79b24-107">Включено в данный выпуск</span><span class="sxs-lookup"><span data-stu-id="79b24-107">Included in this release</span></span>

-  [<span data-ttu-id="79b24-108">Сохраненные представления — общая доступность</span><span class="sxs-lookup"><span data-stu-id="79b24-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="79b24-109">- Дополнительные сведения см. в разделе [Сохраненные представления](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="79b24-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="79b24-110">Форма **Действия должности** имеет обновленную сетку измерений и новый диалог (469495).</span><span class="sxs-lookup"><span data-stu-id="79b24-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="79b24-111">Если установить для параметра **Ограничить доступ к сведениям о работнике** значение "Да" в пункте **Расширенный доступ** раздела **Общие параметры Human Resources**, в формах льгот теперь отображаются только соответствующие работники (393384).</span><span class="sxs-lookup"><span data-stu-id="79b24-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="79b24-112">Новые параметры создания календаря в сущности **WorkCalendar** (477055):</span><span class="sxs-lookup"><span data-stu-id="79b24-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="79b24-113">- Время окончания по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79b24-113">- Default ending time</span></span><br><span data-ttu-id="79b24-114">- Время начала по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79b24-114">-    Default starting time</span></span><br><span data-ttu-id="79b24-115">- Является ли пятница рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-115">-  Is Friday working day</span></span><br><span data-ttu-id="79b24-116">- Является ли понедельник рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-116">-  Is Monday working day</span></span><br><span data-ttu-id="79b24-117">- Является ли суббота рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-117">-  Is Saturday working day</span></span><br><span data-ttu-id="79b24-118">- Является ли воскресенье рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-118">- Is Sunday working day</span></span><br><span data-ttu-id="79b24-119">- Является ли четверг рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-119">- Is Thursday working day</span></span><br><span data-ttu-id="79b24-120">- Является ли вторник рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-120">- Is Tuesday working day</span></span><br><span data-ttu-id="79b24-121">- Является ли среда рабочим днем</span><span class="sxs-lookup"><span data-stu-id="79b24-121">- Is Wednesday working day</span></span><br><span data-ttu-id="79b24-122">- Код праздничного дня в рабочем календаре</span><span class="sxs-lookup"><span data-stu-id="79b24-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="79b24-123">Сущность **LeaveBankTransactionV1** теперь включает код причины (477823).</span><span class="sxs-lookup"><span data-stu-id="79b24-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="79b24-124">Теперь можно сохранять записи задач (492923).</span><span class="sxs-lookup"><span data-stu-id="79b24-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="79b24-125">Данные успешно публикуются из **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="79b24-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="79b24-126">Экспресс-вкладка **Компенсация** теперь отображается для типа сотрудника подрядчика в форме **Действия сотрудников** (482494).</span><span class="sxs-lookup"><span data-stu-id="79b24-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="79b24-127">Поля **Уровень** и **План** теперь являются обязательными, если задана **Фиксированная компенсация**.</span><span class="sxs-lookup"><span data-stu-id="79b24-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="79b24-128">Если эти поля не заполнены, отображается сообщение об ошибке (482497).</span><span class="sxs-lookup"><span data-stu-id="79b24-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="79b24-129">Поле **Тип плана** в разделе **Льготы** является раскрывающимся списком (488768).</span><span class="sxs-lookup"><span data-stu-id="79b24-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="79b24-130">Системные администраторы теперь получают уведомление, если настраиваемое поле удаляется из модуля Human Resources (481408).</span><span class="sxs-lookup"><span data-stu-id="79b24-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="79b24-131">В процессе увольнения сотрудника работа модуля Human Resources должна быть ожидаемой и не изменяет выбранную компанию после появления блокировки (479877).</span><span class="sxs-lookup"><span data-stu-id="79b24-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="79b24-132">Менеджеры больше не могут добавлять числовые столбцы с помощью персонализации (485317).</span><span class="sxs-lookup"><span data-stu-id="79b24-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="79b24-133">Менеджеры больше не могут удалять фильтр диапазона данных из истечения срока действия идентификационных номеров (485321).</span><span class="sxs-lookup"><span data-stu-id="79b24-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="79b24-134">Если поле **Кому подчиняется** пусто, сведения о должности продолжают отображаться при наведении указателя мыши на должность (433328).</span><span class="sxs-lookup"><span data-stu-id="79b24-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="79b24-135">Сотрудники могут теперь просматривать сведения о плане льгот в модуле "Дистанционное обслуживание сотрудников" (481676).</span><span class="sxs-lookup"><span data-stu-id="79b24-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="79b24-136">Сотрудники могут теперь видеть все зарегистрированные курсы (429048).</span><span class="sxs-lookup"><span data-stu-id="79b24-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="79b24-137">Теперь можно ограничить параметры просмотра для страницы **Профессиональные сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="79b24-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="79b24-138">Можно ограничить параметры просмотра для текущего юридического лица, по статусу работника и по типу работника (451501).</span><span class="sxs-lookup"><span data-stu-id="79b24-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="79b24-139">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="79b24-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="79b24-140">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="79b24-140">Human Resources app in Teams</span></span>

<span data-ttu-id="79b24-141">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="79b24-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="79b24-142">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="79b24-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="79b24-143">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="79b24-143">For more information, see:</span></span>

- <span data-ttu-id="79b24-144">[Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 1 за 2020 год</span><span class="sxs-lookup"><span data-stu-id="79b24-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="79b24-145">[Приложение Human Resources в Teams](./hr-admin-teams-leave-app.md) в документации Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="79b24-146">Предварительные версии функций приложения Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="79b24-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="79b24-147">**Уведомления**: отправители и утверждающие запросы отпусков получают уведомления в приложении Human Resources в Teams.</span><span class="sxs-lookup"><span data-stu-id="79b24-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="79b24-148">Утверждающие могут утверждать или отклонять запросы на отсутствие.</span><span class="sxs-lookup"><span data-stu-id="79b24-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="79b24-149">Отправители получат уведомление, если запрос был утвержден или отклонен.</span><span class="sxs-lookup"><span data-stu-id="79b24-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="79b24-150">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="79b24-150">For more information, see:</span></span>
   - <span data-ttu-id="79b24-151">[Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 2 за 2020 год</span><span class="sxs-lookup"><span data-stu-id="79b24-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="79b24-152">[Включение уведомлений для приложения Human Resources в Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) в документации Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="79b24-153">[Включение или выключение уведомлений Teams для отдельных пользователей](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) в документации Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="79b24-154">[Уведомления Teams](./hr-teams-leave-app.md#respond-to-teams-notifications) в документации Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="79b24-155">[Просмотр календаря отпусков вашей рабочей группы](./hr-teams-leave-app.md#view-your-teams-leave-calendar) в документации Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="79b24-156">**Календарь отпусков руководителя**: руководители могут просматривать утвержденные и ожидающие отпуска для их непосредственных подчиненных в представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="79b24-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="79b24-157">Это представление упрощает понимание того, когда члены рабочей группы не находятся на рабочем месте.</span><span class="sxs-lookup"><span data-stu-id="79b24-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="79b24-158">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="79b24-158">For more information, see:</span></span>
   - <span data-ttu-id="79b24-159">[Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 2 за 2020 год</span><span class="sxs-lookup"><span data-stu-id="79b24-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="79b24-160">[Просмотр календаря отпусков вашей рабочей группы](./hr-teams-leave-app.md#view-your-teams-leave-calendar) в документации Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="79b24-161">Параметр конфигурации для размещения списка рабочих элементов, назначенных мне (477004)</span><span class="sxs-lookup"><span data-stu-id="79b24-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="79b24-162">Новый параметр теперь становится доступным для позиционирования списка **Рабочие элементы, назначенные мне** в правом столбце панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="79b24-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="79b24-163">При таком изменении все рабочие элементы и списки дел отображаются в одной области.</span><span class="sxs-lookup"><span data-stu-id="79b24-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="79b24-164">Активируйте эту функцию, включив **Предварительная версия — улучшения рабочего процесса** в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="79b24-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="79b24-165">Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="79b24-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="79b24-166">Эта функция также поддерживает параметры рабочего процесса, которые отображаются в формах действий персонала.</span><span class="sxs-lookup"><span data-stu-id="79b24-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="79b24-167">Параметры рабочего процесса также появляются над экспресс-вкладкой действий для быстрого доступа.</span><span class="sxs-lookup"><span data-stu-id="79b24-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="79b24-168">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="79b24-168">For more information, see:</span></span> 

- <span data-ttu-id="79b24-169">[Улучшения рабочего процесса управления предприятием и персоналом](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) в плане волны 2 выпуска 2020 года Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="79b24-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Рабочие элементы, назначенные мне](./media/hr-workflow-work-items-assigned-to-me.png)

![Быстрый доступ к элементам рабочего процесса](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="79b24-172">Календарь отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="79b24-172">Leave and absence calendar</span></span>

<span data-ttu-id="79b24-173">В этой версии включены дополнительные параметры календаря для календарей отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="79b24-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="79b24-174">Дополнительные сведения см. в разделе [Просмотр календарей рабочей группы и компании](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="79b24-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="79b24-175">Скоро</span><span class="sxs-lookup"><span data-stu-id="79b24-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="79b24-176">Сущности контрольного списка, включенные в Dataverse</span><span class="sxs-lookup"><span data-stu-id="79b24-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="79b24-177">Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="79b24-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="79b24-178">Коды причин управления льготами</span><span class="sxs-lookup"><span data-stu-id="79b24-178">Benefits management reason codes</span></span>

<span data-ttu-id="79b24-179">Коды причин управления льготами скоро будут объединены с существующими кодами причин в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="79b24-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="79b24-180">Если созданные коды причин в модуле управления льготами имеют более 15 символов, необходимо изменить имя кода причины в форме **Коды причин** управления льготами, чтобы оно состояло не более чем из 15 символов.</span><span class="sxs-lookup"><span data-stu-id="79b24-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="79b24-181">После обновления имени код причины появится под существующим кодом причины в управлении персоналом.</span><span class="sxs-lookup"><span data-stu-id="79b24-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="79b24-182">Это изменение будет доступно в будущем и не повлияет на существующие функции.</span><span class="sxs-lookup"><span data-stu-id="79b24-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="79b24-183">См. также</span><span class="sxs-lookup"><span data-stu-id="79b24-183">See also</span></span>

[<span data-ttu-id="79b24-184">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="79b24-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="79b24-185">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="79b24-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="79b24-186">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="79b24-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="79b24-187">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="79b24-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
