---
title: "Регистрация потребления материалов на мобильном устройстве"
description: "В этой теме описывается workflow-процесс, позволяющий регистрировать потребление сырья на производстве с помощью наладонного устройства."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: ru-ru
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="70121-103">Регистрация потребления материалов на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="70121-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="70121-104">В этой теме описывается workflow-процесс, позволяющий регистрировать потребление сырья на производстве с помощью наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="70121-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="70121-105">Приветствие</span><span class="sxs-lookup"><span data-stu-id="70121-105">Introduction</span></span>
------------

<span data-ttu-id="70121-106">Этот workflow-процесс используется при наличии строгих требований к прослеживаемости материалов.</span><span class="sxs-lookup"><span data-stu-id="70121-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="70121-107">В таких случаях для обеспечения прослеживаемости материалов необходимо фиксировать точное время потребления и количество потребленного материала.</span><span class="sxs-lookup"><span data-stu-id="70121-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="70121-108">Этот процесс можно рассматривать как нечто противоположное операциям предварительного или обратного автосписания, где существует смещением между временем регистрации и временем, когда потребление на самом деле имеет место.</span><span class="sxs-lookup"><span data-stu-id="70121-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="70121-109">Это объясняет, почему стратегию автоматического потребления нельзя использовать для некоторых материалов с требованиями к прослеживаемостью.</span><span class="sxs-lookup"><span data-stu-id="70121-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="70121-110">Рассмотрим простой сценарий, который поясняет, как настроить workflow-процесс для регистрации потребления сырья на производстве с помощью наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="70121-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="70121-111">Подробности сценария</span><span class="sxs-lookup"><span data-stu-id="70121-111">Scenario details</span></span>

<span data-ttu-id="70121-112">Непрерывный производственный процесс (5) потребляет контролируемое по партиям сырье RM-100.</span><span class="sxs-lookup"><span data-stu-id="70121-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="70121-113">Сырье имеется в наличии в ячейке Bulk-001 (1) на грузоместе PL-1 в виде двух партий — B1 и B2 — объем каждой из которых составляет 100 фунтов.</span><span class="sxs-lookup"><span data-stu-id="70121-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="70121-114">Работа склада (2) выпускается и обрабатывается для RM-100, и сырье перемещается из ячейки Bulk-001 в ячейку поступления на производство PIL-01 (3), которая не контролируется по грузоместам.</span><span class="sxs-lookup"><span data-stu-id="70121-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="70121-115">Оператор станка отвешивает сырье из ячейки поступления на производство (3) и регистрирует вес и номер партии как потребленные (4).</span><span class="sxs-lookup"><span data-stu-id="70121-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="70121-116">Из ячейки поступления на производство через определенные интервалы времени в производственный процесс вручную добавляется по порции сырья.</span><span class="sxs-lookup"><span data-stu-id="70121-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="70121-117">Когда оператор станка добавляет сырье, оно взвешивается на весах, и регистрируется номер партии.</span><span class="sxs-lookup"><span data-stu-id="70121-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="70121-118">Настройка workflow-процесса для регистрации потребления с помощью наладонного устройства</span><span class="sxs-lookup"><span data-stu-id="70121-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="70121-119">Создайте продукт типа "готовый товар" FG-100 со спецификацией, куда входит контролируемое по партиям сырье RM-100.</span><span class="sxs-lookup"><span data-stu-id="70121-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="70121-120">Добавьте две партии сырья RM-100 — B1 и B2 — в количестве 100 в ячейку Bulk-001 на грузоместе PL-1.</span><span class="sxs-lookup"><span data-stu-id="70121-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="70121-121">Принцип списания в строке спецификации для RM-100 установлен в значение **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="70121-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="70121-122">В качестве ячейки поступления на производство установите PIL-01.</span><span class="sxs-lookup"><span data-stu-id="70121-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="70121-123">Это можно сделать путем выбора этой ячейки в качестве ячейки поступления на производство по умолчанию на складе 51.</span><span class="sxs-lookup"><span data-stu-id="70121-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="70121-124">Создайте новый пункт меню для мобильного устройства:</span><span class="sxs-lookup"><span data-stu-id="70121-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="70121-125">**Наименование пункта меню** — Регистрация потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="70121-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="70121-126">**Заголовок** — Регистрация потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="70121-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="70121-127">**Режим** — Косвенный.</span><span class="sxs-lookup"><span data-stu-id="70121-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="70121-128">**Код мероприятия** — Регистрация потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="70121-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="70121-129">Добавьте пункт меню в меню устройства **Production Mobile**.</span><span class="sxs-lookup"><span data-stu-id="70121-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="70121-130">Создайте производственный заказ на готовую продукцию:</span><span class="sxs-lookup"><span data-stu-id="70121-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="70121-131">**Код номенклатуры** — FG-100</span><span class="sxs-lookup"><span data-stu-id="70121-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="70121-132">**Сайт** — 5</span><span class="sxs-lookup"><span data-stu-id="70121-132">**Site** - 5</span></span> 
-    <span data-ttu-id="70121-133">**Склад** — 51</span><span class="sxs-lookup"><span data-stu-id="70121-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="70121-134">**Количество** — 150</span><span class="sxs-lookup"><span data-stu-id="70121-134">**Quantity** - 150</span></span>

