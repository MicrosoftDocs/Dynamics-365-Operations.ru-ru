---
title: "Синхронизация сведений уровня запасов из Finance and Operations в Field Service"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="239e7-103">Синхронизация сведений уровня запасов из Finance and Operations в Field Service</span><span class="sxs-lookup"><span data-stu-id="239e7-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="239e7-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="239e7-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="239e7-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="239e7-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="239e7-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="239e7-106">Templates and tasks</span></span>
<span data-ttu-id="239e7-107">Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации уровней доступных запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="239e7-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="239e7-108">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="239e7-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="239e7-109">Запасы продуктов (из Finance and Operations в Field Service)</span><span class="sxs-lookup"><span data-stu-id="239e7-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="239e7-110">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="239e7-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="239e7-111">Запасы продуктов</span><span class="sxs-lookup"><span data-stu-id="239e7-111">Product inventory</span></span>

<span data-ttu-id="239e7-112">Чтобы была возможна синхронизация уровней запасов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="239e7-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="239e7-113">Склады (из Finance and Operations в Field Service)</span><span class="sxs-lookup"><span data-stu-id="239e7-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="239e7-114">Продукты Field Service с единицей измерения складских запасов (из Finance and Operations в Sales)</span><span class="sxs-lookup"><span data-stu-id="239e7-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="239e7-115">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="239e7-115">Entity set</span></span>

| <span data-ttu-id="239e7-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="239e7-116">Field Service</span></span>                      | <span data-ttu-id="239e7-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="239e7-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="239e7-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="239e7-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="239e7-119">Запасы CDS в наличии по складам</span><span class="sxs-lookup"><span data-stu-id="239e7-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="239e7-120">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="239e7-120">Entity flow</span></span>
<span data-ttu-id="239e7-121">Сведения об уровне запасов из Finance and Operations отправляются в Field Service для выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="239e7-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="239e7-122">Сведения об уровне запасов включают:</span><span class="sxs-lookup"><span data-stu-id="239e7-122">The inventory level information include:</span></span> 
- <span data-ttu-id="239e7-123">Количество в наличии (текущее зарегистрированное физическое количество, находящееся на складе)</span><span class="sxs-lookup"><span data-stu-id="239e7-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="239e7-124">Количество по заказу (общее зарегистрированное количество по заказу — т. е., заказы на продажу)</span><span class="sxs-lookup"><span data-stu-id="239e7-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="239e7-125">Заказанное количество (общее зарегистрированное заказанное количество — т. е., заказы на покупку)</span><span class="sxs-lookup"><span data-stu-id="239e7-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="239e7-126">Эти сведения фиксируются по выпущенным продуктам для каждого склада и синхронизируются на основе отслеживания изменений при изменении уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="239e7-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="239e7-127">В Field Service решение интеграции создает журналы запасов для разницы, чтобы уровни в Field Service соответствовали уровням в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="239e7-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="239e7-128">Приложение Finance and Operations играет роль ведущего для уровней запасов.</span><span class="sxs-lookup"><span data-stu-id="239e7-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="239e7-129">Поэтому важно настроить интеграцию для рабочих заказы, перемещений и корректировок из Field Service в Finance and Operations, если эта функция используется в Field Service, вместе с синхронизацией уровней запасов из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="239e7-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="239e7-130">Продукты и склады, где уровни запасов поддерживаются из Finance and Operations, могут контролироваться с помощью расширенных запросов и фильтрация (Power Query).</span><span class="sxs-lookup"><span data-stu-id="239e7-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="239e7-131">Примечание. Можно создать несколько складов в Field Service (с настройкой "Управляется извне = Нет") и затем сопоставить их с одним складом в Finance and Operations с функцией расширенного запроса и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="239e7-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="239e7-132">Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и просто отправляло обновления в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="239e7-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="239e7-133">В этом случае Field Service не будет получать обновления уровней запасов из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="239e7-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="239e7-134">См. дополнительные сведения в разделах "Синхронизация корректировок запасов из Field Service в Finance and Operations" и "Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations".</span><span class="sxs-lookup"><span data-stu-id="239e7-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="239e7-135">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="239e7-135">Field Service CRM solution</span></span>
<span data-ttu-id="239e7-136">Сущность внешних запасов продукта — это новая сущность, которая используется только для обработки интеграции на сервере.</span><span class="sxs-lookup"><span data-stu-id="239e7-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="239e7-137">Она получает значения уровня складских запасов из Finance and Operations в интеграции, затем преобразует эти значения для журналов ручных запасов, которые затем изменяют складские продукты на складе.</span><span class="sxs-lookup"><span data-stu-id="239e7-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="239e7-138">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="239e7-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="239e7-139">В проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="239e7-139">In the Data Integration project</span></span>
<span data-ttu-id="239e7-140">Применяйте фильтры с расширенными запросами и фильтрацией для контроля, чтобы только требуемые продукты и склады отправляли информацию об уровне запасов из Finance and Operations в Field Service.</span><span class="sxs-lookup"><span data-stu-id="239e7-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="239e7-141">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="239e7-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="239e7-142">Запасы продуктов (из Finance and Operations в Field Service): Запасы продуктов</span><span class="sxs-lookup"><span data-stu-id="239e7-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="239e7-143">[![Сопоставление шаблона в интеграции данных](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="239e7-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

