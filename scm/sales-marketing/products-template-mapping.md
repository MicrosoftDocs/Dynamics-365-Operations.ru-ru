---
title: "Синхронизация продуктов из Finance and Operations с продуктами в Sales"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise, с Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="bc72d-103">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="bc72d-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="bc72d-104">Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="bc72d-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="bc72d-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise, с Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="bc72d-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="bc72d-106">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="bc72d-106">Template and task</span></span>

<span data-ttu-id="bc72d-107">Следующие шаблоны и базовые задачи используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise, (Finance and Operations) с Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="bc72d-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="bc72d-108">Имя шаблона: продукты (Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="bc72d-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="bc72d-109">Имя задачи в проекте: продукты</span><span class="sxs-lookup"><span data-stu-id="bc72d-109">Name of task in project: Products</span></span>

<span data-ttu-id="bc72d-110">Синхронизацию задач требуется выполнить до синхронизации продуктов: нет</span><span class="sxs-lookup"><span data-stu-id="bc72d-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="bc72d-111">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="bc72d-111">Entity set</span></span>

| <span data-ttu-id="bc72d-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="bc72d-112">**Finance and Operations**</span></span> | <span data-ttu-id="bc72d-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="bc72d-113">**CDS**</span></span> | <span data-ttu-id="bc72d-114">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="bc72d-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="bc72d-115">Запущенные в производство продукты продажи</span><span class="sxs-lookup"><span data-stu-id="bc72d-115">Sellable released products</span></span> | <span data-ttu-id="bc72d-116">Продукт</span><span class="sxs-lookup"><span data-stu-id="bc72d-116">Product</span></span> | <span data-ttu-id="bc72d-117">Товары</span><span class="sxs-lookup"><span data-stu-id="bc72d-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="bc72d-118">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="bc72d-118">Entity flow</span></span>

<span data-ttu-id="bc72d-119">Продукты управляются в Finance and Operations и синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="bc72d-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="bc72d-120">Информационный объект **Запущенные в производство продукты продажи** в Finance and Operations экспортирует только продукты, доступные для продажи, что означает, что продукты имеют сведения, необходимые для использования в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="bc72d-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="bc72d-121">Те же правила применяются при проверке продукта с помощью функции **Проверить** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="bc72d-122">**Номер продукта** используется в качестве ключа, то есть варианты продукта синхронизируются с CDS и Sales с индивидуальным значением **Коды продуктов** на **Вариант продукта**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="bc72d-123">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="bc72d-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="bc72d-124">В Sales добавлено новое поле **Управляется извне** в продуктах для указания того, что данный продукт управляется извне.</span><span class="sxs-lookup"><span data-stu-id="bc72d-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="bc72d-125">По умолчанию при импорте с Sales задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="bc72d-126">**Управляется извне = Да**: продукт поступает из Finance and Operations и будет недоступен для редактирования в Sales.</span><span class="sxs-lookup"><span data-stu-id="bc72d-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="bc72d-127">**Управляется извне = Нет**: продукт вводится непосредственно в Sales.</span><span class="sxs-lookup"><span data-stu-id="bc72d-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="bc72d-128">**Управляется извне = пусто**: продукт существует в Sales до включения решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="bc72d-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="bc72d-129">Информация **Управляется извне** используется, чтобы убедиться, что только **Предложения** и **Заказы на продажу**, имеющие **Управляемые извне продукты**, будут синхронизироваться с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bc72d-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="bc72d-130">**Управляемые извне продукты** автоматически добавляются к первому допустимому списку **Прайс-лист** с той же валютой.</span><span class="sxs-lookup"><span data-stu-id="bc72d-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="bc72d-131">Обратите внимание, что список упорядочен по значению **Имя** в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="bc72d-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="bc72d-132">Цена продажи продукта из Finance and Operations используется как цена в списке **Прайс-лист**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="bc72d-133">Это означает, что он должен иметь **Прайс-лист** в Sales для каждого параметра **Валюта продаж продукта** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bc72d-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="bc72d-134">Валюта в запущенных в производство продуктах продажи задана как валюта учета в юридическом лице, из которого экспортируется продукт.</span><span class="sxs-lookup"><span data-stu-id="bc72d-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="bc72d-135">Синхронизация продуктов не будет выполнена без списка **Прайс-лист** в соответствующей валюте.</span><span class="sxs-lookup"><span data-stu-id="bc72d-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="bc72d-136">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="bc72d-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="bc72d-137">Перед выполнением самой первой синхронизации необходимо заполнить таблицу **Уникально идентифицируемый продукт** для существующих продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bc72d-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="bc72d-138">Существующие продукты не будут синхронизированы, пока не будет выполнено это задание.</span><span class="sxs-lookup"><span data-stu-id="bc72d-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="bc72d-139">В Finance and Operations используйте поиск для поиска команды **Заполнить таблицу уникально идентифицируемых продуктов**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="bc72d-140">Щелкните **Заполнить таблицу уникально идентифицируемых продуктов** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="bc72d-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="bc72d-141">Это задание следует выполнить только один раз.</span><span class="sxs-lookup"><span data-stu-id="bc72d-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="bc72d-142">Убедитесь, что нужное значение **ValueMap** для параметра **Единица измерения** продаже в Finance and Operations существует в **Источник -\> SalesUnitSymbol сопоставления CDS / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="bc72d-143">Убедитесь, что **Число знаков после запятой** для единицы измерения соответствует требованиям в **CDS -\> Назначение**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="bc72d-144">Если требуются другие значения на единицу измерения, это можно сделать с помощью **ValueMap** из единицы измерения, например [Each : 0] & [Pound : 2].</span><span class="sxs-lookup"><span data-stu-id="bc72d-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="bc72d-145">Значение шаблона по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="bc72d-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="bc72d-146">Обновите код организации CDS **Organization_OrganizationId** в **Источник -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="bc72d-147">Значение шаблона по умолчанию — ORG001.</span><span class="sxs-lookup"><span data-stu-id="bc72d-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="bc72d-148">Обновите **ValueMap** для параметра **Группа единиц** (**defaultuomscheduleid.name**) в **CDS -\> Назначение** для соответствия параметру **Группы единиц** в Sales.</span><span class="sxs-lookup"><span data-stu-id="bc72d-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="bc72d-149">Значение шаблона по умолчанию — **Единица измерения по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="bc72d-150">Убедитесь, что все единицы измерения продажи продуктов в Finance and Operations существуют в Sales со значением **Листы подбора CDS**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="bc72d-151">Убедитесь, что **Прайс-листы** существуют Sales для каждой валюты продажи продуктов в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bc72d-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="bc72d-152">Продукты можно создавать в Sales со статусом **Черновик** или **Активно**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="bc72d-153">Этот процесс настраивается в подразделе **Параметры системы** раздела **Продажи** в Sales.</span><span class="sxs-lookup"><span data-stu-id="bc72d-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="bc72d-154">Продукты, созданные со статусом черновик, должны быть активированы, прежде чем их можно будет добавить в **Предложение** или **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="bc72d-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="bc72d-155">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="bc72d-155">Template mapping in data integrator</span></span>

<span data-ttu-id="bc72d-156">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="bc72d-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![сопоставление шаблона в интеграторе данных](./media/products-template-mapping-data-integrator-1.png)

![сопоставление шаблона для продуктов в интеграторе данных](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="bc72d-159">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="bc72d-159">Related topics</span></span>

[<span data-ttu-id="bc72d-160">Синхронизация контактов из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bc72d-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="bc72d-161">Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bc72d-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="bc72d-162">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bc72d-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


