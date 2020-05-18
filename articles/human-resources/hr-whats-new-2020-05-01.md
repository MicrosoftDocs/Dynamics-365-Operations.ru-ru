---
title: Что нового и что изменилось в Dynamics 365 Human Resources (1 мая 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a0cfd1c1b0dcc9defaad7e4cce22ebe1e91fae
ms.sourcegitcommit: cc5dc0bd90277f1ba684dd310da3274886ce573c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "3320927"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="63677-103">Что нового и что изменилось в Dynamics 365 Human Resources (1 мая 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="63677-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

<span data-ttu-id="63677-104">В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63677-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="63677-105">Изменения применяются для номера сборки 8.1.3196.</span><span class="sxs-lookup"><span data-stu-id="63677-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="63677-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="63677-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="63677-107">Новые объекты управления производительностью доступны в структуре управления данными (DMF)</span><span class="sxs-lookup"><span data-stu-id="63677-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="63677-108">Теперь доступны следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="63677-108">The following entities are now available.</span></span> <span data-ttu-id="63677-109">Если эти объекты не отображаются в списке объектов, используйте параметр **Обновить объекты** в пункте **Параметры платформы > Настройки объектов > Обновить список объектов**.</span><span class="sxs-lookup"><span data-stu-id="63677-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="63677-110">**Компетенция обсуждения**</span><span class="sxs-lookup"><span data-stu-id="63677-110">**Discussion Competency**</span></span>
- <span data-ttu-id="63677-111">**Цели обсуждения**</span><span class="sxs-lookup"><span data-stu-id="63677-111">**Discussion Goals**</span></span>
- <span data-ttu-id="63677-112">**Измерение обсуждения**</span><span class="sxs-lookup"><span data-stu-id="63677-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="63677-113">**Тема обсуждения**</span><span class="sxs-lookup"><span data-stu-id="63677-113">**Discussion Topic**</span></span>
- <span data-ttu-id="63677-114">**Журнал показателей производительности**</span><span class="sxs-lookup"><span data-stu-id="63677-114">**Performance Journal**</span></span>
- <span data-ttu-id="63677-115">**Измерение**</span><span class="sxs-lookup"><span data-stu-id="63677-115">**Measurement**</span></span>
- <span data-ttu-id="63677-116">**Измерение цели**</span><span class="sxs-lookup"><span data-stu-id="63677-116">**Goal Measurement**</span></span>

<span data-ttu-id="63677-117">Кроме того, к объекту **Обсуждение** были добавлены **Общая оценка** и **Средняя оценка**.</span><span class="sxs-lookup"><span data-stu-id="63677-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="63677-118">Увеличение длины комментариев к запросу на отпуск (275641)</span><span class="sxs-lookup"><span data-stu-id="63677-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="63677-119">Комментарии к запросам на отпуск в данный момент могут быть более 100 символов.</span><span class="sxs-lookup"><span data-stu-id="63677-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="63677-120">Окончательные комментарии в оценке не отображаются, если руководитель или сотрудник вошли в другую компанию (431688)</span><span class="sxs-lookup"><span data-stu-id="63677-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="63677-121">Все комментарии теперь будут отображаться при просмотре оценок.</span><span class="sxs-lookup"><span data-stu-id="63677-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="63677-122">Определяемые пользователем ссылки не поддерживаются в форме создания работника (390374)</span><span class="sxs-lookup"><span data-stu-id="63677-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="63677-123">Определяемые пользователем ссылки теперь включены в оптимизированной форме **Работник**.</span><span class="sxs-lookup"><span data-stu-id="63677-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="63677-124">HcmRatingLevelEntity вызывает сбой API OData (439476)</span><span class="sxs-lookup"><span data-stu-id="63677-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="63677-125">Это изменение исправляет сбои в работе API.</span><span class="sxs-lookup"><span data-stu-id="63677-125">This change corrects the API crash.</span></span> <span data-ttu-id="63677-126">Эта ошибка вызывается повторяющимся именем.</span><span class="sxs-lookup"><span data-stu-id="63677-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="63677-127">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="63677-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="63677-128">Приостановка отпуска</span><span class="sxs-lookup"><span data-stu-id="63677-128">Leave suspension</span></span>

<span data-ttu-id="63677-129">Для сотрудника можно приостановить отпуск и отгул в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63677-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="63677-130">Приостановка отпуска останавливает начисления отпусков для выбранных типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="63677-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="63677-131">Если приостановка происходит после того, как начисление было обработано, приостановка отпуска создает пропорциональную корректировку сальдо отпуска для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="63677-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="63677-132">Для получения дополнительных сведений см. в разделе [Приостановка отпусков](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="63677-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="63677-133">Обновление пользовательского интерфейса, чтобы показать, что начисление приостановлено (429550)</span><span class="sxs-lookup"><span data-stu-id="63677-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="63677-134">Теперь пользователь видит, что начисление приостановлено для плана.</span><span class="sxs-lookup"><span data-stu-id="63677-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="63677-135">Приостановка начисления отпуска для указанных типов отпусков (272447)</span><span class="sxs-lookup"><span data-stu-id="63677-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="63677-136">В данном выпуске отдел HR может создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="63677-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="63677-137">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="63677-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="63677-138">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="63677-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="63677-139">Объект DMF доступен для приостановки начисления (429549)</span><span class="sxs-lookup"><span data-stu-id="63677-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="63677-140">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="63677-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="63677-141">Добавление кода основания к приостановке начисления (429547)</span><span class="sxs-lookup"><span data-stu-id="63677-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="63677-142">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="63677-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="63677-143">Начало перехода от параметров Human Resources к параметрам отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="63677-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="63677-144">В этой версии начинается объединение параметров Human Resources с параметрами отпуска и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="63677-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="63677-145">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="63677-145">Carry forward rules</span></span>

<span data-ttu-id="63677-146">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="63677-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="63677-147">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="63677-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="63677-148">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="63677-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="63677-149">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="63677-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="63677-150">Предварительный просмотр SharePoint не работает в некоторых средах</span><span class="sxs-lookup"><span data-stu-id="63677-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="63677-151">Если предварительный просмотр документов, хранящихся в SharePoint, не работает, попробуйте выполнить следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="63677-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="63677-152">Убедитесь, что учетная запись администратора имеет адрес электронной почты, связанный с записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="63677-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="63677-153">Можно просмотреть эту информацию на странице **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="63677-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="63677-154">Если адрес электронной почты не настроен, необходимо добавить адрес электронной почты и поставщика с помощью надстройки Excel OData.</span><span class="sxs-lookup"><span data-stu-id="63677-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="63677-155">По умолчанию адрес электронной почты отсутствует в макете Excel.</span><span class="sxs-lookup"><span data-stu-id="63677-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="63677-156">Необходимо отредактировать макет Excel, добавить все поля, применить и обновить.</span><span class="sxs-lookup"><span data-stu-id="63677-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="63677-157">После выполнения этих шагов можно обновить учетную запись администратора.</span><span class="sxs-lookup"><span data-stu-id="63677-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="63677-158">После того как учетная запись администратора имеет связанную учетную запись электронной почты, войдите в Human Resources с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="63677-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="63677-159">Перейдите к вложению в SharePoint для запуска предварительного просмотра документа.</span><span class="sxs-lookup"><span data-stu-id="63677-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="63677-160">Выполните вход с другой учетной записью пользователя, который имеет доступ к вложениям, и убедитесь, что предварительный просмотр выполняется правильно.</span><span class="sxs-lookup"><span data-stu-id="63677-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>