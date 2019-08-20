---
title: Синхронизация сведений уровня запасов из Finance and Operations в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6b56eb545f87c31ef30d6a897f48539068583486
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843441"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="68b2a-103">Синхронизация сведений об уровне запасов Finance and Operations с Field Service</span><span class="sxs-lookup"><span data-stu-id="68b2a-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68b2a-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="68b2a-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="68b2a-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="68b2a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="68b2a-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="68b2a-106">Templates and tasks</span></span>
<span data-ttu-id="68b2a-107">Следующие шаблон и базовые задачи используются для синхронизации корректировок и перемещений наличных запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="68b2a-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="68b2a-108">**Шаблон в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="68b2a-108">**Template in Data integration**</span></span>
- <span data-ttu-id="68b2a-109">Запасы продуктов (из Fin and Ops в Field Service)</span><span class="sxs-lookup"><span data-stu-id="68b2a-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="68b2a-110">**Задача в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="68b2a-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="68b2a-111">Запасы продуктов</span><span class="sxs-lookup"><span data-stu-id="68b2a-111">Product inventory</span></span>

<span data-ttu-id="68b2a-112">Чтобы была возможна синхронизация уровней запасов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="68b2a-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="68b2a-113">Склады (из Fin and Ops в Field Service)</span><span class="sxs-lookup"><span data-stu-id="68b2a-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="68b2a-114">Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="68b2a-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="68b2a-115">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="68b2a-115">Entity set</span></span>

| <span data-ttu-id="68b2a-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="68b2a-116">Field Service</span></span>                      | <span data-ttu-id="68b2a-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68b2a-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="68b2a-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="68b2a-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="68b2a-119">Запасы CDS в наличии по складам</span><span class="sxs-lookup"><span data-stu-id="68b2a-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="68b2a-120">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="68b2a-120">Entity flow</span></span>
<span data-ttu-id="68b2a-121">Сведения об уровне запасов из Finance and Operations отправляются в Field Service для выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="68b2a-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="68b2a-122">Сведения об уровне запасов включают:</span><span class="sxs-lookup"><span data-stu-id="68b2a-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="68b2a-123">Количество в наличии (текущее зарегистрированное физическое количество, находящееся на складе)</span><span class="sxs-lookup"><span data-stu-id="68b2a-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="68b2a-124">Количество по заказу (общее зарегистрированное количество по заказу, например заказы на продажу)</span><span class="sxs-lookup"><span data-stu-id="68b2a-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="68b2a-125">Заказанное количество (общее зарегистрированное заказанное количество, например заказы на покупку)</span><span class="sxs-lookup"><span data-stu-id="68b2a-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="68b2a-126">Эти сведения фиксируются по выпущенным продуктам для каждого склада и синхронизируются на основе отслеживания изменений при изменении уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="68b2a-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="68b2a-127">В Field Service решение интеграции создает журналы запасов для разницы, чтобы уровни в Field Service соответствовали уровням в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68b2a-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="68b2a-128">Приложение Finance and Operations играет роль ведущего для уровней запасов.</span><span class="sxs-lookup"><span data-stu-id="68b2a-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="68b2a-129">Поэтому важно настроить интеграцию для заказов на выполнение работ, перемещений и корректировок из Field Service в Finance and Operations, если эта функция используется в Field Service, вместе с синхронизацией уровней запасов из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68b2a-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="68b2a-130">Продукты и склады, где уровни запасов поддерживаются из Finance and Operations, могут контролироваться с помощью расширенных запросов и фильтрация (Power Query).</span><span class="sxs-lookup"><span data-stu-id="68b2a-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="68b2a-131">Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне = Нет**) и затем сопоставить их с одним складом в Finance and Operations с функцией расширенного запроса и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="68b2a-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="68b2a-132">Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и отправляло только обновления в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68b2a-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="68b2a-133">В этом случае Field Service не будет получать обновления уровней запасов из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68b2a-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="68b2a-134">Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="68b2a-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="68b2a-135">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="68b2a-135">Field Service CRM solution</span></span>
<span data-ttu-id="68b2a-136">Сущность **Внешние запасы продукта** используется только для обработки интеграции на сервере.</span><span class="sxs-lookup"><span data-stu-id="68b2a-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="68b2a-137">Эта сущность получает значения уровня складских запасов из Finance and Operations в интеграции, затем преобразует эти значения для журналов ручных запасов, которые затем изменяют складские продукты на складе.</span><span class="sxs-lookup"><span data-stu-id="68b2a-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="68b2a-138">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="68b2a-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="68b2a-139">Интеграция данных</span><span class="sxs-lookup"><span data-stu-id="68b2a-139">Data integration</span></span>
<span data-ttu-id="68b2a-140">Для работы проекта необходимо убедиться, что ключ интеграции был обновлен для msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="68b2a-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="68b2a-141">Выберите **Интеграция данных > Наборы подключений**.</span><span class="sxs-lookup"><span data-stu-id="68b2a-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="68b2a-142">Выберите использованный набор подключений.</span><span class="sxs-lookup"><span data-stu-id="68b2a-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="68b2a-143">На вкладке **Ключ интеграции** убедитесь, что следующие ключи добавлены в msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="68b2a-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="68b2a-144">msdynce_productnumber (номер продукта)</span><span class="sxs-lookup"><span data-stu-id="68b2a-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="68b2a-145">msdynce_warehouseid (код склада)</span><span class="sxs-lookup"><span data-stu-id="68b2a-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="68b2a-146">Проект интеграции данных</span><span class="sxs-lookup"><span data-stu-id="68b2a-146">Data integration project</span></span>
<span data-ttu-id="68b2a-147">Можно применить фильтры с расширенными запросами и фильтрацией, чтобы только определенные продукты и склады отправляли информацию об уровне запасов из Finance and Operations в Field Service.</span><span class="sxs-lookup"><span data-stu-id="68b2a-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="68b2a-148">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="68b2a-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="68b2a-149">Запасы продуктов (из Fin and Ops в Field Service): Запасы продуктов</span><span class="sxs-lookup"><span data-stu-id="68b2a-149">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="68b2a-150">[![Сопоставление шаблона в интеграции данных](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="68b2a-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
