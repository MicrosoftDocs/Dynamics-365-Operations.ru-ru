---
title: Консолидируйте отгрузки, используя Запуск на склад из рабочего места планирования загрузки
description: В этом разделе представлен сценарий, в котором несколько заказов запущены на склад в одной и той же загрузке, а затем автоматически консолидируются в отгрузки.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c0af6764742532cbe181c8a20e7bf783b0e6d7cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983100"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="3b841-103">Консолидируйте отгрузки, используя Запуск на склад из рабочего места планирования загрузки</span><span class="sxs-lookup"><span data-stu-id="3b841-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b841-104">В этом разделе представлен сценарий, в котором несколько заказов запущены на склад в одной и той же загрузке, а затем автоматически консолидируются в отгрузки.</span><span class="sxs-lookup"><span data-stu-id="3b841-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="3b841-105">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="3b841-105">Make demo data available</span></span>

<span data-ttu-id="3b841-106">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3b841-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3b841-107">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="3b841-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="3b841-108">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="3b841-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="3b841-109">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="3b841-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="3b841-110">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="3b841-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="3b841-111">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="3b841-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="3b841-112">Начнем с создания набора заказов на продажу, с которыми можно работать.</span><span class="sxs-lookup"><span data-stu-id="3b841-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="3b841-113">Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS).</span><span class="sxs-lookup"><span data-stu-id="3b841-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="3b841-114">За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.</span><span class="sxs-lookup"><span data-stu-id="3b841-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="3b841-115">Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="3b841-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="3b841-116">Создать набор заказов 1</span><span class="sxs-lookup"><span data-stu-id="3b841-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="3b841-117">Заказ на продажу 1-1</span><span class="sxs-lookup"><span data-stu-id="3b841-117">Sales order 1-1</span></span>

1. <span data-ttu-id="3b841-118">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="3b841-119">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3b841-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3b841-120">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3b841-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3b841-121">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-122">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-123">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-124">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="3b841-125">Заказ на продажу 1-2</span><span class="sxs-lookup"><span data-stu-id="3b841-125">Sales order 1-2</span></span>

1. <span data-ttu-id="3b841-126">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="3b841-127">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3b841-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3b841-128">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3b841-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3b841-129">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-130">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-131">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-132">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="3b841-133">Заказ на продажу 1-3</span><span class="sxs-lookup"><span data-stu-id="3b841-133">Sales order 1-3</span></span>

1. <span data-ttu-id="3b841-134">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="3b841-135">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3b841-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3b841-136">**Способ поставки:** *10*</span><span class="sxs-lookup"><span data-stu-id="3b841-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="3b841-137">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-138">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-139">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-140">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="3b841-141">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-142">**Код номенклатуры:** *A0002* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-143">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="3b841-144">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3b841-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3b841-145">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="3b841-146">Создать набор заказов 2</span><span class="sxs-lookup"><span data-stu-id="3b841-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="3b841-147">Заказы на продажу 2-1 и 2-2</span><span class="sxs-lookup"><span data-stu-id="3b841-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="3b841-148">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-149">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="3b841-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="3b841-150">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-151">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="3b841-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="3b841-152">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-153">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="3b841-154">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-155">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="3b841-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="3b841-156">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="3b841-157">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3b841-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3b841-158">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="3b841-159">Создать набор заказов 3</span><span class="sxs-lookup"><span data-stu-id="3b841-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="3b841-160">Заказы на продажу 3-1 и 3-2</span><span class="sxs-lookup"><span data-stu-id="3b841-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="3b841-161">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-162">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3b841-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3b841-163">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="3b841-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="3b841-164">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-165">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-166">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-167">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="3b841-168">Заказы на продажу 3-3 и 3-4</span><span class="sxs-lookup"><span data-stu-id="3b841-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="3b841-169">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-170">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3b841-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3b841-171">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="3b841-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="3b841-172">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-173">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-174">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-175">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="3b841-176">Создать набор заказов 4</span><span class="sxs-lookup"><span data-stu-id="3b841-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="3b841-177">Заказы на продажу 4-1 и 4-2</span><span class="sxs-lookup"><span data-stu-id="3b841-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="3b841-178">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-179">**Счет клиента:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="3b841-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="3b841-180">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-181">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-182">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-183">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="3b841-184">Заказы на продажу 4-3 и 4-4</span><span class="sxs-lookup"><span data-stu-id="3b841-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="3b841-185">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-186">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="3b841-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="3b841-187">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-188">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-189">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-190">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="3b841-191">Заказы на продажу 4-5 и 4-6</span><span class="sxs-lookup"><span data-stu-id="3b841-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="3b841-192">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-193">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3b841-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="3b841-194">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3b841-194">**Site:** *6*</span></span>
    - <span data-ttu-id="3b841-195">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="3b841-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="3b841-196">**Кластер:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="3b841-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="3b841-197">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-198">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-199">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-200">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="3b841-201">Заказы на продажу 4-7 и 4-8</span><span class="sxs-lookup"><span data-stu-id="3b841-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="3b841-202">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3b841-203">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3b841-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="3b841-204">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3b841-204">**Site:** *6*</span></span>
    - <span data-ttu-id="3b841-205">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="3b841-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="3b841-206">**Кластер:** Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="3b841-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="3b841-207">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3b841-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3b841-208">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3b841-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3b841-209">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3b841-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3b841-210">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3b841-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="3b841-211">Используйте рабочее место планирования загрузки для создания загрузок и их запуска на склад</span><span class="sxs-lookup"><span data-stu-id="3b841-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="3b841-212">Выполните следующие действия, чтобы создать загрузку для каждого набора заказов, созданного для этого сценария, а затем запустите на склад.</span><span class="sxs-lookup"><span data-stu-id="3b841-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="3b841-213">Перейдите в раздел **Управление складом \> Загрузки \> Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="3b841-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="3b841-214">На вкладке **строки продаж** найдите и выберите все строки заказа на продажу из одного из наборов заказов, созданных для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="3b841-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="3b841-215">На панели операций на вкладке **поставка и спрос** выберите **Добавить \> В новую загрузку**, чтобы добавить выбранные строки заказа в новую загрузку.</span><span class="sxs-lookup"><span data-stu-id="3b841-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="3b841-216">В диалоговом окне **Назначение шаблона загрузки** в поле **Код шаблона загрузки** выберите шаблон загрузки, например *Stnd Load Template*.</span><span class="sxs-lookup"><span data-stu-id="3b841-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="3b841-217">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3b841-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="3b841-218">В разделе **Загрузки** найдите и выберите только что созданную загрузку.</span><span class="sxs-lookup"><span data-stu-id="3b841-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="3b841-219">Выберите **Запуск \> Запуск на склад**, чтобы запустить выбранную загрузку на склад.</span><span class="sxs-lookup"><span data-stu-id="3b841-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="3b841-220">Повторите эту процедуру для других трех наборов заказов, созданных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="3b841-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="3b841-221">Проверка отгрузок</span><span class="sxs-lookup"><span data-stu-id="3b841-221">Verify the shipments</span></span>

