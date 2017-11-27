---
title: "Прямая синхронизация продуктов из Finance and Operations с продуктами в Sales"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, с Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="a1cdf-103">Прямая синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="a1cdf-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a1cdf-104">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="a1cdf-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="a1cdf-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для прямой синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, с Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="a1cdf-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="a1cdf-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="a1cdf-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="a1cdf-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="a1cdf-109">На следующем рисунке показано, как данные синхронизируются между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="a1cdf-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="a1cdf-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a1cdf-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="a1cdf-111">Templates and tasks</span></span>

<span data-ttu-id="a1cdf-112">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="a1cdf-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="a1cdf-113">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a1cdf-114">Следующий шаблон и базовые задачи используются для синхронизации продуктов Finance and Operations с Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="a1cdf-115">**Имя шаблона в интеграции данных:** "Продукты (из Fin and Ops в Sales) - напрямую"</span><span class="sxs-lookup"><span data-stu-id="a1cdf-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="a1cdf-116">**Имена задачи в проекте интеграции данных:** "Продукты"</span><span class="sxs-lookup"><span data-stu-id="a1cdf-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="a1cdf-117">Никакие задачи синхронизации не требуются до того, как можно будет выполнить синхронизацию продуктов.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a1cdf-118">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="a1cdf-118">Entity set</span></span>

| <span data-ttu-id="a1cdf-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a1cdf-119">Finance and Operations</span></span>     | <span data-ttu-id="a1cdf-120">Прод.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="a1cdf-121">Запущенные в производство продукты продажи</span><span class="sxs-lookup"><span data-stu-id="a1cdf-121">Sellable released products</span></span> | <span data-ttu-id="a1cdf-122">Товары</span><span class="sxs-lookup"><span data-stu-id="a1cdf-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="a1cdf-123">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="a1cdf-123">Entity flow</span></span>

<span data-ttu-id="a1cdf-124">Продукты управляются в Finance and Operations и синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="a1cdf-125">Информационный объект **Запущенные в производство продукты продажи** в Finance and Operations экспортирует только продукты, которые *могут продаваться*.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="a1cdf-126">Продукты, которые могут продаваться, — это продукты, имеющие информацию, необходимую для использования в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="a1cdf-127">Те же правила применяются при проверке продукта с помощью функции **Проверить** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="a1cdf-128">Номер продукта используется как ключ.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-128">The product number is used as a key.</span></span> <span data-ttu-id="a1cdf-129">Таким образом, при синхронизации вариантов продукта в Sales каждый вариант имеет отдельный код продукта.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a1cdf-130">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="a1cdf-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a1cdf-131">В Sales для продуктов добавлено новое поле **Управляется извне** для указания того, что данный продукт управляется извне.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="a1cdf-132">По умолчанию при импорте в Sales задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="a1cdf-133">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a1cdf-133">The following values are available:</span></span>

- <span data-ttu-id="a1cdf-134">**Да** — продукта поступил из Finance and Operations и не может быть изменен в Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="a1cdf-135">**Нет** — продукт был введен непосредственно в Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="a1cdf-136">**(Пусто)** — продукт существовали в Sales до включения решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="a1cdf-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="a1cdf-137">Поле **Управляется извне** помогает гарантировать, что предложения и заказы на продажу, имеющие управляемые извне продукты, будут синхронизироваться с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="a1cdf-138">Управляемые извне продукты автоматически добавляются к первому допустимому прайс-листу с той же валютой.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="a1cdf-139">Прайс-листы упорядочены в алфавитном порядке по имени.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="a1cdf-140">Цена продажи продукта из Finance and Operations используется как цена в прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="a1cdf-141">Таким образом, должен быть прайс-лист в Sales для каждой валюты продажи продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="a1cdf-142">Валюта в запущенных в производство продуктах продажи задана как валюта учета в юридическом лице, из которого экспортируется продукт.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="a1cdf-143">Продукт не будет успешно синхронизирован при отсутствии прайс-листа в соответствующей валюте.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a1cdf-144">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="a1cdf-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="a1cdf-145">Перед первым выполнением синхронизации необходимо заполнить таблицу уникально идентифицируемого продукта для существующих продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="a1cdf-146">Существующие продукты не будут синхронизированы, пока не будет выполнено это задание.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="a1cdf-147">В Finance and Operations используйте поиск для поиска команды **Заполнить таблицу уникально идентифицируемых продуктов**.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="a1cdf-148">Выберите **Заполнить таблицу уникально идентифицируемых продуктов** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="a1cdf-149">Это задание должно запускаться только один раз.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-149">This job must be run only one time.</span></span>

- <span data-ttu-id="a1cdf-150">Убедитесь, что требуемое соответствие значений для единицы измерения продажи между Finance and Operations и Sales существует в сопоставлении **SalesUnitSymbol** с **DefaultUnit (Имя)**.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="a1cdf-151">Обновите сопоставление значений для параметра **Группа единиц** (**defaultuomscheduleid.name**), чтобы оно соответствовало параметру **Группы единиц** в Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="a1cdf-152">Значение шаблона по умолчанию — **Единица измерения по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="a1cdf-153">Убедитесь, что единицы измерения при продаже для всех продуктов в Finance and Operations существуют в Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="a1cdf-154">Убедитесь, что прайс-листы существуют Sales для каждой валюты продажи продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="a1cdf-155">При создании продуктов в Sales они могут иметь статус **Черновик** или **Активный**.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="a1cdf-156">Поведение контролируется параметром **Параметры** > **Администрирование** > **Настройки системы** > **Продажи** в Sales.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="a1cdf-157">Продукты, которые при создании имеют статус **Черновик**, должны быть активированы, прежде чем они могут быть добавлены в предложения или заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a1cdf-158">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="a1cdf-158">Template mapping in Data integration</span></span>

<span data-ttu-id="a1cdf-159">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a1cdf-160">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a1cdf-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Сопоставление шаблона в интеграторе данных](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="a1cdf-162">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a1cdf-162">Related topics</span></span>

[<span data-ttu-id="a1cdf-163">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="a1cdf-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="a1cdf-164">Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a1cdf-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="a1cdf-165">Синхронизация контактов непосредственно из Sales с контактами и клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a1cdf-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="a1cdf-166">Синхронизация заголовков и строк заказов на продажу непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="a1cdf-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="a1cdf-167">Синхронизация заголовков и строк счетов продажи непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="a1cdf-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




