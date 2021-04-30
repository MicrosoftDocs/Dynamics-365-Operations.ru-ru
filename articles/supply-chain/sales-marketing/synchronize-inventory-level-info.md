---
title: Синхронизация сведений об уровне запасов из Supply Chain Management с Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910288"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="774fc-103">Синхронизация сведений об уровне запасов из Supply Chain Management с Field Service</span><span class="sxs-lookup"><span data-stu-id="774fc-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="774fc-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="774fc-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="774fc-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="774fc-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="774fc-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="774fc-106">Templates and tasks</span></span>
<span data-ttu-id="774fc-107">Следующие шаблон и базовые задачи используются для синхронизации корректировок и перемещений наличных запасов из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="774fc-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="774fc-108">**Шаблон в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="774fc-108">**Template in Data integration**</span></span>
- <span data-ttu-id="774fc-109">Запасы продуктов (из Supply Chain Management в Field Service)</span><span class="sxs-lookup"><span data-stu-id="774fc-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="774fc-110">**Задача в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="774fc-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="774fc-111">Запасы продуктов</span><span class="sxs-lookup"><span data-stu-id="774fc-111">Product inventory</span></span>

<span data-ttu-id="774fc-112">Чтобы была возможна синхронизация уровней запасов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="774fc-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="774fc-113">Склады (из Supply Chain Management в Field Service)</span><span class="sxs-lookup"><span data-stu-id="774fc-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="774fc-114">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)</span><span class="sxs-lookup"><span data-stu-id="774fc-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="774fc-115">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="774fc-115">Entity set</span></span>

| <span data-ttu-id="774fc-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="774fc-116">Field Service</span></span>                      | <span data-ttu-id="774fc-117">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="774fc-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="774fc-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="774fc-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="774fc-119">Запасы Dataverse в наличии по складам</span><span class="sxs-lookup"><span data-stu-id="774fc-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="774fc-120">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="774fc-120">Entity flow</span></span>
<span data-ttu-id="774fc-121">Сведения об уровне запасов из Finance and Operations отправляются в Field Service для выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="774fc-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="774fc-122">Сведения об уровне запасов включают:</span><span class="sxs-lookup"><span data-stu-id="774fc-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="774fc-123">Количество в наличии (текущее зарегистрированное физическое количество, находящееся на складе)</span><span class="sxs-lookup"><span data-stu-id="774fc-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="774fc-124">Количество по заказу (общее зарегистрированное количество по заказу, например заказы на продажу)</span><span class="sxs-lookup"><span data-stu-id="774fc-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="774fc-125">Заказанное количество (общее зарегистрированное заказанное количество, например заказы на покупку)</span><span class="sxs-lookup"><span data-stu-id="774fc-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="774fc-126">Эти сведения фиксируются по выпущенным продуктам для каждого склада и синхронизируются на основе отслеживания изменений при изменении уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="774fc-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="774fc-127">В Field Service решение интеграции создает журналы запасов для разницы, чтобы уровни в Field Service соответствовали уровням в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="774fc-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="774fc-128">Приложение Supply Chain Management играет роль ведущего для уровней запасов.</span><span class="sxs-lookup"><span data-stu-id="774fc-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="774fc-129">Поэтому важно настроить интеграцию для заказов на выполнение работ, перемещений и корректировок из Field Service в Supply Chain Management, если эта функция используется в Field Service, вместе с синхронизацией уровней запасов из Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="774fc-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="774fc-130">Продукты и склады, где уровни запасов поддерживаются из Supply Chain Management, могут контролироваться с помощью расширенных запросов и фильтрация (Power Query).</span><span class="sxs-lookup"><span data-stu-id="774fc-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="774fc-131">Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне = Нет**) и затем сопоставить их с одним складом в Supply Chain Management с функцией расширенного запроса и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="774fc-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="774fc-132">Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и отправляло только обновления в приложение Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="774fc-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="774fc-133">В этом случае Field Service не будет получать обновления уровней запасов из Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="774fc-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="774fc-134">Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="774fc-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="774fc-135">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="774fc-135">Field Service CRM solution</span></span>
<span data-ttu-id="774fc-136">Сущность **Внешние запасы продукта** используется только для обработки интеграции на сервере.</span><span class="sxs-lookup"><span data-stu-id="774fc-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="774fc-137">Эта сущность получает значения уровня складских запасов из Supply Chain Management в интеграции, затем преобразует эти значения для журналов ручных запасов, которые затем изменяют складские продукты на складе.</span><span class="sxs-lookup"><span data-stu-id="774fc-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="774fc-138">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="774fc-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="774fc-139">Интеграция данных</span><span class="sxs-lookup"><span data-stu-id="774fc-139">Data integration</span></span>
<span data-ttu-id="774fc-140">Для работы проекта необходимо убедиться, что ключ интеграции был обновлен для msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="774fc-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="774fc-141">Выберите **Интеграция данных > Наборы подключений**.</span><span class="sxs-lookup"><span data-stu-id="774fc-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="774fc-142">Выберите использованный набор подключений.</span><span class="sxs-lookup"><span data-stu-id="774fc-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="774fc-143">На вкладке **Ключ интеграции** убедитесь, что следующие ключи добавлены в msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="774fc-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="774fc-144">msdynce_productnumber (номер продукта)</span><span class="sxs-lookup"><span data-stu-id="774fc-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="774fc-145">msdynce_warehouseid (код склада)</span><span class="sxs-lookup"><span data-stu-id="774fc-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="774fc-146">Проект интеграции данных</span><span class="sxs-lookup"><span data-stu-id="774fc-146">Data integration project</span></span>
<span data-ttu-id="774fc-147">Можно применить фильтры с расширенными запросами и фильтрацией, чтобы только определенные продукты и склады отправляли информацию об уровне запасов из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="774fc-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="774fc-148">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="774fc-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="774fc-149">Запасы продуктов (из Supply Chain Management в Field Service): запасы продуктов</span><span class="sxs-lookup"><span data-stu-id="774fc-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="774fc-150">[![Сопоставление шаблона в интеграции данных](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="774fc-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]