<span data-ttu-id="3b841-222">Следующая процедура позволяет проверить отгрузки, которые были созданы или обновлены в результате консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="3b841-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="3b841-223">Используйте его для просмотра каждого набора заказов, созданного для данного сценария, а затем просмотрите подразделы, которые следуют за тем, чтобы убедиться, что получены ожидаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="3b841-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="3b841-224">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="3b841-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="3b841-225">Найдите и выберите нужную отгрузку.</span><span class="sxs-lookup"><span data-stu-id="3b841-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="3b841-226">Если при создании или обновлении отгрузки была использована политика консолидации, ее можно увидеть в поле **Политика консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="3b841-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="3b841-227">Запуск набора заказов 1 в одной загрузке</span><span class="sxs-lookup"><span data-stu-id="3b841-227">Release order set 1 in one load</span></span>

<span data-ttu-id="3b841-228">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3b841-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="3b841-229">Первая отгрузка содержит три строки и была создана с помощью политики консолидации отгрузок *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="3b841-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="3b841-230">Вторая отгрузка, которая не использует режим транспортировки *Airways* поставки, была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="3b841-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="3b841-231">Запуск набора заказов 2 в одной загрузке</span><span class="sxs-lookup"><span data-stu-id="3b841-231">Release order set 2 in one load</span></span>

<span data-ttu-id="3b841-232">Должны быть созданы три отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3b841-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="3b841-233">Первая отгрузка содержит номенклатуры *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="3b841-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="3b841-234">Каждая из двух других отгрузок содержит одну строку, которая имеет номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="3b841-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="3b841-235">Запуск набора заказов 3 в одной загрузке</span><span class="sxs-lookup"><span data-stu-id="3b841-235">Release order set 3 in one load</span></span>

<span data-ttu-id="3b841-236">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3b841-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="3b841-237">Первая отгрузка содержит строки заказа из заказа на продажу, для которого в поле **Заявка клиента** указано значение *1*.</span><span class="sxs-lookup"><span data-stu-id="3b841-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="3b841-238">Вторая отгрузка содержит строки заказа из заказа на продажу, для которого в поле **Заявка клиента** указано значение *2*.</span><span class="sxs-lookup"><span data-stu-id="3b841-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="3b841-239">Запуск набора заказов 4 в одной загрузке</span><span class="sxs-lookup"><span data-stu-id="3b841-239">Release order set 4 in one load</span></span>

<span data-ttu-id="3b841-240">Должны быть созданы четыре отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3b841-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="3b841-241">Строки из двух заказов для счета клиента *US-003* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="3b841-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="3b841-242">Строки из двух заказов для счета клиента *US-004* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="3b841-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="3b841-243">Строки из заказов на продажу 4-5 и 4-6 для счета клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="3b841-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="3b841-244">Строки из заказов на продажу 4-7 и 4-8 для счета клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="3b841-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b841-245">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b841-245">Additional resources</span></span>

- [<span data-ttu-id="3b841-246">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="3b841-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="3b841-247">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="3b841-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
