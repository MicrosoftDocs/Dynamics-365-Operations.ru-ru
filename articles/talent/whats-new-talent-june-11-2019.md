---
title: Что нового и что изменилось в Dynamics 365 for Talent (11 июня 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634488"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a><span data-ttu-id="5e58d-103">Что нового и что изменилось в Dynamics 365 for Talent (11 июня 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="5e58d-103">What's new or changed in Dynamics 365 for Talent (June 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e58d-104">В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="5e58d-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="5e58d-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="5e58d-105">Changes in Attract</span></span>

### <a name="search-engine-optimization-for-job-posts"></a><span data-ttu-id="5e58d-106">Оптимизация поисковой системы для объявлений о вакансиях</span><span class="sxs-lookup"><span data-stu-id="5e58d-106">Search engine optimization for job posts</span></span>

<span data-ttu-id="5e58d-107">После включения параметра **Оптимизация для поисковых систем** в центре администрирования Dynamics 365 for Talent: Attract приложение Attract информирует интерфейс прикладного программирования (API) индексирования Google, чтобы он выполнял обход содержимого веб-страницы при активации и публикации новой вакансии или обновлении существующей вакансии.</span><span class="sxs-lookup"><span data-stu-id="5e58d-107">After you turn on **Search Engine Optimization** in the Dynamics 365 for Talent: Attract Admin center, Attract informs the Google Indexing application programming interface (API) to crawl the webpage whenever you activate and post a new job or update an existing job.</span></span> <span data-ttu-id="5e58d-108">Таким образом, вакансия появится в результатах поиска Google и других поисковых систем.</span><span class="sxs-lookup"><span data-stu-id="5e58d-108">In this way, the job will appear in the search results for Google and other search engines.</span></span>

<span data-ttu-id="5e58d-109">Аналогичным образом, при отмене публикации вакансии Attract информирует интерфейс API индексирования, чтобы отмененная вакансия больше не появлялась в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="5e58d-109">Likewise, whenever you unpost a job, Attract informs the Indexing API, so that the unposted job will stop appearing in search results.</span></span>

> [!NOTE]
> <span data-ttu-id="5e58d-110">Поисковые модули не имеют определенных временных рамок для обхода веб-страниц или обновления результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="5e58d-110">Web crawlers don't have a defined timeframe for crawling webpages or updating search results.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="5e58d-111">Скоро появится в Attract</span><span class="sxs-lookup"><span data-stu-id="5e58d-111">Coming soon in Attract</span></span>

### <a name="job-approvals-appear-on-the-home-page"></a><span data-ttu-id="5e58d-112">Утверждения должностей отображаются на домашней странице</span><span class="sxs-lookup"><span data-stu-id="5e58d-112">Job approvals appear on the home page</span></span>

<span data-ttu-id="5e58d-113">Утверждения отображаются в разделе **Утверждения** на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="5e58d-113">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="5e58d-114">Утверждающие могут просмотреть свои утверждения в разделе **Назначено вам**, который отображает код должности, название должности, других утверждающих и дату назначения должности.</span><span class="sxs-lookup"><span data-stu-id="5e58d-114">Approvers can review their approvals under **Assigned to you**, which shows the job ID, the job title, other approvers, and the date when the job was assigned.</span></span> <span data-ttu-id="5e58d-115">Пользователи, которые отправляют должности на утверждение, могут просматривать свои должности в разделе **Запрошено вами**, в котором отображаются утверждающие, которые все еще должны утвердить отправленную должность.</span><span class="sxs-lookup"><span data-stu-id="5e58d-115">Users who submit a job for approval can review their jobs under **Requested by you**, which shows the approvers who must still approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="5e58d-116">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="5e58d-116">Changes in Onboard</span></span>

<span data-ttu-id="5e58d-117">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 for Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="5e58d-117">This release includes minor bug fixes for Dynamics 365 for Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="5e58d-118">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="5e58d-118">Changes in Core HR</span></span>

<span data-ttu-id="5e58d-119">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2337.</span><span class="sxs-lookup"><span data-stu-id="5e58d-119">The changes that are described in this section apply to build number 8.1.2337.</span></span>

### <a name="platform-update-27"></a><span data-ttu-id="5e58d-120">Обновление платформы update 27</span><span class="sxs-lookup"><span data-stu-id="5e58d-120">Platform update 27</span></span>

<span data-ttu-id="5e58d-121">Дополнительные сведения об обновлении платформы Platform update 27 см. в разделе [Предварительные версии функций в Dynamics 365 for Finance and Operations Platform Update 27 (июнь 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span><span class="sxs-lookup"><span data-stu-id="5e58d-121">For more details about Platform update 27, see [Preview features in Dynamics 365 for Finance and Operations platform update 27 (June 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span></span>

### <a name="feature-management-workspace-in-talent"></a><span data-ttu-id="5e58d-122">Рабочая область управления функциями в Talent</span><span class="sxs-lookup"><span data-stu-id="5e58d-122">Feature management workspace in Talent</span></span>

<span data-ttu-id="5e58d-123">Рабочая область **Управление функциями** в разделе **Администрирование системы** позволяет просматривать, включать, отключать и планировать функции, которые были поставлены в каждом выпуске.</span><span class="sxs-lookup"><span data-stu-id="5e58d-123">The **Feature management** workspace in **System administration** lets you view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="5e58d-124">По умолчанию новые функции отключены.</span><span class="sxs-lookup"><span data-stu-id="5e58d-124">By default, new features are turned off.</span></span> <span data-ttu-id="5e58d-125">Можно использовать рабочую область **Управление функциями** для их включения и просмотра документации по ним.</span><span class="sxs-lookup"><span data-stu-id="5e58d-125">You can use the **Feature management** workspace to turn them on and view the documentation for them.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="5e58d-126">Поддержка сущностей Common Data Service для настраиваемых полей</span><span class="sxs-lookup"><span data-stu-id="5e58d-126">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="5e58d-127">Сущность "Выпускающее агентство" теперь поддерживает настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="5e58d-127">The Issuing agency entity now supports custom fields.</span></span>

### <a name="new-common-data-service-entities"></a><span data-ttu-id="5e58d-128">Новые сущности Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5e58d-128">New Common Data Service entities</span></span>

<span data-ttu-id="5e58d-129">Добавлена сущность "Группа задач".</span><span class="sxs-lookup"><span data-stu-id="5e58d-129">The Task group entity has been added.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5e58d-130">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="5e58d-130">In preview</span></span>

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a><span data-ttu-id="5e58d-131">Функции предварительной версии будут включены только в средах "Песочница"</span><span class="sxs-lookup"><span data-stu-id="5e58d-131">Preview features will be enabled only in sandbox environments</span></span>

<span data-ttu-id="5e58d-132">Дополнительные сведения о порядке публикации изменений см. в разделе [Подготовка Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="5e58d-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="5e58d-133">При подготовке нового экземпляра Talent можно указать, имеет ли данный экземпляр тип "Производство" или "Песочница".</span><span class="sxs-lookup"><span data-stu-id="5e58d-133">When you provision a new instance of Talent, you can indicate whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="5e58d-134">Экземпляр типа "Песочница" позволяет заблаговременно тестировать новые возможности.</span><span class="sxs-lookup"><span data-stu-id="5e58d-134">The Sandbox instance type allows for early testing of new features.</span></span> <span data-ttu-id="5e58d-135">Все существующие экземпляры Talent будут обновлены до типа экземпляра **Производство**.</span><span class="sxs-lookup"><span data-stu-id="5e58d-135">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="5e58d-136">Если необходимо обновить один из существующих экземпляров до типа экземпляра **Песочница**, обратитесь в [службу поддержки](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support), чтобы инициировать запрос на изменение.</span><span class="sxs-lookup"><span data-stu-id="5e58d-136">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="5e58d-137">Ограничение типов отпусков в запросах времени отсутствия</span><span class="sxs-lookup"><span data-stu-id="5e58d-137">Restrict the leave types in time-off requests</span></span>

<span data-ttu-id="5e58d-138">Организации могут предложить сотрудникам различные типы отпусков.</span><span class="sxs-lookup"><span data-stu-id="5e58d-138">Organizations can offer many types of leave to employees.</span></span> <span data-ttu-id="5e58d-139">Однако может быть недопустимо, чтобы сотрудники могли подавать запросы на время отсутствие для некоторых типов отпусков.</span><span class="sxs-lookup"><span data-stu-id="5e58d-139">However, it might not be appropriate for employees to submit time-off requests for some leave types.</span></span> <span data-ttu-id="5e58d-140">Эти типы отпусков могут управляться вместо этого отделом кадров.</span><span class="sxs-lookup"><span data-stu-id="5e58d-140">Those leave types might be managed by Human resources (HR) instead.</span></span> <span data-ttu-id="5e58d-141">В этом выпуске можно настроить, для каких типов отпусков сотрудники могут отправлять запросы времени отсутствия.</span><span class="sxs-lookup"><span data-stu-id="5e58d-141">In this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

## <a name="coming-soon-in-core-hr"></a><span data-ttu-id="5e58d-142">Скоро появится в Core HR</span><span class="sxs-lookup"><span data-stu-id="5e58d-142">Coming soon in Core HR</span></span>

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a><span data-ttu-id="5e58d-143">Просмотр расширенной информации о производительности отчетов на портале самообслуживания менеджера</span><span class="sxs-lookup"><span data-stu-id="5e58d-143">View extended information about report performance in manager self-service</span></span>

<span data-ttu-id="5e58d-144">Новый параметр позволит менеджерам просматривать производительность как своих прямых подчиненных, так и их расширенных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="5e58d-144">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="5e58d-145">В настоящее время линейные менеджеры могут назначать и обновлять цели производительности и выпускать новые обзоры.</span><span class="sxs-lookup"><span data-stu-id="5e58d-145">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="5e58d-146">Кроме того, прямые менеджеры и их сотрудники могут вести поддержку и обновлять журналы производительности, чтобы гарантировать плавность процесса проверки производительности.</span><span class="sxs-lookup"><span data-stu-id="5e58d-146">In addition, direct managers and their employees can maintain and update performance journals to help guarantee that the performance review process goes smoothly.</span></span> <span data-ttu-id="5e58d-147">Когда это изменение будет реализовано, менеджеры смогут просматривать и вести сведения о производительности для расширенных подчиненных в дополнение к их прямым подчиненным.</span><span class="sxs-lookup"><span data-stu-id="5e58d-147">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="5e58d-148">Печать оценок производительности</span><span class="sxs-lookup"><span data-stu-id="5e58d-148">Print performance reviews</span></span>

<span data-ttu-id="5e58d-149">Сотрудники, менеджеры и отдел кадров смогут распечатать обзор производительности сотрудников.</span><span class="sxs-lookup"><span data-stu-id="5e58d-149">Employees, managers, and HR will be able to print an employee's performance review.</span></span>
