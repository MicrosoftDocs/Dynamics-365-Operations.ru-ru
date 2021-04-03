---
title: Что нового и что изменилось в Dynamics 365 Human Resources (28 мая 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 28 мая 2020 года.
author: andreabichsel
manager: tfehr
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e8d7f87f30286eefa1b3b53925702f4735132e6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465278"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="749e9-103">Что нового и что изменилось в Dynamics 365 Human Resources (28 мая 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="749e9-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="749e9-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="749e9-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="749e9-105">Изменения применяются для номера сборки 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="749e9-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="749e9-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="749e9-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="749e9-107">Объект LeaveRequest не работает при включении нескольких типов в план отпусков (447498)</span><span class="sxs-lookup"><span data-stu-id="749e9-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="749e9-108">После такого изменения **LeaveEnrollmentV2Entity** теперь доступен для исправления ошибки, которая происходит, если разрешено использование нескольких типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="749e9-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="749e9-109">Функция уменьшения количества конфликтов партий (предварительная версия) (446619)</span><span class="sxs-lookup"><span data-stu-id="749e9-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="749e9-110">Если эта функция включена, можно ожидать снижения блокировки таблиц структуры пакетной обработки, выбирая задачи и завершая задания.</span><span class="sxs-lookup"><span data-stu-id="749e9-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="749e9-111">UpdateConflict при сохранении работника не допускает редактирования записи в "Люди" (427915)</span><span class="sxs-lookup"><span data-stu-id="749e9-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="749e9-112">Это изменение исправляет ошибку при добавлении нового работника, обновлении сведений об адресе и изменении языковых настроек.</span><span class="sxs-lookup"><span data-stu-id="749e9-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="749e9-113">В этом уникальном случае отображается сообщение об ошибке, указывающее на то, что запись не может быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="749e9-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="749e9-114">Не удается добавить вложение к утвержденному запросу на отпуск для повторной отправки (425407)</span><span class="sxs-lookup"><span data-stu-id="749e9-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="749e9-115">Это изменение разрешает вложения для утвержденных запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="749e9-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="749e9-116">Пользователь может ввести компенсацию для сотрудника в другой форме юридических лиц (409529)</span><span class="sxs-lookup"><span data-stu-id="749e9-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="749e9-117">Это изменение отключает параметры компенсации, чтобы избежать случайного ввода записей компенсаций для неправильного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="749e9-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="749e9-118">Ошибка при переносе сотрудника, дата назначения должности сотрудника предшествует продолжительности должности (429402)</span><span class="sxs-lookup"><span data-stu-id="749e9-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="749e9-119">Сообщения об ошибках при перемещении сотрудника в этом сценарии были обновлены, чтобы лучше описать изменения, необходимые для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="749e9-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="749e9-120">Возможности вложений в регистрацию льгот в службе дистанционного обслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="749e9-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="749e9-121">Теперь можно добавлять вложения во время процесса регистрации льгот для каждого плана, в котором выполняется регистрация сотрудника.</span><span class="sxs-lookup"><span data-stu-id="749e9-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="749e9-122">Затем можно просмотреть вложения в форме **Зарегистрированная льгота работника**.</span><span class="sxs-lookup"><span data-stu-id="749e9-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="749e9-123">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="749e9-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="749e9-124">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="749e9-124">Human Resources application in Teams</span></span>

<span data-ttu-id="749e9-125">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="749e9-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="749e9-126">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="749e9-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="749e9-127">Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="749e9-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="749e9-128">Приостановка отпуска</span><span class="sxs-lookup"><span data-stu-id="749e9-128">Leave suspension</span></span>

<span data-ttu-id="749e9-129">Для сотрудника можно приостановить отпуск и отгул в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="749e9-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="749e9-130">Приостановка отпуска останавливает начисления отпусков для выбранных типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="749e9-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="749e9-131">Если приостановка происходит после того, как начисление было обработано, приостановка отпуска создает пропорциональную корректировку сальдо отпуска для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="749e9-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="749e9-132">Для получения дополнительных сведений см. в разделе [Приостановка отпусков](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="749e9-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="749e9-133">Обновление пользовательского интерфейса, чтобы показать, что начисление приостановлено (429550)</span><span class="sxs-lookup"><span data-stu-id="749e9-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="749e9-134">Теперь пользователь видит, что начисление приостановлено для плана.</span><span class="sxs-lookup"><span data-stu-id="749e9-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="749e9-135">Скоро</span><span class="sxs-lookup"><span data-stu-id="749e9-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="749e9-136">Ведение журнала базы данных (предварительная версия в июне)</span><span class="sxs-lookup"><span data-stu-id="749e9-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="749e9-137">Функция ведения журнала базы данных позволяет определить, какую таблицу и какие поля следует отслеживать.</span><span class="sxs-lookup"><span data-stu-id="749e9-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="749e9-138">Она также позволяет определить события, которые должны вызывать отслеживание изменений.</span><span class="sxs-lookup"><span data-stu-id="749e9-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="749e9-139">Доступны возможности запроса, которые позволяют увидеть эти изменения за период времени.</span><span class="sxs-lookup"><span data-stu-id="749e9-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="749e9-140">Покупка и продажа отпуска (предварительная версия, 1 июня)</span><span class="sxs-lookup"><span data-stu-id="749e9-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="749e9-141">Некоторые организации предоставляют льготу, позволяющую сотрудникам покупать или продавать отпуск.</span><span class="sxs-lookup"><span data-stu-id="749e9-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="749e9-142">Этот процесс часто управляется вручную.</span><span class="sxs-lookup"><span data-stu-id="749e9-142">This process is often managed manually.</span></span> <span data-ttu-id="749e9-143">Эта функция предоставляет более автоматизированный способ управления политиками и запросами для отдела кадров и помогает избежать ошибок при оптимизации процесса управления отпусками.</span><span class="sxs-lookup"><span data-stu-id="749e9-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="749e9-144">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="749e9-144">For more information, see:</span></span>

- [<span data-ttu-id="749e9-145">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="749e9-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="749e9-146">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="749e9-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="749e9-147">Объекты платформы управления данными (ДМФ) для управления льготами</span><span class="sxs-lookup"><span data-stu-id="749e9-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="749e9-148">Объекты управления льготами выпускаются.</span><span class="sxs-lookup"><span data-stu-id="749e9-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="749e9-149">Объекты DMF позволяют импортировать и экспортировать данные для упрощения настройки управления льготами.</span><span class="sxs-lookup"><span data-stu-id="749e9-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="749e9-150">Также будет доступен шаблон управления льготами для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="749e9-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="749e9-151">Шаблон экспортирует и импортирует данные последовательным способом с учетом зависимостей данных.</span><span class="sxs-lookup"><span data-stu-id="749e9-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="749e9-152">Добавление кода основания к приостановке начисления (июнь 1)</span><span class="sxs-lookup"><span data-stu-id="749e9-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="749e9-153">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="749e9-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="749e9-154">Правила переноса (июнь 1)</span><span class="sxs-lookup"><span data-stu-id="749e9-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="749e9-155">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="749e9-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="749e9-156">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="749e9-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="749e9-157">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="749e9-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="749e9-158">Приостановка начисления отпуска для указанных типов отпусков (июнь 1)</span><span class="sxs-lookup"><span data-stu-id="749e9-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="749e9-159">В данном выпуске отдел HR может создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="749e9-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="749e9-160">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="749e9-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="749e9-161">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="749e9-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="749e9-162">Объект DMF доступен для приостановки начисления (июнь 1)</span><span class="sxs-lookup"><span data-stu-id="749e9-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="749e9-163">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="749e9-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="749e9-164">См. также</span><span class="sxs-lookup"><span data-stu-id="749e9-164">See also</span></span>

[<span data-ttu-id="749e9-165">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="749e9-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="749e9-166">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="749e9-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="749e9-167">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="749e9-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="749e9-168">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="749e9-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]