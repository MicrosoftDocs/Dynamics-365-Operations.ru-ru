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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 376c7418b61c0192f9071a879b50b9ece7699894
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970364"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="d73b0-103">Консолидируйте отгрузки, когда они выпускаются на склад, используя автоматический запуск заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="d73b0-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d73b0-104">В этом разделе представлен сценарий, в котором несколько заказов запущены на склад в одной периодической автоматической выпуске на склад.</span><span class="sxs-lookup"><span data-stu-id="d73b0-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="d73b0-105">Заказы будут автоматически консолидированы в отгрузки на основе правил, определенных как политики консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="d73b0-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="d73b0-106">В ходе сценария будут созданы наборы заказов на продажу, и каждый из них будет выпущен на склад.</span><span class="sxs-lookup"><span data-stu-id="d73b0-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="d73b0-107">Затем будут просмотрены отгрузки, созданные или обновленные в ходе консолидации отгрузок на основе настроенных политик.</span><span class="sxs-lookup"><span data-stu-id="d73b0-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="d73b0-108">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="d73b0-108">Make demo data available</span></span>

<span data-ttu-id="d73b0-109">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d73b0-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d73b0-110">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="d73b0-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="d73b0-111">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="d73b0-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="d73b0-112">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="d73b0-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="d73b0-113">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="d73b0-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="d73b0-114">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="d73b0-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="d73b0-115">Начнем с создания набора заказов на продажу, с которыми можно работать.</span><span class="sxs-lookup"><span data-stu-id="d73b0-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="d73b0-116">Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS).</span><span class="sxs-lookup"><span data-stu-id="d73b0-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="d73b0-117">За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.</span><span class="sxs-lookup"><span data-stu-id="d73b0-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="d73b0-118">Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="d73b0-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="d73b0-119">Создать набор заказов 1</span><span class="sxs-lookup"><span data-stu-id="d73b0-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="d73b0-120">Заказ на продажу 1-1</span><span class="sxs-lookup"><span data-stu-id="d73b0-120">Sales order 1-1</span></span>

1. <span data-ttu-id="d73b0-121">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-122">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d73b0-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d73b0-123">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d73b0-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="d73b0-124">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-125">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-126">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="d73b0-127">Заказ на продажу 1-2</span><span class="sxs-lookup"><span data-stu-id="d73b0-127">Sales order 1-2</span></span>

1. <span data-ttu-id="d73b0-128">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-129">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d73b0-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d73b0-130">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d73b0-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="d73b0-131">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-132">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-133">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="d73b0-134">Заказ на продажу 1-3</span><span class="sxs-lookup"><span data-stu-id="d73b0-134">Sales order 1-3</span></span>

1. <span data-ttu-id="d73b0-135">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-136">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d73b0-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d73b0-137">**Способ поставки:** *10*</span><span class="sxs-lookup"><span data-stu-id="d73b0-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="d73b0-138">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-139">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-140">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d73b0-141">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-142">**Код номенклатуры:** *A0002* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-143">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="d73b0-144">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d73b0-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="d73b0-145">Создать набор заказов 2</span><span class="sxs-lookup"><span data-stu-id="d73b0-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="d73b0-146">Заказы на продажу 2-1 и 2-2</span><span class="sxs-lookup"><span data-stu-id="d73b0-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="d73b0-147">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d73b0-148">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d73b0-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="d73b0-149">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-150">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="d73b0-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="d73b0-151">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d73b0-152">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-153">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="d73b0-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="d73b0-154">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="d73b0-155">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d73b0-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="d73b0-156">Создать набор заказов 3</span><span class="sxs-lookup"><span data-stu-id="d73b0-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="d73b0-157">Заказ на продажу 3-1</span><span class="sxs-lookup"><span data-stu-id="d73b0-157">Sales order 3-1</span></span>

1. <span data-ttu-id="d73b0-158">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-159">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d73b0-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="d73b0-160">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-161">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="d73b0-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="d73b0-162">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d73b0-163">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-164">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="d73b0-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="d73b0-165">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="d73b0-166">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d73b0-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="d73b0-167">Этот заказ идентичен двум заказам, созданным для набора заказов 2.</span><span class="sxs-lookup"><span data-stu-id="d73b0-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="d73b0-168">Однако он указан как свой собственный порядок, так как он будет выводиться отдельно позже в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="d73b0-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="d73b0-169">Создать набор заказов 4</span><span class="sxs-lookup"><span data-stu-id="d73b0-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="d73b0-170">Заказ на продажу 4-1</span><span class="sxs-lookup"><span data-stu-id="d73b0-170">Sales order 4-1</span></span>

