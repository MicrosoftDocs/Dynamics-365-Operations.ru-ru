---
title: Организационная иерархия в Dataverse
description: Эта тема описывает интеграцию организационных данных между приложениями Finance and Operations и Dataverse.
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
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680080"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="2add4-103">Организационная иерархия в Dataverse</span><span class="sxs-lookup"><span data-stu-id="2add4-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2add4-104">Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="2add4-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="2add4-105">Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.</span><span class="sxs-lookup"><span data-stu-id="2add4-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="2add4-106">Хотя Dataverse не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж.</span><span class="sxs-lookup"><span data-stu-id="2add4-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="2add4-107">В рамках интеграции Dataverse структура данных иерархии организации добавляется в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2add4-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="2add4-108">Поток данных</span><span class="sxs-lookup"><span data-stu-id="2add4-108">Data flow</span></span>

<span data-ttu-id="2add4-109">Бизнес-экосистема, состоящая из приложений Finance and Operations и Dataverse, будет по-прежнему иметь организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="2add4-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="2add4-110">Эта организационная иерархия построена на приложениях Finance and Operations, но она доступна в Dataverse для целей информации и расширения.</span><span class="sxs-lookup"><span data-stu-id="2add4-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="2add4-111">На следующей иллюстрации показана информация об иерархии организации, которая доступна в Dataverse в качестве одностороннего потока данных из приложений Finance and Operations в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2add4-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Изображение архитектуры](media/dual-write-data-flow.png)

<span data-ttu-id="2add4-113">Сопоставления таблицы организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2add4-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="2add4-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="2add4-114">Templates</span></span>

<span data-ttu-id="2add4-115">Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения.</span><span class="sxs-lookup"><span data-stu-id="2add4-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="2add4-116">Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="2add4-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="2add4-117">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2add4-117">Finance and Operations apps</span></span> | <span data-ttu-id="2add4-118">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2add4-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="2add4-119">описание</span><span class="sxs-lookup"><span data-stu-id="2add4-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="2add4-120">Цели организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="2add4-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="2add4-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="2add4-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="2add4-122">Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="2add4-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="2add4-123">Тип организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="2add4-123">Organization hierarchy type</span></span> | <span data-ttu-id="2add4-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="2add4-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="2add4-125">Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="2add4-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="2add4-126">Организационная иерархия — опубликованная</span><span class="sxs-lookup"><span data-stu-id="2add4-126">Organization hierarchy - published</span></span> | <span data-ttu-id="2add4-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="2add4-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="2add4-128">Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="2add4-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="2add4-129">Операционная единица</span><span class="sxs-lookup"><span data-stu-id="2add4-129">Operating unit</span></span> | <span data-ttu-id="2add4-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="2add4-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="2add4-131">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="2add4-131">Legal entities</span></span> | <span data-ttu-id="2add4-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="2add4-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="2add4-133">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="2add4-133">Legal entities</span></span> | <span data-ttu-id="2add4-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="2add4-134">cdm_companies</span></span> | <span data-ttu-id="2add4-135">Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).</span><span class="sxs-lookup"><span data-stu-id="2add4-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="2add4-136">Внутренняя организация</span><span class="sxs-lookup"><span data-stu-id="2add4-136">Internal Organization</span></span>

<span data-ttu-id="2add4-137">Сведения о внутренней организации в Dataverse поступают из двух таблиц, **операционная единица** и **юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="2add4-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
