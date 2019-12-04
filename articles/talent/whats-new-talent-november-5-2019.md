---
title: Что нового и что изменилось в Dynamics 365 Talent (5 ноября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778390"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="38696-103">Что нового и что изменилось в Dynamics 365 Talent (5 ноября 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="38696-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38696-104">В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="38696-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="38696-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="38696-105">Changes in Attract</span></span>

<span data-ttu-id="38696-106">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="38696-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="38696-107">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="38696-107">Changes in Onboard</span></span>

<span data-ttu-id="38696-108">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="38696-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="38696-109">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="38696-109">Changes in Core HR</span></span>

<span data-ttu-id="38696-110">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2598.</span><span class="sxs-lookup"><span data-stu-id="38696-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="38696-111">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="38696-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="38696-112">Копирование экземпляра Core HR</span><span class="sxs-lookup"><span data-stu-id="38696-112">Copy a Core HR instance</span></span>

<span data-ttu-id="38696-113">В выпуске этой недели можно использовать Microsoft Dynamics Lifecycle Services (LCS) для копирования базы данных Microsoft Dynamics 365 Talent: Core HR в среду в песочнице.</span><span class="sxs-lookup"><span data-stu-id="38696-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="38696-114">При наличии другой среды-песочницы можно также скопировать базу данных из этой среды в целевую среду-песочницу.</span><span class="sxs-lookup"><span data-stu-id="38696-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="38696-115">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="38696-115">For more information, see:</span></span>

- <span data-ttu-id="38696-116">[Расширенное управление средой](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) в Dynamics 365: 2019, план волны выпуска 2</span><span class="sxs-lookup"><span data-stu-id="38696-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="38696-117">[Копирование экземпляра Core HR](hr-copy-instance.md) в документацию Talent</span><span class="sxs-lookup"><span data-stu-id="38696-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="38696-118">Пакетные задания интеграции Common Data Service не создаются, когда включена интеграция Common Data Service (388030)</span><span class="sxs-lookup"><span data-stu-id="38696-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="38696-119">Это изменение создает пакетные задания для интеграции Common Data Service, когда она активирована.</span><span class="sxs-lookup"><span data-stu-id="38696-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="38696-120">HcmPersonImageEntity не изменяет размер изображения сотрудника при отправке (369469)</span><span class="sxs-lookup"><span data-stu-id="38696-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="38696-121">В выпуске этой недели изменены способы изменения размеров изображений для повышения производительности при импорте через управление данными.</span><span class="sxs-lookup"><span data-stu-id="38696-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="38696-122">Дата, доступная для данной должности, может предшествовать дате активации (340103)</span><span class="sxs-lookup"><span data-stu-id="38696-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="38696-123">В этом изменении появляется предупреждение, если выбрана **Дата, доступная для данной должности**, которая раньше **Дата активации** для должности.</span><span class="sxs-lookup"><span data-stu-id="38696-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="38696-124">Невозможно создать запрос на изменение компенсации в дистанционном обслуживании сотрудников для пошаговых планов (376872)</span><span class="sxs-lookup"><span data-stu-id="38696-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="38696-125">В этом выпуске исправлена проблема с запросом изменений компенсации через дистанционное обслуживание сотрудников для пошаговых планов.</span><span class="sxs-lookup"><span data-stu-id="38696-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="38696-126">Код причины не синхронизируется с Common Data Service, если описание длиннее 30 символов, Core HR допускают 60 (352682)</span><span class="sxs-lookup"><span data-stu-id="38696-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="38696-127">При этом изменении коды причин размером более 30 символов будут обновлены в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="38696-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="38696-128">Изменения, сделанные в Common Data Service, также будут отражены в Talent.</span><span class="sxs-lookup"><span data-stu-id="38696-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="38696-129">Интеграция адреса из Talent в Finance and Operations (351961)</span><span class="sxs-lookup"><span data-stu-id="38696-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="38696-130">В этом выпуске исправлена проблема, когда адреса, обновляемые в Talent, не обновлялись в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="38696-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="38696-131">Изменения в блоках адресов будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="38696-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="38696-132">Скоро</span><span class="sxs-lookup"><span data-stu-id="38696-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="38696-133">Печать оценок производительности</span><span class="sxs-lookup"><span data-stu-id="38696-133">Print performance reviews</span></span>

<span data-ttu-id="38696-134">См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.</span><span class="sxs-lookup"><span data-stu-id="38696-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="38696-135">Рабочая область управления функциями</span><span class="sxs-lookup"><span data-stu-id="38696-135">Feature management workspace</span></span>

<span data-ttu-id="38696-136">Функции добавляются и обновляются в каждом выпуске.</span><span class="sxs-lookup"><span data-stu-id="38696-136">Features are added and updated in every release.</span></span> <span data-ttu-id="38696-137">Опыт управления функциями предоставляет рабочую область, в которой можно просматривать список функций, которые были поставлены в каждом выпуске.</span><span class="sxs-lookup"><span data-stu-id="38696-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="38696-138">По умолчанию новые функции отключены.</span><span class="sxs-lookup"><span data-stu-id="38696-138">By default, new features are turned off.</span></span> <span data-ttu-id="38696-139">Можно использовать рабочую область для их включения и просмотра документации по ним.</span><span class="sxs-lookup"><span data-stu-id="38696-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="38696-140">Для получения дополнительных сведений об изменениях, связанных с управлением функциями, см. раздел [Обзор управления функциями,](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="38696-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