1. <span data-ttu-id="d73b0-171">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-172">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d73b0-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d73b0-173">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="d73b0-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="d73b0-174">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-175">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-176">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="d73b0-177">Создать набор заказов 5</span><span class="sxs-lookup"><span data-stu-id="d73b0-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="d73b0-178">Заказы на продажу 5-1 и 5-2</span><span class="sxs-lookup"><span data-stu-id="d73b0-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="d73b0-179">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d73b0-180">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d73b0-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d73b0-181">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="d73b0-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="d73b0-182">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-183">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-184">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="d73b0-185">Заказ на продажу 5-3</span><span class="sxs-lookup"><span data-stu-id="d73b0-185">Sales order 5-3</span></span>

1. <span data-ttu-id="d73b0-186">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-187">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d73b0-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d73b0-188">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="d73b0-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="d73b0-189">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-190">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-191">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="d73b0-192">Создать набор заказов 6</span><span class="sxs-lookup"><span data-stu-id="d73b0-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="d73b0-193">Заказы на продажу 6-1 и 6-2</span><span class="sxs-lookup"><span data-stu-id="d73b0-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="d73b0-194">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d73b0-195">**Счет клиента:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="d73b0-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="d73b0-196">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="d73b0-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="d73b0-197">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-198">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-199">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="d73b0-200">Заказы на продажу 6-3 и 6-4</span><span class="sxs-lookup"><span data-stu-id="d73b0-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="d73b0-201">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d73b0-202">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="d73b0-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="d73b0-203">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="d73b0-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="d73b0-204">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-205">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-206">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="d73b0-207">Заказы на продажу 6-5 и 6-6</span><span class="sxs-lookup"><span data-stu-id="d73b0-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="d73b0-208">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d73b0-209">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="d73b0-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="d73b0-210">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="d73b0-210">**Site:** *6*</span></span>
    - <span data-ttu-id="d73b0-211">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="d73b0-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="d73b0-212">**Кластер:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="d73b0-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="d73b0-213">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-214">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-215">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="d73b0-216">Заказы на продажу 6-7 и 6-8</span><span class="sxs-lookup"><span data-stu-id="d73b0-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="d73b0-217">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d73b0-218">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="d73b0-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="d73b0-219">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="d73b0-219">**Site:** *6*</span></span>
    - <span data-ttu-id="d73b0-220">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="d73b0-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="d73b0-221">**Кластер:** Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="d73b0-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="d73b0-222">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d73b0-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d73b0-223">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="d73b0-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d73b0-224">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d73b0-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="d73b0-225">Автоматический выпуск заказов на продажу на склад</span><span class="sxs-lookup"><span data-stu-id="d73b0-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="d73b0-226">Для каждого набора заказов на продажу, созданного ранее, необходимо выполнить процедуру автоматического запуска на склад.</span><span class="sxs-lookup"><span data-stu-id="d73b0-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="d73b0-227">В каждом случае будет выполняться [базовая процедура запуска на склад](#release-procedure), предоставляемая здесь.</span><span class="sxs-lookup"><span data-stu-id="d73b0-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="d73b0-228">Обычная процедура запуска на склад</span><span class="sxs-lookup"><span data-stu-id="d73b0-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="d73b0-229">Для каждого набора заказов на продажу, созданного ранее, необходимо выполнить три процедуры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="d73b0-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="d73b0-230">Обновление шаблона волн, который будет использоваться в процессе запуска</span><span class="sxs-lookup"><span data-stu-id="d73b0-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="d73b0-231">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="d73b0-232">Задайте в поле **Тип шаблона волн** значение *отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="d73b0-233">Найдите и выберите шаблон волн, связанный со складом, который использовался в наборах заказов, созданных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="d73b0-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="d73b0-234">Например, если был использован склад *24*, выберите шаблон волн **24 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="d73b0-235">Если был использован склад *61*, выберите шаблон волн **61 Отгрузка**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="d73b0-236">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d73b0-237">Установите для параметра **Обрабатывать волну перед запуском на склад** значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="d73b0-238">Запуск на склад</span><span class="sxs-lookup"><span data-stu-id="d73b0-238">Release to the warehouse</span></span>

