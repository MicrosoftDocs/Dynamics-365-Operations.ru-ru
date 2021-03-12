---
title: Заявки на закупку
description: В этой теме описывается, как заявки на закупку поддерживаются при оптимизации планирования.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8075f8d7c3868c6d6012edbce17dbbb4749209ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992353"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="5447a-103">Заявки на закупку</span><span class="sxs-lookup"><span data-stu-id="5447a-103">Purchase requisitions</span></span>

<span data-ttu-id="5447a-104">Сводное планирование может пополнять утвержденные заявки на закупку.</span><span class="sxs-lookup"><span data-stu-id="5447a-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="5447a-105">Таким образом, для покрытия заявок на закупку пользователям не придется использовать рабочий процесс для создания заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="5447a-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="5447a-106">Вместо этого заявки на закупку могут охватываться сводными планированием.</span><span class="sxs-lookup"><span data-stu-id="5447a-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="5447a-107">В связи с этой функциональностью заявка на закупку может создать заказ на покупку, заказ на перемещение или производственный заказ, в зависимости от значения **Типа "спланированного заказа**, которое задано для соответствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="5447a-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="5447a-108">Включение сводных планах для включения заявок</span><span class="sxs-lookup"><span data-stu-id="5447a-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="5447a-109">Чтобы включить заявки в расчет покрытия для сводного плана, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5447a-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="5447a-110">Выберите **Сводное планирование** \> **Настройка** \> **Планы** \> **Сводные планы**.</span><span class="sxs-lookup"><span data-stu-id="5447a-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="5447a-111">Создайте или выберите сводный план.</span><span class="sxs-lookup"><span data-stu-id="5447a-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="5447a-112">На экспресс-вкладке **Общие** задайте для параметра **Включить заявки** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="5447a-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="5447a-113">Повторите шаги 2 и 3 для каждого дополнительного сводного плана, для которого требуется включить заявки.</span><span class="sxs-lookup"><span data-stu-id="5447a-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="5447a-114">Временная граница утвержденных заявок</span><span class="sxs-lookup"><span data-stu-id="5447a-114">Approved requisitions time fence</span></span>

<span data-ttu-id="5447a-115">*Временная граница утвержденных заявок* определяет, как далеко назад (в днях) сводный план будет включать спрос из утвержденных заявок на пополнение запасов.</span><span class="sxs-lookup"><span data-stu-id="5447a-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="5447a-116">Временную границу утвержденных заявок можно настроить как на уровне группы покрытия, так и на уровне сводного плана.</span><span class="sxs-lookup"><span data-stu-id="5447a-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="5447a-117">Настройка временной границы утвержденных заявок для группы покрытия</span><span class="sxs-lookup"><span data-stu-id="5447a-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="5447a-118">Выберите **Сводное планирование** \> **Настройка** \> **Покрытие** \> **Группа покрытия**.</span><span class="sxs-lookup"><span data-stu-id="5447a-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage group**.</span></span>
1. <span data-ttu-id="5447a-119">Создайте или выберите группу покрытия.</span><span class="sxs-lookup"><span data-stu-id="5447a-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="5447a-120">На экспресс-вкладке **Прочее** установите в поле **Временная граница утвержденных заявок (дни)** число дней, которое будет включено во временную границу.</span><span class="sxs-lookup"><span data-stu-id="5447a-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="5447a-121">Повторите шаги 2 и 3 для каждой дополнительной группы покрытия, в которой необходимо настроить временную границу утвержденных заявок.</span><span class="sxs-lookup"><span data-stu-id="5447a-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="5447a-122">Настройка временной границы утвержденных заявок для отдельных сводных планов</span><span class="sxs-lookup"><span data-stu-id="5447a-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="5447a-123">При настройке временных границ утвержденных заявок для отдельного сводного плана этот параметр переопределяет настройку временных границ для любой применимой группы покрытия.</span><span class="sxs-lookup"><span data-stu-id="5447a-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="5447a-124">Выберите **Сводное планирование** \> **Настройка** \> **Планы** \> **Сводные планы**.</span><span class="sxs-lookup"><span data-stu-id="5447a-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="5447a-125">Создайте или выберите сводный план.</span><span class="sxs-lookup"><span data-stu-id="5447a-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="5447a-126">На экспресс-вкладке **Временные границы в днях** установите в поле **Временная граница утвержденных заявок (дни)** число дней, которое будет включено во временную границу.</span><span class="sxs-lookup"><span data-stu-id="5447a-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="5447a-127">Повторите шаги 2 и 3 для каждого дополнительного сводного плана, в котором необходимо настроить временную границу утвержденных заявок.</span><span class="sxs-lookup"><span data-stu-id="5447a-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5447a-128">**Скоро появится:** временные границы утвержденных заявок еще не поддерживаются для оптимизации планирования.</span><span class="sxs-lookup"><span data-stu-id="5447a-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="5447a-129">Пока они не будут поддерживаемыми, все значения, введенные в поле **Временная граница утвержденных заявок (дни)**, будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="5447a-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="5447a-130">Независимые поставки, независимо от кода покрытия</span><span class="sxs-lookup"><span data-stu-id="5447a-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="5447a-131">Заявки на закупку всегда покрываются независимыми спланированными заказами, независимо от кода покрытия.</span><span class="sxs-lookup"><span data-stu-id="5447a-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="5447a-132">Таким образом обеспечивается четкая трассировка и рабочие потоки между заявками на закупку и заказами на пополнение запасов.</span><span class="sxs-lookup"><span data-stu-id="5447a-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="5447a-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5447a-133">Example 1</span></span>

