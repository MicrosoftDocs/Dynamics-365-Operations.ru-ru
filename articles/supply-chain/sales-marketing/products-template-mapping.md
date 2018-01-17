---
title: "Синхронизация продуктов из Finance and Operations с продуктами в Sales"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, с Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b949701604d0cbca2728a0055d52f7385106082b
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="0a386-103">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="0a386-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0a386-104">Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="0a386-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="0a386-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, с Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="0a386-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="0a386-106">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="0a386-106">Template and task</span></span>

<span data-ttu-id="0a386-107">Следующие шаблоны и базовые задачи используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, (Finance and Operations) с Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="0a386-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="0a386-108">Имя шаблона: продукты (Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="0a386-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="0a386-109">Имя задачи в проекте: продукты</span><span class="sxs-lookup"><span data-stu-id="0a386-109">Name of task in project: Products</span></span>

<span data-ttu-id="0a386-110">Синхронизацию задач требуется выполнить до синхронизации продуктов: нет</span><span class="sxs-lookup"><span data-stu-id="0a386-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="0a386-111">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="0a386-111">Entity set</span></span>

| <span data-ttu-id="0a386-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="0a386-112">**Finance and Operations**</span></span> | <span data-ttu-id="0a386-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="0a386-113">**CDS**</span></span> | <span data-ttu-id="0a386-114">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="0a386-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="0a386-115">Запущенные в производство продукты продажи</span><span class="sxs-lookup"><span data-stu-id="0a386-115">Sellable released products</span></span> | <span data-ttu-id="0a386-116">Продукт</span><span class="sxs-lookup"><span data-stu-id="0a386-116">Product</span></span> | <span data-ttu-id="0a386-117">Товары</span><span class="sxs-lookup"><span data-stu-id="0a386-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="0a386-118">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="0a386-118">Entity flow</span></span>

<span data-ttu-id="0a386-119">Продукты управляются в Finance and Operations и синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="0a386-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="0a386-120">Информационный объект **Запущенные в производство продукты продажи** в Finance and Operations экспортирует только продукты, доступные для продажи, что означает, что продукты имеют сведения, необходимые для использования в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="0a386-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="0a386-121">Те же правила применяются при проверке продукта с помощью функции **Проверить** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="0a386-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="0a386-122">**Номер продукта** используется в качестве ключа, то есть варианты продукта синхронизируются с CDS и Sales с индивидуальным значением **Коды продуктов** на **Вариант продукта**.</span><span class="sxs-lookup"><span data-stu-id="0a386-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0a386-123">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="0a386-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="0a386-124">В Sales добавлено новое поле **Управляется извне** в продуктах для указания того, что данный продукт управляется извне.</span><span class="sxs-lookup"><span data-stu-id="0a386-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="0a386-125">По умолчанию при импорте с Sales задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="0a386-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="0a386-126">**Управляется извне = Да**: продукт поступает из Finance and Operations и будет недоступен для редактирования в Sales.</span><span class="sxs-lookup"><span data-stu-id="0a386-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="0a386-127">**Управляется извне = Нет**: продукт вводится непосредственно в Sales.</span><span class="sxs-lookup"><span data-stu-id="0a386-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="0a386-128">**Управляется извне = пусто**: продукт существует в Sales до включения решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="0a386-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="0a386-129">Информация **Управляется извне** используется, чтобы убедиться, что только **Предложения** и **Заказы на продажу**, имеющие **Управляемые извне продукты**, будут синхронизироваться с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a386-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="0a386-130">**Управляемые извне продукты** автоматически добавляются к первому допустимому списку **Прайс-лист** с той же валютой.</span><span class="sxs-lookup"><span data-stu-id="0a386-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="0a386-131">Обратите внимание, что список упорядочен по значению **Имя** в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="0a386-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="0a386-132">Цена продажи продукта из Finance and Operations используется как цена в списке **Прайс-лист**.</span><span class="sxs-lookup"><span data-stu-id="0a386-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="0a386-133">Это означает, что он должен иметь **Прайс-лист** в Sales для каждого параметра **Валюта продаж продукта** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a386-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="0a386-134">Валюта в запущенных в производство продуктах продажи задана как валюта учета в юридическом лице, из которого экспортируется продукт.</span><span class="sxs-lookup"><span data-stu-id="0a386-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="0a386-135">Синхронизация продуктов не будет выполнена без списка **Прайс-лист** в соответствующей валюте.</span><span class="sxs-lookup"><span data-stu-id="0a386-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0a386-136">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="0a386-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="0a386-137">Перед выполнением самой первой синхронизации необходимо заполнить таблицу **Уникально идентифицируемый продукт** для существующих продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a386-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="0a386-138">Существующие продукты не будут синхронизированы, пока не будет выполнено это задание.</span><span class="sxs-lookup"><span data-stu-id="0a386-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="0a386-139">В Finance and Operations используйте поиск для поиска команды **Заполнить таблицу уникально идентифицируемых продуктов**.</span><span class="sxs-lookup"><span data-stu-id="0a386-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="0a386-140">Щелкните **Заполнить таблицу уникально идентифицируемых продуктов** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="0a386-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="0a386-141">Это задание следует выполнить только один раз.</span><span class="sxs-lookup"><span data-stu-id="0a386-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="0a386-142">Убедитесь, что нужное значение **ValueMap** для параметра **Единица измерения** продаже в Finance and Operations существует в **Источник -\> SalesUnitSymbol сопоставления CDS / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="0a386-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="0a386-143">Обновите код организации CDS **Organization_OrganizationId** в **Источник -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="0a386-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="0a386-144">Значение шаблона по умолчанию — ORG001.</span><span class="sxs-lookup"><span data-stu-id="0a386-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="0a386-145">Обновите **ValueMap** для параметра **Группа единиц** (**defaultuomscheduleid.name**) в **CDS -\> Назначение** для соответствия параметру **Группы единиц** в Sales.</span><span class="sxs-lookup"><span data-stu-id="0a386-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="0a386-146">Значение шаблона по умолчанию — **Единица измерения по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="0a386-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="0a386-147">Убедитесь, что все единицы измерения продажи продуктов в Finance and Operations существуют в Sales со значением **Листы подбора CDS**.</span><span class="sxs-lookup"><span data-stu-id="0a386-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="0a386-148">Убедитесь, что **Прайс-листы** существуют Sales для каждой валюты продажи продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a386-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="0a386-149">Продукты можно создавать в Sales со статусом **Черновик** или **Активно**.</span><span class="sxs-lookup"><span data-stu-id="0a386-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="0a386-150">Этот процесс настраивается в подразделе **Параметры системы** раздела **Продажи** в Sales.</span><span class="sxs-lookup"><span data-stu-id="0a386-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="0a386-151">Продукты, созданные со статусом черновик, должны быть активированы, прежде чем их можно будет добавить в **Предложение** или **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0a386-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0a386-152">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="0a386-152">Template mapping in data integrator</span></span>

<span data-ttu-id="0a386-153">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="0a386-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![сопоставление шаблона в интеграторе данных](./media/products-template-mapping-data-integrator-1.png)

![сопоставление шаблона для продуктов в интеграторе данных](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="0a386-156">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="0a386-156">Related topics</span></span>

[<span data-ttu-id="0a386-157">Синхронизация контактов из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a386-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0a386-158">Синхронизация контактов из Finance and Operations с контактами в Sales</span><span class="sxs-lookup"><span data-stu-id="0a386-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="0a386-159">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a386-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="0a386-160">Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="0a386-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="0a386-161">Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="0a386-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


