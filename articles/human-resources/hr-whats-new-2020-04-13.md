---
title: Что нового или что изменилось в Dynamics 365 Human Resources (13 апреля 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 711cc4491024e647429b108438ce1d88483ea63c
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259825"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="9b65a-103">Что нового или что изменилось в Dynamics 365 Human Resources (13 апреля 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="9b65a-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="9b65a-104">В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b65a-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9b65a-105">Изменения применяются для номера сборки 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="9b65a-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="9b65a-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="9b65a-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="9b65a-107">Новая ритмичность выпуска производственных выпусков</span><span class="sxs-lookup"><span data-stu-id="9b65a-107">New production release cadence</span></span>

<span data-ttu-id="9b65a-108">С выпуском на этой неделе ритмичности выпуска Human Resources изменяется с еженедельного обновления на обновление раз в две недели.</span><span class="sxs-lookup"><span data-stu-id="9b65a-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="9b65a-109">Чтобы обеспечить согласованность с рекомендациями по безопасному развертыванию и обеспечить высокие стандарты стабильности и надежности в службе, процесс развертывания обновлений службы для всех регионов в данный состав составляет две недели.</span><span class="sxs-lookup"><span data-stu-id="9b65a-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="9b65a-110">Дополнительное тестирование и мониторинг применяются для проверки успешности развертывания на каждом этапе процесса.</span><span class="sxs-lookup"><span data-stu-id="9b65a-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="9b65a-111">Дополнительные сведения о ритмичности выпуска см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="9b65a-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="9b65a-112">Поле точности округления не редактируется после указания типа округления (435616)</span><span class="sxs-lookup"><span data-stu-id="9b65a-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="9b65a-113">После этого изменения поле **Точность округления** становится доступным после обновления поля **Тип округления**.</span><span class="sxs-lookup"><span data-stu-id="9b65a-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="9b65a-114">Невозможно изменить дату окончания регистрации отпуска, если план отпусков не имеет периодов начисления (413628)</span><span class="sxs-lookup"><span data-stu-id="9b65a-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="9b65a-115">Теперь можно изменить дату окончания регистрации без получения ошибки "Необходимо заполнить поле базиса даты начисления".</span><span class="sxs-lookup"><span data-stu-id="9b65a-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="9b65a-116">Объект занятости не синхронизируется с Common Data Service (430834)</span><span class="sxs-lookup"><span data-stu-id="9b65a-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="9b65a-117">Это изменение исправляет вопрос, в котором данные о приеме на работу не синхронизировались с Common Data Service после добавления финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="9b65a-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="9b65a-118">Удаление множественного родителя для объекта интервала времени рабочего календаря (431775)</span><span class="sxs-lookup"><span data-stu-id="9b65a-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="9b65a-119">Это изменение удаляет множественные родительские объекты для объекта **Интервал времени рабочего календаря**.</span><span class="sxs-lookup"><span data-stu-id="9b65a-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="9b65a-120">Фильтр с функцией CAST не работает в вызове OData объекта назначения работника на должность (431699)</span><span class="sxs-lookup"><span data-stu-id="9b65a-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="9b65a-121">Это обновление включает изменение, позволяющее использовать фильтр с функцией CAST в OData для объекта **Назначение работника на должность**.</span><span class="sxs-lookup"><span data-stu-id="9b65a-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="9b65a-122">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="9b65a-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="9b65a-123">Приостановка отпуска</span><span class="sxs-lookup"><span data-stu-id="9b65a-123">Leave suspension</span></span>

<span data-ttu-id="9b65a-124">Для сотрудника можно приостановить отпуск и отгул в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b65a-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="9b65a-125">Приостановка отпуска останавливает начисления отпусков для выбранных типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="9b65a-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="9b65a-126">Если приостановка происходит после того, как начисление было обработано, приостановка отпуска создает пропорциональную корректировку сальдо отпуска для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9b65a-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="9b65a-127">Для получения дополнительных сведений см. в разделе [Приостановка отпусков](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="9b65a-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="9b65a-128">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="9b65a-128">Carry forward rules</span></span>

<span data-ttu-id="9b65a-129">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="9b65a-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="9b65a-130">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="9b65a-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="9b65a-131">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="9b65a-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="9b65a-132">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="9b65a-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="9b65a-133">Объект сведений о трудоустройстве</span><span class="sxs-lookup"><span data-stu-id="9b65a-133">Employment Details entity</span></span>

<span data-ttu-id="9b65a-134">Объект **Сведений о трудоустройстве** был обновлен следующими полями:</span><span class="sxs-lookup"><span data-stu-id="9b65a-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="9b65a-135">**Частота платежей**</span><span class="sxs-lookup"><span data-stu-id="9b65a-135">**PayFrequency**</span></span>
- <span data-ttu-id="9b65a-136">**Код категории трудоустройства**</span><span class="sxs-lookup"><span data-stu-id="9b65a-136">**Employment Category ID**</span></span>
- <span data-ttu-id="9b65a-137">**Тип трудоустройства**</span><span class="sxs-lookup"><span data-stu-id="9b65a-137">**Employment Type**</span></span>
- <span data-ttu-id="9b65a-138">**Код типа трудоустройства**</span><span class="sxs-lookup"><span data-stu-id="9b65a-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="9b65a-139">**Статус льгот при трудоустройстве**</span><span class="sxs-lookup"><span data-stu-id="9b65a-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="9b65a-140">Данные настройки для этих полей зависят от того, включено ли управление льготами в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="9b65a-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="9b65a-141">Не заполняйте и не обновляйте эти поля в объекте **Сведения о трудоустройстве**, так как это приведет к ошибкам при импорте.</span><span class="sxs-lookup"><span data-stu-id="9b65a-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="9b65a-142">Предварительный просмотр SharePoint не работает в некоторых средах</span><span class="sxs-lookup"><span data-stu-id="9b65a-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="9b65a-143">Если предварительный просмотр документов, хранящихся в SharePoint, не работает, попробуйте выполнить следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="9b65a-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="9b65a-144">Убедитесь, что учетная запись администратора имеет адрес электронной почты, связанный с записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b65a-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="9b65a-145">Можно просмотреть эту информацию на странице **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="9b65a-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="9b65a-146">Если адрес электронной почты не настроен, необходимо добавить адрес электронной почты и поставщика с помощью надстройки Excel OData.</span><span class="sxs-lookup"><span data-stu-id="9b65a-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="9b65a-147">По умолчанию адрес электронной почты отсутствует в макете Excel.</span><span class="sxs-lookup"><span data-stu-id="9b65a-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="9b65a-148">Необходимо отредактировать макет Excel, добавить все поля, применить и обновить.</span><span class="sxs-lookup"><span data-stu-id="9b65a-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="9b65a-149">После выполнения этих шагов можно обновить учетную запись администратора.</span><span class="sxs-lookup"><span data-stu-id="9b65a-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="9b65a-150">После того как учетная запись администратора имеет связанную учетную запись электронной почты, войдите в Human Resources с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="9b65a-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="9b65a-151">Перейдите к вложению в SharePoint для запуска предварительного просмотра документа.</span><span class="sxs-lookup"><span data-stu-id="9b65a-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="9b65a-152">Выполните вход с другой учетной записью пользователя, который имеет доступ к вложениям, и убедитесь, что предварительный просмотр выполняется правильно.</span><span class="sxs-lookup"><span data-stu-id="9b65a-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>
