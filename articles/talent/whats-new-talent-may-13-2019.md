---
title: Что нового и что изменилось в Dynamics 365 for Talent (13 мая 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ffeeb3e2f5279a84c4c060b04fe46836b778f6c5
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856456"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a><span data-ttu-id="34139-103">Что нового и что изменилось в Dynamics 365 for Talent (13 мая 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="34139-103">What's new or changed in Dynamics 365 for Talent (May 13, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34139-104">В этой теме описываются новые и измененные компоненты Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="34139-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="34139-105">Скоро появится в Attract</span><span class="sxs-lookup"><span data-stu-id="34139-105">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="34139-106">Утверждения должностей на домашней странице</span><span class="sxs-lookup"><span data-stu-id="34139-106">Job approvals on home page</span></span>

<span data-ttu-id="34139-107">Утверждения отображаются в разделе **Утверждения** на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="34139-107">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="34139-108">Утверждающие могут просмотреть свои утверждения в разделе **Назначено вам**, который отображает код должности, название, других утверждающих и дату назначения.</span><span class="sxs-lookup"><span data-stu-id="34139-108">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="34139-109">Пользователи, которые отправляют должности на утверждение, могут просматривать свои должности в разделе **Запрошено вами**, в котором отображаются утверждающие, которые все еще должны утвердить отправленную должность.</span><span class="sxs-lookup"><span data-stu-id="34139-109">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="34139-110">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="34139-110">Changes in Onboard</span></span>

<span data-ttu-id="34139-111">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="34139-111">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="34139-112">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="34139-112">Changes in Core HR</span></span>

<span data-ttu-id="34139-113">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2297.</span><span class="sxs-lookup"><span data-stu-id="34139-113">Changes described in this section apply to build number 8.1.2297.</span></span> <span data-ttu-id="34139-114">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="34139-114">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="34139-115">Указание типа экземпляра при подготовке Talent</span><span class="sxs-lookup"><span data-stu-id="34139-115">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="34139-116">При подготовке нового экземпляра Talent можно указать тип экземпляра **Производство** или **Песочница**, который позволяет производить раннее тестирование новых функций.</span><span class="sxs-lookup"><span data-stu-id="34139-116">When provisioning a new instance of Talent, you can indicate whether the instance type is **Production** or **Sandbox**, which allows for early testing of new features.</span></span> <span data-ttu-id="34139-117">Все существующие экземпляры Talent будут обновлены до типа экземпляра **Производство**.</span><span class="sxs-lookup"><span data-stu-id="34139-117">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="34139-118">Если необходимо обновить один из существующих экземпляров до типа экземпляра **Песочница**, обратитесь в [службу поддержки](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), чтобы инициировать запрос на изменение.</span><span class="sxs-lookup"><span data-stu-id="34139-118">If you want one of your existing instances to be updated to the **Sandbox** instance type, please contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="34139-119">Поддержка сущностей Common Data Service для настраиваемых полей</span><span class="sxs-lookup"><span data-stu-id="34139-119">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="34139-120">В выпуске этой недели следующие сущности Common Data Service теперь поддерживают настраиваемые поля: занятость, частота расчета льгот, ставка расчета льгот, выходной рабочего календаря и тип идентификации.</span><span class="sxs-lookup"><span data-stu-id="34139-120">In this week's release, the following Common Data Service entities now support custom fields: Employment, Benefit calc frequency, Benefit calc rate, Work calendar holiday, and Identification type.</span></span>

### <a name="common-data-service-integration-page"></a><span data-ttu-id="34139-121">Страница интеграции Common Data Service</span><span class="sxs-lookup"><span data-stu-id="34139-121">Common Data Service integration page</span></span>

<span data-ttu-id="34139-122">В этом выпуске представлен новый параметр в разделе **Администрирование системы > Ссылки > Интеграция > Конфигурация Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="34139-122">This release provides a new option in **System Administration > Links > Integrations > Common Data Service configuration**.</span></span> <span data-ttu-id="34139-123">Параметр **Конфигурация Common Data Service** обеспечивает администратору или администратору управления данными некоторую гибкость и аналитическую информацию с использованием Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="34139-123">The **Common Data Service configuration** option allows an administrator or data management administrator some flexibility and insights with the Common Data Service.</span></span> <span data-ttu-id="34139-124">С помощью этого параметра можно включить или отключить интеграцию Common Data Service с экземпляром Talent, а также просмотреть сведения о синхронизации между экземпляром Talent и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="34139-124">With this option, you can enable or disable Common Data Service integration with a Talent instance and view the sync details between the Talent instance and the Common Data Service.</span></span>

### <a name="import-performance-data-with-final-employee-rating-316710"></a><span data-ttu-id="34139-125">Импорт данных производительности с окончательной оценкой сотрудника (316710)</span><span class="sxs-lookup"><span data-stu-id="34139-125">Import performance data with final employee rating (316710)</span></span>

<span data-ttu-id="34139-126">В этом выпуске можно импортировать исторические данные рейтинга сотрудника.</span><span class="sxs-lookup"><span data-stu-id="34139-126">In this release, you can import historical employee rating data.</span></span> <span data-ttu-id="34139-127">Поле **FinalEmployeeRatingId** теперь имеет разрешение на запись.</span><span class="sxs-lookup"><span data-stu-id="34139-127">The **FinalEmployeeRatingId** field now has write permission.</span></span>

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a><span data-ttu-id="34139-128">Невозможно создать адрес работника в Common Data Service и синхронизировать его с Talent (317555)</span><span class="sxs-lookup"><span data-stu-id="34139-128">Can't create Worker address in Common Data Service and sync it with Talent (317555)</span></span>

<span data-ttu-id="34139-129">Это изменение разрешает создание данных адресов в Common Data Service для синхронизации с Talent.</span><span class="sxs-lookup"><span data-stu-id="34139-129">This change allows address data created in Common Data Service to sync with Talent.</span></span>

## <a name="in-preview"></a><span data-ttu-id="34139-130">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="34139-130">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="34139-131">Новая страница для проверки данных иерархии должностей</span><span class="sxs-lookup"><span data-stu-id="34139-131">New page to validate position hierarchy data</span></span>

<span data-ttu-id="34139-132">Отдел кадров и администраторы могут проверять иерархию управления на наличие любых циклических ссылок, которые могли быть случайно импортированы.</span><span class="sxs-lookup"><span data-stu-id="34139-132">Human resources (HR) and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="34139-133">Эту новую страницу можно открыть по пути **Управление организацией > Ссылки > Должности > Проверка иерархии должностей**.</span><span class="sxs-lookup"><span data-stu-id="34139-133">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="34139-134">Указание кодов причин для типов отпусков</span><span class="sxs-lookup"><span data-stu-id="34139-134">Specify reason codes on leave types</span></span>

<span data-ttu-id="34139-135">Организациям могут потребоваться дополнительные сведения о запросах выходных.</span><span class="sxs-lookup"><span data-stu-id="34139-135">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="34139-136">Теперь можно задать коды причин для типов отпуска и позволить рабочим выбирать код причины в их запросе выходных.</span><span class="sxs-lookup"><span data-stu-id="34139-136">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="34139-137">Требование кодов причин для определенных типов отпусков для запросов отпусков</span><span class="sxs-lookup"><span data-stu-id="34139-137">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="34139-138">Организации могут требовать коды причины для определенных типов отпусков, когда сотрудники отправляют запросы выходных.</span><span class="sxs-lookup"><span data-stu-id="34139-138">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="34139-139">Это требование может быть вызвано политикой компании или нормативными требованиями.</span><span class="sxs-lookup"><span data-stu-id="34139-139">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="34139-140">Можно указать, какие типы отпусков требуют код причины, и можно потребовать, чтобы сотрудники указывали код причины для данного типа отпуска в их запросах отпусков.</span><span class="sxs-lookup"><span data-stu-id="34139-140">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="34139-141">Предоставление отпуска и списка проводок отсутствия для отдела кадров</span><span class="sxs-lookup"><span data-stu-id="34139-141">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="34139-142">Возможность отслеживания времени отсутствия сотрудника и понимание того, как нерабочее время вычисляется, не только помогает отделу кадров отвечать на вопросы сотрудников, но и также помогает обеспечить точное назначение выходных для сотрудников.</span><span class="sxs-lookup"><span data-stu-id="34139-142">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="34139-143">Отдел кадров теперь имеет новое представление проводок (гранты, начисления, корректировки и запросы), чтобы персонал отдела кадров мог просматривать причины в основе сальдо выходных.</span><span class="sxs-lookup"><span data-stu-id="34139-143">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
