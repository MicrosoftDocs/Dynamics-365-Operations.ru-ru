---
title: Организационная иерархия в Common Data Service
description: Эта тема описывает интеграцию организационных данных между Finance and Operations и Common Data Service.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789238"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="6f772-103">Организационная иерархия в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6f772-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="6f772-104">Поскольку Microsoft Dynamics 365 for Finance and Operations — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="6f772-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="6f772-105">Финансы и операции бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.</span><span class="sxs-lookup"><span data-stu-id="6f772-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="6f772-106">Хотя Common Data Service не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж.</span><span class="sxs-lookup"><span data-stu-id="6f772-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="6f772-107">В рамках интеграции Common Data Service структура данных иерархии организации добавляется в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6f772-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="6f772-108">Поток данных</span><span class="sxs-lookup"><span data-stu-id="6f772-108">Data flow</span></span>

<span data-ttu-id="6f772-109">Бизнес-экосистема, состоящая из Finance and Operations и Common Data Service, будет по-прежнему иметь организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="6f772-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="6f772-110">Эта иерархия организации построена на Finance and Operations, но она доступна Common Data Service для целей информации и расширения.</span><span class="sxs-lookup"><span data-stu-id="6f772-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="6f772-111">На следующей иллюстрации показана информация об иерархии организации, которая доступна в Common Data Service в качестве одностороннего потока данных из Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6f772-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Изображение архитектуры](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="6f772-113">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="6f772-113">Templates</span></span>

<span data-ttu-id="6f772-114">Сопоставления сущности организационной иерархии доступны для односторонней синхронизации данных из Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6f772-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="6f772-115">Цель внутренней организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="6f772-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="6f772-116">Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии из Finance and Operations в Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6f772-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="6f772-117">Поле источника</span><span class="sxs-lookup"><span data-stu-id="6f772-117">Source field</span></span> | <span data-ttu-id="6f772-118">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="6f772-118">Map type</span></span> | <span data-ttu-id="6f772-119">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="6f772-119">Destination field</span></span>
---|---|---
<span data-ttu-id="6f772-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6f772-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6f772-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="6f772-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="6f772-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6f772-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6f772-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6f772-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="6f772-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="6f772-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="6f772-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="6f772-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="6f772-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="6f772-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="6f772-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="6f772-127">msdyn\_immutable</span></span>
<span data-ttu-id="6f772-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="6f772-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="6f772-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="6f772-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="6f772-130">Тип внутренней организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="6f772-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="6f772-131">Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии из Finance and Operations в Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6f772-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="6f772-132">Поле источника</span><span class="sxs-lookup"><span data-stu-id="6f772-132">Source field</span></span> | <span data-ttu-id="6f772-133">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="6f772-133">Map type</span></span> | <span data-ttu-id="6f772-134">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="6f772-134">Destination field</span></span>
---|---|---
<span data-ttu-id="6f772-135">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f772-135">NAME</span></span> | \> | <span data-ttu-id="6f772-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6f772-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="6f772-137">Внутренняя организационная иерархия</span><span class="sxs-lookup"><span data-stu-id="6f772-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="6f772-138">Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии из Finance and Operations в Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6f772-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="6f772-139">Поле источника</span><span class="sxs-lookup"><span data-stu-id="6f772-139">Source field</span></span> | <span data-ttu-id="6f772-140">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="6f772-140">Map type</span></span> | <span data-ttu-id="6f772-141">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="6f772-141">Destination field</span></span>
---|---|---
<span data-ttu-id="6f772-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="6f772-142">VALIDTO</span></span> | \> | <span data-ttu-id="6f772-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="6f772-143">msdyn\_validto</span></span>
<span data-ttu-id="6f772-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="6f772-144">VALIDFROM</span></span> | \> | <span data-ttu-id="6f772-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="6f772-145">msdyn\_validfrom</span></span>
<span data-ttu-id="6f772-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6f772-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6f772-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="6f772-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="6f772-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6f772-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6f772-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="6f772-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="6f772-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6f772-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6f772-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="6f772-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="6f772-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6f772-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6f772-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6f772-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="6f772-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6f772-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6f772-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6f772-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="6f772-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6f772-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6f772-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6f772-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="6f772-158">Внутренняя организация</span><span class="sxs-lookup"><span data-stu-id="6f772-158">Internal Organization</span></span>

<span data-ttu-id="6f772-159">Сведения о внутренней организации в Common Data Service поступают из двух сущностей Finance and Operations, **операционная единица** и **юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="6f772-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="6f772-160">Операционная единица</span><span class="sxs-lookup"><span data-stu-id="6f772-160">Operating unit</span></span>

<span data-ttu-id="6f772-161">Поле источника</span><span class="sxs-lookup"><span data-stu-id="6f772-161">Source field</span></span> | <span data-ttu-id="6f772-162">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="6f772-162">Map type</span></span> | <span data-ttu-id="6f772-163">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="6f772-163">Destination field</span></span>
---|---|---
<span data-ttu-id="6f772-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="6f772-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="6f772-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="6f772-165">msdyn\_languageid</span></span>
<span data-ttu-id="6f772-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="6f772-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="6f772-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="6f772-167">msdyn\_namealias</span></span>
<span data-ttu-id="6f772-168">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f772-168">NAME</span></span> | \> | <span data-ttu-id="6f772-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6f772-169">msdyn\_name</span></span>
<span data-ttu-id="6f772-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6f772-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="6f772-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6f772-171">msdyn\_partynumber</span></span>
<span data-ttu-id="6f772-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="6f772-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="6f772-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="6f772-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="6f772-174">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="6f772-174">Legal entity</span></span>

<span data-ttu-id="6f772-175">Поле источника</span><span class="sxs-lookup"><span data-stu-id="6f772-175">Source field</span></span> | <span data-ttu-id="6f772-176">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="6f772-176">Map type</span></span> | <span data-ttu-id="6f772-177">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="6f772-177">Destination field</span></span>
---|---|---
<span data-ttu-id="6f772-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="6f772-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="6f772-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="6f772-179">msdyn\_namealias</span></span>
<span data-ttu-id="6f772-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="6f772-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="6f772-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="6f772-181">msdyn\_languageid</span></span>
<span data-ttu-id="6f772-182">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f772-182">NAME</span></span> | \> | <span data-ttu-id="6f772-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6f772-183">msdyn\_name</span></span>
<span data-ttu-id="6f772-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6f772-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="6f772-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6f772-185">msdyn\_partynumber</span></span>
<span data-ttu-id="6f772-186">нет</span><span class="sxs-lookup"><span data-stu-id="6f772-186">none</span></span> | \>\> | <span data-ttu-id="6f772-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="6f772-187">msdyn\_type</span></span>
<span data-ttu-id="6f772-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="6f772-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="6f772-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="6f772-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="6f772-190">Организация</span><span class="sxs-lookup"><span data-stu-id="6f772-190">Company</span></span>

<span data-ttu-id="6f772-191">Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании) между Finance and Operations и Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6f772-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="6f772-192">Поле источника</span><span class="sxs-lookup"><span data-stu-id="6f772-192">Source field</span></span> | <span data-ttu-id="6f772-193">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="6f772-193">Map type</span></span> | <span data-ttu-id="6f772-194">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="6f772-194">Destination field</span></span>
---|---|---
<span data-ttu-id="6f772-195">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f772-195">NAME</span></span> | = | <span data-ttu-id="6f772-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="6f772-196">cdm\_name</span></span>
<span data-ttu-id="6f772-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="6f772-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="6f772-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="6f772-198">cdm\_companycode</span></span>