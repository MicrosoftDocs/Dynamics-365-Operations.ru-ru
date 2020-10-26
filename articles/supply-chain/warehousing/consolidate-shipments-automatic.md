---
title: Консолидируйте отгрузки, когда они выпускаются на склад, используя автоматический запуск заказов на продажу
description: В этом разделе представлен сценарий, в котором несколько заказов запущены на склад в одной периодической автоматической выпуске на склад.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f4d095456435a3401daa173d79b80b81176a3c17
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987126"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="87ad1-103">Консолидируйте отгрузки, когда они выпускаются на склад, используя автоматический запуск заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="87ad1-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87ad1-104">В этом разделе представлен сценарий, в котором несколько заказов запущены на склад в одной периодической автоматической выпуске на склад.</span><span class="sxs-lookup"><span data-stu-id="87ad1-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="87ad1-105">Заказы будут автоматически консолидированы в отгрузки на основе правил, определенных как политики консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="87ad1-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="87ad1-106">В ходе сценария будут созданы наборы заказов на продажу, и каждый из них будет выпущен на склад.</span><span class="sxs-lookup"><span data-stu-id="87ad1-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="87ad1-107">Затем будут просмотрены отгрузки, созданные или обновленные в ходе консолидации отгрузок на основе настроенных политик.</span><span class="sxs-lookup"><span data-stu-id="87ad1-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="87ad1-108">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="87ad1-108">Make demo data available</span></span>

<span data-ttu-id="87ad1-109">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="87ad1-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="87ad1-110">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="87ad1-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="87ad1-111">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="87ad1-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="87ad1-112">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="87ad1-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="87ad1-113">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="87ad1-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="87ad1-114">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="87ad1-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="87ad1-115">Начнем с создания набора заказов на продажу, с которыми можно работать.</span><span class="sxs-lookup"><span data-stu-id="87ad1-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="87ad1-116">Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS).</span><span class="sxs-lookup"><span data-stu-id="87ad1-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="87ad1-117">За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.</span><span class="sxs-lookup"><span data-stu-id="87ad1-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="87ad1-118">Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="87ad1-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="87ad1-119">Создать набор заказов 1</span><span class="sxs-lookup"><span data-stu-id="87ad1-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="87ad1-120">Заказ на продажу 1-1</span><span class="sxs-lookup"><span data-stu-id="87ad1-120">Sales order 1-1</span></span>

1. <span data-ttu-id="87ad1-121">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-122">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="87ad1-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="87ad1-123">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="87ad1-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="87ad1-124">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-125">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-126">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="87ad1-127">Заказ на продажу 1-2</span><span class="sxs-lookup"><span data-stu-id="87ad1-127">Sales order 1-2</span></span>

1. <span data-ttu-id="87ad1-128">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-129">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="87ad1-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="87ad1-130">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="87ad1-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="87ad1-131">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-132">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-133">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="87ad1-134">Заказ на продажу 1-3</span><span class="sxs-lookup"><span data-stu-id="87ad1-134">Sales order 1-3</span></span>

1. <span data-ttu-id="87ad1-135">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-136">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="87ad1-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="87ad1-137">**Способ поставки:** *10*</span><span class="sxs-lookup"><span data-stu-id="87ad1-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="87ad1-138">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-139">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-140">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="87ad1-141">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-142">**Код номенклатуры:** *A0002* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-143">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="87ad1-144">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="87ad1-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="87ad1-145">Создать набор заказов 2</span><span class="sxs-lookup"><span data-stu-id="87ad1-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="87ad1-146">Заказы на продажу 2-1 и 2-2</span><span class="sxs-lookup"><span data-stu-id="87ad1-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="87ad1-147">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="87ad1-148">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="87ad1-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="87ad1-149">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-150">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="87ad1-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="87ad1-151">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="87ad1-152">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-153">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="87ad1-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="87ad1-154">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="87ad1-155">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="87ad1-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="87ad1-156">Создать набор заказов 3</span><span class="sxs-lookup"><span data-stu-id="87ad1-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="87ad1-157">Заказ на продажу 3-1</span><span class="sxs-lookup"><span data-stu-id="87ad1-157">Sales order 3-1</span></span>

1. <span data-ttu-id="87ad1-158">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-159">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="87ad1-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="87ad1-160">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-161">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="87ad1-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="87ad1-162">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="87ad1-163">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-164">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="87ad1-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="87ad1-165">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="87ad1-166">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="87ad1-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="87ad1-167">Этот заказ идентичен двум заказам, созданным для набора заказов 2.</span><span class="sxs-lookup"><span data-stu-id="87ad1-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="87ad1-168">Однако он указан как свой собственный порядок, так как он будет выводиться отдельно позже в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="87ad1-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="87ad1-169">Создать набор заказов 4</span><span class="sxs-lookup"><span data-stu-id="87ad1-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="87ad1-170">Заказ на продажу 4-1</span><span class="sxs-lookup"><span data-stu-id="87ad1-170">Sales order 4-1</span></span>