<span data-ttu-id="5447a-134">Продукт настраивается таким образом, чтобы он имел значение **Код покрытия**, равное *Мин./Макс.* Он имеет следующие статусы запасов и заявки:</span><span class="sxs-lookup"><span data-stu-id="5447a-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="5447a-135">Количество запасов в наличии = 10.</span><span class="sxs-lookup"><span data-stu-id="5447a-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="5447a-136">Минимальное количество запасов = 15.</span><span class="sxs-lookup"><span data-stu-id="5447a-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="5447a-137">Максимальное количество запасов = 20.</span><span class="sxs-lookup"><span data-stu-id="5447a-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="5447a-138">Существует заявка на закупку для одной штуки.</span><span class="sxs-lookup"><span data-stu-id="5447a-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="5447a-139">Она имеет запрошенную дату сегодня.</span><span class="sxs-lookup"><span data-stu-id="5447a-139">It has a requested date of today.</span></span>

<span data-ttu-id="5447a-140">При выполнении сводного планирования создаются два спланированных заказа: один на 10 штук, чтобы пополнять запасы до максимального количества, а один на одну штуку для пополнения заявки на закупку.</span><span class="sxs-lookup"><span data-stu-id="5447a-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="5447a-141">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5447a-141">Example 2</span></span>

<span data-ttu-id="5447a-142">Продукт настраивается таким образом, чтобы он имел значение **Код покрытия**, равное *Мин./Макс.* Он имеет следующие статусы запасов и заявки:</span><span class="sxs-lookup"><span data-stu-id="5447a-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="5447a-143">Количество запасов в наличии = 17.</span><span class="sxs-lookup"><span data-stu-id="5447a-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="5447a-144">Минимальное количество запасов = 15.</span><span class="sxs-lookup"><span data-stu-id="5447a-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="5447a-145">Максимальное количество запасов = 20.</span><span class="sxs-lookup"><span data-stu-id="5447a-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="5447a-146">Существует заявка на закупку для одной штуки.</span><span class="sxs-lookup"><span data-stu-id="5447a-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="5447a-147">Она имеет запрошенную дату сегодня.</span><span class="sxs-lookup"><span data-stu-id="5447a-147">It has a requested date of today.</span></span>

<span data-ttu-id="5447a-148">При выполнении сводного планирования создается один спланированный заказ для одной штуки, чтобы пополнять заявку на закупку.</span><span class="sxs-lookup"><span data-stu-id="5447a-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="5447a-149">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5447a-149">Example 3</span></span>

<span data-ttu-id="5447a-150">Продукт настраивается таким образом, чтобы у него было значение **Код покрытия**, равное *Период* и длина периода составляет семь дней.</span><span class="sxs-lookup"><span data-stu-id="5447a-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="5447a-151">Он имеет следующие статусы запасов, заказа на продажу и заявки:</span><span class="sxs-lookup"><span data-stu-id="5447a-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="5447a-152">Количество запасов в наличии = 0.</span><span class="sxs-lookup"><span data-stu-id="5447a-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="5447a-153">Заказ на продажу для пяти штук существует.</span><span class="sxs-lookup"><span data-stu-id="5447a-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="5447a-154">Он имеет ожидаемую дату отгрузки сегодня плюс один день.</span><span class="sxs-lookup"><span data-stu-id="5447a-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="5447a-155">Существует заявка на закупку для трех штук.</span><span class="sxs-lookup"><span data-stu-id="5447a-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="5447a-156">Она имеет запрошенную дату сегодня плюс три дня.</span><span class="sxs-lookup"><span data-stu-id="5447a-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="5447a-157">При выполнении сводного планирования создаются два спланированных заказа: один на три штуки, чтобы пополнять заявку на закупку, один на пять штук для пополнения спроса заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5447a-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="5447a-158">После утверждения спланированного заказа, прикрепленного к заявке на закупку, механизм планирования сохраняет закрепление к заявке на закупку.</span><span class="sxs-lookup"><span data-stu-id="5447a-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="5447a-159">Если в дальнейшем будет обнаружено, что утвержденный заказ не содержит некоторого количества, необходимого для удовлетворения заявки на закупку, система создаст новый спланированный заказ для этой разницы.</span><span class="sxs-lookup"><span data-stu-id="5447a-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="5447a-160">Дополнительные общие сведения о заявках на закупку см. в разделе [Обзор заявок на закупку](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5447a-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>
