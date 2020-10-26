---
title: Консолидируйте отгрузки, используя рабочее место консолидации отгрузок
description: В этом разделе представлен сценарий, в котором несколько заказов запущены на склад, а затем консолидируются в отгрузки с помощью рабочее место консолидации отгрузок.
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
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8320c8aab82a39a8a5565e6b3e805e1065c67453
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986824"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="c44ad-103">Консолидируйте отгрузки, используя рабочее место консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="c44ad-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c44ad-104">В этом разделе представлен сценарий, в котором несколько заказов запущены на склад, а затем консолидируются в отгрузки с помощью рабочее место консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="c44ad-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c44ad-105">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="c44ad-105">Make demo data available</span></span>

<span data-ttu-id="c44ad-106">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c44ad-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c44ad-107">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="c44ad-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="c44ad-108">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="c44ad-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="c44ad-109">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="c44ad-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="c44ad-110">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="c44ad-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="c44ad-111">Включение функции консолидации отгрузок вручную</span><span class="sxs-lookup"><span data-stu-id="c44ad-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="c44ad-112">Прежде чем можно будет использовать функцию *Консолидация отгрузок вручную*, необходимо включить ее в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="c44ad-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="c44ad-113">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="c44ad-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c44ad-114">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c44ad-115">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="c44ad-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c44ad-116">**Имя функции:** *консолидация отгрузок вручную*</span><span class="sxs-lookup"><span data-stu-id="c44ad-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="c44ad-117">Как указано в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), необходимо также включить функцию *Консолидация отгрузок*, прежде чем можно будет создавать политики.</span><span class="sxs-lookup"><span data-stu-id="c44ad-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="c44ad-118">Однако этот шаг уже должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="c44ad-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="c44ad-119">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="c44ad-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="c44ad-120">Начнем с создания набора заказов на продажу, с которыми можно работать.</span><span class="sxs-lookup"><span data-stu-id="c44ad-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="c44ad-121">Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS).</span><span class="sxs-lookup"><span data-stu-id="c44ad-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="c44ad-122">За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.</span><span class="sxs-lookup"><span data-stu-id="c44ad-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="c44ad-123">Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="c44ad-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="c44ad-124">Создать набор заказов 1</span><span class="sxs-lookup"><span data-stu-id="c44ad-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="c44ad-125">Заказы на продажу 1-1 и 1-2</span><span class="sxs-lookup"><span data-stu-id="c44ad-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="c44ad-126">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-127">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c44ad-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c44ad-128">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c44ad-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c44ad-129">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-130">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-131">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-132">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="c44ad-133">Заказ на продажу 1-3</span><span class="sxs-lookup"><span data-stu-id="c44ad-133">Sales order 1-3</span></span>

1. <span data-ttu-id="c44ad-134">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-135">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c44ad-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c44ad-136">**Способ поставки:** *10*</span><span class="sxs-lookup"><span data-stu-id="c44ad-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="c44ad-137">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-138">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-139">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-140">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="c44ad-141">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-142">**Код номенклатуры:** *A0002* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-143">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c44ad-144">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c44ad-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c44ad-145">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="c44ad-146">Создать набор заказов 2</span><span class="sxs-lookup"><span data-stu-id="c44ad-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="c44ad-147">Заказы на продажу 2-1 и 2-2</span><span class="sxs-lookup"><span data-stu-id="c44ad-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="c44ad-148">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-149">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="c44ad-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="c44ad-150">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c44ad-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c44ad-151">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-152">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="c44ad-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="c44ad-153">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-154">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="c44ad-155">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-156">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="c44ad-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="c44ad-157">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c44ad-158">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c44ad-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c44ad-159">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="c44ad-160">Создать набор заказов 3</span><span class="sxs-lookup"><span data-stu-id="c44ad-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="c44ad-161">Заказы на продажу 3-1 и 3-2</span><span class="sxs-lookup"><span data-stu-id="c44ad-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="c44ad-162">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-163">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c44ad-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c44ad-164">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="c44ad-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="c44ad-165">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-166">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-167">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-168">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="c44ad-169">Заказы на продажу 3-3 и 3-4</span><span class="sxs-lookup"><span data-stu-id="c44ad-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="c44ad-170">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-171">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c44ad-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c44ad-172">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="c44ad-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="c44ad-173">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-174">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-175">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-176">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="c44ad-177">Создать набор заказов 4</span><span class="sxs-lookup"><span data-stu-id="c44ad-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="c44ad-178">Заказы на продажу 4-1 и 4-2</span><span class="sxs-lookup"><span data-stu-id="c44ad-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="c44ad-179">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-180">**Счет клиента:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="c44ad-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="c44ad-181">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-182">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-183">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-184">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="c44ad-185">Заказы на продажу 4-3 и 4-4</span><span class="sxs-lookup"><span data-stu-id="c44ad-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="c44ad-186">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-187">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="c44ad-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="c44ad-188">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-189">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-190">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-191">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="c44ad-192">Заказы на продажу 4-5 и 4-6</span><span class="sxs-lookup"><span data-stu-id="c44ad-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="c44ad-193">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-194">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c44ad-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c44ad-195">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="c44ad-195">**Site:** *6*</span></span>
    - <span data-ttu-id="c44ad-196">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="c44ad-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c44ad-197">**Кластер:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c44ad-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="c44ad-198">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-199">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-200">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-201">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="c44ad-202">Заказы на продажу 4-7 и 4-8</span><span class="sxs-lookup"><span data-stu-id="c44ad-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="c44ad-203">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c44ad-204">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c44ad-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c44ad-205">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="c44ad-205">**Site:** *6*</span></span>
    - <span data-ttu-id="c44ad-206">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="c44ad-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c44ad-207">**Кластер:** Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="c44ad-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="c44ad-208">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c44ad-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c44ad-209">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="c44ad-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c44ad-210">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c44ad-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c44ad-211">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="c44ad-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="c44ad-212">Запуск заказов на склад</span><span class="sxs-lookup"><span data-stu-id="c44ad-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="c44ad-213">Выполните следующие действия, чтобы запустить каждый заказ на продажу, созданный для этого сценария, на склад.</span><span class="sxs-lookup"><span data-stu-id="c44ad-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="c44ad-214">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c44ad-215">Найдите и выберите заказ на продажу, который требуется запустить.</span><span class="sxs-lookup"><span data-stu-id="c44ad-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="c44ad-216">На панели операций на вкладке **Склад** выберите вариант **Действия \> Запуск на склад**, чтобы запустить выбранный заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="c44ad-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="c44ad-217">Повторите эту процедуру для других заказов на продажу, созданных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="c44ad-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="c44ad-218">Консолидируйте отгрузки, используя рабочее место консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="c44ad-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="c44ad-219">Перейдите на страницу **Управление складом \> Запуск на склад \> Рабочее место консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="c44ad-220">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c44ad-221">В диалоговое окно редактора запросов на вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку со следующими настройками в сетку:</span><span class="sxs-lookup"><span data-stu-id="c44ad-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="c44ad-222">**Таблица:** *Заказы на продажу*</span><span class="sxs-lookup"><span data-stu-id="c44ad-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="c44ad-223">**Поля** — *заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="c44ad-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="c44ad-224">**Критерий:** Введите список номеров заказов на продажу с разделителями-запятыми для каждого набора заказов, созданного для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="c44ad-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="c44ad-225">Выберите **OK**, чтобы сохранить ваш запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c44ad-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="c44ad-226">На панели операций выберите **Консолидация отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="c44ad-227">Выберите все отгрузки, затем на панели операций выберите **Консолидировать**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="c44ad-228">Проверка отгрузок</span><span class="sxs-lookup"><span data-stu-id="c44ad-228">Verify the shipments</span></span>

