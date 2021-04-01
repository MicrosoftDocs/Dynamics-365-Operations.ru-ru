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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9b7dc72d789fd331c3636c406ac6a45566ba81ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242189"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="3723d-103">Консолидируйте отгрузки, используя рабочее место консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="3723d-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3723d-104">В этом разделе представлен сценарий, в котором несколько заказов запущены на склад, а затем консолидируются в отгрузки с помощью рабочее место консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="3723d-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="3723d-105">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="3723d-105">Make demo data available</span></span>

<span data-ttu-id="3723d-106">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3723d-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3723d-107">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="3723d-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="3723d-108">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="3723d-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="3723d-109">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="3723d-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="3723d-110">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="3723d-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="3723d-111">Включение функции консолидации отгрузок вручную</span><span class="sxs-lookup"><span data-stu-id="3723d-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="3723d-112">Прежде чем можно будет использовать функцию *Консолидация отгрузок вручную*, необходимо включить ее в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="3723d-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="3723d-113">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="3723d-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="3723d-114">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="3723d-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3723d-115">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="3723d-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3723d-116">**Имя функции:** *консолидация отгрузок вручную*</span><span class="sxs-lookup"><span data-stu-id="3723d-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="3723d-117">Как указано в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), необходимо также включить функцию *Консолидация отгрузок*, прежде чем можно будет создавать политики.</span><span class="sxs-lookup"><span data-stu-id="3723d-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="3723d-118">Однако этот шаг уже должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="3723d-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="3723d-119">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="3723d-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="3723d-120">Начнем с создания набора заказов на продажу, с которыми можно работать.</span><span class="sxs-lookup"><span data-stu-id="3723d-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="3723d-121">Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS).</span><span class="sxs-lookup"><span data-stu-id="3723d-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="3723d-122">За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.</span><span class="sxs-lookup"><span data-stu-id="3723d-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="3723d-123">Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="3723d-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="3723d-124">Создать набор заказов 1</span><span class="sxs-lookup"><span data-stu-id="3723d-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="3723d-125">Заказы на продажу 1-1 и 1-2</span><span class="sxs-lookup"><span data-stu-id="3723d-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="3723d-126">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-127">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3723d-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3723d-128">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3723d-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3723d-129">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-130">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-131">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-132">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="3723d-133">Заказ на продажу 1-3</span><span class="sxs-lookup"><span data-stu-id="3723d-133">Sales order 1-3</span></span>

1. <span data-ttu-id="3723d-134">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="3723d-135">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3723d-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3723d-136">**Способ поставки:** *10*</span><span class="sxs-lookup"><span data-stu-id="3723d-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="3723d-137">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-138">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-139">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-140">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="3723d-141">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-142">**Код номенклатуры:** *A0002* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-143">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="3723d-144">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3723d-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3723d-145">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="3723d-146">Создать набор заказов 2</span><span class="sxs-lookup"><span data-stu-id="3723d-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="3723d-147">Заказы на продажу 2-1 и 2-2</span><span class="sxs-lookup"><span data-stu-id="3723d-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="3723d-148">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-149">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="3723d-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="3723d-150">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3723d-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3723d-151">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-152">**Код номенклатуры:** *M9200* (номенклатура, в которой фильтр **код 4** имеет значение *Воспламеняющиеся*)</span><span class="sxs-lookup"><span data-stu-id="3723d-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="3723d-153">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-154">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="3723d-155">Добавьте вторую строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-156">**Код номенклатуры:** *M9201* (номенклатура, в которой фильтр **код 4** имеет значение *Взрывоопасные*)</span><span class="sxs-lookup"><span data-stu-id="3723d-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="3723d-157">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="3723d-158">**Способ поставки:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="3723d-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="3723d-159">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="3723d-160">Создать набор заказов 3</span><span class="sxs-lookup"><span data-stu-id="3723d-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="3723d-161">Заказы на продажу 3-1 и 3-2</span><span class="sxs-lookup"><span data-stu-id="3723d-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="3723d-162">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-163">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3723d-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3723d-164">**Заявка клиента:** *1*</span><span class="sxs-lookup"><span data-stu-id="3723d-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="3723d-165">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-166">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-167">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-168">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="3723d-169">Заказы на продажу 3-3 и 3-4</span><span class="sxs-lookup"><span data-stu-id="3723d-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="3723d-170">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-171">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3723d-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="3723d-172">**Заявка клиента:** *2*</span><span class="sxs-lookup"><span data-stu-id="3723d-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="3723d-173">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-174">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-175">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-176">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="3723d-177">Создать набор заказов 4</span><span class="sxs-lookup"><span data-stu-id="3723d-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="3723d-178">Заказы на продажу 4-1 и 4-2</span><span class="sxs-lookup"><span data-stu-id="3723d-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="3723d-179">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-180">**Счет клиента:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="3723d-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="3723d-181">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-182">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-183">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-184">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="3723d-185">Заказы на продажу 4-3 и 4-4</span><span class="sxs-lookup"><span data-stu-id="3723d-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="3723d-186">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-187">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="3723d-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="3723d-188">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-189">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-190">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-191">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="3723d-192">Заказы на продажу 4-5 и 4-6</span><span class="sxs-lookup"><span data-stu-id="3723d-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="3723d-193">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-194">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3723d-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="3723d-195">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3723d-195">**Site:** *6*</span></span>
    - <span data-ttu-id="3723d-196">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="3723d-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="3723d-197">**Кластер:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="3723d-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="3723d-198">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-199">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-200">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-201">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="3723d-202">Заказы на продажу 4-7 и 4-8</span><span class="sxs-lookup"><span data-stu-id="3723d-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="3723d-203">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3723d-204">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3723d-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="3723d-205">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3723d-205">**Site:** *6*</span></span>
    - <span data-ttu-id="3723d-206">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="3723d-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="3723d-207">**Кластер:** Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="3723d-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="3723d-208">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="3723d-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3723d-209">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="3723d-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3723d-210">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3723d-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3723d-211">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3723d-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="3723d-212">Запуск заказов на склад</span><span class="sxs-lookup"><span data-stu-id="3723d-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="3723d-213">Выполните следующие действия, чтобы запустить каждый заказ на продажу, созданный для этого сценария, на склад.</span><span class="sxs-lookup"><span data-stu-id="3723d-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="3723d-214">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3723d-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3723d-215">Найдите и выберите заказ на продажу, который требуется запустить.</span><span class="sxs-lookup"><span data-stu-id="3723d-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="3723d-216">На панели операций на вкладке **Склад** выберите вариант **Действия \> Запуск на склад**, чтобы запустить выбранный заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3723d-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="3723d-217">Повторите эту процедуру для других заказов на продажу, созданных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="3723d-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="3723d-218">Консолидируйте отгрузки, используя рабочее место консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="3723d-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="3723d-219">Перейдите на страницу **Управление складом \> Запуск на склад \> Рабочее место консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="3723d-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="3723d-220">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="3723d-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="3723d-221">В диалоговое окно редактора запросов на вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку со следующими настройками в сетку:</span><span class="sxs-lookup"><span data-stu-id="3723d-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="3723d-222">**Таблица:** *Заказы на продажу*</span><span class="sxs-lookup"><span data-stu-id="3723d-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="3723d-223">**Поля** — *заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="3723d-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="3723d-224">**Критерий:** Введите список номеров заказов на продажу с разделителями-запятыми для каждого набора заказов, созданного для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="3723d-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="3723d-225">Выберите **OK**, чтобы сохранить ваш запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3723d-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="3723d-226">На панели операций выберите **Консолидация отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="3723d-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="3723d-227">Выберите все отгрузки, затем на панели операций выберите **Консолидировать**.</span><span class="sxs-lookup"><span data-stu-id="3723d-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="3723d-228">Проверка отгрузок</span><span class="sxs-lookup"><span data-stu-id="3723d-228">Verify the shipments</span></span>

