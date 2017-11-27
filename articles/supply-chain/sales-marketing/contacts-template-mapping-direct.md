---
title: "Синхронизация контактов непосредственно из Sales с контактами и клиентами в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации объектов Контакт (контакты) и Контакт (клиенты) из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="b75de-103">Синхронизация контактов непосредственно из Sales с контактами и клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b75de-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b75de-104">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="b75de-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="b75de-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации объектов Контакт (контакты) и Контакт (клиенты) непосредственно из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="b75de-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b75de-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="b75de-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b75de-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="b75de-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="b75de-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="b75de-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="b75de-109">На следующем рисунке показано, как данные синхронизируются между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="b75de-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="b75de-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b75de-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b75de-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="b75de-111">Templates and tasks</span></span>

<span data-ttu-id="b75de-112">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b75de-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b75de-113">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="b75de-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b75de-114">Следующие шаблоны и базовые задачи используются для синхронизации объектов "Контакт" (контакты) в Sales с объектами "Контакт" (клиенты) в Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b75de-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="b75de-115">**Имена шаблонов в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="b75de-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="b75de-116">Контакты (из Sales в Fin and Ops) — напрямую</span><span class="sxs-lookup"><span data-stu-id="b75de-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="b75de-117">Контакты с клиентом (из Sales в Fin and Ops) — напрямую</span><span class="sxs-lookup"><span data-stu-id="b75de-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="b75de-118">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="b75de-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b75de-119">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="b75de-119">Contacts</span></span>
    - <span data-ttu-id="b75de-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="b75de-120">ContactToCustomer</span></span>

