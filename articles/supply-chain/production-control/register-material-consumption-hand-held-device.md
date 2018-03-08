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
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: b84b63ec519ae686b55905170c956fcb2b08334a
ms.contentlocale: ru-ru
ms.lasthandoff: 03/08/2018

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="16b07-103">Регистрация потребления материалов на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="16b07-103">Register material consumption using a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="16b07-104">В этой теме описывается workflow-процесс, позволяющий регистрировать потребление сырья на производстве с помощью наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="16b07-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="16b07-105">Приветствие</span><span class="sxs-lookup"><span data-stu-id="16b07-105">Introduction</span></span>
------------

<span data-ttu-id="16b07-106">Этот workflow-процесс используется при наличии строгих требований к прослеживаемости материалов.</span><span class="sxs-lookup"><span data-stu-id="16b07-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="16b07-107">В таких случаях для обеспечения прослеживаемости материалов необходимо фиксировать точное время потребления и количество потребленного материала.</span><span class="sxs-lookup"><span data-stu-id="16b07-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="16b07-108">Этот процесс можно рассматривать как нечто противоположное операциям предварительного или обратного автосписания, где существует смещением между временем регистрации и временем, когда потребление на самом деле имеет место.</span><span class="sxs-lookup"><span data-stu-id="16b07-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="16b07-109">Это объясняет, почему стратегию автоматического потребления нельзя использовать для некоторых материалов с требованиями к прослеживаемостью.</span><span class="sxs-lookup"><span data-stu-id="16b07-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="16b07-110">Рассмотрим простой сценарий, который поясняет, как настроить workflow-процесс для регистрации потребления сырья на производстве с помощью наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="16b07-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="16b07-111">[![Настройка workflow-процесса для регистрации потребления сырья с помощью наладонного устройства](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="16b07-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="16b07-112">Подробности сценария</span><span class="sxs-lookup"><span data-stu-id="16b07-112">Scenario details</span></span>

<span data-ttu-id="16b07-113">Непрерывный производственный процесс (5) потребляет контролируемое по партиям сырье RM-100.</span><span class="sxs-lookup"><span data-stu-id="16b07-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="16b07-114">Сырье имеется в наличии в ячейке Bulk-001 (1) на грузоместе PL-1 в виде двух партий — B1 и B2 — объем каждой из которых составляет 100 фунтов.</span><span class="sxs-lookup"><span data-stu-id="16b07-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="16b07-115">Работа склада (2) выпускается и обрабатывается для RM-100, и сырье перемещается из ячейки Bulk-001 в ячейку поступления на производство PIL-01 (3), которая не контролируется по грузоместам.</span><span class="sxs-lookup"><span data-stu-id="16b07-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="16b07-116">Оператор станка отвешивает сырье из ячейки поступления на производство (3) и регистрирует вес и номер партии как потребленные (4).</span><span class="sxs-lookup"><span data-stu-id="16b07-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="16b07-117">Из ячейки поступления на производство через определенные интервалы времени в производственный процесс вручную добавляется по порции сырья.</span><span class="sxs-lookup"><span data-stu-id="16b07-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="16b07-118">Когда оператор станка добавляет сырье, оно взвешивается на весах, и регистрируется номер партии.</span><span class="sxs-lookup"><span data-stu-id="16b07-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="16b07-119">Настройка workflow-процесса для регистрации потребления с помощью наладонного устройства</span><span class="sxs-lookup"><span data-stu-id="16b07-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="16b07-120">Создайте продукт типа "готовый товар" FG-100 со спецификацией, куда входит контролируемое по партиям сырье RM-100.</span><span class="sxs-lookup"><span data-stu-id="16b07-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="16b07-121">Добавьте две партии сырья RM-100 — B1 и B2 — в количестве 100 в ячейку Bulk-001 на грузоместе PL-1.</span><span class="sxs-lookup"><span data-stu-id="16b07-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="16b07-122">Принцип списания в строке спецификации для RM-100 установлен в значение **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="16b07-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="16b07-123">В качестве ячейки поступления на производство установите PIL-01.</span><span class="sxs-lookup"><span data-stu-id="16b07-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="16b07-124">Это можно сделать путем выбора этой ячейки в качестве ячейки поступления на производство по умолчанию на складе 51.</span><span class="sxs-lookup"><span data-stu-id="16b07-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="16b07-125">Создайте новый пункт меню для мобильного устройства:</span><span class="sxs-lookup"><span data-stu-id="16b07-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="16b07-126">**Наименование пункта меню** — Регистрация потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="16b07-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="16b07-127">**Заголовок** — Регистрация потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="16b07-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="16b07-128">**Режим** — Косвенный.</span><span class="sxs-lookup"><span data-stu-id="16b07-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="16b07-129">**Код мероприятия** — Регистрация потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="16b07-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="16b07-130">Добавьте пункт меню в меню устройства **Production Mobile**.</span><span class="sxs-lookup"><span data-stu-id="16b07-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="16b07-131">Создайте производственный заказ на готовую продукцию:</span><span class="sxs-lookup"><span data-stu-id="16b07-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="16b07-132">**Код номенклатуры** — FG-100</span><span class="sxs-lookup"><span data-stu-id="16b07-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="16b07-133">**Сайт** — 5</span><span class="sxs-lookup"><span data-stu-id="16b07-133">**Site** - 5</span></span> 
-    <span data-ttu-id="16b07-134">**Склад** — 51</span><span class="sxs-lookup"><span data-stu-id="16b07-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="16b07-135">**Количество** — 150</span><span class="sxs-lookup"><span data-stu-id="16b07-135">**Quantity** - 150</span></span>

