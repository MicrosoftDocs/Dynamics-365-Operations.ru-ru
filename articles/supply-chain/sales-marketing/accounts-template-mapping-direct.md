---
title: Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management
description: В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации организаций из Dynamics 365 Sales в Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fff9171966045e9dad5f2c70087a568cfa075e43
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908140"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="1c40d-103">Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1c40d-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="1c40d-104">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных в Microsoft Dataverse для приложений](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="1c40d-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="1c40d-105">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации организаций непосредственно из Dynamics 365 Sales в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="1c40d-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="1c40d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="1c40d-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="1c40d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="1c40d-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="1c40d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="1c40d-109">На следующем рисунке показано, как данные синхронизируются между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="1c40d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="1c40d-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="1c40d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1c40d-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="1c40d-111">Templates and tasks</span></span>

<span data-ttu-id="1c40d-112">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="1c40d-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="1c40d-113">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="1c40d-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1c40d-114">Следующий шаблон и базовая задача используется для синхронизации счетов из Sales с Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="1c40d-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="1c40d-115">**Имя шаблона в интеграции данных:** "Организации (из Sales в Fin and Ops) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="1c40d-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="1c40d-116">**Имя задачи в проекте:** Организации — Клиенты</span><span class="sxs-lookup"><span data-stu-id="1c40d-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="1c40d-117">Никакие задачи синхронизации не требуются до того, как можно будет выполнить синхронизацию организаций/клиентов.</span><span class="sxs-lookup"><span data-stu-id="1c40d-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="1c40d-118">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="1c40d-118">Entity set</span></span>

| <span data-ttu-id="1c40d-119">Прод.</span><span class="sxs-lookup"><span data-stu-id="1c40d-119">Sales</span></span>    | <span data-ttu-id="1c40d-120">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="1c40d-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="1c40d-121">Счета</span><span class="sxs-lookup"><span data-stu-id="1c40d-121">Accounts</span></span> | <span data-ttu-id="1c40d-122">Клиенты V2</span><span class="sxs-lookup"><span data-stu-id="1c40d-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="1c40d-123">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="1c40d-123">Entity flow</span></span>

<span data-ttu-id="1c40d-124">Для управления организациями используется приложение Sales, из которого они синхронизируются с Supply Chain Management в качестве клиентов.</span><span class="sxs-lookup"><span data-stu-id="1c40d-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="1c40d-125">Свойство **Управляется извне** этих клиентов имеет значение **Да** для отслеживания клиентов, которые происходят из Sales.</span><span class="sxs-lookup"><span data-stu-id="1c40d-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="1c40d-126">Во время выставления накладных эта информация используется для фильтрации накладных, которые синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="1c40d-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1c40d-127">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="1c40d-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1c40d-128">Столбец **Номер счета** доступен на странице **Счет**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-128">The **Account Number** column is available on the **Account** page.</span></span> <span data-ttu-id="1c40d-129">Оно является естественным и уникальным ключом для поддержки интеграции.</span><span class="sxs-lookup"><span data-stu-id="1c40d-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="1c40d-130">Функция естественного ключа решения управления взаимоотношениями с клиентами (CRM) могут повлиять на клиентов, уже использующих столбец **Номер счета**, но не использующих уникальные значения **Номер счета** для каждого счета.</span><span class="sxs-lookup"><span data-stu-id="1c40d-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** column, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="1c40d-131">В настоящее время решение интеграции не поддерживает это.</span><span class="sxs-lookup"><span data-stu-id="1c40d-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="1c40d-132">При создании нового счета, если значение **Номер счета** еще не существует, оно создается автоматически с использованием номерной серии.</span><span class="sxs-lookup"><span data-stu-id="1c40d-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="1c40d-133">Значение состоит из **ACC**, после чего следует увеличивающая номерная серия и суффикс из шести символов.</span><span class="sxs-lookup"><span data-stu-id="1c40d-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="1c40d-134">Пример: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="1c40d-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="1c40d-135">При применении решения интеграции для Sales сценарий обновления задает значение в столбце **Номер счета** для существующих счетов в Sales.</span><span class="sxs-lookup"><span data-stu-id="1c40d-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** column for existing accounts in Sales.</span></span> <span data-ttu-id="1c40d-136">Если значения **Номер счета** не существуют, используется номерная серия, упомянутая выше.</span><span class="sxs-lookup"><span data-stu-id="1c40d-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1c40d-137">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="1c40d-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="1c40d-138">Сопоставление **CustomerGroupId** необходимо обновить до допустимого значения в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="1c40d-139">Можно указать значение по умолчанию или задать значение, используя сопоставление значений.</span><span class="sxs-lookup"><span data-stu-id="1c40d-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="1c40d-140">Значение шаблона по умолчанию — **10**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-140">The default template value is **10**.</span></span>

- <span data-ttu-id="1c40d-141">Добавляя следующие сопоставления, можно уменьшить число обновлений вручную, необходимых в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="1c40d-142">Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="1c40d-143">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="1c40d-144">Сайт по умолчанию может использоваться из продукта или из клиента в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="1c40d-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="1c40d-145">Значение шаблона по умолчанию — **1**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="1c40d-146">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="1c40d-147">Склад по умолчанию может использоваться из продукта или из клиента в заголовке заказа в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="1c40d-148">Значение шаблона по умолчанию — **13**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="1c40d-149">**LanguageId** — язык необходим для создания предложений и заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="1c40d-150">По умолчанию используется язык из заголовка заказа от клиента.</span><span class="sxs-lookup"><span data-stu-id="1c40d-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="1c40d-151">Значение шаблона по умолчанию — **en-us**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1c40d-152">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="1c40d-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="1c40d-153">Столбцы **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c40d-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="1c40d-154">Чтобы сопоставить эти столбцы, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется таблица.</span><span class="sxs-lookup"><span data-stu-id="1c40d-154">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synchronized between.</span></span>

<span data-ttu-id="1c40d-155">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="1c40d-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c40d-156">Сопоставление показывает, какие данные столбцов будут синхронизированы из Sales в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c40d-156">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

![Сопоставление шаблона в интеграции данных](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="1c40d-158">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="1c40d-158">Related topics</span></span>


[<span data-ttu-id="1c40d-159">Продажа перспективному клиенту</span><span class="sxs-lookup"><span data-stu-id="1c40d-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="1c40d-160">Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1c40d-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="1c40d-161">Синхронизация контактов непосредственно из Sales с контактами или клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1c40d-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="1c40d-162">Синхронизация заказов на продажу напрямую между Sales и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1c40d-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="1c40d-163">Синхронизация заголовков и строк накладной по продаже непосредственно из Supply Chain Management с Sales</span><span class="sxs-lookup"><span data-stu-id="1c40d-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]