1. <span data-ttu-id="87ad1-171">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-172">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="87ad1-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="87ad1-173">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="87ad1-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="87ad1-174">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-175">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-176">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="87ad1-177">Создать набор заказов 5</span><span class="sxs-lookup"><span data-stu-id="87ad1-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="87ad1-178">Заказы на продажу 5-1 и 5-2</span><span class="sxs-lookup"><span data-stu-id="87ad1-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="87ad1-179">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="87ad1-180">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="87ad1-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="87ad1-181">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="87ad1-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="87ad1-182">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-183">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-184">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="87ad1-185">Заказ на продажу 5-3</span><span class="sxs-lookup"><span data-stu-id="87ad1-185">Sales order 5-3</span></span>

1. <span data-ttu-id="87ad1-186">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-187">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="87ad1-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="87ad1-188">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="87ad1-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="87ad1-189">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-190">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-191">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="87ad1-192">Создать набор заказов 6</span><span class="sxs-lookup"><span data-stu-id="87ad1-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="87ad1-193">Заказы на продажу 6-1 и 6-2</span><span class="sxs-lookup"><span data-stu-id="87ad1-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="87ad1-194">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="87ad1-195">**Счет клиента:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="87ad1-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="87ad1-196">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="87ad1-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="87ad1-197">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-198">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-199">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="87ad1-200">Заказы на продажу 6-3 и 6-4</span><span class="sxs-lookup"><span data-stu-id="87ad1-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="87ad1-201">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="87ad1-202">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="87ad1-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="87ad1-203">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="87ad1-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="87ad1-204">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-205">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-206">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="87ad1-207">Заказы на продажу 6-5 и 6-6</span><span class="sxs-lookup"><span data-stu-id="87ad1-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="87ad1-208">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="87ad1-209">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="87ad1-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="87ad1-210">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="87ad1-210">**Site:** *6*</span></span>
    - <span data-ttu-id="87ad1-211">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="87ad1-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="87ad1-212">**Кластер:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="87ad1-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="87ad1-213">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-214">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-215">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="87ad1-216">Заказы на продажу 6-7 и 6-8</span><span class="sxs-lookup"><span data-stu-id="87ad1-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="87ad1-217">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="87ad1-218">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="87ad1-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="87ad1-219">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="87ad1-219">**Site:** *6*</span></span>
    - <span data-ttu-id="87ad1-220">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="87ad1-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="87ad1-221">**Кластер:** Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="87ad1-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="87ad1-222">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="87ad1-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="87ad1-223">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="87ad1-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="87ad1-224">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="87ad1-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="87ad1-225">Автоматический выпуск заказов на продажу на склад</span><span class="sxs-lookup"><span data-stu-id="87ad1-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="87ad1-226">Для каждого набора заказов на продажу, созданного ранее, необходимо выполнить процедуру автоматического запуска на склад.</span><span class="sxs-lookup"><span data-stu-id="87ad1-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="87ad1-227">В каждом случае будет выполняться [базовая процедура запуска на склад](#release-procedure), предоставляемая здесь.</span><span class="sxs-lookup"><span data-stu-id="87ad1-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="87ad1-228">Обычная процедура запуска на склад</span><span class="sxs-lookup"><span data-stu-id="87ad1-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="87ad1-229">Для каждого набора заказов на продажу, созданного ранее, необходимо выполнить три процедуры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="87ad1-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="87ad1-230">Обновление шаблона волн, который будет использоваться в процессе запуска</span><span class="sxs-lookup"><span data-stu-id="87ad1-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="87ad1-231">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="87ad1-232">Задайте в поле **Тип шаблона волн** значение *отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="87ad1-233">Найдите и выберите шаблон волн, связанный со складом, который использовался в наборах заказов, созданных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="87ad1-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="87ad1-234">Например, если был использован склад *24*, выберите шаблон волн **24 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="87ad1-235">Если был использован склад *61*, выберите шаблон волн **61 Отгрузка**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="87ad1-236">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="87ad1-237">Установите для параметра **Обрабатывать волну перед запуском на склад** значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="87ad1-238">Запуск на склад</span><span class="sxs-lookup"><span data-stu-id="87ad1-238">Release to the warehouse</span></span>

