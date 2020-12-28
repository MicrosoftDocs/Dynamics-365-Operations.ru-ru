---
title: Что нового и что изменилось в Dynamics 365 Talent (29 октября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529692"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="9d08f-103">Что нового и что изменилось в Dynamics 365 Talent (29 октября 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="9d08f-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9d08f-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="9d08f-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="9d08f-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="9d08f-105">Changes in Attract</span></span>

<span data-ttu-id="9d08f-106">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="9d08f-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="9d08f-107">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="9d08f-107">Changes in Onboard</span></span>

<span data-ttu-id="9d08f-108">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="9d08f-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="9d08f-109">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="9d08f-109">Changes in Core HR</span></span>

<span data-ttu-id="9d08f-110">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="9d08f-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="9d08f-111">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9d08f-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="9d08f-112">Удаление субъектов, не имеющих ролей, должно быть включено по умолчанию (371233)</span><span class="sxs-lookup"><span data-stu-id="9d08f-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="9d08f-113">При подготовке новой среды в Talent **Удалить субъекты, если роли не существуют** включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9d08f-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="9d08f-114">При удалении работника связанный с ним субъект не удаляется, если этот параметр не включен.</span><span class="sxs-lookup"><span data-stu-id="9d08f-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="9d08f-115">Это изменение ограничит повторяющиеся записи в глобальной адресной книге, когда требуется импортировать, изменить или повторно импортировать работников.</span><span class="sxs-lookup"><span data-stu-id="9d08f-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="9d08f-116">Запросы на отпуск "Черновик" или "Отменено" должны удаляться в Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="9d08f-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="9d08f-117">Теперь это изменение позволяет удалять запросы на отпуск со статусом **Черновик** или **Отменено** в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9d08f-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="9d08f-118">Дополнительные значения списка в настраиваемых полях не отображаются в Common Data Service после нажатия "Применить" в форме настраиваемых полей (379599)</span><span class="sxs-lookup"><span data-stu-id="9d08f-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="9d08f-119">При добавлении значений нового списка в существующее настраиваемое поле, которое уже было синхронизировано с Common Data Service, теперь они доступны в Common Data Serivce после применения изменений в форме **настраиваемых полей**.</span><span class="sxs-lookup"><span data-stu-id="9d08f-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="9d08f-120">Применение контрольных списков адаптации для юридических лиц при наличии нескольких сотрудников (371270)</span><span class="sxs-lookup"><span data-stu-id="9d08f-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="9d08f-121">В выпуске этой недели можно применять контрольные списки к сотрудникам с более чем одной занятостью в **форме сотрудника > контрольные списки**.</span><span class="sxs-lookup"><span data-stu-id="9d08f-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="9d08f-122">Удалена функция предварительного просмотра открытой регистрации льгот</span><span class="sxs-lookup"><span data-stu-id="9d08f-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="9d08f-123">В сочетании с нашим объявлением в записи блога [Стратегические инвестиции в Core HR способствуют повышению производительности](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Корпорация Майкрософт удаляет функцию открытой регистрации льгот из общедоступной предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="9d08f-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="9d08f-124">В будущем будут выпущены новые функции.</span><span class="sxs-lookup"><span data-stu-id="9d08f-124">New functionality will be released in the future.</span></span> <span data-ttu-id="9d08f-125">Использование функции регистрации открытых льгот не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d08f-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="9d08f-126">Скоро</span><span class="sxs-lookup"><span data-stu-id="9d08f-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="9d08f-127">Печать оценок производительности</span><span class="sxs-lookup"><span data-stu-id="9d08f-127">Print performance reviews</span></span>

<span data-ttu-id="9d08f-128">См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.</span><span class="sxs-lookup"><span data-stu-id="9d08f-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="9d08f-129">Рабочая область управления функциями</span><span class="sxs-lookup"><span data-stu-id="9d08f-129">Feature management workspace</span></span>

<span data-ttu-id="9d08f-130">Функции добавляются и обновляются в каждом выпуске.</span><span class="sxs-lookup"><span data-stu-id="9d08f-130">Features are added and updated in every release.</span></span> <span data-ttu-id="9d08f-131">Опыт управления функциями предоставляет рабочую область, в которой можно просматривать список функций, которые были поставлены в каждом выпуске.</span><span class="sxs-lookup"><span data-stu-id="9d08f-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="9d08f-132">По умолчанию новые функции отключены.</span><span class="sxs-lookup"><span data-stu-id="9d08f-132">By default, new features are turned off.</span></span> <span data-ttu-id="9d08f-133">Можно использовать рабочую область для их включения и просмотра документации по ним.</span><span class="sxs-lookup"><span data-stu-id="9d08f-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="9d08f-134">Для получения дополнительных сведений об изменениях, связанных с управлением функциями, см. раздел [Обзор управления функциями,](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="9d08f-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
