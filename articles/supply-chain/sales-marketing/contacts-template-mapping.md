---
title: "Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации контакта (контакты) и контакта (клиенты) из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="ac8d7-103">Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac8d7-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ac8d7-104">Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="ac8d7-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="ac8d7-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации объектов "Контакт" (контакты) и "Контакт" (клиенты) из Microsoft Dynamics 365 for Sales (Sales) с Microsoft Dynamics 365 for Finance and Operations , выпуск Enterprise, (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="ac8d7-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ac8d7-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="ac8d7-106">Templates and tasks</span></span>

<span data-ttu-id="ac8d7-107">Следующие шаблоны и базовые задачи используются для синхронизации объекта "Контакт" (контакты) в Sales с объектом "Контакт" (клиенты) в Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="ac8d7-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="ac8d7-108">**Имена шаблонов:**</span><span class="sxs-lookup"><span data-stu-id="ac8d7-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="ac8d7-109">Контакты (Sales в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ac8d7-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="ac8d7-110">Контакты в клиента (Sales в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ac8d7-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="ac8d7-111">**Имена задач в проекте:**</span><span class="sxs-lookup"><span data-stu-id="ac8d7-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="ac8d7-112">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="ac8d7-112">Contacts</span></span>
    - <span data-ttu-id="ac8d7-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="ac8d7-113">ContactToCustomer</span></span>

<span data-ttu-id="ac8d7-114">Следующая задача синхронизации необходима до синхронизации контактов: счета (Sales в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ac8d7-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="ac8d7-115">Наборы объектов</span><span class="sxs-lookup"><span data-stu-id="ac8d7-115">Entity sets</span></span>

| <span data-ttu-id="ac8d7-116">Прод.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-116">Sales</span></span>    | <span data-ttu-id="ac8d7-117">CDS</span><span class="sxs-lookup"><span data-stu-id="ac8d7-117">CDS</span></span>     | <span data-ttu-id="ac8d7-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac8d7-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="ac8d7-119">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="ac8d7-119">Contacts</span></span> | <span data-ttu-id="ac8d7-120">Контакт</span><span class="sxs-lookup"><span data-stu-id="ac8d7-120">Contact</span></span> | <span data-ttu-id="ac8d7-121">Контакты CDS</span><span class="sxs-lookup"><span data-stu-id="ac8d7-121">CDS Contacts</span></span>           |
| <span data-ttu-id="ac8d7-122">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="ac8d7-122">Contacts</span></span> | <span data-ttu-id="ac8d7-123">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="ac8d7-123">Account</span></span> | <span data-ttu-id="ac8d7-124">Клиенты V2</span><span class="sxs-lookup"><span data-stu-id="ac8d7-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="ac8d7-125">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="ac8d7-125">Entity flow</span></span>

<span data-ttu-id="ac8d7-126">Контакты управляются в Sales и синхронизируются с Common Data Service (CDS) и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="ac8d7-127">Контакт в Sales может стать контактом в CDS и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="ac8d7-128">Либо он может стать счетом в CDS и клиентом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-129">Для определения того, должен ли контакт извлекаться из Sales для синхронизации с CDS и Finance and Operations (например, контакты из Sales &gt; контакт в CDS &gt; контакты в Finance and Operations), система рассматривает следующие свойства контакта в Sales:</span><span class="sxs-lookup"><span data-stu-id="ac8d7-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="ac8d7-130">**Синхронизация со счетом в CDS и клиентом в Finance and Operations:** контакты, параметр **Является активным клиентом** которых имеет значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="ac8d7-131">**Синхронизация с контактом в CDS и контактом в Finance and Operations:** контакты, для параметра **Является активным клиентом** которых задано значение **Нет**, и параметр **Компания** (родительский счет/контакт) указывает на счет (не контакт).</span><span class="sxs-lookup"><span data-stu-id="ac8d7-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ac8d7-132">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="ac8d7-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="ac8d7-133">Новое поле **Является активным клиентов** добавлено к контакту.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="ac8d7-134">Это поле используется для разделения контактов, имеющих мероприятия по продаже, и контактов, не имеющих мероприятия по продаже.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="ac8d7-135">В поле **Является активным клиентов** установлено значение **Да** только для контактов, с которыми связаны предложения, заказы или счета.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="ac8d7-136">Только эти контакты синхронизируются с Finance and Operations как клиенты.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="ac8d7-137">Новое поле **IsCompanyAnAccount** добавлено к контакту.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="ac8d7-138">Это поле используется для указания того, связан ли контакт с компанией (родительским счетом/контактом) типа **Счет**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="ac8d7-139">Эта информация используется для определения контактов, которые должны синхронизироваться с Finance and Operations как контакты.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="ac8d7-140">Новое поле **Номер контакта** добавлено к контакту для предоставления естественного и уникального ключа для интеграции.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="ac8d7-141">Когда создается новый контакт, значение **Номер контакта** обновляется автоматически с использованием номерной серии.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="ac8d7-142">Значение состоит из **CON**, после чего следует увеличивающая номерная серия и суффикс из шести символов.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="ac8d7-143">Пример: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="ac8d7-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="ac8d7-144">При добавлении решения интеграции для Sales в Sales сценарий обновления задает значение в поле **Номер контакта** для существующих контактов с использованием номерной серии, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="ac8d7-145">Сценарий обновления также задает для поля **Является активным клиентом** значение **Да** для всех контактов, имеющие мероприятия по продажам.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="ac8d7-146">В Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac8d7-146">In Finance and Operations</span></span> 

<span data-ttu-id="ac8d7-147">Контакты, помеченные с помощью свойства **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="ac8d7-148">Это свойство указывает, что данный контакт ведется извне.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="ac8d7-149">В этом случае контакты, ведение которых выполняется извне, ведутся в Sales.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ac8d7-150">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="ac8d7-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="ac8d7-151">Контакт в контакт</span><span class="sxs-lookup"><span data-stu-id="ac8d7-151">Contact to Contact</span></span>

- <span data-ttu-id="ac8d7-152">Обновите **Код организации CDS** в сопоставлении **Источник &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="ac8d7-153">Значение шаблона по умолчанию для **Organization_OrganizationId [Organization ID]** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="ac8d7-154">Значение шаблона по умолчанию для **PrimaryAccount_Organization_OrganizationId [Organization ID]** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="ac8d7-155">Поле **Код страны/региона адреса** является обязательным в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-156">Чтобы избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении **CDS &gt; Операции**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="ac8d7-157">Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="ac8d7-158">Значение шаблона по умолчанию для **PrimaryAddressCountryRegionISOCode** — **США**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="ac8d7-159">Убедитесь, что значение в следующем поле существует в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-160">Если информация не требуется в Finance and Operations, можно удалить сопоставление из сопоставления **CDS &gt; Место назначения**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="ac8d7-161">**Имя поля в Finance and Operations:** "Решение"</span><span class="sxs-lookup"><span data-stu-id="ac8d7-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="ac8d7-162">**Сопоставление:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="ac8d7-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="ac8d7-163">Контакт в клиента</span><span class="sxs-lookup"><span data-stu-id="ac8d7-163">Contact to Customer</span></span>

- <span data-ttu-id="ac8d7-164">Обновите **Код организации CDS** в сопоставлении **Источник &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="ac8d7-165">Значение шаблона по умолчанию для **Organization_OrganizationId [Organization ID]** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="ac8d7-166">Поле **Код страны/региона адреса** является обязательным в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-167">Чтобы избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении **CDS &gt; Место назначения**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="ac8d7-168">Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="ac8d7-169">Значение шаблона по умолчанию для **PrimaryAddressCountryRegionISOCode** — **США**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="ac8d7-170">Поле **CustomerGroup** является обязательным в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-171">Чтобы избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении **CDS &gt; Место назначения**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="ac8d7-172">Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="ac8d7-173">Значение шаблона по умолчанию для **CustomerGroupId** — **10**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="ac8d7-174">Добавляя следующие сопоставления из **CDS &gt; Место назначения**, можно уменьшить число обновлений вручную в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-175">Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="ac8d7-176">**SiteId** — сайт по умолчанию также может быть определен в продуктах в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-177">Сайт необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-178">Значение шаблона для **SiteId** не определено.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="ac8d7-179">**WarehouseId** — склад по умолчанию также может быть определен в продуктах в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-180">Склад необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-181">Значение шаблона для **WarehouseId** не определено.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="ac8d7-182">**LanguageId** — язык необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="ac8d7-183">Значение шаблона по умолчанию для **LanguageId** — **en-us**.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ac8d7-184">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="ac8d7-184">Template mapping in data integrator</span></span>

<span data-ttu-id="ac8d7-185">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="ac8d7-186">Контакт в контакт</span><span class="sxs-lookup"><span data-stu-id="ac8d7-186">Contact to Contact</span></span>

![Сопоставление шаблона в интеграторе данных](./media/contacts-template-mapping-data-integrator-1.png)

![Сопоставление шаблона для контактов в интеграторе данных](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="ac8d7-189">Контакт в клиента</span><span class="sxs-lookup"><span data-stu-id="ac8d7-189">Contact to Customer</span></span>

![Сопоставление шаблона в интеграторе данных](./media/contacts-template-mapping-data-integrator-3.png)

![Сопоставление шаблона для контактов в интеграторе данных](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="ac8d7-192">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="ac8d7-192">Related topics</span></span>

[<span data-ttu-id="ac8d7-193">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="ac8d7-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="ac8d7-194">Синхронизация контактов из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac8d7-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="ac8d7-195">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac8d7-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="ac8d7-196">Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="ac8d7-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="ac8d7-197">Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="ac8d7-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

