---
title: Планирование использования загрузки
description: В этом разделе объясняется, как настроить и спланировать загрузку для склада.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435829"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="b3b08-103">Планирование использования загрузки</span><span class="sxs-lookup"><span data-stu-id="b3b08-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b3b08-104">Вы можете планировать загрузку для выбранных типов местоположений, а также прогнозировать текущую и будущую загрузку.</span><span class="sxs-lookup"><span data-stu-id="b3b08-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="b3b08-105">Можно прогнозировать загрузку для одного или нескольких сайтов, для единиц загрузки (зона или склад) или для сочетаний зоны и склада.</span><span class="sxs-lookup"><span data-stu-id="b3b08-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="b3b08-106">Планирование и просмотр загрузки для склада или объекта</span><span class="sxs-lookup"><span data-stu-id="b3b08-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="b3b08-107">Для планирования с загрузки для объектов, складов или зон создайте конфигурацию использования места и свяжите ее со сводным планом.</span><span class="sxs-lookup"><span data-stu-id="b3b08-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="b3b08-108">При настройке использования места использование места задается с помощью типов местоположений, таких как **Буферная ячейка** и **Ячейка комплектации**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="b3b08-109">Можно также указать режим загрузки хранилища, например **Зона**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="b3b08-110">Прогнозирование будущего использования места основывается на данных, которые рассчитываются по связанному сводному плану.</span><span class="sxs-lookup"><span data-stu-id="b3b08-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="b3b08-111">Сводные планы прогнозируют ресурсы для входящих и исходящих заказов на производство и операций.</span><span class="sxs-lookup"><span data-stu-id="b3b08-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="b3b08-112">Прогноз доступного места основывается на связи между конфигурацией использования места и выбранным сводным планом.</span><span class="sxs-lookup"><span data-stu-id="b3b08-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="b3b08-113">С помощью режима загрузки хранилища, выбранного в параметрах использования места, можно указать, следует ли прогнозировать загрузку для каждого склада или зоны или же прогноз должен включать информацию и о складах, и о зонах.</span><span class="sxs-lookup"><span data-stu-id="b3b08-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="b3b08-114">Можно также определить, нужно ли исключать блокированные местоположения из расчета использования загрузки.</span><span class="sxs-lookup"><span data-stu-id="b3b08-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="b3b08-115">Спрогнозировать использование места можно, создав отчет **Использование загрузки склада**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="b3b08-116">При создании этого отчета можно определить, должно ли использование загрузки прогнозироваться для каждого сайта отдельно или для всех сайтов или для выбранной единицы загрузки, например для зоны или склада.</span><span class="sxs-lookup"><span data-stu-id="b3b08-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="b3b08-117">Создание конфигурации использования свободного места для склада</span><span class="sxs-lookup"><span data-stu-id="b3b08-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="b3b08-118">Выберите **Управление запасами** \> **Настройка** \> **Мониторинг склада** \> **Использование места**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="b3b08-119">Выберите **Создать** для создания настройки использования места.</span><span class="sxs-lookup"><span data-stu-id="b3b08-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="b3b08-120">Укажите код и имя для новой настройки.</span><span class="sxs-lookup"><span data-stu-id="b3b08-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="b3b08-121">В поле **Режим загрузки хранилища** выберите, к чему должен относиться обзор использования места, — к складу, к зоне или к складу и зоне.</span><span class="sxs-lookup"><span data-stu-id="b3b08-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="b3b08-122">Задайте для параметра **Исключить заблокированные ячейки** значение **Да**, чтобы исключить заблокированные ячейки запасов из расчета доступного места.</span><span class="sxs-lookup"><span data-stu-id="b3b08-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="b3b08-123">Вы можете заблокировать место хранения для приемки и выпуска, выбрав причину блокировки для местоположения в поле **Блокировка приемки** или **Блокировка выпуска** на экспресс-вкладке **Прочее** на странице **Места хранения**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="b3b08-124">На экспресс-вкладке **Тип местоположения** выберите типы местоположений для включения в расчет использования места.</span><span class="sxs-lookup"><span data-stu-id="b3b08-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="b3b08-125">Необходимо выбрать как минимум один тип местоположения для прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="b3b08-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="b3b08-126">Свяжите конфигурацию свободного места со сводным планом</span><span class="sxs-lookup"><span data-stu-id="b3b08-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="b3b08-127">Щелкните **Управление запасами** \> **Периодические задачи** \> **Планирование использования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="b3b08-128">В поле **Сводный план** выберите сводный план.</span><span class="sxs-lookup"><span data-stu-id="b3b08-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="b3b08-129">В поле **Число дней** укажите количество дней для включения в прогноз текущих и будущих рабочих нагрузок.</span><span class="sxs-lookup"><span data-stu-id="b3b08-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="b3b08-130">В поле **Использование места** выберите конфигурацию использования места для использования при прогнозировании текущих и будущих рабочих нагрузок.</span><span class="sxs-lookup"><span data-stu-id="b3b08-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="b3b08-131">Определение прогноза использования загрузки и просмотр информации</span><span class="sxs-lookup"><span data-stu-id="b3b08-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="b3b08-132">Выберите **Управление запасами** \> **Запросы и отчеты** \> **Отчеты по физическим запасам** \> **Использование загрузки склада**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="b3b08-133">В поле **Показать по** выберите уровень прогнозирования использования места.</span><span class="sxs-lookup"><span data-stu-id="b3b08-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="b3b08-134">**Сайт** — прогнозирование использования места для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="b3b08-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="b3b08-135">Этот прогноз полезен, если, например, необходимо просмотреть все склады для объекта, чтобы сбалансировать использование места между складами.</span><span class="sxs-lookup"><span data-stu-id="b3b08-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="b3b08-136">**Единица загрузки** — прогнозирование использования места для зон или складов.</span><span class="sxs-lookup"><span data-stu-id="b3b08-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="b3b08-137">Свободное место затем прогнозируется в зависимости от значения, выбранного в поле **Режим загрузки хранилища** на странице **Использование места** при создании настройки использования места.</span><span class="sxs-lookup"><span data-stu-id="b3b08-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="b3b08-138">Выполните одно из следующих действий в зависимости от значения, выбранного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="b3b08-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="b3b08-139">Если вы выбрали **Сайт** в поле **Показать по**, доступно поле **Сайт**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="b3b08-140">Выберите один или несколько сайтов для включения в прогноз.</span><span class="sxs-lookup"><span data-stu-id="b3b08-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="b3b08-141">Если вы выбрали **Единица загрузки** в поле **Показать по**, доступно поле **Единица загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b3b08-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="b3b08-142">Выберите единицу загрузки.</span><span class="sxs-lookup"><span data-stu-id="b3b08-142">Select the load unit.</span></span>

4. <span data-ttu-id="b3b08-143">В поле **Тип загрузки** выберите **Объем** или **Вес**, чтобы указать операционную единицу склада для прогнозирования свободного места.</span><span class="sxs-lookup"><span data-stu-id="b3b08-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="b3b08-144">В поле **Настройка использования места** выберите конфигурацию использования места, на которой должен быть основан прогноз.</span><span class="sxs-lookup"><span data-stu-id="b3b08-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
