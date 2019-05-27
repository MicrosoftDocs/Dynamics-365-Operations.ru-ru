---
title: Что нового и что изменилось в Dynamics 365 for Talent (6 мая 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4830c5d626e5e10972c81c3445eb54e4b6b00e6c
ms.sourcegitcommit: 0400bfd66e98af50e64444a1c102575099a9312f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/09/2019
ms.locfileid: "1539413"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-6-2019"></a><span data-ttu-id="b0b03-103">Что нового и что изменилось в Dynamics 365 for Talent (6 мая 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="b0b03-103">What's new or changed in Dynamics 365 for Talent (May 6, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0b03-104">В этой теме описываются новые и измененные компоненты Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="b0b03-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="b0b03-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="b0b03-105">Changes in Attract</span></span>

### <a name="select-optional-documents-upon-offer-creation"></a><span data-ttu-id="b0b03-106">Выбор дополнительных документов при создании предложения</span><span class="sxs-lookup"><span data-stu-id="b0b03-106">Select optional documents upon offer creation</span></span>

<span data-ttu-id="b0b03-107">После выбора шаблона пакета предложений Attract теперь предлагает выбрать применимые дополнительные документы из шаблона пакета.</span><span class="sxs-lookup"><span data-stu-id="b0b03-107">When you select an offer package template, Attract now prompts you to select the applicable, optional documents from that package template.</span></span> <span data-ttu-id="b0b03-108">При подготовке предложения можно добавлять дополнительные документы.</span><span class="sxs-lookup"><span data-stu-id="b0b03-108">You can add other optional documents while preparing the offer.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="b0b03-109">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="b0b03-109">Changes in Onboard</span></span>

<span data-ttu-id="b0b03-110">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="b0b03-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="b0b03-111">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="b0b03-111">Changes in Core HR</span></span>

<span data-ttu-id="b0b03-112">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2282.</span><span class="sxs-lookup"><span data-stu-id="b0b03-112">Changes described in this section apply to build number 8.1.2282.</span></span> <span data-ttu-id="b0b03-113">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b0b03-113">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="platform-update-26"></a><span data-ttu-id="b0b03-114">Обновление платформы update 26</span><span class="sxs-lookup"><span data-stu-id="b0b03-114">Platform update 26</span></span>

<span data-ttu-id="b0b03-115">Дополнительные сведения об обновлении платформы Platform update 26 см. в разделе [Предварительные версии функций в Dynamics 365 for Finance and Operations Platform Update 26 (май 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span><span class="sxs-lookup"><span data-stu-id="b0b03-115">For additional details about Platform update 26, see [Preview features in Dynamics 365 for Finance and Operations platform update 26 (May 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span></span> 

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="b0b03-116">Поддержка сущностей Common Data Service для настраиваемых полей</span><span class="sxs-lookup"><span data-stu-id="b0b03-116">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="b0b03-117">В выпуске этой недели следующие сущности теперь поддерживают настраиваемые поля: частота расчета льгот, ставка расчета льгот, тип льготы, рабочий календарь, выходной рабочего календаря, цикл оплаты и типы идентификации работников.</span><span class="sxs-lookup"><span data-stu-id="b0b03-117">In this week's release, the following entities now support custom fields: Benefit calc frequency, Benefit calc rate, Benefit type, Work calendar, Work calendar holiday, Pay cycle, and Worker identification types.</span></span>

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a><span data-ttu-id="b0b03-118">В массовой регистрации отпусков при изменении базы уровня "Дата трудового стажа" не обновляется исходная ставка начисления (318526)</span><span class="sxs-lookup"><span data-stu-id="b0b03-118">Leave mass enrollment, changing the tier basis to "Seniority date" doesn't refresh the initial accrual rate (318526)</span></span>

<span data-ttu-id="b0b03-119">При массовой регистрации сотрудников и изменении базы уровня первоначальное начисление теперь отражает выбранную базу уровня.</span><span class="sxs-lookup"><span data-stu-id="b0b03-119">When you mass enroll employees and change the tier basis, the initial accrual now reflects the tier basis that you selected.</span></span>

### <a name="workflow-showing-duplicate-place-holders-313636"></a><span data-ttu-id="b0b03-120">Рабочий процесс отображает повторяющиеся заполнители (313636)</span><span class="sxs-lookup"><span data-stu-id="b0b03-120">Workflow showing duplicate place holders (313636)</span></span>

<span data-ttu-id="b0b03-121">Изменения в этом выпуске устраняют дублирование заполнителей при отправке уведомлений рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="b0b03-121">Changes in this release eliminate duplication of placeholders when workflow notifications are sent.</span></span>

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a><span data-ttu-id="b0b03-122">Поля аналитики не обновляются при использовании "Открыть в Excel" (176261)</span><span class="sxs-lookup"><span data-stu-id="b0b03-122">Dimension fields aren't updated when using "Open in Excel" (176261)</span></span>

<span data-ttu-id="b0b03-123">В этом выпуске теперь можно обновить финансовую аналитику, используя команду **Открыть в Excel** на странице **Работник**.</span><span class="sxs-lookup"><span data-stu-id="b0b03-123">With this release, you can now update financial dimension using **Open in Excel** from the **Worker** page.</span></span> 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a><span data-ttu-id="b0b03-124">Адрес работника, созданный в Common Data Service, не синхронизируется с Talent (317555)</span><span class="sxs-lookup"><span data-stu-id="b0b03-124">Worker address created in Common Data Service isn't synced to Talent (317555)</span></span>

<span data-ttu-id="b0b03-125">С этим изменением адреса, созданные в Common Data Service, обновляются в Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="b0b03-125">With this change, addresses created in Common Data Service are updated in Talent Core HR.</span></span>


## <a name="in-preview"></a><span data-ttu-id="b0b03-126">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="b0b03-126">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="b0b03-127">Новая страница для проверки данных иерархии должностей</span><span class="sxs-lookup"><span data-stu-id="b0b03-127">New page to validate position hierarchy data</span></span>

<span data-ttu-id="b0b03-128">Отдел кадров и администраторы теперь могут проверять иерархию управления на наличие любых циклических ссылок, которые могли быть случайно импортированы.</span><span class="sxs-lookup"><span data-stu-id="b0b03-128">Human resources (HR) and administrators can now validate the managerial hierarchy for any circular references that might have inadvertently been imported.</span></span> <span data-ttu-id="b0b03-129">Эту новую страницу можно открыть по пути **Управление организацией > Ссылки > Должности > Проверка иерархии должностей**.</span><span class="sxs-lookup"><span data-stu-id="b0b03-129">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="b0b03-130">Указание кодов причин для типов отпусков</span><span class="sxs-lookup"><span data-stu-id="b0b03-130">Specify reason codes on leave types</span></span>

<span data-ttu-id="b0b03-131">Организациям могут потребоваться дополнительные сведения о запросах выходных.</span><span class="sxs-lookup"><span data-stu-id="b0b03-131">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="b0b03-132">Теперь можно задать коды причин для типов отпуска и позволить рабочим выбирать код причины в их запросе выходных.</span><span class="sxs-lookup"><span data-stu-id="b0b03-132">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="b0b03-133">Требование кодов причин для определенных типов отпусков для запросов отпусков</span><span class="sxs-lookup"><span data-stu-id="b0b03-133">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="b0b03-134">Организации могут требовать коды причины для определенных типов отпусков, когда сотрудники отправляют запросы выходных.</span><span class="sxs-lookup"><span data-stu-id="b0b03-134">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="b0b03-135">Это требование может быть вызвано политикой компании или нормативными требованиями.</span><span class="sxs-lookup"><span data-stu-id="b0b03-135">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="b0b03-136">Теперь можно указать, какие типы отпусков требуют код причины, и можно потребовать, чтобы сотрудники указывали код причины для данного типа отпуска в их запросах отпусков.</span><span class="sxs-lookup"><span data-stu-id="b0b03-136">You can now specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="b0b03-137">Предоставление отпуска и списка проводок отсутствия для отдела кадров</span><span class="sxs-lookup"><span data-stu-id="b0b03-137">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="b0b03-138">Возможность отслеживания времени отсутствия сотрудника и понимание того, как нерабочее время вычисляется, не только помогает отделу кадров отвечать на вопросы сотрудников, но и также помогает обеспечить точное назначение выходных для сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b0b03-138">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="b0b03-139">Отдел кадров теперь имеет новое представление проводок (гранты, начисления, корректировки и запросы), чтобы персонал отдела кадров мог просматривать причины в основе сальдо.</span><span class="sxs-lookup"><span data-stu-id="b0b03-139">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b0b03-140">Скоро</span><span class="sxs-lookup"><span data-stu-id="b0b03-140">Coming soon</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="b0b03-141">Указание типа экземпляра при подготовке Talent</span><span class="sxs-lookup"><span data-stu-id="b0b03-141">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="b0b03-142">При подготовке нового экземпляра Talent можно будет указать тип экземпляра **Производство** или **Песочница**, позволяя производить раннее тестирование новых функций.</span><span class="sxs-lookup"><span data-stu-id="b0b03-142">When provisioning a new instance of Talent, you will be able to indicate whether the instance type is **Production** or **Sandbox**, allowing for early testing of new features.</span></span> <span data-ttu-id="b0b03-143">Все существующие экземпляры Talent будут обновлены до типа экземпляра "Производство".</span><span class="sxs-lookup"><span data-stu-id="b0b03-143">All existing Talent instances will be updated to the Production instance type.</span></span> <span data-ttu-id="b0b03-144">Если необходимо обновить один из существующих экземпляров до типа экземпляра "Песочница", обратитесь в службу поддержки, чтобы инициировать запрос на изменение.</span><span class="sxs-lookup"><span data-stu-id="b0b03-144">If you want one of your existing instances to be updated to the Sandbox instance type, please contact Support to initiate the change request.</span></span>