1. <span data-ttu-id="87ad1-239">Перейдите на **Управление складом \> Запуск на склад \> Автоматический выпуск заказов на продажу**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="87ad1-240">В поле **количество к запуску** выберите *все*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="87ad1-241">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно запроса.</span><span class="sxs-lookup"><span data-stu-id="87ad1-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="87ad1-242">На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку со следующими настройками в сетку:</span><span class="sxs-lookup"><span data-stu-id="87ad1-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="87ad1-243">**Таблица:** *Заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="87ad1-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="87ad1-244">**Производная таблица:** *Заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="87ad1-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="87ad1-245">**Поля** — *заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="87ad1-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="87ad1-246">**Критерий:** Введите список номеров заказов на продажу через запятую из нужного набора заказов.</span><span class="sxs-lookup"><span data-stu-id="87ad1-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="87ad1-247">Нажмите кнопку **ОК** , чтобы сохранить запрос.</span><span class="sxs-lookup"><span data-stu-id="87ad1-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="87ad1-248">Нажмите кнопку **ОК** , чтобы запустить процедуру *Автоматический запуск в на склад*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="87ad1-249">Просмотр созданного или обновленного отгрузки</span><span class="sxs-lookup"><span data-stu-id="87ad1-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="87ad1-250">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="87ad1-251">Найдите и выберите нужную отгрузку.</span><span class="sxs-lookup"><span data-stu-id="87ad1-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="87ad1-252">Если при создании или обновлении отгрузки была использована политика консолидации, ее можно увидеть в поле **Политика консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="87ad1-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="87ad1-253">Запуск заказов на продажу из набора заказов 1</span><span class="sxs-lookup"><span data-stu-id="87ad1-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="87ad1-254">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 1.</span><span class="sxs-lookup"><span data-stu-id="87ad1-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="87ad1-255">После завершения следует увидеть, что были созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="87ad1-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="87ad1-256">Первая отгрузка содержит три строки и была создана с помощью политики консолидации отгрузок *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="87ad1-257">Вторая отгрузка, которая не использует режим транспортировки *Airways* поставки, была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="87ad1-258">Запуск заказов на продажу из набора заказов 2</span><span class="sxs-lookup"><span data-stu-id="87ad1-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="87ad1-259">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 2.</span><span class="sxs-lookup"><span data-stu-id="87ad1-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="87ad1-260">После завершения следует увидеть, что были созданы три отгрузки:</span><span class="sxs-lookup"><span data-stu-id="87ad1-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="87ad1-261">Первая отгрузка содержит номенклатуры *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="87ad1-262">Каждая из двух других отгрузок содержит одну строку, которая имеет номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="87ad1-263">Запуск заказов на продажу из набора заказов 3</span><span class="sxs-lookup"><span data-stu-id="87ad1-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="87ad1-264">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 3.</span><span class="sxs-lookup"><span data-stu-id="87ad1-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="87ad1-265">После завершения вы увидите, что выполнены следующие действия:</span><span class="sxs-lookup"><span data-stu-id="87ad1-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="87ad1-266">Была обновлена одна отгрузка (отгрузка, созданная, когда заказ на набор 2 был запущен на склад).</span><span class="sxs-lookup"><span data-stu-id="87ad1-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="87ad1-267">Была добавлена строка с номенклатурой *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="87ad1-268">Была создана одна новая отгрузка, содержащая номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="87ad1-269">Запуск заказов на продажу из набора заказов 4</span><span class="sxs-lookup"><span data-stu-id="87ad1-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="87ad1-270">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 4.</span><span class="sxs-lookup"><span data-stu-id="87ad1-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="87ad1-271">После завершения следует увидеть, что одна существующая отгрузка (в поле **Заявка клиента** установлена на *1*) обновлена.</span><span class="sxs-lookup"><span data-stu-id="87ad1-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="87ad1-272">К ней была добавлена одна новая строка.</span><span class="sxs-lookup"><span data-stu-id="87ad1-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="87ad1-273">Запуск заказов на продажу из набора заказов 5</span><span class="sxs-lookup"><span data-stu-id="87ad1-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="87ad1-274">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 5.</span><span class="sxs-lookup"><span data-stu-id="87ad1-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="87ad1-275">После завершения вы увидите, что выполнены следующие действия:</span><span class="sxs-lookup"><span data-stu-id="87ad1-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="87ad1-276">Обновлена одна существующая отгрузка (где в поле **заявки клиента** установлено значение *1*).</span><span class="sxs-lookup"><span data-stu-id="87ad1-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="87ad1-277">В нее было добавлено строка из заказа на продажу 5-3 (где поле **Заявка клиента** установлено на *1*).</span><span class="sxs-lookup"><span data-stu-id="87ad1-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="87ad1-278">Была создана одна новая отгрузка, в которой строки из заказов на продажу 5-1 и 5-2 группируются в одну отгрузку.</span><span class="sxs-lookup"><span data-stu-id="87ad1-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="87ad1-279">Запуск заказов на продажу из набора заказов 6</span><span class="sxs-lookup"><span data-stu-id="87ad1-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="87ad1-280">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 6.</span><span class="sxs-lookup"><span data-stu-id="87ad1-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="87ad1-281">После завершения следует увидеть, что были созданы четыре отгрузки:</span><span class="sxs-lookup"><span data-stu-id="87ad1-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="87ad1-282">Строки из двух заказов для клиента *US-003* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="87ad1-283">Строки из двух заказов для клиента *US-004* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="87ad1-284">Строки из заказов на продажу 6-5 и 6-6 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="87ad1-285">Строки из заказов на продажу 6-7 и 6-8 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="87ad1-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87ad1-286">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87ad1-286">Additional resources</span></span>

- [<span data-ttu-id="87ad1-287">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="87ad1-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="87ad1-288">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="87ad1-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