<span data-ttu-id="b75de-121">Следующая задача синхронизации необходима, чтобы стала возможна синхронизации контактов: счета (из Sales в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b75de-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="b75de-122">Наборы объектов</span><span class="sxs-lookup"><span data-stu-id="b75de-122">Entity sets</span></span>

| <span data-ttu-id="b75de-123">Прод.</span><span class="sxs-lookup"><span data-stu-id="b75de-123">Sales</span></span>    | <span data-ttu-id="b75de-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b75de-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="b75de-125">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="b75de-125">Contacts</span></span> | <span data-ttu-id="b75de-126">Контакты CDS</span><span class="sxs-lookup"><span data-stu-id="b75de-126">CDS Contacts</span></span>           |
| <span data-ttu-id="b75de-127">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="b75de-127">Contacts</span></span> | <span data-ttu-id="b75de-128">Клиенты V2</span><span class="sxs-lookup"><span data-stu-id="b75de-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b75de-129">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="b75de-129">Entity flow</span></span>

<span data-ttu-id="b75de-130">Контакты управляются в Sales и синхронизируются с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="b75de-131">Контакт в Sales может стать контактом или клиентом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="b75de-132">Чтобы определить, должен ли контакт в Sales синхронизироваться в Finance and Operations в качестве контакта или клиента, система проверяет следующие свойства контакта в Sales:</span><span class="sxs-lookup"><span data-stu-id="b75de-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="b75de-133">**Синхронизация с клиентом в Finance and Operations:** контакты, в которых для параметра **Является активным клиентом** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b75de-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="b75de-134">**Синхронизация с контактом в Finance and Operations:** контакты, у которых для параметра **Является активным клиентом** задано значение **Нет**, а параметр **Компания** (родительская организация/контакт) указывает на организацию (не на контакт).</span><span class="sxs-lookup"><span data-stu-id="b75de-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b75de-135">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="b75de-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b75de-136">Новое поле **Является активным клиентов** добавлено к контакту.</span><span class="sxs-lookup"><span data-stu-id="b75de-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="b75de-137">Это поле используется для разделения контактов, имеющих мероприятия по продаже, и контактов, не имеющих мероприятий по продаже.</span><span class="sxs-lookup"><span data-stu-id="b75de-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="b75de-138">В поле **Является активным клиентом** установлено значение **Да** только для контактов, с которыми связаны предложения, заказы или счета.</span><span class="sxs-lookup"><span data-stu-id="b75de-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="b75de-139">Только эти контакты синхронизируются с Finance and Operations как клиенты.</span><span class="sxs-lookup"><span data-stu-id="b75de-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="b75de-140">Новое поле **IsCompanyAnAccount** добавлено к контакту.</span><span class="sxs-lookup"><span data-stu-id="b75de-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="b75de-141">Это поле указывает, связан ли контакт с компанией (родительской организацией/контактом) типа **Организация**.</span><span class="sxs-lookup"><span data-stu-id="b75de-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="b75de-142">Эта информация используется для определения контактов, которые должны синхронизироваться с Finance and Operations как контакты.</span><span class="sxs-lookup"><span data-stu-id="b75de-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="b75de-143">Новое поле **Номер контакта** добавлено к контакту для предоставления естественного и уникального ключа для интеграции.</span><span class="sxs-lookup"><span data-stu-id="b75de-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="b75de-144">Когда создается новый контакт, значение **Номер контакта** обновляется автоматически с использованием номерной серии.</span><span class="sxs-lookup"><span data-stu-id="b75de-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="b75de-145">Значение состоит из **CON**, после чего следует увеличивающая номерная серия и суффикс из шести символов.</span><span class="sxs-lookup"><span data-stu-id="b75de-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="b75de-146">Пример: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="b75de-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="b75de-147">При применении решения интеграции для Sales сценарий обновления задает значение в поле **Номер контакта** для существующих контактов с использованием номерной серии, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="b75de-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="b75de-148">Сценарий обновления также задает для поля **Является активным клиентом** значение **Да** для всех контактов, имеющие мероприятия по продажам.</span><span class="sxs-lookup"><span data-stu-id="b75de-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="b75de-149">В Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b75de-149">In Finance and Operations</span></span>

<span data-ttu-id="b75de-150">Контакты, помеченные с помощью свойства **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="b75de-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="b75de-151">Это свойство указывает, что данный контакт ведется извне.</span><span class="sxs-lookup"><span data-stu-id="b75de-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="b75de-152">В этом случае контакты, ведение которых выполняется извне, ведутся в Sales.</span><span class="sxs-lookup"><span data-stu-id="b75de-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b75de-153">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="b75de-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="b75de-154">Контакт в клиента</span><span class="sxs-lookup"><span data-stu-id="b75de-154">Contact to customer</span></span>

- <span data-ttu-id="b75de-155">Поле **CustomerGroup** является обязательным в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="b75de-156">Чтобы помочь избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="b75de-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="b75de-157">Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales.</span><span class="sxs-lookup"><span data-stu-id="b75de-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="b75de-158">Значение шаблона по умолчанию — **10**.</span><span class="sxs-lookup"><span data-stu-id="b75de-158">The default template value is **10**.</span></span>

- <span data-ttu-id="b75de-159">Добавляя следующие сопоставления, можно уменьшить число обновлений вручную, необходимых в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="b75de-160">Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.</span><span class="sxs-lookup"><span data-stu-id="b75de-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="b75de-161">**SiteId** — сайт по умолчанию также может быть определен в продуктах в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="b75de-162">Сайт необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="b75de-163">Значение шаблона для **SiteId** не определено.</span><span class="sxs-lookup"><span data-stu-id="b75de-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="b75de-164">**WarehouseId** — склад по умолчанию также может быть определен в продуктах в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="b75de-165">Склад необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="b75de-166">Значение шаблона для **WarehouseId** не определено.</span><span class="sxs-lookup"><span data-stu-id="b75de-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="b75de-167">**LanguageId** — язык необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="b75de-168">Значение шаблона по умолчанию — **en-us**.</span><span class="sxs-lookup"><span data-stu-id="b75de-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b75de-169">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="b75de-169">Template mapping in Data integration</span></span>

<span data-ttu-id="b75de-170">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b75de-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b75de-171">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b75de-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="b75de-172">Контакт в контакт</span><span class="sxs-lookup"><span data-stu-id="b75de-172">Contact to contact</span></span>

![Сопоставление шаблона в интеграторе данных](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="b75de-174">Контакт в клиента</span><span class="sxs-lookup"><span data-stu-id="b75de-174">Contact to customer</span></span>

![Сопоставление шаблона в интеграторе данных](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="b75de-176">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="b75de-176">Related topics</span></span>

[<span data-ttu-id="b75de-177">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="b75de-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b75de-178">Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b75de-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b75de-179">Прямая синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="b75de-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="b75de-180">Синхронизация заголовков и строк заказов на продажу непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="b75de-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="b75de-181">Синхронизация заголовков и строк счетов продажи непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="b75de-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



