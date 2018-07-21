---
title: "Планирование мощности загрузки"
description: "В этом разделе объясняется, как настроить и запланировать мощность загрузки для работников на складе или для всего склада."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: ba2386ba51a018990cf879edcdbbaa716437a216
ms.contentlocale: ru-ru
ms.lasthandoff: 07/21/2018

---

# <a name="schedule-workload-capacity"></a><span data-ttu-id="f457f-103">Планирование мощности загрузки</span><span class="sxs-lookup"><span data-stu-id="f457f-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f457f-104">Вы можете планировать мощность загрузки для складов, а также планировать текущие и будущие загрузки для работников в отдельных складах.</span><span class="sxs-lookup"><span data-stu-id="f457f-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="f457f-105">Можно проектировать загрузки для целого склада или можно проектировать загрузку отдельно для входящих и исходящих загрузок.</span><span class="sxs-lookup"><span data-stu-id="f457f-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="f457f-106">Чтобы спроектировать выходную загрузку для выбранных складов, сведения сводного планирования должны быть доступны для этих складов.</span><span class="sxs-lookup"><span data-stu-id="f457f-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="f457f-107">Дополнительные сведения см. в разделе [Сводные планы](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="f457f-107">For more information, see [Master plans](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="f457f-108">Планирование и просмотр загрузок для склада</span><span class="sxs-lookup"><span data-stu-id="f457f-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="f457f-109">Для планирования мощности загрузки для склада, вы создаете настройку загрузки для одного или нескольких складов, а затем связываете настройку загрузки со сводным планом.</span><span class="sxs-lookup"><span data-stu-id="f457f-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="f457f-110">В настройке мощности загрузки можно определить максимальное значение веса или объема для входящих и исходящих проводок.</span><span class="sxs-lookup"><span data-stu-id="f457f-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="f457f-111">Можно также создать несколько настроек для каждого склада, а затем связать настройку с отдельными сводными планами.</span><span class="sxs-lookup"><span data-stu-id="f457f-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="f457f-112">Например, это можно сделать, чтобы соответствовать сезонными изменениям в количестве работников.</span><span class="sxs-lookup"><span data-stu-id="f457f-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="f457f-113">Если работники для склада работают с проводками для входящих и исходящих загрузок, можно настроить настройку мощности склада для проектирования загрузки в совмещенном представлении.</span><span class="sxs-lookup"><span data-stu-id="f457f-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="f457f-114">Для планирования и просмотра загрузок для складов, необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="f457f-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="f457f-115">Создайте настройки мощности загрузки и определите пределы мощности загрузки для одного или нескольких складов.</span><span class="sxs-lookup"><span data-stu-id="f457f-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="f457f-116">Свяжите настройку мощности загрузки со сводным планом, чтобы создать прогнозы загрузки и указать срок их действия.</span><span class="sxs-lookup"><span data-stu-id="f457f-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="f457f-117">Создание настройки мощности загрузки для склада</span><span class="sxs-lookup"><span data-stu-id="f457f-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="f457f-118">Выберите **Управление запасами** \> **Настройка** \> **Мониторинг склада** \> **Мощность загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f457f-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="f457f-119">В разделе "Панель операций" выберите **Создать** для создания настройки мощности загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="f457f-120">На экспресс-вкладке **Склады** выберите **Создать**, а затем введите значения в строке, чтобы связать склад с настройкой мощности загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="f457f-121">Установите флажок **Объединенная входящая и исходящая загрузка**, если в отчете **Мощность загрузки** должна отображаться общая загрузка для входящих и исходящих проводок в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="f457f-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="f457f-122">На экспресс-вкладке **Типы проводок** выберите типы входящих и исходящих проводок, к которым будут применяться пределы загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f457f-123">Необходимо выбрать как минимум один тип проводки для входящей и исходящей загрузок.</span><span class="sxs-lookup"><span data-stu-id="f457f-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="f457f-124">Определение пределов для объема или веса</span><span class="sxs-lookup"><span data-stu-id="f457f-124">Define limits for volume or weight</span></span>

<span data-ttu-id="f457f-125">Можно настроить пределы для объема или веса в зависимости от того, какие ограничения применяются к рабочей силе склада.</span><span class="sxs-lookup"><span data-stu-id="f457f-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="f457f-126">Указанные пределы включены в прогноз мощности загрузки, который можно просмотреть в отчете **Мощность загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f457f-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="f457f-127">Чтобы спрогнозировать сведения об объеме и весе для номенклатур, необходимо определить стандартный объем одной складируемой номенклатуры и вес одной складируемой номенклатуры для всех продуктов.</span><span class="sxs-lookup"><span data-stu-id="f457f-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="f457f-128">Обязательные поля доступны в следующих группах полей на экспресс-вкладке **Управление складскими запасами** на странице **Сведения об используемом продукте**.</span><span class="sxs-lookup"><span data-stu-id="f457f-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="f457f-129">Обработка</span><span class="sxs-lookup"><span data-stu-id="f457f-129">Handling</span></span>
- <span data-ttu-id="f457f-130">Физические размеры</span><span class="sxs-lookup"><span data-stu-id="f457f-130">Physical dimensions</span></span>
- <span data-ttu-id="f457f-131">Взвешенные измерения</span><span class="sxs-lookup"><span data-stu-id="f457f-131">Weight measurements</span></span>

<span data-ttu-id="f457f-132">Если эти сведения указаны неправильно, вы получите сообщение при создании отчета **Мощность загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f457f-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="f457f-133">Из отчета можно перейти к детализации сведений, которых не хватает для прогнозирования будущей загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="f457f-134">Связывание настройки мощности загрузки со сводным планом</span><span class="sxs-lookup"><span data-stu-id="f457f-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="f457f-135">Щелкните **Управление запасами** \> **Периодические задачи** \> **Запланировать загрузку**.</span><span class="sxs-lookup"><span data-stu-id="f457f-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="f457f-136">В поле **Сводный план** выберите сводный план, который будет использоваться для прогнозов загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="f457f-137">В поле **Число дней** укажите количество дней, которые покрывает прогноз загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="f457f-138">В поле **Загрузка** выберите настройку загрузки, чтобы связать со сводным планом.</span><span class="sxs-lookup"><span data-stu-id="f457f-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="f457f-139">Просмотр мощности загрузки</span><span class="sxs-lookup"><span data-stu-id="f457f-139">View workload capacity</span></span>

1. <span data-ttu-id="f457f-140">Выберите **Управление запасами** \> **Запросы и отчеты** \> **Отчеты по физическим запасам** \> **Мощность загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f457f-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="f457f-141">В поле **Число столбцов** укажите число столбцов для отображения в отчете.</span><span class="sxs-lookup"><span data-stu-id="f457f-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="f457f-142">В поле **Тип заказа** выберите **Запланировано и подтверждено**, **Запланировано** или **Подтверждено** для указания типа заказов для прогнозирования в отчете.</span><span class="sxs-lookup"><span data-stu-id="f457f-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="f457f-143">В поле **Тип загрузки** выберите тип загрузки для указания того, должна ли мощность загрузки прогнозироваться для объема или веса.</span><span class="sxs-lookup"><span data-stu-id="f457f-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="f457f-144">В поле **Мощность загрузки** выберите настройку мощности загрузки.</span><span class="sxs-lookup"><span data-stu-id="f457f-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>

