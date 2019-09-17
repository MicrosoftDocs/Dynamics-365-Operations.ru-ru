---
title: Что нового и что изменилось в Dynamics 365 for Talent (5 марта 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fe24846ab98a75d474df045a62a72bfc41c64866
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741898"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="1f5cf-103">Что нового и что изменилось в Dynamics 365 for Talent (5 марта 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="1f5cf-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f5cf-104">В этой теме описываются новые и измененные компоненты в Talent</span><span class="sxs-lookup"><span data-stu-id="1f5cf-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="1f5cf-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="1f5cf-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="1f5cf-106">Расширение наборов параметров в Attract</span><span class="sxs-lookup"><span data-stu-id="1f5cf-106">Extending option sets in Attract</span></span>

<span data-ttu-id="1f5cf-107">В Attract имеется несколько полей, которые являются наборам параметров в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="1f5cf-108">Были добавлены новые возможности для расширения наборов параметров, начиная с поля **Причина отклонения**, поля **Тип трудоустройства** и поле **Типа трудового стажа**.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f5cf-109">Для функциональности публикации объявлений о вакансии в LinkedIn необходимо использовать поля **Тип трудоустройства** и **Тип трудового стажа** на странице **Сведения о вакансии**.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="1f5cf-110">Значения по умолчанию в этих полях поддерживаются LinkedIn и отображаются при публикации вакансии.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="1f5cf-111">Если при публикации вакансий в LinkedIn изменить существующие значения набора параметров для этих полей, вакансия по-прежнему будут опубликована, но LinkedIn не будет отображать настраиваемые значения **Тип трудоустройства** и **Тип трудового стажа**.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="1f5cf-112">Изменения в Onboarding</span><span class="sxs-lookup"><span data-stu-id="1f5cf-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="1f5cf-113">Закрытая предварительная версия для рабочих групп Onboard</span><span class="sxs-lookup"><span data-stu-id="1f5cf-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="1f5cf-114">Теперь можно легко совместно использовать шаблоны и совместно работать над ними во всей организации.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="1f5cf-115">Дополнительные сведения см. в разделе [Совместного использования передового опыта в вашей организации с помощью рабочих групп Onboard](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="1f5cf-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="1f5cf-116">Закрытая предварительная версия местозаполнителей уполномоченного</span><span class="sxs-lookup"><span data-stu-id="1f5cf-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="1f5cf-117">Шаблоны можно расширить путем назначения действий ролям, а не отдельным лицам.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="1f5cf-118">Затем роли назначаются отдельным пользователям во время создания руководства.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="1f5cf-119">Дополнительные сведения см. в разделе [Упрощение администрирования руководств путем назначения действий ролям](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="1f5cf-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="1f5cf-120">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="1f5cf-120">Changes in Core HR</span></span>
<span data-ttu-id="1f5cf-121">**Сборка 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="1f5cf-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="1f5cf-122">Настройка workflow-процесса для автоматического утверждения или следование workflow-процессу, когда менеджер отдела кадров или менеджер строки отправляет или обновляет запросы отгулов</span><span class="sxs-lookup"><span data-stu-id="1f5cf-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="1f5cf-123">Новые условия workflow-процесса были добавлены, чтобы разрешить автоматическое утверждение запросов на отпуск, если они отправлены менеджером сотрудника или отделом кадров.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="1f5cf-124">Один из способов достижения такого автоматического утверждения в workflow-процессе заключается во включении автоматического действия по утверждению workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="1f5cf-125">Условия, которые были добавлены, включают:</span><span class="sxs-lookup"><span data-stu-id="1f5cf-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="1f5cf-126">Кем отправлено — используется для оценки кода пользователя системы для пользователя, который отправил запрос в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="1f5cf-127">Отправлено от имени — используется для оценки, если запрос отпуска отправлен от имени работника, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="1f5cf-128">Отправлено отделом кадров — используется для оценки, если пользователь системы, который отправил запрос в workflow-процесс, имеет роль сотрудника отдела кадров.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="1f5cf-129">Отправлено руководителем — используется для оценки, если пользователь, который отправил запрос отпуска в workflow-процесс, является руководителем строки иерархии для работника, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="1f5cf-130">Включение фиксированной компенсации сотрудникам для будущих назначений на должность</span><span class="sxs-lookup"><span data-stu-id="1f5cf-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="1f5cf-131">Часто сотрудники принимаются в организацию с датой выхода на работу в будущем.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="1f5cf-132">Это изменение позволяет определять фиксированную компенсацию для сотрудников, имеющих будущие назначения на должность.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="1f5cf-133">Поля зарплаты должности пусты при редактировании должности</span><span class="sxs-lookup"><span data-stu-id="1f5cf-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="1f5cf-134">В результате этого изменения при запросе изменений в существующих должностях поля зарплаты теперь по умолчанию заполняются текущими значениями.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="1f5cf-135">Исправление прочих ошибок</span><span class="sxs-lookup"><span data-stu-id="1f5cf-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="1f5cf-136">Другие исправления незначительных ошибок включены в этот выпуск.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="1f5cf-137">Обновление до Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1f5cf-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="1f5cf-138">Крайние сроки для обновления до Common Data Service быстро приближаются.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="1f5cf-139">Войдите в центр администрирования PowerApps для определения, необходимо ли обновить вашу базу данных.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="1f5cf-140">Дополнительные сведения о крайних сроках и необходимых действиях по обновлению см. в разделе [Обновление до Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="1f5cf-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1f5cf-141">Скоро</span><span class="sxs-lookup"><span data-stu-id="1f5cf-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="1f5cf-142">Расширенная безопасность компенсации (фиксированной и переменной)</span><span class="sxs-lookup"><span data-stu-id="1f5cf-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="1f5cf-143">Во многих организациях менеджеры компенсаций и льгот имеют доступ только к определенным записям компенсаций, например записям для руководителей или региональных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="1f5cf-144">С эим изменением вы можете управлять и обслуживать планы компенсации для различных совокупностей сотрудников в организации.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="1f5cf-145">Фиксированные и переменные планам могут назначаться ролям безопасности, которые будут определять доступ к этим планам и данным о сотрудниках, относящихся к планам, таким как записи сведений о зарплате и премиях.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="1f5cf-146">Только роли, которым предоставлен доступ, смогут обрабатывать компенсации для таких сотрудников.</span><span class="sxs-lookup"><span data-stu-id="1f5cf-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="1f5cf-147">Обновление платформы update 24</span><span class="sxs-lookup"><span data-stu-id="1f5cf-147">Platform update 24</span></span>
<span data-ttu-id="1f5cf-148">Дополнительные сведения об обновлении платформы 24 см. в разделе [Что нового и что изменилось в Finance and Operations с обновлением платформы 24 (март 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="1f5cf-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