<span data-ttu-id="3723d-229">Следующая процедура позволяет проверить отгрузки, которые были созданы или обновлены в результате консолидации отгрузок.</span><span class="sxs-lookup"><span data-stu-id="3723d-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="3723d-230">Используйте его для просмотра каждого набора заказов, созданного для данного сценария, а затем просмотрите подразделы, которые следуют за тем, чтобы убедиться, что получены ожидаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="3723d-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="3723d-231">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="3723d-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="3723d-232">Найдите и выберите нужную отгрузку.</span><span class="sxs-lookup"><span data-stu-id="3723d-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="3723d-233">Если при создании или обновлении отгрузки была использована политика консолидации, ее можно увидеть в поле **Политика консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="3723d-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="3723d-234">Соответствующие отгрузки для набора заказов 1</span><span class="sxs-lookup"><span data-stu-id="3723d-234">Related shipments for order set 1</span></span>

<span data-ttu-id="3723d-235">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3723d-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="3723d-236">Первая отгрузка содержит три строки и была создана с помощью политики консолидации отгрузок *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="3723d-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="3723d-237">Вторая отгрузка, которая не использует режим транспортировки *Airways* поставки, была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="3723d-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="3723d-238">Соответствующие отгрузки для набора заказов 2</span><span class="sxs-lookup"><span data-stu-id="3723d-238">Related shipments for order set 2</span></span>

<span data-ttu-id="3723d-239">Должны быть созданы три отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3723d-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="3723d-240">Первая отгрузка содержит номенклатуры *Воспламеняющиеся*.</span><span class="sxs-lookup"><span data-stu-id="3723d-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="3723d-241">Каждая из двух других отгрузок содержит одну строку, которая имеет номенклатуру *Взрывоопасные*.</span><span class="sxs-lookup"><span data-stu-id="3723d-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="3723d-242">Соответствующие отгрузки для набора заказов 3</span><span class="sxs-lookup"><span data-stu-id="3723d-242">Related shipments for order set 3</span></span>

<span data-ttu-id="3723d-243">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3723d-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="3723d-244">Первая отгрузка содержит строки заказа из заказа на продажу, для которого в поле **Заявка клиента** указано значение *1*.</span><span class="sxs-lookup"><span data-stu-id="3723d-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="3723d-245">Вторая отгрузка содержит строки заказа из заказа на продажу, для которого в поле **Заявка клиента** указано значение *2*.</span><span class="sxs-lookup"><span data-stu-id="3723d-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="3723d-246">Соответствующие отгрузки для набора заказов 4</span><span class="sxs-lookup"><span data-stu-id="3723d-246">Related shipments for order set 4</span></span>

<span data-ttu-id="3723d-247">Должны быть созданы четыре отгрузки:</span><span class="sxs-lookup"><span data-stu-id="3723d-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="3723d-248">Строки из двух заказов для клиента *US-003* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="3723d-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="3723d-249">Строки из двух заказов для клиента *US-004* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="3723d-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="3723d-250">Строки из заказов на продажу 4-5 и 4-6 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *Кластер заказов*.</span><span class="sxs-lookup"><span data-stu-id="3723d-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="3723d-251">Строки из заказов на продажу 4-7 и 4-8 для клиента *US-007* сгруппированы в одну отгрузку, используя политику консолидации отгрузок *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="3723d-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3723d-252">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3723d-252">Additional resources</span></span>

- [<span data-ttu-id="3723d-253">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="3723d-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="3723d-254">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="3723d-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]