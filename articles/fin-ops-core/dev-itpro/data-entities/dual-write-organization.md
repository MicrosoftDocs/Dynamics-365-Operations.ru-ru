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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572457"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="b4824-103">Организационная иерархия в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b4824-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="b4824-104">Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b4824-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="b4824-105">Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.</span><span class="sxs-lookup"><span data-stu-id="b4824-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="b4824-106">Хотя Common Data Service не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж.</span><span class="sxs-lookup"><span data-stu-id="b4824-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="b4824-107">В рамках интеграции Common Data Service структура данных иерархии организации добавляется в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b4824-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="b4824-108">Поток данных</span><span class="sxs-lookup"><span data-stu-id="b4824-108">Data flow</span></span>

<span data-ttu-id="b4824-109">Бизнес-экосистема, состоящая из приложений Finance and Operations и Common Data Service, будет по-прежнему иметь организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="b4824-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="b4824-110">Эта иерархия организации построена на приложениях Finance and Operations, но она доступна Common Data Service для целей информации и расширения.</span><span class="sxs-lookup"><span data-stu-id="b4824-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="b4824-111">На следующей иллюстрации показана информация об иерархии организации, которая доступна в Common Data Service в качестве одностороннего потока данных из приложений Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b4824-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Изображение архитектуры](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="b4824-113">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="b4824-113">Templates</span></span>

<span data-ttu-id="b4824-114">Сопоставления сущности организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b4824-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="b4824-115">Цель внутренней организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b4824-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="b4824-116">Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии из Finance and Operations в другие приложения Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b4824-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="b4824-117">Поле источника</span><span class="sxs-lookup"><span data-stu-id="b4824-117">Source field</span></span> | <span data-ttu-id="b4824-118">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="b4824-118">Map type</span></span> | <span data-ttu-id="b4824-119">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="b4824-119">Destination field</span></span>
---|---|---
<span data-ttu-id="b4824-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="b4824-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="b4824-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="b4824-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="b4824-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="b4824-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="b4824-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="b4824-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="b4824-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="b4824-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="b4824-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="b4824-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="b4824-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="b4824-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="b4824-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="b4824-127">msdyn\_immutable</span></span>
<span data-ttu-id="b4824-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="b4824-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="b4824-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="b4824-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="b4824-130">Тип внутренней организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b4824-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="b4824-131">Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии из Finance and Operations в другие приложения Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b4824-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="b4824-132">Поле источника</span><span class="sxs-lookup"><span data-stu-id="b4824-132">Source field</span></span> | <span data-ttu-id="b4824-133">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="b4824-133">Map type</span></span> | <span data-ttu-id="b4824-134">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="b4824-134">Destination field</span></span>
---|---|---
<span data-ttu-id="b4824-135">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4824-135">NAME</span></span> | \> | <span data-ttu-id="b4824-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="b4824-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="b4824-137">Внутренняя организационная иерархия</span><span class="sxs-lookup"><span data-stu-id="b4824-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="b4824-138">Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии из Finance and Operations в другие приложения Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b4824-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="b4824-139">Поле источника</span><span class="sxs-lookup"><span data-stu-id="b4824-139">Source field</span></span> | <span data-ttu-id="b4824-140">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="b4824-140">Map type</span></span> | <span data-ttu-id="b4824-141">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="b4824-141">Destination field</span></span>
---|---|---
<span data-ttu-id="b4824-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="b4824-142">VALIDTO</span></span> | \> | <span data-ttu-id="b4824-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="b4824-143">msdyn\_validto</span></span>
<span data-ttu-id="b4824-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="b4824-144">VALIDFROM</span></span> | \> | <span data-ttu-id="b4824-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="b4824-145">msdyn\_validfrom</span></span>
<span data-ttu-id="b4824-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="b4824-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="b4824-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="b4824-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="b4824-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="b4824-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="b4824-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="b4824-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="b4824-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="b4824-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="b4824-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="b4824-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="b4824-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="b4824-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="b4824-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="b4824-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="b4824-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="b4824-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="b4824-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="b4824-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="b4824-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="b4824-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="b4824-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="b4824-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="b4824-158">Внутренняя организация</span><span class="sxs-lookup"><span data-stu-id="b4824-158">Internal Organization</span></span>

<span data-ttu-id="b4824-159">Сведения о внутренней организации в Common Data Service поступают из двух объектов, **операционная единица** и **юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="b4824-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="b4824-160">Операционная единица</span><span class="sxs-lookup"><span data-stu-id="b4824-160">Operating unit</span></span>

<span data-ttu-id="b4824-161">Поле источника</span><span class="sxs-lookup"><span data-stu-id="b4824-161">Source field</span></span> | <span data-ttu-id="b4824-162">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="b4824-162">Map type</span></span> | <span data-ttu-id="b4824-163">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="b4824-163">Destination field</span></span>
---|---|---
<span data-ttu-id="b4824-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="b4824-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="b4824-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="b4824-165">msdyn\_languageid</span></span>
<span data-ttu-id="b4824-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="b4824-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="b4824-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="b4824-167">msdyn\_namealias</span></span>
<span data-ttu-id="b4824-168">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4824-168">NAME</span></span> | \> | <span data-ttu-id="b4824-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="b4824-169">msdyn\_name</span></span>
<span data-ttu-id="b4824-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="b4824-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="b4824-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="b4824-171">msdyn\_partynumber</span></span>
<span data-ttu-id="b4824-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="b4824-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="b4824-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="b4824-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="b4824-174">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="b4824-174">Legal entity</span></span>

<span data-ttu-id="b4824-175">Поле источника</span><span class="sxs-lookup"><span data-stu-id="b4824-175">Source field</span></span> | <span data-ttu-id="b4824-176">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="b4824-176">Map type</span></span> | <span data-ttu-id="b4824-177">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="b4824-177">Destination field</span></span>
---|---|---
<span data-ttu-id="b4824-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="b4824-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="b4824-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="b4824-179">msdyn\_namealias</span></span>
<span data-ttu-id="b4824-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="b4824-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="b4824-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="b4824-181">msdyn\_languageid</span></span>
<span data-ttu-id="b4824-182">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4824-182">NAME</span></span> | \> | <span data-ttu-id="b4824-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="b4824-183">msdyn\_name</span></span>
<span data-ttu-id="b4824-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="b4824-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="b4824-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="b4824-185">msdyn\_partynumber</span></span>
<span data-ttu-id="b4824-186">нет</span><span class="sxs-lookup"><span data-stu-id="b4824-186">none</span></span> | \>\> | <span data-ttu-id="b4824-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="b4824-187">msdyn\_type</span></span>
<span data-ttu-id="b4824-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="b4824-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="b4824-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="b4824-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="b4824-190">Организация</span><span class="sxs-lookup"><span data-stu-id="b4824-190">Company</span></span>

<span data-ttu-id="b4824-191">Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании) между Finance and Operations и другими приложениями Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b4824-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="b4824-192">Поле источника</span><span class="sxs-lookup"><span data-stu-id="b4824-192">Source field</span></span> | <span data-ttu-id="b4824-193">Тип сопоставления</span><span class="sxs-lookup"><span data-stu-id="b4824-193">Map type</span></span> | <span data-ttu-id="b4824-194">Поле назначения</span><span class="sxs-lookup"><span data-stu-id="b4824-194">Destination field</span></span>
---|---|---
<span data-ttu-id="b4824-195">НАИМЕНОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4824-195">NAME</span></span> | = | <span data-ttu-id="b4824-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="b4824-196">cdm\_name</span></span>
<span data-ttu-id="b4824-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="b4824-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="b4824-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="b4824-198">cdm\_companycode</span></span>
