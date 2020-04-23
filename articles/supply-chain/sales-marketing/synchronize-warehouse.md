---
title: Синхронизация складов из Supply Chain Management в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации складов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
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
ms.openlocfilehash: 6617b258a85a8f45b89a38f86919b44edc2100da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215892"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="0c9ba-103">Синхронизация складов из Supply Chain Management в Field Service</span><span class="sxs-lookup"><span data-stu-id="0c9ba-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0c9ba-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации складов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="0c9ba-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="0c9ba-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0c9ba-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="0c9ba-106">Templates and tasks</span></span>
<span data-ttu-id="0c9ba-107">Следующий шаблон и базовые задачи используются для выполнения синхронизации складов из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="0c9ba-108">**Шаблон в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="0c9ba-108">**Template in Data integration**</span></span>
- <span data-ttu-id="0c9ba-109">Склады (из Supply Chain Management в Field Service)</span><span class="sxs-lookup"><span data-stu-id="0c9ba-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="0c9ba-110">**Задача в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="0c9ba-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="0c9ba-111">Склад</span><span class="sxs-lookup"><span data-stu-id="0c9ba-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="0c9ba-112">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="0c9ba-112">Entity set</span></span>
| <span data-ttu-id="0c9ba-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="0c9ba-113">Field Service</span></span>    | <span data-ttu-id="0c9ba-114">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="0c9ba-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="0c9ba-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="0c9ba-115">msdyn_warehouses</span></span> | <span data-ttu-id="0c9ba-116">Склады</span><span class="sxs-lookup"><span data-stu-id="0c9ba-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="0c9ba-117">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="0c9ba-117">Entity flow</span></span>
<span data-ttu-id="0c9ba-118">Склады, которые создаются и поддерживаются в Supply Chain Management, можно синхронизировать с Field Service через проект интеграции данных службы Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="0c9ba-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="0c9ba-119">Склады, которые требуется синхронизировать с Field Service, можно контролировать с помощью расширенных запросов и фильтрации по проекту.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="0c9ba-120">Склады, которые синхронизируются из Supply Chain Management, создаются в Field Service с полем **Поддерживается извне** со значением **Да**, и запись становится записью только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="0c9ba-121">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="0c9ba-121">Field Service CRM solution</span></span>
<span data-ttu-id="0c9ba-122">Для поддержки интеграции между Field Service и Supply Chain Management требуется дополнительная функциональная возможность решения Field Service CRM.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="0c9ba-123">В решении поле **Поддерживается извне** было добавлено в объект **Склад (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="0c9ba-124">Это поле помогает определить, обрабатывается ли склад из Supply Chain Management, или он существует только в Field Service.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="0c9ba-125">Для этого поля предусмотрены следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0c9ba-125">The settings for this field include:</span></span>
- <span data-ttu-id="0c9ba-126">**Да** — склад поступил из Supply Chain Management и не может быть изменен в Sales.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="0c9ba-127">**Нет** — склад был введен непосредственно в Field Service и поддерживается здесь.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="0c9ba-128">Поле **Поддерживается извне** помогает контролировать синхронизацию уровней запасов, корректировки, передачи и использования в заказах на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="0c9ba-129">Только склады, для которых параметр **Поддерживается извне** имеет значение **Да**, может использоваться для синхронизации непосредственно с тем же складом в другой системе.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="0c9ba-130">Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне** = "Нет") и затем сопоставить их с одним складом с функцией расширенного запроса и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="0c9ba-131">Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и отправляло только обновления в приложение Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="0c9ba-132">В этом случае Field Service не будет получать обновления уровней запасов из Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="0c9ba-133">Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="0c9ba-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="0c9ba-134">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="0c9ba-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="0c9ba-135">Проект интеграции данных</span><span class="sxs-lookup"><span data-stu-id="0c9ba-135">Data Integration project</span></span>
<span data-ttu-id="0c9ba-136">Перед синхронизацией складов обязательно обновите расширенный запрос и фильтрацию в проекте, чтобы она включала только склады, которые необходимо внести из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="0c9ba-137">Обратите внимание, что понадобится склад в Field Service, чтобы применять его в заказах на выполнение работ, корректировках и перемещениях.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="0c9ba-138">Чтобы убедиться, что значение **Ключ интеграции** существует для **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="0c9ba-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="0c9ba-139">Перейдите в раздел "Интеграция данных".</span><span class="sxs-lookup"><span data-stu-id="0c9ba-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="0c9ba-140">Перейдите на вкладку **Набор подключений**.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="0c9ba-141">Выберите набор подключений, используемый для синхронизации заказа на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="0c9ba-142">Перейдите на вкладку **Ключ интеграции**.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="0c9ba-143">Найдите msdyn_warehouses и проверьте, что добавлен ключ **msdyn_name (имя)**.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="0c9ba-144">Если ключ не отображается, добавьте его, щелкнув команду **Добавить ключ**, затем нажмите кнопку **Сохранить** вверху страницы.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0c9ba-145">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="0c9ba-145">Template mapping in Data integration</span></span>

<span data-ttu-id="0c9ba-146">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="0c9ba-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="0c9ba-147">Склады (из Supply Chain Management в Field Service): Склад</span><span class="sxs-lookup"><span data-stu-id="0c9ba-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="0c9ba-148">[![Сопоставление шаблона в интеграции данных](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="0c9ba-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
