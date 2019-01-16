---
title: "Синхронизация складов из Finance and Operations в Field Service"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации складов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e91ba-103">Синхронизация складов из Finance and Operations в Field Service</span><span class="sxs-lookup"><span data-stu-id="e91ba-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e91ba-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации складов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e91ba-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e91ba-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="e91ba-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e91ba-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="e91ba-106">Templates and tasks</span></span>
<span data-ttu-id="e91ba-107">Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации складов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e91ba-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e91ba-108">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="e91ba-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e91ba-109">Склады (из Finance and Operations в Field Service)</span><span class="sxs-lookup"><span data-stu-id="e91ba-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="e91ba-110">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="e91ba-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e91ba-111">Склад</span><span class="sxs-lookup"><span data-stu-id="e91ba-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="e91ba-112">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="e91ba-112">Entity set</span></span>
| <span data-ttu-id="e91ba-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="e91ba-113">Field Service</span></span>    | <span data-ttu-id="e91ba-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e91ba-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="e91ba-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="e91ba-115">msdyn_warehouses</span></span> | <span data-ttu-id="e91ba-116">Склады</span><span class="sxs-lookup"><span data-stu-id="e91ba-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="e91ba-117">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="e91ba-117">Entity flow</span></span>
<span data-ttu-id="e91ba-118">Склады, которые создаются и поддерживаются в Finance and Operations, можно синхронизировать с Field Service через проект интеграции данных службы Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="e91ba-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="e91ba-119">Требуемые склады, которые синхронизируются с Field Service, можно контролировать с помощью расширенных запросов и фильтрации по проекту.</span><span class="sxs-lookup"><span data-stu-id="e91ba-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="e91ba-120">Склады, которые синхронизируются из Finance and Operations, создаются в Field Service с полем "Поддерживается извне" со значением "Да", и запись становится записью только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e91ba-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="e91ba-121">Решение Field Service CRM Для поддержки интеграции между Field Service и Finance and Operations требуется дополнительная функциональная возможность решения Field Service CRM.</span><span class="sxs-lookup"><span data-stu-id="e91ba-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="e91ba-122">Это решение включает в себя следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="e91ba-122">The solution includes the following changes.</span></span>
<span data-ttu-id="e91ba-123">Поле **Поддерживается извне** было добавлено в объект **Склад (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="e91ba-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="e91ba-124">Это поле помогает определить, обрабатывается ли склад из Operations, или он существует только в Field Service.</span><span class="sxs-lookup"><span data-stu-id="e91ba-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="e91ba-125">Да — склад происходит из Finance and Operations и не может быть изменен в Sales.</span><span class="sxs-lookup"><span data-stu-id="e91ba-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="e91ba-126">Нет — склад был введен непосредственно в Field Service и поддерживается здесь.</span><span class="sxs-lookup"><span data-stu-id="e91ba-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="e91ba-127">Поле **Поддерживается извне** помогает контролировать синхронизацию уровней запасов, корректировки, передачи и использования в заказах на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="e91ba-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="e91ba-128">Только склады, для которых параметр **Поддерживается извне** = "Да", может использоваться для синхронизации непосредственно с тем же складом в другой системе.</span><span class="sxs-lookup"><span data-stu-id="e91ba-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="e91ba-129">Примечание. Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне** = "Нет") и затем сопоставить их с одним складом в Finance and Operations с функцией расширенного запроса и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="e91ba-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e91ba-130">Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и просто отправляло обновления в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e91ba-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="e91ba-131">В этом случае Field Service не будет получать обновления уровней запасов из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e91ba-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="e91ba-132">См. дополнительные сведения в разделах "Синхронизация корректировок запасов из Field Service в Finance and Operations" и "Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations".</span><span class="sxs-lookup"><span data-stu-id="e91ba-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e91ba-133">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="e91ba-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="e91ba-134">В проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="e91ba-134">In the Data Integration project</span></span>
<span data-ttu-id="e91ba-135">Перед синхронизацией складов обязательно обновите расширенный запрос и фильтрацию в проекте, чтобы она включала только склады, которые необходимо внести из Finance and Operations в Field Service.</span><span class="sxs-lookup"><span data-stu-id="e91ba-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="e91ba-136">Обратите внимание, что понадобится склад в Field Service, чтобы применять его в заказах на выполнение работ, корректировках и перемещениях.</span><span class="sxs-lookup"><span data-stu-id="e91ba-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="e91ba-137">Проверьте, что значение **Ключ интеграции** существует для **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="e91ba-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="e91ba-138">Перейдите в раздел "Интеграция данных".</span><span class="sxs-lookup"><span data-stu-id="e91ba-138">Go to Data Integration</span></span>
2. <span data-ttu-id="e91ba-139">Перейдите на вкладку **Набор подключений**.</span><span class="sxs-lookup"><span data-stu-id="e91ba-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="e91ba-140">Выберите набор подключений, используемый для синхронизации заказа на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="e91ba-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="e91ba-141">Перейдите на вкладку **Ключ интеграции**.</span><span class="sxs-lookup"><span data-stu-id="e91ba-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="e91ba-142">Найдите msdyn_warehouses и проверьте, что добавлен ключ **msdyn_name (имя)**.</span><span class="sxs-lookup"><span data-stu-id="e91ba-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="e91ba-143">Если ключ не отображается, добавьте его с помощью команды **Добавить ключ** и нажмите кнопку **Сохранить** вверху страницы.</span><span class="sxs-lookup"><span data-stu-id="e91ba-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e91ba-144">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="e91ba-144">Template mapping in Data integration</span></span>

<span data-ttu-id="e91ba-145">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="e91ba-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="e91ba-146">Склады (из Finance and Operations в Field Service): Склад</span><span class="sxs-lookup"><span data-stu-id="e91ba-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="e91ba-147">[![Сопоставление шаблона в интеграции данных](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="e91ba-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