1. <span data-ttu-id="d73b0-239">Перейдите на **Управление складом \> Запуск на склад \> Автоматический выпуск заказов на продажу**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="d73b0-240">В поле **количество к запуску** выберите *все*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="d73b0-241">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно запроса.</span><span class="sxs-lookup"><span data-stu-id="d73b0-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="d73b0-242">На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку со следующими настройками в сетку:</span><span class="sxs-lookup"><span data-stu-id="d73b0-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="d73b0-243">**Таблица:** *Заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="d73b0-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="d73b0-244">**Производная таблица:** *Заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="d73b0-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="d73b0-245">**Поля** — *заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="d73b0-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="d73b0-246">**Критерий:** Введите список номеров заказов на продажу через запятую из нужного набора заказов.</span><span class="sxs-lookup"><span data-stu-id="d73b0-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="d73b0-247">Нажмите кнопку **ОК** , чтобы сохранить запрос.</span><span class="sxs-lookup"><span data-stu-id="d73b0-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="d73b0-248">Нажмите кнопку **ОК** , чтобы запустить процедуру *Автоматический запуск в на склад*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="d73b0-249">Просмотр созданного или обновленного отгрузки</span><span class="sxs-lookup"><span data-stu-id="d73b0-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="d73b0-250">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="d73b0-251">Найдите и выберите нужную отгрузку.</span><span class="sxs-lookup"><span data-stu-id="d73b0-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="d73b0-252">Если при создании или обновлении отгрузки была использована политика консолидации, ее можно увидеть в поле **Политика консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="d73b0-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="d73b0-253">Запуск заказов на продажу из набора заказов 1</span><span class="sxs-lookup"><span data-stu-id="d73b0-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="d73b0-254">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 1.</span><span class="sxs-lookup"><span data-stu-id="d73b0-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="d73b0-255">После завершения следует увидеть, что были созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="d73b0-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="d73b0-256">Первая отгрузка содержит три строки и была создана с помощью политики консолидации отгрузок *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="d73b0-257">Вторая отгрузка, которая не использует режим транспортировки *Airways* поставки, была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="d73b0-258">Запуск заказов на продажу из набора заказов 2</span><span class="sxs-lookup"><span data-stu-id="d73b0-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="d73b0-259">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 2.</span><span class="sxs-lookup"><span data-stu-id="d73b0-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="d73b0-260">После завершения следует увидеть, что были созданы три отгрузки:</span><span class="sxs-lookup"><span data-stu-id="d73b0-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="d73b0-261">Первая отгрузка содержит номенклатуры *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="d73b0-262">Каждая из двух других отгрузок содержит одну строку, которая имеет номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="d73b0-263">Запуск заказов на продажу из набора заказов 3</span><span class="sxs-lookup"><span data-stu-id="d73b0-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="d73b0-264">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 3.</span><span class="sxs-lookup"><span data-stu-id="d73b0-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="d73b0-265">После завершения вы увидите, что выполнены следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d73b0-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="d73b0-266">Была обновлена одна отгрузка (отгрузка, созданная, когда заказ на набор 2 был запущен на склад).</span><span class="sxs-lookup"><span data-stu-id="d73b0-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="d73b0-267">Была добавлена строка с номенклатурой *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="d73b0-268">Была создана одна новая отгрузка, содержащая номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="d73b0-269">Запуск заказов на продажу из набора заказов 4</span><span class="sxs-lookup"><span data-stu-id="d73b0-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="d73b0-270">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 4.</span><span class="sxs-lookup"><span data-stu-id="d73b0-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="d73b0-271">После завершения следует увидеть, что одна существующая отгрузка (в поле **Заявка клиента** установлена на *1*) обновлена.</span><span class="sxs-lookup"><span data-stu-id="d73b0-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="d73b0-272">К ней была добавлена одна новая строка.</span><span class="sxs-lookup"><span data-stu-id="d73b0-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="d73b0-273">Запуск заказов на продажу из набора заказов 5</span><span class="sxs-lookup"><span data-stu-id="d73b0-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="d73b0-274">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 5.</span><span class="sxs-lookup"><span data-stu-id="d73b0-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="d73b0-275">После завершения вы увидите, что выполнены следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d73b0-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="d73b0-276">Обновлена одна существующая отгрузка (где в поле **заявки клиента** установлено значение *1*).</span><span class="sxs-lookup"><span data-stu-id="d73b0-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="d73b0-277">В нее было добавлено строка из заказа на продажу 5-3 (где поле **Заявка клиента** установлено на *1*).</span><span class="sxs-lookup"><span data-stu-id="d73b0-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="d73b0-278">Была создана одна новая отгрузка, в которой строки из заказов на продажу 5-1 и 5-2 группируются в одну отгрузку.</span><span class="sxs-lookup"><span data-stu-id="d73b0-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="d73b0-279">Запуск заказов на продажу из набора заказов 6</span><span class="sxs-lookup"><span data-stu-id="d73b0-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="d73b0-280">Выполните [базовую процедуру "Запуск в склад"](#release-procedure), чтобы выпустить заказы на продажу из набора заказов 6.</span><span class="sxs-lookup"><span data-stu-id="d73b0-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="d73b0-281">После завершения следует увидеть, что были созданы четыре отгрузки:</span><span class="sxs-lookup"><span data-stu-id="d73b0-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="d73b0-282">Строки из двух заказов для клиента *US-003* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="d73b0-283">Строки из двух заказов для клиента *US-004* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="d73b0-284">Строки из заказов на продажу 6-5 и 6-6 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="d73b0-285">Строки из заказов на продажу 6-7 и 6-8 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="d73b0-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d73b0-286">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d73b0-286">Additional resources</span></span>

- [<span data-ttu-id="d73b0-287">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="d73b0-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="d73b0-288">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="d73b0-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
