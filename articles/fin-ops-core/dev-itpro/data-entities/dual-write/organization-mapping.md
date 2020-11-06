---
title: Организационная иерархия в Common Data Service
description: Эта тема описывает интеграцию организационных данных между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000742"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="7b528-103">Организационная иерархия в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7b528-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b528-104">Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="7b528-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="7b528-105">Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.</span><span class="sxs-lookup"><span data-stu-id="7b528-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="7b528-106">Хотя Common Data Service не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж.</span><span class="sxs-lookup"><span data-stu-id="7b528-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="7b528-107">В рамках интеграции Common Data Service структура данных иерархии организации добавляется в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7b528-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="7b528-108">Поток данных</span><span class="sxs-lookup"><span data-stu-id="7b528-108">Data flow</span></span>

<span data-ttu-id="7b528-109">Бизнес-экосистема, состоящая из приложений Finance and Operations и Common Data Service, будет по-прежнему иметь организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="7b528-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="7b528-110">Эта организационная иерархия построена на приложениях Finance and Operations, но она доступна в Common Data Service для целей информации и расширения.</span><span class="sxs-lookup"><span data-stu-id="7b528-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="7b528-111">На следующей иллюстрации показана информация об иерархии организации, которая доступна в Common Data Service в качестве одностороннего потока данных из приложений Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7b528-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Изображение архитектуры](media/dual-write-data-flow.png)

<span data-ttu-id="7b528-113">Сопоставления сущности организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7b528-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="7b528-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="7b528-114">Templates</span></span>

<span data-ttu-id="7b528-115">Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения.</span><span class="sxs-lookup"><span data-stu-id="7b528-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="7b528-116">Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений объектов.</span><span class="sxs-lookup"><span data-stu-id="7b528-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="7b528-117">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b528-117">Finance and Operations apps</span></span> | <span data-ttu-id="7b528-118">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7b528-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="7b528-119">описание</span><span class="sxs-lookup"><span data-stu-id="7b528-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="7b528-120">Цели организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="7b528-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="7b528-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="7b528-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="7b528-122">Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="7b528-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="7b528-123">Тип организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="7b528-123">Organization hierarchy type</span></span> | <span data-ttu-id="7b528-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="7b528-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="7b528-125">Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="7b528-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="7b528-126">Организационная иерархия — опубликованная</span><span class="sxs-lookup"><span data-stu-id="7b528-126">Organization hierarchy - published</span></span> | <span data-ttu-id="7b528-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="7b528-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="7b528-128">Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="7b528-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="7b528-129">Операционная единица</span><span class="sxs-lookup"><span data-stu-id="7b528-129">Operating unit</span></span> | <span data-ttu-id="7b528-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="7b528-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="7b528-131">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="7b528-131">Legal entities</span></span> | <span data-ttu-id="7b528-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="7b528-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="7b528-133">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="7b528-133">Legal entities</span></span> | <span data-ttu-id="7b528-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="7b528-134">cdm_companies</span></span> | <span data-ttu-id="7b528-135">Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).</span><span class="sxs-lookup"><span data-stu-id="7b528-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="7b528-136">Внутренняя организация</span><span class="sxs-lookup"><span data-stu-id="7b528-136">Internal Organization</span></span>

<span data-ttu-id="7b528-137">Сведения о внутренней организации в Common Data Service поступают из двух объектов, **операционная единица** и **юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="7b528-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
