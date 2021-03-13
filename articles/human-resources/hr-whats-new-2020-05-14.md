---
title: Что нового и что изменилось в Dynamics 365 Human Resources (14 мая 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 14 мая 2020 года.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
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
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127857"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="8845d-103">Что нового и что изменилось в Dynamics 365 Human Resources (14 мая 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="8845d-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8845d-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8845d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8845d-105">Изменения применяются для номера сборки 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="8845d-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="8845d-106">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.</span><span class="sxs-lookup"><span data-stu-id="8845d-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="8845d-107">Изменения платформы</span><span class="sxs-lookup"><span data-stu-id="8845d-107">Platform changes</span></span>

<span data-ttu-id="8845d-108">Изменения платформы включены в выпуск данной недели.</span><span class="sxs-lookup"><span data-stu-id="8845d-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="8845d-109">Дополнительные сведения см. в разделе [Обновления платформы для версии 10.0.10 приложений Finance and Operations (май 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span><span class="sxs-lookup"><span data-stu-id="8845d-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="8845d-110">В состав данного выпуска входят исправления ошибок и изменения в сохраненных представлениях.</span><span class="sxs-lookup"><span data-stu-id="8845d-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="8845d-111">Убедитесь, что списки выбора Dataverse соответствуют перечислениям Отпуск (436343)</span><span class="sxs-lookup"><span data-stu-id="8845d-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="8845d-112">Теперь списки выбора Dataverse соответствуют перечислениям Отпуск.</span><span class="sxs-lookup"><span data-stu-id="8845d-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="8845d-113">Разрешить пользователям настраивать workflow-процесс для запроса на отпуск на основе суммы запроса (300044)</span><span class="sxs-lookup"><span data-stu-id="8845d-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="8845d-114">Пользователи могут настраивать workflow-процессы для запроса на отпуск на основе сумм запроса.</span><span class="sxs-lookup"><span data-stu-id="8845d-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="8845d-115">Форма Новый работник предоставляет данные через меню Вид, когда включена расширенная безопасность (403185)</span><span class="sxs-lookup"><span data-stu-id="8845d-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="8845d-116">В этом выпуске исправляется, как просматриваются работники в функциях юридических лиц, когда включен расширенный доступ, а работники других компаний доступны.</span><span class="sxs-lookup"><span data-stu-id="8845d-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="8845d-117">Разрешить выполнение начислений отпусков для одного плана или одной компании (318844)</span><span class="sxs-lookup"><span data-stu-id="8845d-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="8845d-118">При таком изменении можно выполнить начисления для компании или плана.</span><span class="sxs-lookup"><span data-stu-id="8845d-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="8845d-119">Отображение эквивалента полной занятости (FTE) для должности в форме Зарегистрированные работники (414658)</span><span class="sxs-lookup"><span data-stu-id="8845d-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="8845d-120">Значение FTE из должности работника определяет ставку начисления работника, когда в типе отпуска активирована опция FTE.</span><span class="sxs-lookup"><span data-stu-id="8845d-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="8845d-121">Это поле отображается в форме **зарегистрированные работники** и в диалоговом окне **массовой регистрации** .</span><span class="sxs-lookup"><span data-stu-id="8845d-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="8845d-122">Пакетное задание Добавить окончание срока действия сальдо отпуска (431266)</span><span class="sxs-lookup"><span data-stu-id="8845d-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="8845d-123">Теперь доступно новое пакетное задание, которое выполняется ежедневно.</span><span class="sxs-lookup"><span data-stu-id="8845d-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="8845d-124">Оно уменьшает остаток сальдо отпуска, когда даты окончания срока действия становятся текущими.</span><span class="sxs-lookup"><span data-stu-id="8845d-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="8845d-125">Экспорт личных контактов для сотрудника с помощью объекта личного контактного лица сотрудника не экспортирует личные контакты с родительским типом отношений (345893)</span><span class="sxs-lookup"><span data-stu-id="8845d-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="8845d-126">Объект данных **личного контактного лица сотрудника** (**HcmPersonalContactPersonEntity** в ДМФ и **PersonalContactPerson** в OData) не может экспортировать личные контакты, имеющие тип отношения **родитель**.</span><span class="sxs-lookup"><span data-stu-id="8845d-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="8845d-127">Эта проблема исправлена для личных контактов, которые создаются после этого изменения.</span><span class="sxs-lookup"><span data-stu-id="8845d-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="8845d-128">Существующие личные контакты типа **родитель** будут исправлены в более позднем выпуске.</span><span class="sxs-lookup"><span data-stu-id="8845d-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="8845d-129">Коды причин могут быть отображены в нескольких сценариях, когда они помечены как отпуск и отсутствие и активирована упрощенная форма "сотрудник" (434163)</span><span class="sxs-lookup"><span data-stu-id="8845d-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="8845d-130">Это изменение ограничивает коды причин только кодами отпуска и отсутствия, когда включается упрощенная запись сотрудника.</span><span class="sxs-lookup"><span data-stu-id="8845d-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="8845d-131">Функция предварительного просмотра Назначить сотрудникам план отпусков в будущем выводит сообщение об ошибке (433555)</span><span class="sxs-lookup"><span data-stu-id="8845d-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="8845d-132">Это изменение исправляет ошибку, если план отпусков имеет два присвоенных типа отпусков и предпринимается попытка назначить сотрудника.</span><span class="sxs-lookup"><span data-stu-id="8845d-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="8845d-133">Для всех пользователей отображается баннер Приступая к работе (441731)</span><span class="sxs-lookup"><span data-stu-id="8845d-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="8845d-134">Благодаря этому изменению баннер "Приступая к работе" скрыт для пользователей, не являющихся системными администраторами или администраторами управления данными.</span><span class="sxs-lookup"><span data-stu-id="8845d-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="8845d-135">Объект адреса работника Dataverse действует по-разному в отношении дат и времени дат вступления в силу в Human Resources (425071)</span><span class="sxs-lookup"><span data-stu-id="8845d-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="8845d-136">Это изменение позволяет сохранить сведения об адресе, согласованные по определенным сценариям, на основе дат адреса.</span><span class="sxs-lookup"><span data-stu-id="8845d-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="8845d-137">Не удается добавить вложение к утвержденному запросу на отпуск (425407)</span><span class="sxs-lookup"><span data-stu-id="8845d-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="8845d-138">С помощью выпуска данной недели можно добавлять вложения к утвержденным запросам на отпуск без изменения запроса на отпуск.</span><span class="sxs-lookup"><span data-stu-id="8845d-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8845d-139">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="8845d-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="8845d-140">Приостановка отпуска</span><span class="sxs-lookup"><span data-stu-id="8845d-140">Leave suspension</span></span>

<span data-ttu-id="8845d-141">Для сотрудника можно приостановить отпуск и отгул в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8845d-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="8845d-142">Приостановка отпуска останавливает начисления отпусков для выбранных типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="8845d-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="8845d-143">Если приостановка происходит после того, как начисление было обработано, приостановка отпуска создает пропорциональную корректировку сальдо отпуска для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="8845d-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="8845d-144">Для получения дополнительных сведений см. в разделе [Приостановка отпусков](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="8845d-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="8845d-145">Обновление пользовательского интерфейса, чтобы показать, что начисление приостановлено (429550)</span><span class="sxs-lookup"><span data-stu-id="8845d-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="8845d-146">Теперь пользователь видит, что начисление приостановлено для плана.</span><span class="sxs-lookup"><span data-stu-id="8845d-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="8845d-147">Приостановка начисления отпуска для указанных типов отпусков (272447)</span><span class="sxs-lookup"><span data-stu-id="8845d-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="8845d-148">В данном выпуске отдел HR может создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="8845d-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="8845d-149">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="8845d-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="8845d-150">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="8845d-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="8845d-151">Объект DMF доступен для приостановки начисления (429549)</span><span class="sxs-lookup"><span data-stu-id="8845d-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="8845d-152">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="8845d-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="8845d-153">Добавление кода основания к приостановке начисления (429547)</span><span class="sxs-lookup"><span data-stu-id="8845d-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="8845d-154">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="8845d-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="8845d-155">Начало перехода от параметров Human Resources к параметрам отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="8845d-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="8845d-156">В этой версии начинается объединение параметров Human Resources с параметрами отпуска и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="8845d-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="8845d-157">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="8845d-157">Carry forward rules</span></span>

<span data-ttu-id="8845d-158">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="8845d-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="8845d-159">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="8845d-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="8845d-160">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="8845d-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8845d-161">См. также</span><span class="sxs-lookup"><span data-stu-id="8845d-161">See also</span></span>

[<span data-ttu-id="8845d-162">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="8845d-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8845d-163">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="8845d-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8845d-164">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="8845d-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8845d-165">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="8845d-165">Manage features</span></span>](hr-admin-manage-features.md)