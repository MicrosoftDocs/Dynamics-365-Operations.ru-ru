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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769668"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="c624f-103">Организационная иерархия в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c624f-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c624f-104">Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="c624f-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="c624f-105">Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.</span><span class="sxs-lookup"><span data-stu-id="c624f-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="c624f-106">Хотя Common Data Service не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж.</span><span class="sxs-lookup"><span data-stu-id="c624f-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="c624f-107">В рамках интеграции Common Data Service структура данных иерархии организации добавляется в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c624f-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="c624f-108">Поток данных</span><span class="sxs-lookup"><span data-stu-id="c624f-108">Data flow</span></span>

<span data-ttu-id="c624f-109">Бизнес-экосистема, состоящая из приложений Finance and Operations и Common Data Service, будет по-прежнему иметь организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="c624f-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="c624f-110">Эта иерархия организации построена на приложениях Finance and Operations, но она доступна Common Data Service для целей информации и расширения.</span><span class="sxs-lookup"><span data-stu-id="c624f-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="c624f-111">На следующей иллюстрации показана информация об иерархии организации, которая доступна в Common Data Service в качестве одностороннего потока данных из приложений Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c624f-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Изображение архитектуры](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="c624f-113">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c624f-113">Templates</span></span>

<span data-ttu-id="c624f-114">Сопоставления сущности организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c624f-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="c624f-115">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c624f-115">Templates</span></span>

<span data-ttu-id="c624f-116">Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения.</span><span class="sxs-lookup"><span data-stu-id="c624f-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="c624f-117">Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений объектов.</span><span class="sxs-lookup"><span data-stu-id="c624f-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="c624f-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c624f-118">Finance and Operations</span></span> | <span data-ttu-id="c624f-119">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c624f-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="c624f-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c624f-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="c624f-121">Цели организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="c624f-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="c624f-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="c624f-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="c624f-123">Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="c624f-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="c624f-124">Тип организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="c624f-124">Organization hierarchy type</span></span> | <span data-ttu-id="c624f-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="c624f-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="c624f-126">Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="c624f-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="c624f-127">Организационная иерархия — опубликованная</span><span class="sxs-lookup"><span data-stu-id="c624f-127">Organization hierarchy - published</span></span> | <span data-ttu-id="c624f-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="c624f-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="c624f-129">Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="c624f-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="c624f-130">Операционная единица</span><span class="sxs-lookup"><span data-stu-id="c624f-130">Operating unit</span></span> | <span data-ttu-id="c624f-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="c624f-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="c624f-132">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="c624f-132">Legal entities</span></span> | <span data-ttu-id="c624f-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="c624f-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="c624f-134">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="c624f-134">Legal entities</span></span> | <span data-ttu-id="c624f-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="c624f-135">cdm_companies</span></span> | <span data-ttu-id="c624f-136">Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).</span><span class="sxs-lookup"><span data-stu-id="c624f-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="c624f-137">Внутренняя организация</span><span class="sxs-lookup"><span data-stu-id="c624f-137">Internal Organization</span></span>

<span data-ttu-id="c624f-138">Сведения о внутренней организации в Common Data Service поступают из двух объектов, **операционная единица** и **юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="c624f-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]

