---
title: Что нового и что изменилось в Dynamics 365 Human Resources (11 июня 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 11 июня 2020 года.
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8e5fa842739bbc0070f892c7f19e84ac6ac0ceb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463654"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="d719e-103">Что нового и что изменилось в Dynamics 365 Human Resources (11 июня 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="d719e-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d719e-104">В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d719e-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d719e-105">Изменения применяются для номера сборки 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="d719e-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="d719e-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="d719e-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="d719e-107">Усовершенствованная форма сотрудника иногда приводит к прекращению работы кнопок закрытия (X) дочерних форм (442369)</span><span class="sxs-lookup"><span data-stu-id="d719e-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="d719e-108">Когда новая форма **Работник** была активирована, кнопка Закрыть (**X**) периодически не работала в дочерних формах.</span><span class="sxs-lookup"><span data-stu-id="d719e-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="d719e-109">Эта проблема была прерывистой.</span><span class="sxs-lookup"><span data-stu-id="d719e-109">This problem was intermittent.</span></span> <span data-ttu-id="d719e-110">После выхода из формы и возврата к ней ее можно было закрыть.</span><span class="sxs-lookup"><span data-stu-id="d719e-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="d719e-111">Например, можно выбрать пункт меню слева, вернуться к форме **Работник** и затем закрыть ее.</span><span class="sxs-lookup"><span data-stu-id="d719e-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="d719e-112">Выпуск данной недели устраняет эту проблему.</span><span class="sxs-lookup"><span data-stu-id="d719e-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="d719e-113">Сущность личного контакта сотрудника не экспортирует личные контакты с родительским типом отношений</span><span class="sxs-lookup"><span data-stu-id="d719e-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="d719e-114">В этом выпуске сущность **Личное контактное лицо сотрудника** экспортирует все типы отношений.</span><span class="sxs-lookup"><span data-stu-id="d719e-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="d719e-115">HcmPositionWorkerAssignmentV2Entity должен входить в состав пакета интеграции зарплаты Ceridian по умолчанию (448506)</span><span class="sxs-lookup"><span data-stu-id="d719e-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="d719e-116">При этом изменении **HcmPositionWorkerAssignmentV2Entity** входит в состав пакета интеграции зарплаты Ceridian.</span><span class="sxs-lookup"><span data-stu-id="d719e-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d719e-117">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="d719e-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="d719e-118">Регистрация базы данных</span><span class="sxs-lookup"><span data-stu-id="d719e-118">Database logging</span></span>

<span data-ttu-id="d719e-119">Функция ведения журнала базы данных позволяет определить, какие таблицы и какие поля следует отслеживать.</span><span class="sxs-lookup"><span data-stu-id="d719e-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="d719e-120">Она также позволяет определить события, которые должны вызывать отслеживание изменений.</span><span class="sxs-lookup"><span data-stu-id="d719e-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="d719e-121">Для просмотра этих изменений со временем используются средства ведения журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="d719e-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="d719e-122">Дополнительные сведения см. в разделе [Настройка ведения журнала базы данных и управление этим журналом](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="d719e-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="d719e-123">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="d719e-123">Human Resources application in Teams</span></span>

<span data-ttu-id="d719e-124">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d719e-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d719e-125">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="d719e-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d719e-126">Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="d719e-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="d719e-127">Объекты платформы управления данными (ДМФ) для управления льготами</span><span class="sxs-lookup"><span data-stu-id="d719e-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="d719e-128">Объекты управления льготами выпускаются.</span><span class="sxs-lookup"><span data-stu-id="d719e-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="d719e-129">Объекты DMF позволяют импортировать и экспортировать данные для упрощения настройки управления льготами.</span><span class="sxs-lookup"><span data-stu-id="d719e-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="d719e-130">Будет доступен шаблон управления льготами для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="d719e-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="d719e-131">Шаблон экспортирует и импортирует данные последовательно для учета зависимостей данных.</span><span class="sxs-lookup"><span data-stu-id="d719e-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="d719e-132">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="d719e-132">Buy and sell leave</span></span> 

<span data-ttu-id="d719e-133">Некоторые организации предоставляют льготу, позволяющую сотрудникам покупать или продавать отпуск.</span><span class="sxs-lookup"><span data-stu-id="d719e-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="d719e-134">Этот процесс часто управляется вручную.</span><span class="sxs-lookup"><span data-stu-id="d719e-134">This process is often managed manually.</span></span> <span data-ttu-id="d719e-135">Эта функция автоматизирует управление политиками и запросами для отдела кадров.</span><span class="sxs-lookup"><span data-stu-id="d719e-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="d719e-136">Она упрощает процесс управления отпусками и помогает исключить ошибки.</span><span class="sxs-lookup"><span data-stu-id="d719e-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="d719e-137">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="d719e-137">For more information, see:</span></span>

- [<span data-ttu-id="d719e-138">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="d719e-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="d719e-139">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="d719e-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="d719e-140">Начисление отпуска для одной компании или одного плана</span><span class="sxs-lookup"><span data-stu-id="d719e-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="d719e-141">Клиенты могут обрабатывать начисления для одной компании или для одного плана отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="d719e-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="d719e-142">Эта возможность обеспечивает ясность процесса начисления для клиентов с различными политиками лет отпусков или начисления отпусков.</span><span class="sxs-lookup"><span data-stu-id="d719e-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="d719e-143">Дополнительные сведения см. в разделе [Начисление отпуска по компаниям или по плану отпуска](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="d719e-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="d719e-144">Добавление вложений в запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="d719e-144">Add attachments to time off requests</span></span>

<span data-ttu-id="d719e-145">Возможность добавлять вложения к утвержденным запросам отпусков является критической в текущей среде COVID-19.</span><span class="sxs-lookup"><span data-stu-id="d719e-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="d719e-146">Сотрудники теперь смогут добавлять эти вложения.</span><span class="sxs-lookup"><span data-stu-id="d719e-146">Employees can now add these attachments.</span></span> <span data-ttu-id="d719e-147">Они также имеют более глубокое представление о том, как выполняются запросы на отпуск.</span><span class="sxs-lookup"><span data-stu-id="d719e-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="d719e-148">Дополнительные сведения см. в разделе [Добавление вложений к существующему запросу](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="d719e-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="d719e-149">Добавление кода основания к приостановке начисления</span><span class="sxs-lookup"><span data-stu-id="d719e-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="d719e-150">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="d719e-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d719e-151">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="d719e-151">Carry forward rules</span></span> 

<span data-ttu-id="d719e-152">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="d719e-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d719e-153">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="d719e-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d719e-154">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="d719e-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="d719e-155">Приостановка начисления отпуска для указанных типов отпусков</span><span class="sxs-lookup"><span data-stu-id="d719e-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="d719e-156">Вы можете создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="d719e-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d719e-157">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="d719e-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d719e-158">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="d719e-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d719e-159">Объект DMF доступен для приостановки начисления</span><span class="sxs-lookup"><span data-stu-id="d719e-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="d719e-160">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="d719e-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d719e-161">Скоро</span><span class="sxs-lookup"><span data-stu-id="d719e-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="d719e-162">Новые возможности платформы</span><span class="sxs-lookup"><span data-stu-id="d719e-162">New platform capabilities</span></span> 

<span data-ttu-id="d719e-163">Вы сможете сделать поля обязательными путем использования персонализации.</span><span class="sxs-lookup"><span data-stu-id="d719e-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="d719e-164">Для этой функции потребуется включить **Сохраненные представления**.</span><span class="sxs-lookup"><span data-stu-id="d719e-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="d719e-165">Настройка имени самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="d719e-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="d719e-166">Новый параметр будет доступен в параметрах Human Resources, чтобы обновить имя рабочей области самообслуживания сотрудников на самообслуживание.</span><span class="sxs-lookup"><span data-stu-id="d719e-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="d719e-167">См. также</span><span class="sxs-lookup"><span data-stu-id="d719e-167">See also</span></span>

[<span data-ttu-id="d719e-168">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="d719e-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d719e-169">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="d719e-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d719e-170">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="d719e-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d719e-171">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="d719e-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]