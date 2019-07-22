---
title: Прямая синхронизация продуктов из Finance and Operations с продуктами в Sales
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 06/10/2019
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
ms.openlocfilehash: ff284585a2eb4c5cf55d2e3a3e0f317d1fb218bb
ms.sourcegitcommit: 51dc11919fcb2324482b48cc4ce4484945ade803
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624343"
---
# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="9ea81-103">Синхронизация продуктов непосредственно из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="9ea81-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9ea81-104">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="9ea81-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="9ea81-105">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации продуктов непосредственно из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="9ea81-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="9ea81-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="9ea81-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="9ea81-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="9ea81-109">На следующем рисунке показано, как данные синхронизируются между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="9ea81-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="9ea81-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9ea81-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="9ea81-111">Templates and tasks</span></span>

<span data-ttu-id="9ea81-112">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования PowerApps](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="9ea81-112">To access the available templates, open [PowerApps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="9ea81-113">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="9ea81-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9ea81-114">Следующий шаблон и базовые задачи используются для синхронизации продуктов Finance and Operations с Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="9ea81-115">**Имя шаблона в интеграции данных:** "Продукты (из Fin and Ops в Sales) - напрямую"</span><span class="sxs-lookup"><span data-stu-id="9ea81-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="9ea81-116">**Имена задачи в проекте интеграции данных:** "Продукты"</span><span class="sxs-lookup"><span data-stu-id="9ea81-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="9ea81-117">Никакие задачи синхронизации не требуются до того, как можно будет выполнить синхронизацию продуктов.</span><span class="sxs-lookup"><span data-stu-id="9ea81-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="9ea81-118">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="9ea81-118">Entity set</span></span>

| <span data-ttu-id="9ea81-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ea81-119">Finance and Operations</span></span>     | <span data-ttu-id="9ea81-120">Прод.</span><span class="sxs-lookup"><span data-stu-id="9ea81-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="9ea81-121">Запущенные в производство продукты продажи</span><span class="sxs-lookup"><span data-stu-id="9ea81-121">Sellable released products</span></span> | <span data-ttu-id="9ea81-122">Товары</span><span class="sxs-lookup"><span data-stu-id="9ea81-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="9ea81-123">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="9ea81-123">Entity flow</span></span>

<span data-ttu-id="9ea81-124">Продукты управляются в Finance and Operations и синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="9ea81-125">Информационный объект **Запущенные в производство продукты продажи** в Finance and Operations экспортирует только продукты, которые *могут продаваться*.</span><span class="sxs-lookup"><span data-stu-id="9ea81-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="9ea81-126">Продукты, которые могут продаваться, — это продукты, имеющие информацию, необходимую для использования в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="9ea81-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="9ea81-127">Те же правила применяются при проверке продукта с помощью функции **Проверить** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="9ea81-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="9ea81-128">Номер продукта используется как ключ.</span><span class="sxs-lookup"><span data-stu-id="9ea81-128">The product number is used as a key.</span></span> <span data-ttu-id="9ea81-129">Таким образом, при синхронизации вариантов продукта в Sales каждый вариант имеет отдельный код продукта.</span><span class="sxs-lookup"><span data-stu-id="9ea81-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9ea81-130">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="9ea81-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9ea81-131">В Sales для продуктов добавлено новое поле **Управляется извне** для указания того, что данный продукт управляется извне.</span><span class="sxs-lookup"><span data-stu-id="9ea81-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="9ea81-132">По умолчанию при импорте в Sales задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="9ea81-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="9ea81-133">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9ea81-133">The following values are available:</span></span>

- <span data-ttu-id="9ea81-134">**Да** — продукта поступил из Finance and Operations и не может быть изменен в Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="9ea81-135">**Нет** — продукт был введен непосредственно в Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="9ea81-136">**(Пусто)** — продукт существовали в Sales до включения решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="9ea81-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="9ea81-137">Поле **Управляется извне** помогает гарантировать, что предложения и заказы на продажу, имеющие управляемые извне продукты, будут синхронизироваться с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ea81-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="9ea81-138">Управляемые извне продукты автоматически добавляются к первому допустимому прайс-листу с той же валютой.</span><span class="sxs-lookup"><span data-stu-id="9ea81-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="9ea81-139">Прайс-листы упорядочены в алфавитном порядке по имени.</span><span class="sxs-lookup"><span data-stu-id="9ea81-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="9ea81-140">Цена продажи продукта из Finance and Operations используется как цена в прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="9ea81-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="9ea81-141">Таким образом, должен быть прайс-лист в Sales для каждой валюты продажи продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ea81-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="9ea81-142">Валюта в запущенных в производство продуктах продажи задана как валюта учета в юридическом лице, из которого экспортируется продукт.</span><span class="sxs-lookup"><span data-stu-id="9ea81-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="9ea81-143">Продукт не будет успешно синхронизирован при отсутствии прайс-листа в соответствующей валюте.</span><span class="sxs-lookup"><span data-stu-id="9ea81-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="9ea81-144">Вы можете управлять используемым прайс-листом с интеграцией путем соответствия pricelevelid.name [Прайс-лист по умолчанию (Имя)] в проекте интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="9ea81-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="9ea81-145">Ввод данных должен осуществляться буквами нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="9ea81-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="9ea81-146">Например, для прайс-листа в Продажи с именем «Стандарт» будет стоять по умолчанию: поле назначения: pricelevelid.name [Прайс-лист по умолчанию (Имя)] и тип карты: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="9ea81-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9ea81-147">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="9ea81-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="9ea81-148">Перед первым выполнением синхронизации необходимо заполнить таблицу уникально идентифицируемого продукта для существующих продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ea81-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="9ea81-149">Существующие продукты не будут синхронизированы, пока не будет выполнено это задание.</span><span class="sxs-lookup"><span data-stu-id="9ea81-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="9ea81-150">В Finance and Operations используйте поиск для поиска команды **Заполнить таблицу уникально идентифицируемых продуктов**.</span><span class="sxs-lookup"><span data-stu-id="9ea81-150">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="9ea81-151">Выберите **Заполнить таблицу уникально идентифицируемых продуктов** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="9ea81-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="9ea81-152">Это задание должно запускаться только один раз.</span><span class="sxs-lookup"><span data-stu-id="9ea81-152">This job must be run only one time.</span></span>

- <span data-ttu-id="9ea81-153">Убедитесь, что требуемое соответствие значений для единицы измерения продажи между Finance and Operations и Sales существует в сопоставлении **SalesUnitSymbol** с **DefaultUnit (Имя)**.</span><span class="sxs-lookup"><span data-stu-id="9ea81-153">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="9ea81-154">Обновите сопоставление значений для параметра **Группа единиц** (**defaultuomscheduleid.name**), чтобы оно соответствовало параметру **Группы единиц** в Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="9ea81-155">Значение шаблона по умолчанию — **Единица измерения по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="9ea81-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="9ea81-156">Убедитесь, что единицы измерения при продаже для всех продуктов в Finance and Operations существуют в Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-156">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="9ea81-157">Убедитесь, что прайс-листы существуют Sales для каждой валюты продажи продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ea81-157">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="9ea81-158">При создании продуктов в Sales они могут иметь статус **Черновик** или **Активный**.</span><span class="sxs-lookup"><span data-stu-id="9ea81-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="9ea81-159">Поведение контролируется параметром **Параметры** > **Администрирование** > **Настройки системы** > **Продажи** в Sales.</span><span class="sxs-lookup"><span data-stu-id="9ea81-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="9ea81-160">Продукты, которые при создании имеют статус **Черновик**, должны быть активированы, прежде чем они могут быть добавлены в предложения или заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="9ea81-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9ea81-161">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="9ea81-161">Template mapping in Data integration</span></span>

<span data-ttu-id="9ea81-162">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="9ea81-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="9ea81-163">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ea81-163">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Сопоставление шаблона в интеграторе данных](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="9ea81-165">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="9ea81-165">Related topics</span></span>

[<span data-ttu-id="9ea81-166">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="9ea81-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="9ea81-167">Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ea81-167">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="9ea81-168">Синхронизация контактов непосредственно из Sales с контактами и клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ea81-168">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="9ea81-169">Синхронизация заголовков и строк заказов на продажу непосредственно из Finance and Operations с Sales</span><span class="sxs-lookup"><span data-stu-id="9ea81-169">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="9ea81-170">Синхронизация заголовков и строк счетов продажи непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="9ea81-170">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



