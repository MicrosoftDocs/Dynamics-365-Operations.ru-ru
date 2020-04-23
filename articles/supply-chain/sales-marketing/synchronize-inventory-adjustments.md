---
title: Синхронизация перемещений и корректировок запасов Field Service с Supply Chain Management
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204432"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="fce11-103">Синхронизация перемещений и корректировок запасов Field Service с Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fce11-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fce11-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="fce11-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="fce11-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="fce11-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fce11-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="fce11-106">Templates and tasks</span></span>
<span data-ttu-id="fce11-107">Следующие шаблон и базовые задачи используются для синхронизации корректировок и перемещений запасов из Field Service в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fce11-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="fce11-108">**Шаблоны в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="fce11-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="fce11-109">Корректировка запасов (из Field Service в Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="fce11-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="fce11-110">Перемещение запасов (из Field Service в Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="fce11-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="fce11-111">**Задачи в проектах интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="fce11-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="fce11-112">Корректировки запасов</span><span class="sxs-lookup"><span data-stu-id="fce11-112">Inventory Adjustments</span></span>
- <span data-ttu-id="fce11-113">Перемещение запасов</span><span class="sxs-lookup"><span data-stu-id="fce11-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="fce11-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="fce11-114">Entity set</span></span>
| <span data-ttu-id="fce11-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="fce11-115">Field Service</span></span>                     | <span data-ttu-id="fce11-116">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="fce11-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="fce11-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="fce11-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="fce11-118">Заголовки и строки журналов корректировки запасов CDS</span><span class="sxs-lookup"><span data-stu-id="fce11-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="fce11-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="fce11-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="fce11-120">Заголовки и строки журналов перемещения запасов CDS</span><span class="sxs-lookup"><span data-stu-id="fce11-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="fce11-121">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="fce11-121">Entity flow</span></span>
<span data-ttu-id="fce11-122">Корректировки и перемещения запасов, выполненные в приложении Field Service, синхронизируются с Supply Chain Management после изменения значения в поле **Состояние разноски** изменяется с **Создано** на **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="fce11-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="fce11-123">В этом случае заказ на корректировку или перемещение будет заблокирован и становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fce11-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="fce11-124">Это означает, что корректировки и переносы можно разносить в Supply Chain Management, но не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="fce11-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="fce11-125">В Supply Chain Management можно настроить пакетное задание для автоматической разноски журналов корректировок и перемещений запасов, которые были созданы во время интеграции.</span><span class="sxs-lookup"><span data-stu-id="fce11-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="fce11-126">Подробные сведения о том, как включить это пакетное задание, см. в следующих предварительных условиях.</span><span class="sxs-lookup"><span data-stu-id="fce11-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="fce11-127">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="fce11-127">Field Service CRM solution</span></span> 
<span data-ttu-id="fce11-128">Поле **Ед. изм. складского учета** было добавлено в сущность **Продукт**.</span><span class="sxs-lookup"><span data-stu-id="fce11-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="fce11-129">Это поле требуется, так как единицы измерения продаж и складского учета не всегда совпадают в Supply Chain Management, и единица измерения складского учета требуется для складских запасов в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fce11-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="fce11-130">При установке продукта для продукта корректировки запасов для корректировки запасов и перемещения запасов единицы измерения извлекается из значения продукта запасов продуктов.</span><span class="sxs-lookup"><span data-stu-id="fce11-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="fce11-131">Если значение найдено, поле **Единица измерения** будет заблокировано в продукте корректировки запасов.</span><span class="sxs-lookup"><span data-stu-id="fce11-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="fce11-132">Поле **Состояние разноски** было добавлено как в сущность **Корректировка запасов**, так и в сущность **Перемещение запасов**.</span><span class="sxs-lookup"><span data-stu-id="fce11-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="fce11-133">Это поле используется как фильтр при отправке корректировки или перемещения в приложение Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fce11-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="fce11-134">По умолчанию для этого поля задано значение "Создано (1)", однако оно не передается в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fce11-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="fce11-135">После обновления значения на "Разнесено (2)", оно отправляется в Supply Chain Management, но после этого вы больше не сможете изменить корректировку или перемещение или добавить новые строки.</span><span class="sxs-lookup"><span data-stu-id="fce11-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="fce11-136">Поле **Номерная серия** было добавлено в сущность **Продукт корректировки запасов**.</span><span class="sxs-lookup"><span data-stu-id="fce11-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="fce11-137">Это поле гарантирует, что интеграция имеет уникальный номер, поэтому интеграция может создавать и обновлять корректировку.</span><span class="sxs-lookup"><span data-stu-id="fce11-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="fce11-138">При создании первого продукта корректировки запасов создается новая запись в сущности **P2C AutoNumber** для поддержания номерных серий и префикса, который используется.</span><span class="sxs-lookup"><span data-stu-id="fce11-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="fce11-139">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="fce11-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="fce11-140">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="fce11-140">Supply Chain Management</span></span>
<span data-ttu-id="fce11-141">Журналы запасов интеграции, созданные при интеграции, могут быть автоматически разнесены с использованием пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="fce11-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="fce11-142">Эта функция включается из пункта **Управление запасами > Периодические задачи > Интеграция CDS > Разноска журналов запасов интеграции**.</span><span class="sxs-lookup"><span data-stu-id="fce11-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fce11-143">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="fce11-143">Template mapping in Data integration</span></span>

<span data-ttu-id="fce11-144">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="fce11-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="fce11-145">Корректировка запасов (из Field Service в Supply Chain Management): корректировка запасов</span><span class="sxs-lookup"><span data-stu-id="fce11-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="fce11-146">[![Сопоставление шаблона в интеграции данных](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="fce11-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="fce11-147">Перемещение запасов (из Field Service в Supply Chain Management): перемещение запасов</span><span class="sxs-lookup"><span data-stu-id="fce11-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="fce11-148">[![Сопоставление шаблона в интеграции данных](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="fce11-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
