---
title: Что нового или что изменилось в Dynamics 365 Talent (2 апреля 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
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
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 86d81d60fcbc77375f3b8c525e8c084e3a3d8a99
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773701"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a><span data-ttu-id="627b4-103">Что нового или что изменилось в Dynamics 365 Talent (2 апреля 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="627b4-103">What's new or changed in Dynamics 365 Talent (April 2, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="627b4-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="627b4-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="627b4-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="627b4-105">Changes in Attract</span></span>

### <a name="approval-emails-in-attract"></a><span data-ttu-id="627b4-106">Сообщения электронной почты об утверждении в Attract</span><span class="sxs-lookup"><span data-stu-id="627b4-106">Approval emails in Attract</span></span>
<span data-ttu-id="627b4-107">Новые сообщения электронной почты улучшают прозрачность процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="627b4-107">New approval emails improve visibility into the approval process.</span></span> <span data-ttu-id="627b4-108">Сообщения электронной почты отправляются утверждающим при возникновении одного из следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="627b4-108">Emails are sent to approvers when one of the following scenarios occur:</span></span>

- <span data-ttu-id="627b4-109">Инициатор запроса отправляет должность на утверждение.</span><span class="sxs-lookup"><span data-stu-id="627b4-109">A requestor submits a job for approval.</span></span>
- <span data-ttu-id="627b4-110">Должность отклонена или утверждена.</span><span class="sxs-lookup"><span data-stu-id="627b4-110">A job is either rejected or approved.</span></span>
- <span data-ttu-id="627b4-111">Утверждающее лицо не обработало запрос утверждение в течение 24 часов.</span><span class="sxs-lookup"><span data-stu-id="627b4-111">An approver hasn't acted on an approval request within 24 hours.</span></span>

<span data-ttu-id="627b4-112">Можно настроить содержание сообщений электронной почты об утверждении с новыми шаблонами.</span><span class="sxs-lookup"><span data-stu-id="627b4-112">You can customize the content of approval emails with new templates.</span></span>

### <a name="application-and-profile-attachments"></a><span data-ttu-id="627b4-113">Вложения для заявлений и профилей</span><span class="sxs-lookup"><span data-stu-id="627b4-113">Application and profile attachments</span></span>
<span data-ttu-id="627b4-114">Улучшения на вкладке **Документы** в заявлениях и профилях кадровых пулов теперь отображают как название, так и тип документа.</span><span class="sxs-lookup"><span data-stu-id="627b4-114">Improvements to the **Documents** tab on applications and talent pool profiles now display both the document name and the type.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="627b4-115">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="627b4-115">Changes in Onboard</span></span>
<span data-ttu-id="627b4-116">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="627b4-116">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="coming-soon-attract-and-onboard"></a><span data-ttu-id="627b4-117">Скоро появится (Attract и Onboard)</span><span class="sxs-lookup"><span data-stu-id="627b4-117">Coming soon (Attract and Onboard)</span></span>

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a><span data-ttu-id="627b4-118">Интеграция Lifecycle Services (LCS) с функцией сообщения о проблеме</span><span class="sxs-lookup"><span data-stu-id="627b4-118">Lifecycle Services (LCS) integration with report a problem</span></span>
<span data-ttu-id="627b4-119">В Attract и Onboard проблемы, зарегистрированные конечными пользователями через функцию сообщения о проблеме, теперь автоматически создают проблемы технической поддержки в проекте LCS клиента.</span><span class="sxs-lookup"><span data-stu-id="627b4-119">In Attract and Onboard, problems logged by end users through the report a problem feature now automatically create support issues in the customer's LCS project.</span></span> <span data-ttu-id="627b4-120">Администраторы могут затем сортировать проблемы и передавать их в корпорацию Майкрософт при необходимости.</span><span class="sxs-lookup"><span data-stu-id="627b4-120">Admins can then triage the issues and submit them to Microsoft when needed.</span></span> <span data-ttu-id="627b4-121">Это согласуется с тем, как Core HR обрабатывает проблемы технической поддержки конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="627b4-121">This is consistent with how Core HR handles end user support issues.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="627b4-122">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="627b4-122">Changes in Core HR</span></span>
<span data-ttu-id="627b4-123">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2216.</span><span class="sxs-lookup"><span data-stu-id="627b4-123">Changes described in this section apply to build number 8.1.2216.</span></span>

### <a name="platform-update-25-for-finance-and-operations"></a><span data-ttu-id="627b4-124">Platform update 25 для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="627b4-124">Platform update 25 for Finance and Operations</span></span>
<span data-ttu-id="627b4-125">Дополнительные сведения об обновлении платформы Platform Update 25 для Finance and Operations см. в разделе [Предварительные версии функций в Dynamics 365 for Finance and Operations Platform Update 25 (апрель 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).</span><span class="sxs-lookup"><span data-stu-id="627b4-125">For more information about Platform update 25 for Finance and Operations, see [Preview features in Dynamics 365 for Finance and Operations platform update 25 (April 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="627b4-126">Расширенная безопасность компенсации (фиксированной и переменной)</span><span class="sxs-lookup"><span data-stu-id="627b4-126">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="627b4-127">Во многих организациях менеджеры по компенсации и льготам могут иметь доступ только к определенным записям компенсаций.</span><span class="sxs-lookup"><span data-stu-id="627b4-127">In many organizations, compensation and benefits managers might only have access to certain compensation records.</span></span> <span data-ttu-id="627b4-128">Эти записи могут включать записи для руководителей или региональных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="627b4-128">These might include records for executives or regional employees.</span></span> <span data-ttu-id="627b4-129">Это изменение позволяет отделу кадров управлять и обслуживать планы компенсации для различных групп сотрудников в организации.</span><span class="sxs-lookup"><span data-stu-id="627b4-129">This change allows HR to manage and maintain compensation plans for different employee groups in the organization.</span></span> <span data-ttu-id="627b4-130">Можно назначить роли безопасности для фиксированных и переменных планов.</span><span class="sxs-lookup"><span data-stu-id="627b4-130">You can assign security roles to fixed and variable plans.</span></span> <span data-ttu-id="627b4-131">Эти роли безопасности определяют доступ к планам и соответствующим данным сотрудников, таким как записи зарплаты или премий, чтобы только эти роли может обрабатывать компенсацию для групп сотрудников.</span><span class="sxs-lookup"><span data-stu-id="627b4-131">These security roles determine access to plans and related employee data, such as salary or bonus records, so that only those roles can process compensation for the employee groups.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="627b4-132">Обновление до Common Data Service</span><span class="sxs-lookup"><span data-stu-id="627b4-132">Upgrade to Common Data Service</span></span>
<span data-ttu-id="627b4-133">Крайние сроки для обновления до Common Data Service быстро приближаются.</span><span class="sxs-lookup"><span data-stu-id="627b4-133">Deadlines to upgrade to Common Data Service are rapidly approaching.</span></span> <span data-ttu-id="627b4-134">Войдите в центр администрирования Microsoft Power Apps для определения, необходимо ли обновить вашу базу данных.</span><span class="sxs-lookup"><span data-stu-id="627b4-134">Sign in to the Microsoft Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="627b4-135">Дополнительные сведения о крайних сроках и необходимых действиях по обновлению см. в разделе [Обновление до Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="627b4-135">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="in-preview"></a><span data-ttu-id="627b4-136">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="627b4-136">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="627b4-137">Разрешить указывать коды причины для типов отпусков</span><span class="sxs-lookup"><span data-stu-id="627b4-137">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="627b4-138">Организациям могут потребоваться дополнительные сведения о запросах выходных.</span><span class="sxs-lookup"><span data-stu-id="627b4-138">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="627b4-139">Теперь можно задать коды причин для типов отпуска и дать рабочим возможность выбрать код причины в их запросе выходных.</span><span class="sxs-lookup"><span data-stu-id="627b4-139">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="627b4-140">Требование кодов причин для определенных типов отпусков для запросов отпусков</span><span class="sxs-lookup"><span data-stu-id="627b4-140">Require reason codes for certain leave types on time-off requests</span></span>
<span data-ttu-id="627b4-141">Организации могут требовать коды причины для определенных типов отпусков, когда сотрудники отправляют запрос выходных.</span><span class="sxs-lookup"><span data-stu-id="627b4-141">Organizations might require reason codes for specific leave types when employees submit time-off.</span></span> <span data-ttu-id="627b4-142">Это может быть из-за политики компании или нормативных требований.</span><span class="sxs-lookup"><span data-stu-id="627b4-142">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="627b4-143">Теперь можно указать, какие типы отпусков требуют код причины, и можно потребовать, чтобы сотрудники указывали код причины для данного типа отпуска в их запросах отпусков.</span><span class="sxs-lookup"><span data-stu-id="627b4-143">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="627b4-144">Скоро</span><span class="sxs-lookup"><span data-stu-id="627b4-144">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="627b4-145">Улучшения интерфейса пользователя для проверки дубликатов сотрудников</span><span class="sxs-lookup"><span data-stu-id="627b4-145">Improvements to the user interface for duplicate employee check</span></span>
<span data-ttu-id="627b4-146">После этого изменения дубликаты определяются по мере ввода полей имени, и статус отображает число обнаруженных дубликатов.</span><span class="sxs-lookup"><span data-stu-id="627b4-146">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="627b4-147">Можно выбрать предоставленную ссылку, чтобы открыть новую страницу для оценки, следует ли использовать обнаруженное соответствие.</span><span class="sxs-lookup"><span data-stu-id="627b4-147">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="627b4-148">Во избежание прерывания ввода данных форма дубликатов не открывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="627b4-148">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="627b4-149">Поддержка по электронной почте для оповещений</span><span class="sxs-lookup"><span data-stu-id="627b4-149">Email support for alerts</span></span>
<span data-ttu-id="627b4-150">С обновлением платформы Platform Update 25 для Finance and Operations пользователи могут создавать правила оповещений, которые автоматически отправляют уведомления по электронной почте контактам при наступлении события.</span><span class="sxs-lookup"><span data-stu-id="627b4-150">With Platform update 25 for Finance and Operations, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span> 
