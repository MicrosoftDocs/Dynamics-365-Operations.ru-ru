---
title: "Синхронизация контактов из Sales с клиентами в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации счетов из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise."
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
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="a6313-103">Синхронизация контактов из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6313-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a6313-104">Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="a6313-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="a6313-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации счетов из Microsoft Dynamics 365 for Sales (Sales) с Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise, (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="a6313-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a6313-106">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="a6313-106">Template and task</span></span>

<span data-ttu-id="a6313-107">Следующие шаблоны и базовые задачи используются для синхронизации счетов из Sales с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a6313-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="a6313-108">**Имя шаблона:** счета (Sales в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a6313-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="a6313-109">**Имя задачи в проекте:** Счета — Счет — Клиенты</span><span class="sxs-lookup"><span data-stu-id="a6313-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="a6313-110">Синхронизацию задач требуется выполнить до синхронизации счета/клиента: нет</span><span class="sxs-lookup"><span data-stu-id="a6313-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="a6313-111">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="a6313-111">Entity set</span></span>

| <span data-ttu-id="a6313-112">Прод.</span><span class="sxs-lookup"><span data-stu-id="a6313-112">Sales</span></span>    | <span data-ttu-id="a6313-113">CDS</span><span class="sxs-lookup"><span data-stu-id="a6313-113">CDS</span></span>     | <span data-ttu-id="a6313-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6313-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="a6313-115">Счета</span><span class="sxs-lookup"><span data-stu-id="a6313-115">Accounts</span></span> | <span data-ttu-id="a6313-116">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="a6313-116">Account</span></span> | <span data-ttu-id="a6313-117">Клиенты</span><span class="sxs-lookup"><span data-stu-id="a6313-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="a6313-118">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="a6313-118">Entity flow</span></span>

<span data-ttu-id="a6313-119">Счета управляются в Sales и синхронизируются с Finance and Operations как клиенты.</span><span class="sxs-lookup"><span data-stu-id="a6313-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="a6313-120">Свойство **Управляется извне** этих клиентов имеет значение **Да** для отслеживания клиентов, которые создаются в Sales.</span><span class="sxs-lookup"><span data-stu-id="a6313-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="a6313-121">Во время выставления накладных эта информация используется для фильтрации накладных, которые синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="a6313-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a6313-122">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="a6313-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a6313-123">Поле **Номер счета** доступно на странице **Счет**.</span><span class="sxs-lookup"><span data-stu-id="a6313-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="a6313-124">Оно является естественным и уникальным ключом для поддержки интеграции.</span><span class="sxs-lookup"><span data-stu-id="a6313-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="a6313-125">Функция естественного ключа решения управления взаимоотношениями с клиентами (CRM) могут повлиять на клиентов, уже использующих поле **Номер счета**, но не использующих значение **Номер счета** для счета.</span><span class="sxs-lookup"><span data-stu-id="a6313-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="a6313-126">В настоящее время решение интеграции не поддерживает это.</span><span class="sxs-lookup"><span data-stu-id="a6313-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="a6313-127">При создании нового счета, если значение **Номер счета** еще не существует, оно создается автоматически с использованием номерной серии.</span><span class="sxs-lookup"><span data-stu-id="a6313-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a6313-128">Значение состоит из **ACC**, после чего следует увеличивающая номерная серия и суффикс из шести символов.</span><span class="sxs-lookup"><span data-stu-id="a6313-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a6313-129">Пример: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a6313-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="a6313-130">При применении решения интеграции для Sales сценарий обновления задает значение в поле **Номер счета** для существующих счетов в Sales.</span><span class="sxs-lookup"><span data-stu-id="a6313-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="a6313-131">Если значения **Номер счета** не существуют, используется номерная серия, описанная выше.</span><span class="sxs-lookup"><span data-stu-id="a6313-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a6313-132">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="a6313-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="a6313-133">Сопоставление **CustomerGroupId** из **CDS &gt; Место назначения** необходимо исправить на значение, допустимое в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="a6313-134">Можно указать значение по умолчанию или задать значение, используя сопоставление значений.</span><span class="sxs-lookup"><span data-stu-id="a6313-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="a6313-135">Значение шаблона по умолчанию — **10**.</span><span class="sxs-lookup"><span data-stu-id="a6313-135">The default template value is **10**.</span></span>
- <span data-ttu-id="a6313-136">Поле **Код страны/региона адреса** является обязательным в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="a6313-137">Чтобы избежать ошибок синхронизации, можно указать в сопоставлении из **CDS &gt; Место назначения** значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6313-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="a6313-138">Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales.</span><span class="sxs-lookup"><span data-stu-id="a6313-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="a6313-139">Значение шаблона по умолчанию для **AddressCountryRegionISOCode** — **США**.</span><span class="sxs-lookup"><span data-stu-id="a6313-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="a6313-140">Значение шаблона по умолчанию для **DeliveryAddressCountryRegionISOCode** — **США**.</span><span class="sxs-lookup"><span data-stu-id="a6313-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="a6313-141">Добавляя следующие сопоставления из **CDS &gt; Место назначения**, можно уменьшить число обновлений вручную, необходимых в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="a6313-142">Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.</span><span class="sxs-lookup"><span data-stu-id="a6313-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a6313-143">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="a6313-144">Сайт по умолчанию может использоваться из продукта или из клиента в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="a6313-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="a6313-145">Значение шаблона по умолчанию для **SiteId** — **1**.</span><span class="sxs-lookup"><span data-stu-id="a6313-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="a6313-146">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="a6313-147">Склад по умолчанию может использоваться из продукта или из клиента в заголовке заказа в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="a6313-148">Значение шаблона по умолчанию для **WarehouseId** — **13**.</span><span class="sxs-lookup"><span data-stu-id="a6313-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="a6313-149">**LanguageId** — язык необходим для создания предложений и заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6313-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="a6313-150">По умолчанию используется язык из заголовка заказа от клиента.</span><span class="sxs-lookup"><span data-stu-id="a6313-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="a6313-151">Значение шаблона по умолчанию для **LanguageId** — **en-us**.</span><span class="sxs-lookup"><span data-stu-id="a6313-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="a6313-152">Обновите код организации CDS (**Organization_OrganizationId**) в сопоставлении **Источник &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="a6313-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="a6313-153">Значение шаблона по умолчанию — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="a6313-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="a6313-154">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="a6313-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="a6313-155">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6313-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="a6313-156">Чтобы сопоставить эти поля, необходимо настроить преобразование значений.</span><span class="sxs-lookup"><span data-stu-id="a6313-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="a6313-157">Преобразование значений относится к данным в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="a6313-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a6313-158">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="a6313-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Сопоставление шаблона в интеграторе данных](./media/accounts-template-mapping-data-integrator-1.png)

![Сопоставление шаблона для счетов в интеграторе данных](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="a6313-161">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a6313-161">Related topics</span></span>

[<span data-ttu-id="a6313-162">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="a6313-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="a6313-163">Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6313-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="a6313-164">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6313-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="a6313-165">Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="a6313-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="a6313-166">Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="a6313-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