<span data-ttu-id="c44ad-229">Следующая процедура позволяет проверить отгрузки, которые были созданы или обновлены в результате консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="c44ad-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="c44ad-230">Используйте его для просмотра каждого набора заказов, созданного для данного сценария, а затем просмотрите подразделы, которые следуют за тем, чтобы убедиться, что получены ожидаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="c44ad-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="c44ad-231">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c44ad-232">Найдите и выберите нужную отгрузку.</span><span class="sxs-lookup"><span data-stu-id="c44ad-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="c44ad-233">Если при создании или обновлении отгрузки была использована политика консолидации, ее можно увидеть в поле **Политика консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="c44ad-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="c44ad-234">Соответствующие отгрузки для набора заказов 1</span><span class="sxs-lookup"><span data-stu-id="c44ad-234">Related shipments for order set 1</span></span>

<span data-ttu-id="c44ad-235">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="c44ad-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="c44ad-236">Первая отгрузка содержит три строки и была создана с помощью политики консолидации отгрузок *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="c44ad-237">Вторая отгрузка, которая не использует режим транспортировки *Airways* поставки, была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="c44ad-238">Соответствующие отгрузки для набора заказов 2</span><span class="sxs-lookup"><span data-stu-id="c44ad-238">Related shipments for order set 2</span></span>

<span data-ttu-id="c44ad-239">Должны быть созданы три отгрузки:</span><span class="sxs-lookup"><span data-stu-id="c44ad-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="c44ad-240">Первая отгрузка содержит номенклатуры *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="c44ad-241">Каждая из двух других отгрузок содержит одну строку, которая имеет номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="c44ad-242">Соответствующие отгрузки для набора заказов 3</span><span class="sxs-lookup"><span data-stu-id="c44ad-242">Related shipments for order set 3</span></span>

<span data-ttu-id="c44ad-243">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="c44ad-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="c44ad-244">Первая отгрузка содержит строки заказа из заказа на продажу, для которого в поле **Заявка клиента** указано значение *1*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="c44ad-245">Вторая отгрузка содержит строки заказа из заказа на продажу, для которого в поле **Заявка клиента** указано значение *2*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="c44ad-246">Соответствующие отгрузки для набора заказов 4</span><span class="sxs-lookup"><span data-stu-id="c44ad-246">Related shipments for order set 4</span></span>

<span data-ttu-id="c44ad-247">Должны быть созданы четыре отгрузки:</span><span class="sxs-lookup"><span data-stu-id="c44ad-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="c44ad-248">Строки из двух заказов для клиента *US-003* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c44ad-249">Строки из двух заказов для клиента *US-004* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c44ad-250">Строки из заказов на продажу 4-5 и 4-6 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c44ad-251">Строки из заказов на продажу 4-7 и 4-8 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="c44ad-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c44ad-252">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c44ad-252">Additional resources</span></span>

- [<span data-ttu-id="c44ad-253">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="c44ad-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="c44ad-254">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="c44ad-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
