---
title: Консолидируйте отгрузки вручную, используя страницу Консолидация отгрузок
description: В этом разделе представлен сценарий, в котором несколько заказов запущены на склад, а затем консолидируются в отгрузки с помощью страницы Консолидация отгрузок.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: e4e6dac1d1b4a304062e852526235eeee6579540
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840397"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="b7a95-103">Консолидируйте отгрузки вручную, используя страницу Консолидация отгрузок</span><span class="sxs-lookup"><span data-stu-id="b7a95-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7a95-104">В этом разделе представлен сценарий, в котором несколько заказов запущены на склад, а затем консолидируются в отгрузки с помощью страницы **Консолидация отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="b7a95-105">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="b7a95-105">Make demo data available</span></span>

<span data-ttu-id="b7a95-106">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7a95-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b7a95-107">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="b7a95-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="b7a95-108">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="b7a95-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="b7a95-109">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="b7a95-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="b7a95-110">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="b7a95-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="b7a95-111">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="b7a95-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="b7a95-112">Начнем с создания набора заказов на продажу, с которыми можно работать.</span><span class="sxs-lookup"><span data-stu-id="b7a95-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="b7a95-113">Необходимо работать со складом, для которого разрешены расширенные складские процессы (WMS).</span><span class="sxs-lookup"><span data-stu-id="b7a95-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="b7a95-114">За исключением случаев, когда явно упоминается отдельный склад, этот же склад должен использоваться для каждого из следующих наборов заказов.</span><span class="sxs-lookup"><span data-stu-id="b7a95-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="b7a95-115">Перейти к **Расчеты с клиентами \> заказы \> все заказы на продажу** и создать коллекцию заказов на продажу, в которых имеются параметры, описанные в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="b7a95-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="b7a95-116">Создание заказов на продажу 1 и 2</span><span class="sxs-lookup"><span data-stu-id="b7a95-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="b7a95-117">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b7a95-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b7a95-118">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b7a95-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b7a95-119">**Кластер:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="b7a95-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="b7a95-120">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b7a95-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b7a95-121">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="b7a95-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b7a95-122">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b7a95-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b7a95-123">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="b7a95-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="b7a95-124">Создание заказов на продажу 3 и 4</span><span class="sxs-lookup"><span data-stu-id="b7a95-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="b7a95-125">Создайте два одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b7a95-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b7a95-126">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b7a95-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b7a95-127">**Кластер:** Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="b7a95-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="b7a95-128">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b7a95-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b7a95-129">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="b7a95-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b7a95-130">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b7a95-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b7a95-131">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="b7a95-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="b7a95-132">Запуск заказов на склад</span><span class="sxs-lookup"><span data-stu-id="b7a95-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="b7a95-133">Выполните следующие действия, чтобы запустить каждый заказ на продажу, созданный для этого сценария, на склад.</span><span class="sxs-lookup"><span data-stu-id="b7a95-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="b7a95-134">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b7a95-135">Найдите и выберите заказ на продажу, который требуется запустить.</span><span class="sxs-lookup"><span data-stu-id="b7a95-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="b7a95-136">На панели операций на вкладке **Склад** выберите вариант **Действия \> Запуск на склад**, чтобы запустить выбранный заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="b7a95-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="b7a95-137">Повторите эту процедуру для других заказов на продажу, созданных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="b7a95-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="b7a95-138">Консолидация отгрузок</span><span class="sxs-lookup"><span data-stu-id="b7a95-138">Consolidate shipments</span></span>

1. <span data-ttu-id="b7a95-139">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="b7a95-140">Поиск и выбор отгрузки, которая была создана, когда заказ на продажу 1 был запущен на склад.</span><span class="sxs-lookup"><span data-stu-id="b7a95-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="b7a95-141">(В поле **Политика консолидации отгрузок** должно быть установлено значение *кластер заказов*.)</span><span class="sxs-lookup"><span data-stu-id="b7a95-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="b7a95-142">На панели операций откройте вкладку **Отгрузки** и выберите **Отгрузки \> Консолидация отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="b7a95-143">Проверьте, какие отгрузки предлагаются для консолидации.</span><span class="sxs-lookup"><span data-stu-id="b7a95-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="b7a95-144">Только одна отгрузка с одной и той же политикой должна предлагаться для консолидации.</span><span class="sxs-lookup"><span data-stu-id="b7a95-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="b7a95-145">Закройте страницу **консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="b7a95-146">Поиск и выбор отгрузки, которая была создана, когда заказ на продажу 3 был запущен на склад.</span><span class="sxs-lookup"><span data-stu-id="b7a95-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="b7a95-147">(В поле **Политика консолидации отгрузок** должно быть установлено значение *По умолчанию*.)</span><span class="sxs-lookup"><span data-stu-id="b7a95-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="b7a95-148">На панели операций откройте вкладку **Отгрузки** и выберите **Отгрузки \> Консолидация отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="b7a95-149">Убедитесь, что для консолидации не предлагается никаких отгрузок.</span><span class="sxs-lookup"><span data-stu-id="b7a95-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="b7a95-150">Выберите **Показать фильтры**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="b7a95-151">На панели **фильтров** удалите Фильтр **номер заказа**, а затем выберите **применить**.</span><span class="sxs-lookup"><span data-stu-id="b7a95-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="b7a95-152">Проверьте, какие отгрузки предлагаются для консолидации.</span><span class="sxs-lookup"><span data-stu-id="b7a95-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="b7a95-153">Только одна отгрузка с одной и той же политикой должна предлагаться для консолидации.</span><span class="sxs-lookup"><span data-stu-id="b7a95-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7a95-154">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7a95-154">Additional resources</span></span>

- [<span data-ttu-id="b7a95-155">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="b7a95-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="b7a95-156">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="b7a95-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]