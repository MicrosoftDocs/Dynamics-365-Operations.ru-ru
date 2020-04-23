---
title: Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Sales
description: В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Dynamics 365 Supply Chain Management в Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 85ea6d37079c965ac5ddfdc4cdd20f2f3d184e4f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216121"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="b60dd-103">Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="b60dd-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b60dd-104">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b60dd-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="b60dd-105">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации продуктов непосредственно из Dynamics 365 Supply Chain Management в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b60dd-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="b60dd-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b60dd-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="b60dd-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="b60dd-109">На следующем рисунке показано, как данные синхронизируются между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="b60dd-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b60dd-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b60dd-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="b60dd-111">Templates and tasks</span></span>

<span data-ttu-id="b60dd-112">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования Power Apps](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b60dd-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b60dd-113">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="b60dd-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b60dd-114">Следующий шаблон и базовые задачи используются для синхронизации продуктов из Supply Chain Management в Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="b60dd-115">**Имя шаблона в интеграции данных:** "Продукты (из Supply Chain Management в Sales) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="b60dd-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="b60dd-116">**Имена задачи в проекте интеграции данных:** "Продукты"</span><span class="sxs-lookup"><span data-stu-id="b60dd-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="b60dd-117">Никакие задачи синхронизации не требуются до того, как можно будет выполнить синхронизацию продуктов.</span><span class="sxs-lookup"><span data-stu-id="b60dd-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b60dd-118">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="b60dd-118">Entity set</span></span>

| <span data-ttu-id="b60dd-119">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="b60dd-119">Supply Chain Management</span></span>    | <span data-ttu-id="b60dd-120">Прод.</span><span class="sxs-lookup"><span data-stu-id="b60dd-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="b60dd-121">Запущенные в производство продукты продажи</span><span class="sxs-lookup"><span data-stu-id="b60dd-121">Sellable released products</span></span> | <span data-ttu-id="b60dd-122">Товары</span><span class="sxs-lookup"><span data-stu-id="b60dd-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b60dd-123">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="b60dd-123">Entity flow</span></span>

<span data-ttu-id="b60dd-124">Для управления продуктами используется приложение Supply Chain Management, из которого они синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="b60dd-125">Информационный объект **Запущенные в производство продукты продажи** в Supply Chain Management экспортирует только продукты, которые *могут продаваться*.</span><span class="sxs-lookup"><span data-stu-id="b60dd-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="b60dd-126">Продукты, которые могут продаваться, — это продукты, имеющие информацию, необходимую для использования в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="b60dd-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="b60dd-127">Те же правила применяются при проверке продукта с помощью функции **Проверить** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="b60dd-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="b60dd-128">Номер продукта используется как ключ.</span><span class="sxs-lookup"><span data-stu-id="b60dd-128">The product number is used as a key.</span></span> <span data-ttu-id="b60dd-129">Таким образом, при синхронизации вариантов продукта в Sales каждый вариант имеет отдельный код продукта.</span><span class="sxs-lookup"><span data-stu-id="b60dd-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b60dd-130">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="b60dd-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b60dd-131">В Sales для продуктов добавлено новое поле **Управляется извне** для указания того, что данный продукт управляется извне.</span><span class="sxs-lookup"><span data-stu-id="b60dd-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="b60dd-132">По умолчанию при импорте в Sales задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b60dd-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="b60dd-133">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b60dd-133">The following values are available:</span></span>

- <span data-ttu-id="b60dd-134">**Да** — продукта поступил из Supply Chain Management и не может быть изменен в Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="b60dd-135">**Нет** — продукт был введен непосредственно в Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="b60dd-136">**(Пусто)** — продукт существовали в Sales до включения решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="b60dd-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="b60dd-137">Поле **Управляется извне** помогает обеспечить, что предложения и заказы на продажу, имеющие управляемые извне продукты, будут синхронизироваться с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b60dd-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="b60dd-138">Управляемые извне продукты автоматически добавляются к первому допустимому прайс-листу с той же валютой.</span><span class="sxs-lookup"><span data-stu-id="b60dd-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="b60dd-139">Прайс-листы упорядочены в алфавитном порядке по имени.</span><span class="sxs-lookup"><span data-stu-id="b60dd-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="b60dd-140">Цена продажи продукта из Supply Chain Management используется как цена в прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="b60dd-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="b60dd-141">Таким образом, должен быть прайс-лист в Sales для каждой валюты продажи продуктов в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b60dd-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="b60dd-142">Валюта в запущенных в производство продуктах продажи задана как валюта учета в юридическом лице, из которого экспортируется продукт.</span><span class="sxs-lookup"><span data-stu-id="b60dd-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="b60dd-143">Продукт не будет успешно синхронизирован при отсутствии прайс-листа в соответствующей валюте.</span><span class="sxs-lookup"><span data-stu-id="b60dd-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="b60dd-144">Вы можете управлять используемым прайс-листом с интеграцией путем соответствия pricelevelid.name [Прайс-лист по умолчанию (Имя)] в проекте интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b60dd-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="b60dd-145">Ввод данных должен осуществляться буквами нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="b60dd-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="b60dd-146">Например, для прайс-листа в Продажи с именем «Стандарт» будет стоять по умолчанию: поле назначения: pricelevelid.name [Прайс-лист по умолчанию (Имя)] и тип карты: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="b60dd-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b60dd-147">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="b60dd-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="b60dd-148">Перед первым выполнением синхронизации необходимо заполнить таблицу уникально идентифицируемого продукта для существующих продуктов в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b60dd-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="b60dd-149">Существующие продукты не будут синхронизированы, пока не будет выполнено это задание.</span><span class="sxs-lookup"><span data-stu-id="b60dd-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="b60dd-150">В Supply Chain Management используйте поиск для поиска команды **Заполнить таблицу уникально идентифицируемых продуктов**.</span><span class="sxs-lookup"><span data-stu-id="b60dd-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="b60dd-151">Выберите **Заполнить таблицу уникально идентифицируемых продуктов** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="b60dd-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="b60dd-152">Это задание должно запускаться только один раз.</span><span class="sxs-lookup"><span data-stu-id="b60dd-152">This job must be run only one time.</span></span>

- <span data-ttu-id="b60dd-153">Убедитесь, что требуемое соответствие значений для единицы измерения продажи между Supply Chain Management и Sales существует в сопоставлении **SalesUnitSymbol** с **DefaultUnit (Имя)**.</span><span class="sxs-lookup"><span data-stu-id="b60dd-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="b60dd-154">Обновите сопоставление значений для параметра **Группа единиц** (**defaultuomscheduleid.name**), чтобы оно соответствовало параметру **Группы единиц** в Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="b60dd-155">Значение шаблона по умолчанию — **Единица измерения по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="b60dd-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="b60dd-156">Убедитесь, что единицы измерения при продаже для всех продуктов в Supply Chain Management существуют в Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="b60dd-157">Убедитесь, что прайс-листы существуют Sales для каждой валюты продажи продуктов в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b60dd-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="b60dd-158">При создании продуктов в Sales они могут иметь статус **Черновик** или **Активный**.</span><span class="sxs-lookup"><span data-stu-id="b60dd-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="b60dd-159">Поведение контролируется параметром **Параметры** > **Администрирование** > **Настройки системы** > **Продажи** в Sales.</span><span class="sxs-lookup"><span data-stu-id="b60dd-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="b60dd-160">Продукты, которые при создании имеют статус **Черновик**, должны быть активированы, прежде чем они могут быть добавлены в предложения или заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="b60dd-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b60dd-161">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="b60dd-161">Template mapping in Data integration</span></span>

<span data-ttu-id="b60dd-162">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b60dd-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b60dd-163">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b60dd-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Сопоставление шаблона в интеграторе данных](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="b60dd-165">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="b60dd-165">Related topics</span></span>

[<span data-ttu-id="b60dd-166">Продажа перспективному клиенту</span><span class="sxs-lookup"><span data-stu-id="b60dd-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b60dd-167">Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b60dd-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b60dd-168">Синхронизация контактов непосредственно из Sales с контактами или клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b60dd-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="b60dd-169">Синхронизация заказов на продажу напрямую между Sales и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b60dd-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="b60dd-170">Синхронизация заголовков и строк накладной по продаже непосредственно из Supply Chain Management с Sales</span><span class="sxs-lookup"><span data-stu-id="b60dd-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



