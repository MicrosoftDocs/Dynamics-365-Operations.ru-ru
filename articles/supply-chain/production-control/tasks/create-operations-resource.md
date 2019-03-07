---
title: Создание операционного ресурса
description: Операционный ресурс участвует в мероприятиях проекта или производственного процесса.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9d8f13e29ea813eb9721ddca795b67837e2aa5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "350075"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="bb4fc-103">Создание операционного ресурса</span><span class="sxs-lookup"><span data-stu-id="bb4fc-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb4fc-104">Операционный ресурс участвует в мероприятиях проекта или производственного процесса.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="bb4fc-105">В этой процедуре показано, как определить операционный ресурс.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="bb4fc-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="bb4fc-107">Перейдите в раздел "Ресурсы".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-107">Go to Resources.</span></span>
2. <span data-ttu-id="bb4fc-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-108">Click New.</span></span>
3. <span data-ttu-id="bb4fc-109">В поле "Ресурс" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="bb4fc-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="bb4fc-111">Определение параметров мощности и потребления</span><span class="sxs-lookup"><span data-stu-id="bb4fc-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="bb4fc-112">Разверните раздел "Операция".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="bb4fc-113">В поле "Процент отходов" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="bb4fc-114">В поле "Категория настройки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="bb4fc-115">Укажите категорию затрат, которая определяет способ учета затрат на настройку.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="bb4fc-116">В поле "Категория времени выполнения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="bb4fc-117">Укажите категорию затрат, которая определяет способ учета затрат на время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="bb4fc-118">В поле "Количественная категория" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="bb4fc-119">Укажите категорию затрат, которая определяет способ учета стоимости ресурсов на основании выпускаемого количества.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="bb4fc-120">В поле "Ед. изм. мощности" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="bb4fc-121">Укажите единицу измерения, в которой выражается мощность операционного ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="bb4fc-122">В поле "Мощность" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="bb4fc-123">В поле "Процент эффективности" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="bb4fc-124">Укажите процент эффективности, ожидаемый от операционного ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="bb4fc-125">Процент эффективности корректирует пропускную способность операционного ресурса и влияет на время, зарезервированное для ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="bb4fc-126">В поле "Процент планирования операций" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="bb4fc-127">Укажите максимальный процент мощности операционного ресурса, который требуется использовать при планировании операций.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="bb4fc-128">Выберите значение "Да" в поле "Ограничение по мощности".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="bb4fc-129">Задайте для этого параметра значение "Да", если операционный ресурс должен планироваться на основании фактической доступной мощности и если должны учитываться существующие резервирования мощностей.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="bb4fc-130">Если для этого параметра задать значение "Нет", будет предполагаться, что операционный ресурс имеет неограниченную мощность и может быть зарезервирован с превышением.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="bb4fc-131">Выберите значение "Да" в поле "Минимальный ресурс".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="bb4fc-132">Определение рабочего времени</span><span class="sxs-lookup"><span data-stu-id="bb4fc-132">Define working times</span></span>
1. <span data-ttu-id="bb4fc-133">Разверните раздел "Календари".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="bb4fc-134">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-134">Click Add.</span></span>
3. <span data-ttu-id="bb4fc-135">В поле "Календарь" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="bb4fc-136">Укажите календарь рабочего времени, определяющий мощность ресурса (в часах).</span><span class="sxs-lookup"><span data-stu-id="bb4fc-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="bb4fc-137">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bb4fc-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="bb4fc-139">Определение возможностей ресурса</span><span class="sxs-lookup"><span data-stu-id="bb4fc-139">Define resource capabilities</span></span>
1. <span data-ttu-id="bb4fc-140">Разверните раздел "Возможности".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="bb4fc-141">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-141">Click Add.</span></span>
    * <span data-ttu-id="bb4fc-142">Возможность — это способность операционного ресурса участвовать в определенном мероприятии.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="bb4fc-143">Механизм планирования распределяет ресурсы, сопоставляя требования каждого мероприятия к ресурсам с возможностями доступных операционных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="bb4fc-144">В поле "Возможность" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="bb4fc-145">В поле "Уровень" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="bb4fc-146">Укажите уровень квалификации, по которому обрабатывается возможность ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="bb4fc-147">В поле "Приоритет" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="bb4fc-148">Укажите приоритет операционного ресурса по отношению к возможности.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="bb4fc-149">При планировании по приоритету операционный ресурс с наивысшим приоритетом (наименьшим числовым значением) выбирается первым.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="bb4fc-150">Назначение ресурса группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="bb4fc-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="bb4fc-151">Разверните раздел "Группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="bb4fc-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="bb4fc-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-152">Click Add.</span></span>
    * <span data-ttu-id="bb4fc-153">Группа ресурсов определяет сайт, производственное подразделение и контекст склада для операционных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="bb4fc-154">Операционный ресурс можно запланировать, только если он назначен группе ресурсов и только на сайте, на котором находится группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="bb4fc-155">В поле "Группа ресурсов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="bb4fc-156">В поле "Место хранения на складе получения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="bb4fc-157">Укажите местонахождение склада, из которого операционный ресурс потребляет материалы.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

