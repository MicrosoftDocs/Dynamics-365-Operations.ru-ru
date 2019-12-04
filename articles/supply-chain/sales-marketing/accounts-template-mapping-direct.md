---
title: Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management
description: В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации организаций из Dynamics 365 Sales в Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ebca416e94f44d0448a4f4d0be08f13e30e749e9
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813232"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="f3fda-103">Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f3fda-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f3fda-104">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="f3fda-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="f3fda-105">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации организаций непосредственно из Dynamics 365 Sales в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="f3fda-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="f3fda-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="f3fda-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="f3fda-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="f3fda-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="f3fda-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="f3fda-109">На следующем рисунке показано, как данные синхронизируются между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="f3fda-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="f3fda-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="f3fda-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f3fda-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="f3fda-111">Templates and tasks</span></span>

<span data-ttu-id="f3fda-112">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="f3fda-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="f3fda-113">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="f3fda-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f3fda-114">Следующий шаблон и базовая задача используется для синхронизации счетов из Sales с Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="f3fda-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="f3fda-115">**Имя шаблона в интеграции данных:** "Организации (из Sales в Fin and Ops) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="f3fda-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="f3fda-116">**Имя задачи в проекте:** Организации — Клиенты</span><span class="sxs-lookup"><span data-stu-id="f3fda-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="f3fda-117">Никакие задачи синхронизации не требуются до того, как можно будет выполнить синхронизацию организаций/клиентов.</span><span class="sxs-lookup"><span data-stu-id="f3fda-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f3fda-118">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="f3fda-118">Entity set</span></span>

| <span data-ttu-id="f3fda-119">Прод.</span><span class="sxs-lookup"><span data-stu-id="f3fda-119">Sales</span></span>    | <span data-ttu-id="f3fda-120">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="f3fda-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="f3fda-121">Счета</span><span class="sxs-lookup"><span data-stu-id="f3fda-121">Accounts</span></span> | <span data-ttu-id="f3fda-122">Клиенты V2</span><span class="sxs-lookup"><span data-stu-id="f3fda-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="f3fda-123">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="f3fda-123">Entity flow</span></span>

<span data-ttu-id="f3fda-124">Для управления организациями используется приложение Sales, из которого они синхронизируются с Supply Chain Management в качестве клиентов.</span><span class="sxs-lookup"><span data-stu-id="f3fda-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="f3fda-125">Свойство **Управляется извне** этих клиентов имеет значение **Да** для отслеживания клиентов, которые происходят из Sales.</span><span class="sxs-lookup"><span data-stu-id="f3fda-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="f3fda-126">Во время выставления накладных эта информация используется для фильтрации накладных, которые синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="f3fda-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f3fda-127">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="f3fda-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f3fda-128">Поле **Номер счета** доступно на странице **Счет**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="f3fda-129">Оно является естественным и уникальным ключом для поддержки интеграции.</span><span class="sxs-lookup"><span data-stu-id="f3fda-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="f3fda-130">Функция естественного ключа решения управления взаимоотношениями с клиентами (CRM) могут повлиять на клиентов, уже использующих поле **Номер счета**, но не использующих значение **Номер счета** для счета.</span><span class="sxs-lookup"><span data-stu-id="f3fda-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="f3fda-131">В настоящее время решение интеграции не поддерживает это.</span><span class="sxs-lookup"><span data-stu-id="f3fda-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="f3fda-132">При создании нового счета, если значение **Номер счета** еще не существует, оно создается автоматически с использованием номерной серии.</span><span class="sxs-lookup"><span data-stu-id="f3fda-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="f3fda-133">Значение состоит из **ACC**, после чего следует увеличивающая номерная серия и суффикс из шести символов.</span><span class="sxs-lookup"><span data-stu-id="f3fda-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="f3fda-134">Пример: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="f3fda-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="f3fda-135">При применении решения интеграции для Sales сценарий обновления задает значение в поле **Номер счета** для существующих счетов в Sales.</span><span class="sxs-lookup"><span data-stu-id="f3fda-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="f3fda-136">Если значения **Номер счета** не существуют, используется номерная серия, упомянутая выше.</span><span class="sxs-lookup"><span data-stu-id="f3fda-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f3fda-137">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="f3fda-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="f3fda-138">Сопоставление **CustomerGroupId** необходимо обновить до допустимого значения в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="f3fda-139">Можно указать значение по умолчанию или задать значение, используя сопоставление значений.</span><span class="sxs-lookup"><span data-stu-id="f3fda-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="f3fda-140">Значение шаблона по умолчанию — **10**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-140">The default template value is **10**.</span></span>

- <span data-ttu-id="f3fda-141">Добавляя следующие сопоставления, можно уменьшить число обновлений вручную, необходимых в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="f3fda-142">Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="f3fda-143">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="f3fda-144">Сайт по умолчанию может использоваться из продукта или из клиента в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="f3fda-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="f3fda-145">Значение шаблона по умолчанию — **1**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="f3fda-146">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="f3fda-147">Склад по умолчанию может использоваться из продукта или из клиента в заголовке заказа в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="f3fda-148">Значение шаблона по умолчанию — **13**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="f3fda-149">**LanguageId** — язык необходим для создания предложений и заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="f3fda-150">По умолчанию используется язык из заголовка заказа от клиента.</span><span class="sxs-lookup"><span data-stu-id="f3fda-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="f3fda-151">Значение шаблона по умолчанию — **en-us**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f3fda-152">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="f3fda-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="f3fda-153">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3fda-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="f3fda-154">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="f3fda-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f3fda-155">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="f3fda-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="f3fda-156">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3fda-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Сопоставление шаблона в интеграции данных](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="f3fda-158">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="f3fda-158">Related topics</span></span>


[<span data-ttu-id="f3fda-159">Продажа перспективному клиенту</span><span class="sxs-lookup"><span data-stu-id="f3fda-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="f3fda-160">Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f3fda-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="f3fda-161">Синхронизация контактов непосредственно из Sales с контактами или клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f3fda-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="f3fda-162">Синхронизация заказов на продажу напрямую между Sales и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f3fda-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="f3fda-163">Синхронизация заголовков и строк накладной по продаже непосредственно из Supply Chain Management с Sales</span><span class="sxs-lookup"><span data-stu-id="f3fda-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