<span data-ttu-id="16b07-136">Производственный заказ проходит этапы **Оценено** и **Выпущено**, и создается работа склада.</span><span class="sxs-lookup"><span data-stu-id="16b07-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="16b07-137">Выполните работу, используя workflow-процесс для комплектации сырья для наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="16b07-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="16b07-138">В результате этого сырье из буферной ячейки будет перемещено в ячейку поступления на производство PIL-01.</span><span class="sxs-lookup"><span data-stu-id="16b07-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="16b07-139">После завершения работы сырье имеет статус **Скомплектовано в ячейке поступления на производство**.</span><span class="sxs-lookup"><span data-stu-id="16b07-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="16b07-140">Статус после обработки работы может быть либо **Скомплектовано**, либо **Физ. зарезервировано**.</span><span class="sxs-lookup"><span data-stu-id="16b07-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="16b07-141">Это настраивается с помощью параметра **Статус расхода после помещения на склад**.</span><span class="sxs-lookup"><span data-stu-id="16b07-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="16b07-142">Запустите производственный заказ либо из клиента, либо с наладонного устройства с помощью пункта меню **Начало производства**.</span><span class="sxs-lookup"><span data-stu-id="16b07-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="16b07-143">После запуска производственного заказа можно зарегистрировать потребление материала с помощью workflow-процесса для наладонного устройства.</span><span class="sxs-lookup"><span data-stu-id="16b07-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="16b07-144">Давайте начнем с регистрации потребления 25 фунтов партии B1.</span><span class="sxs-lookup"><span data-stu-id="16b07-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="16b07-145">Выберите пункт меню **Регистрация потребления** **материалов** в меню наладонного устройства и введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="16b07-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="16b07-146">Номер производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="16b07-146">The production order number.</span></span> 
-    <span data-ttu-id="16b07-147">Ячейку, в которой будет происходить потребление материала, в данном случае PIL-01.</span><span class="sxs-lookup"><span data-stu-id="16b07-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="16b07-148">Код номенклатуры: RM-100.</span><span class="sxs-lookup"><span data-stu-id="16b07-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="16b07-149">Номер партии: B1.</span><span class="sxs-lookup"><span data-stu-id="16b07-149">Batch number B1.</span></span> 
-    <span data-ttu-id="16b07-150">Количество: 25.</span><span class="sxs-lookup"><span data-stu-id="16b07-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="16b07-151">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="16b07-151">Select **OK**.</span></span>

<span data-ttu-id="16b07-152">Обратите внимание, что на экране появилось сообщение "Создана строка журнала".</span><span class="sxs-lookup"><span data-stu-id="16b07-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="16b07-153">В производственном заказе есть открытый журнал типа **Ведомость комплектации производства** для кода номенклатуры RM-100 и номера партии B1.</span><span class="sxs-lookup"><span data-stu-id="16b07-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="16b07-154">Теперь можно продолжить регистрацию, например партии номер B2; при каждом нажатии кнопки **ОК** в открытый журнал будет добавляться новая строка журнала.</span><span class="sxs-lookup"><span data-stu-id="16b07-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="16b07-155">Закончив регистрацию, выберите **Готово**, чтобы разнести журнал и закончить workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="16b07-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="16b07-156">Дополнительные комментарии</span><span class="sxs-lookup"><span data-stu-id="16b07-156">Additional comments</span></span> 

-   <span data-ttu-id="16b07-157">Если пользователь отменит workflow-процесс после создания строки журнала, журнал будет находиться в неразнесенном состоянии, но если позднее пользователь будет использовать workflow-процесс для того же производственного заказа, строки будут добавляться в открытый журнал, а не в новый журнал.</span><span class="sxs-lookup"><span data-stu-id="16b07-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="16b07-158">Новый workflow-процесс также поддерживает регистрацию серийных номеров.</span><span class="sxs-lookup"><span data-stu-id="16b07-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="16b07-159">Зарегистрировать можно только код номенклатуры, определенный в спецификации или в формуле для выбранного производственного заказа или партионного заказа.</span><span class="sxs-lookup"><span data-stu-id="16b07-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="16b07-160">Материал может потребляться с превышением.</span><span class="sxs-lookup"><span data-stu-id="16b07-160">Material can be overconsumed.</span></span> <span data-ttu-id="16b07-161">Например, если по оценке материал должен потребляться в количестве 100 фунтов, он может быть потреблен с превышением — например, в количестве 105 фунтов.</span><span class="sxs-lookup"><span data-stu-id="16b07-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



