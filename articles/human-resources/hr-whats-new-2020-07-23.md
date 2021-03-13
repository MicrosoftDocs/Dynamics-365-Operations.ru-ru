---
title: Что нового и что изменилось в Dynamics 365 Human Resources (23 июля 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 23 июля 2020 года.
author: andreabichsel
manager: tfehr
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f5e10d6d1dedfc251a1a00110b50c9096314d75b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127529"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="2d098-103">Что нового и что изменилось в Dynamics 365 Human Resources (23 июля 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="2d098-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2d098-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2d098-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2d098-105">Изменения применяются для номера сборки 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="2d098-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="2d098-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="2d098-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="2d098-107">Удаление финансовых аналитик для позиции не работает должным образом (445476)</span><span class="sxs-lookup"><span data-stu-id="2d098-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="2d098-108">После удаления аналитик из позиции эти же позиции удаляются из Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2d098-108">Removing dimensions from a position now removes those same positions from Dataverse.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="2d098-109">Позиции не в иерархии показывают неактивные позиции (397257)</span><span class="sxs-lookup"><span data-stu-id="2d098-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="2d098-110">Неактивные позиции (с истекшим сроком действия) не отображаются в иерархии позиций в качестве **Позиции не в иерархии**.</span><span class="sxs-lookup"><span data-stu-id="2d098-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="2d098-111">Проверка между LeaveEnrollmentEntity и HcmWorkerEntity в импорте в структуре управления данными (DMF) вызывает медленную загрузку данных (442324)</span><span class="sxs-lookup"><span data-stu-id="2d098-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="2d098-112">Изменения в этом выпуске увеличивают производительность **LeaveEnrollmentEntity**.</span><span class="sxs-lookup"><span data-stu-id="2d098-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="2d098-113">Невозможно выполнить индивидуальную настройку в администрировании организации (447490)</span><span class="sxs-lookup"><span data-stu-id="2d098-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="2d098-114">С этим изменением теперь можно персонализировать ссылки в **Администрирование организации**.</span><span class="sxs-lookup"><span data-stu-id="2d098-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2d098-115">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="2d098-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="2d098-116">Обязательные поля</span><span class="sxs-lookup"><span data-stu-id="2d098-116">Mandatory fields</span></span> 

<span data-ttu-id="2d098-117">Теперь можно сделать поля обязательными, используя возможности персонализации в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2d098-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="2d098-118">Для этой функции требуются **сохраненные представления**.</span><span class="sxs-lookup"><span data-stu-id="2d098-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="2d098-119">Приложение Human Resources в Teams</span><span class="sxs-lookup"><span data-stu-id="2d098-119">Human Resources application in Teams</span></span>

<span data-ttu-id="2d098-120">Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2d098-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="2d098-121">Они могут взаимодействовать с ботом для создания запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="2d098-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="2d098-122">Дополнительные сведения см. в разделе [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="2d098-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="2d098-123">Объекты платформы управления данными (ДМФ) для управления льготами</span><span class="sxs-lookup"><span data-stu-id="2d098-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="2d098-124">Объекты управления льготами выпускаются.</span><span class="sxs-lookup"><span data-stu-id="2d098-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="2d098-125">Объекты DMF позволяют импортировать и экспортировать данные для упрощения настройки управления льготами.</span><span class="sxs-lookup"><span data-stu-id="2d098-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="2d098-126">Будет доступен шаблон управления льготами для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="2d098-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="2d098-127">Шаблон экспортирует и импортирует данные последовательно для учета зависимостей данных.</span><span class="sxs-lookup"><span data-stu-id="2d098-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="2d098-128">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="2d098-128">Buy and sell leave</span></span> 

<span data-ttu-id="2d098-129">Некоторые организации предоставляют льготу, позволяющую сотрудникам покупать или продавать отпуск.</span><span class="sxs-lookup"><span data-stu-id="2d098-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="2d098-130">Этот процесс часто управляется вручную.</span><span class="sxs-lookup"><span data-stu-id="2d098-130">This process is often managed manually.</span></span> <span data-ttu-id="2d098-131">Эта функция автоматизирует управление политиками и запросами для отдела кадров.</span><span class="sxs-lookup"><span data-stu-id="2d098-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="2d098-132">Она упрощает процесс управления отпусками и помогает исключить ошибки.</span><span class="sxs-lookup"><span data-stu-id="2d098-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="2d098-133">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="2d098-133">For more information, see:</span></span>

- [<span data-ttu-id="2d098-134">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="2d098-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="2d098-135">Покупка и продажа отпуска</span><span class="sxs-lookup"><span data-stu-id="2d098-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="2d098-136">Начисление отпуска для одной компании или одного плана</span><span class="sxs-lookup"><span data-stu-id="2d098-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="2d098-137">Клиенты могут обрабатывать начисления для одной компании или для одного плана отпусков и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="2d098-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="2d098-138">Эта возможность обеспечивает ясность для процесса начисления для клиентов с различными политиками лет отпусков или начисления отпусков.</span><span class="sxs-lookup"><span data-stu-id="2d098-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="2d098-139">Дополнительные сведения см. в разделе [Начисление отпуска по компаниям или по плану отпуска](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="2d098-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="2d098-140">Добавление вложений в запросы на отгулы</span><span class="sxs-lookup"><span data-stu-id="2d098-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="2d098-141">Возможность добавлять вложения к утвержденным запросам отпусков является критической в текущей среде COVID-19.</span><span class="sxs-lookup"><span data-stu-id="2d098-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="2d098-142">Сотрудники теперь смогут добавлять эти вложения.</span><span class="sxs-lookup"><span data-stu-id="2d098-142">Employees can now add these attachments.</span></span> <span data-ttu-id="2d098-143">Они также имеют более глубокое представление о том, как выполняются запросы на отпуск.</span><span class="sxs-lookup"><span data-stu-id="2d098-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="2d098-144">Дополнительные сведения см. в разделе [Добавление вложений к существующему запросу](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="2d098-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="2d098-145">Добавление кода основания к приостановке начисления</span><span class="sxs-lookup"><span data-stu-id="2d098-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="2d098-146">Коды основания были добавлены в приостановку начисления.</span><span class="sxs-lookup"><span data-stu-id="2d098-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2d098-147">Правила переноса</span><span class="sxs-lookup"><span data-stu-id="2d098-147">Carry forward rules</span></span> 

<span data-ttu-id="2d098-148">Можно указать тип переноса отпуска для переноса сальдо, где переносятся корректировки переноса.</span><span class="sxs-lookup"><span data-stu-id="2d098-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2d098-149">Например, если сотрудник переносит на 10 дней вперед, можно выбрать другой тип отпуска для этих 10 дней.</span><span class="sxs-lookup"><span data-stu-id="2d098-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2d098-150">Дополнительные сведения см. в разделе [Настройка типов отпусков и отгулов](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2d098-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="2d098-151">Приостановка начисления отпуска для указанных типов отпусков</span><span class="sxs-lookup"><span data-stu-id="2d098-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="2d098-152">Вы можете создать правило приостановки начисления для сотрудников с запросами на отпуск, которые выбрали неоплачиваемый отпуск.</span><span class="sxs-lookup"><span data-stu-id="2d098-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="2d098-153">Тип "Неоплачиваемый отпуск" возможен, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="2d098-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="2d098-154">Можно приостановить любой отпуск на основе другого типа отпуска.</span><span class="sxs-lookup"><span data-stu-id="2d098-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="2d098-155">Объект DMF доступен для приостановки начисления</span><span class="sxs-lookup"><span data-stu-id="2d098-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="2d098-156">Объект DMF теперь доступен для приостановки начисления.</span><span class="sxs-lookup"><span data-stu-id="2d098-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2d098-157">Скоро</span><span class="sxs-lookup"><span data-stu-id="2d098-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="2d098-158">Сущности контрольного списка, включенные в Dataverse</span><span class="sxs-lookup"><span data-stu-id="2d098-158">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="2d098-159">Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2d098-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="2d098-160">Изменения платформы</span><span class="sxs-lookup"><span data-stu-id="2d098-160">Platform changes</span></span>

<span data-ttu-id="2d098-161">Обновление платформы 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="2d098-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="2d098-162">См. также</span><span class="sxs-lookup"><span data-stu-id="2d098-162">See also</span></span>

[<span data-ttu-id="2d098-163">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="2d098-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2d098-164">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="2d098-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2d098-165">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="2d098-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2d098-166">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="2d098-166">Manage features</span></span>](hr-admin-manage-features.md)