<span data-ttu-id="70121-135">Производственный заказ проходит этапы **Оценено** и **Выпущено**, и создается работа склада.</span><span class="sxs-lookup"><span data-stu-id="70121-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="70121-136">Выполните работу, используя workflow-процесс для комплектации сырья для наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="70121-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="70121-137">В результате этого сырье из буферной ячейки будет перемещено в ячейку поступления на производство PIL-01.</span><span class="sxs-lookup"><span data-stu-id="70121-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="70121-138">После завершения работы сырье имеет статус **Скомплектовано в ячейке поступления на производство**.</span><span class="sxs-lookup"><span data-stu-id="70121-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="70121-139">Статус после обработки работы может быть либо **Скомплектовано**, либо **Физ. зарезервировано**.</span><span class="sxs-lookup"><span data-stu-id="70121-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="70121-140">Это настраивается с помощью параметра **Статус расхода после помещения на склад**.</span><span class="sxs-lookup"><span data-stu-id="70121-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="70121-141">Запустите производственный заказ либо из клиента, либо с наладонного устройства с помощью пункта меню **Начало производства**.</span><span class="sxs-lookup"><span data-stu-id="70121-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="70121-142">После запуска производственного заказа можно зарегистрировать потребление материала с помощью workflow-процесса для наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="70121-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="70121-143">Давайте начнем с регистрации потребления 25 фунтов партии B1.</span><span class="sxs-lookup"><span data-stu-id="70121-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="70121-144">Выберите пункт меню **Регистрация потребления** **материалов** в меню наладонного устройства и введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="70121-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="70121-145">Номер производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="70121-145">The production order number.</span></span> 
-    <span data-ttu-id="70121-146">Ячейку, в которой будет происходить потребление материала, в данном случае PIL-01.</span><span class="sxs-lookup"><span data-stu-id="70121-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="70121-147">Код номенклатуры: RM-100.</span><span class="sxs-lookup"><span data-stu-id="70121-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="70121-148">Номер партии: B1.</span><span class="sxs-lookup"><span data-stu-id="70121-148">Batch number B1.</span></span> 
-    <span data-ttu-id="70121-149">Количество: 25.</span><span class="sxs-lookup"><span data-stu-id="70121-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="70121-150">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="70121-150">Select **OK**.</span></span>

<span data-ttu-id="70121-151">Обратите внимание, что на экране появилось сообщение "Создана строка журнала".</span><span class="sxs-lookup"><span data-stu-id="70121-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="70121-152">В производственном заказе есть открытый журнал типа **Ведомость комплектации производства** для кода номенклатуры RM-100 и номера партии B1.</span><span class="sxs-lookup"><span data-stu-id="70121-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="70121-153">Теперь можно продолжить регистрацию, например партии номер B2; при каждом нажатии кнопки **ОК** в открытый журнал будет добавляться новая строка журнала.</span><span class="sxs-lookup"><span data-stu-id="70121-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="70121-154">Закончив регистрацию, выберите **Готово**, чтобы разнести журнал и закончить workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="70121-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="70121-155">Дополнительные комментарии</span><span class="sxs-lookup"><span data-stu-id="70121-155">Additional comments</span></span> 

-   <span data-ttu-id="70121-156">Если пользователь отменит workflow-процесс после создания строки журнала, журнал будет находиться в неразнесенном состоянии, но если позднее пользователь будет использовать workflow-процесс для того же производственного заказа, строки будут добавляться в открытый журнал, а не в новый журнал.</span><span class="sxs-lookup"><span data-stu-id="70121-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="70121-157">Новый workflow-процесс также поддерживает регистрацию серийных номеров.</span><span class="sxs-lookup"><span data-stu-id="70121-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="70121-158">Зарегистрировать можно только код номенклатуры, определенный в спецификации или в формуле для выбранного производственного заказа или партионного заказа.</span><span class="sxs-lookup"><span data-stu-id="70121-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="70121-159">Материал может потребляться с превышением.</span><span class="sxs-lookup"><span data-stu-id="70121-159">Material can be overconsumed.</span></span> <span data-ttu-id="70121-160">Например, если по оценке материал должен потребляться в количестве 100 фунтов, он может быть потреблен с превышением — например, в количестве 105 фунтов.</span><span class="sxs-lookup"><span data-stu-id="70121-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



