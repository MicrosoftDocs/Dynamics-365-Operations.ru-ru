---
title: Организационная иерархия в Dataverse
description: Эта тема описывает интеграцию организационных данных между приложениями Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750820"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="b2dc0-103">Организационная иерархия в Dataverse</span><span class="sxs-lookup"><span data-stu-id="b2dc0-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b2dc0-104">Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="b2dc0-105">Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="b2dc0-106">Хотя Dataverse не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="b2dc0-107">В рамках интеграции Dataverse структура данных иерархии организации добавляется в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="b2dc0-108">Поток данных</span><span class="sxs-lookup"><span data-stu-id="b2dc0-108">Data flow</span></span>

<span data-ttu-id="b2dc0-109">Бизнес-экосистема, состоящая из приложений Finance and Operations и Dataverse, будет по-прежнему иметь организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="b2dc0-110">Эта организационная иерархия построена на приложениях Finance and Operations, но она доступна в Dataverse для целей информации и расширения.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="b2dc0-111">На следующей иллюстрации показана информация об иерархии организации, которая доступна в Dataverse в качестве одностороннего потока данных из приложений Finance and Operations в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Изображение архитектуры](media/dual-write-data-flow.png)

<span data-ttu-id="b2dc0-113">Сопоставления таблицы организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="b2dc0-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="b2dc0-114">Templates</span></span>

<span data-ttu-id="b2dc0-115">Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="b2dc0-116">Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="b2dc0-117">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b2dc0-117">Finance and Operations apps</span></span> | <span data-ttu-id="b2dc0-118">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b2dc0-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b2dc0-119">описание</span><span class="sxs-lookup"><span data-stu-id="b2dc0-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="b2dc0-120">Цели организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b2dc0-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="b2dc0-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="b2dc0-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="b2dc0-122">Этот шаблон обеспечивает одностороннюю синхронизацию таблицы цели организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="b2dc0-123">Тип организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b2dc0-123">Organization hierarchy type</span></span> | <span data-ttu-id="b2dc0-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="b2dc0-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="b2dc0-125">Этот шаблон обеспечивает одностороннюю синхронизацию таблицы типа организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="b2dc0-126">Организационная иерархия — опубликованная версия</span><span class="sxs-lookup"><span data-stu-id="b2dc0-126">Organization hierarchy - published</span></span> | <span data-ttu-id="b2dc0-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="b2dc0-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="b2dc0-128">Этот шаблон обеспечивает одностороннюю синхронизацию таблицы опубликованной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="b2dc0-129">Операционная единица</span><span class="sxs-lookup"><span data-stu-id="b2dc0-129">Operating unit</span></span> | <span data-ttu-id="b2dc0-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="b2dc0-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="b2dc0-131">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="b2dc0-131">Legal entities</span></span> | <span data-ttu-id="b2dc0-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="b2dc0-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="b2dc0-133">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="b2dc0-133">Legal entities</span></span> | <span data-ttu-id="b2dc0-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="b2dc0-134">cdm_companies</span></span> | <span data-ttu-id="b2dc0-135">Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).</span><span class="sxs-lookup"><span data-stu-id="b2dc0-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="b2dc0-136">Внутренняя организация</span><span class="sxs-lookup"><span data-stu-id="b2dc0-136">Internal Organization</span></span>

<span data-ttu-id="b2dc0-137">Сведения о внутренней организации в Dataverse поступают из двух таблиц, **операционная единица** и **юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="b2dc0-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]