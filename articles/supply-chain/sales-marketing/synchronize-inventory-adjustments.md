---
title: "Синхронизация перемещений и корректировок запасов из Field Service в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="b9a8a-103">Синхронизация корректировок запасов из Field Service в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b9a8a-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b9a8a-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b9a8a-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="b9a8a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b9a8a-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="b9a8a-106">Templates and tasks</span></span>
<span data-ttu-id="b9a8a-107">Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b9a8a-108">**Имя шаблонов в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="b9a8a-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="b9a8a-109">Корректировка запасов (из Field Service в Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b9a8a-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="b9a8a-110">Перемещение запасов (из Field Service в Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b9a8a-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="b9a8a-111">**Имена задач в проектах интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="b9a8a-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="b9a8a-112">Корректировки запасов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-112">Inventory Adjustments</span></span>
- <span data-ttu-id="b9a8a-113">Перемещение запасов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="b9a8a-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-114">Entity set</span></span>
| <span data-ttu-id="b9a8a-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="b9a8a-115">Field Service</span></span>                     | <span data-ttu-id="b9a8a-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b9a8a-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="b9a8a-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="b9a8a-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="b9a8a-118">Заголовки и строки журналов корректировки запасов CDS</span><span class="sxs-lookup"><span data-stu-id="b9a8a-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="b9a8a-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="b9a8a-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="b9a8a-120">Заголовки и строки журналов перемещения запасов CDS</span><span class="sxs-lookup"><span data-stu-id="b9a8a-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="b9a8a-121">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-121">Entity flow</span></span>
<span data-ttu-id="b9a8a-122">Корректировки и перемещения запасов, выполненные в приложении Field Service, синхронизируются с Finance and Operations, когда значение в поле **Состояние разноски** изменяется с "Создано" на "Разнесено".</span><span class="sxs-lookup"><span data-stu-id="b9a8a-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="b9a8a-123">Когда это происходит, заказ на корректировку или перемещение будет заблокирован и станет доступен только для чтения, так как корректировки и перемещения могут быть разнесены в Finance and Operations и, следовательно, не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="b9a8a-124">В Finance and Operations можно настроить пакетное задание для автоматической разноски журналов корректировок и перемещений запасов, созданных с интеграцией.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="b9a8a-125">Подробные сведения о том, как включить это пакетное задание, см. в предварительных условиях ниже.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b9a8a-126">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="b9a8a-126">Field Service CRM solution</span></span> 
<span data-ttu-id="b9a8a-127">Поле "Ед. изм. складского учета" было добавлено в сущность "Продукт".</span><span class="sxs-lookup"><span data-stu-id="b9a8a-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="b9a8a-128">Это поле требуется, так как единицы измерения продаж и складского учета не всегда совпадают в Operations, и для складских запасов в Operations требуется единица измерения складского учета.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="b9a8a-129">При установке продукта для продукта корректировки запасов для корректировки запасов и перемещения запасов единицы измерения извлекается из значения продукта запасов продуктов.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="b9a8a-130">Если значение найдено, поле единицы измерения будет заблокировано в продукте корректировки запасов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="b9a8a-131">Поле "Состояние разноски" было добавлено как в сущность корректировки запасов, так и в сущность перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="b9a8a-132">Это поле используется как фильтр при отправке корректировки или перемещения в приложение Operations.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="b9a8a-133">Поле по умолчанию принимает значение "Создано (1)", затем оно не отправляется в Operations.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="b9a8a-134">После изменения значения на "Разнесено (2)" оно отправляется в Operations, но вы больше не сможете изменить ничего в корректировках или перемещениях или добавить новые строки в нее.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="b9a8a-135">Поле номерной серии было добавлено в сущность продукта корректировки запасов.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="b9a8a-136">Это поле помогает интеграции иметь уникальный номер, чтобы интеграция знала, когда выполняется создание, а когда — обновление.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="b9a8a-137">При создании первого продукта корректировки запасов создается новая запись в сущности P2C AutoNumber для поддержания номерных серий и префикса, который используется.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b9a8a-138">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="b9a8a-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="b9a8a-139">В Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b9a8a-139">In Finance and Operations</span></span>
<span data-ttu-id="b9a8a-140">Журналы запасов интеграции, созданные при интеграции, могут быть автоматически разнесены с помощью пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="b9a8a-141">Эта функция включается из пункта: Управление запасами > Периодические задачи > Интеграция CDS > Разноска журналов запасов интеграции</span><span class="sxs-lookup"><span data-stu-id="b9a8a-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b9a8a-142">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="b9a8a-142">Template mapping in Data integration</span></span>

<span data-ttu-id="b9a8a-143">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b9a8a-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="b9a8a-144">Корректировка запасов (Field Service с Finance and Operations): Корректировка запасов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="b9a8a-145">[![Сопоставление шаблона в интеграции данных](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="b9a8a-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="b9a8a-146">Перемещение запасов (Field Service с Finance and Operations): Перемещение запасов</span><span class="sxs-lookup"><span data-stu-id="b9a8a-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="b9a8a-147">[![Сопоставление шаблона в интеграции данных](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="b9a8a-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

