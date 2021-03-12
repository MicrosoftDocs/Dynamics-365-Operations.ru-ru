---
title: Консолидируйте отгрузки, когда политика консолидации отгрузок переопределяется на странице Запуск на склад
description: В этом разделе представлен сценарий, в котором одна или несколько строк продаж должны быть запущены на склад вручную со страницы Запуск на склад, а политика консолидации отгрузок, определяемая системой, должна быть переопределена до запуска.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4aaaa7949d988607b38dd6e38a3c3497f227b8af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963345"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="749ec-103">Консолидируйте отгрузки, когда политика консолидации отгрузок переопределяется на странице Запуск на склад</span><span class="sxs-lookup"><span data-stu-id="749ec-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="749ec-104">В этом разделе представлен сценарий, в котором одна или несколько строк продаж должны быть запущены на склад вручную со страницы **Запуск на склад**, а политика консолидации отгрузок, определяемая системой, должна быть переопределена до запуска.</span><span class="sxs-lookup"><span data-stu-id="749ec-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="749ec-105">Переопределение политики консолидации отгрузок может потребоваться, например, если заказ, который обычно не был консолидирован с открытыми отгрузками, должен быть консолидирован с открытыми отгрузками.</span><span class="sxs-lookup"><span data-stu-id="749ec-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="749ec-106">В ходе сценария создается набор заказов на продажу, а затем политика консолидации отгрузок по умолчанию переопределяется до запуска заказов на склад.</span><span class="sxs-lookup"><span data-stu-id="749ec-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="749ec-107">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="749ec-107">Make demo data available</span></span>

<span data-ttu-id="749ec-108">Сценарий в этом разделе ссылается на значения и записи, включенные в стандартные демонстрационные данные, предоставляемые в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="749ec-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="749ec-109">Если вы хотите использовать значения, указанные здесь, в ходе выполнения упражнений, убедитесь, что вы работаете в среде, в которой установлены демонстрационные данные, и настройте юридическое лицо на **USMF** перед началом работы.</span><span class="sxs-lookup"><span data-stu-id="749ec-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="749ec-110">Настройка политик консолидации отгрузок и фильтров продуктов</span><span class="sxs-lookup"><span data-stu-id="749ec-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="749ec-111">Описанный здесь сценарий предполагает, что функция уже включена, выполнены упражнения в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md), а также создаются политики и другие записи, которые описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="749ec-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="749ec-112">Обязательно выполните эти упражнения перед выполнением этого сценария.</span><span class="sxs-lookup"><span data-stu-id="749ec-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="749ec-113">Создание заказов на продажу для этого сценария</span><span class="sxs-lookup"><span data-stu-id="749ec-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="749ec-114">Перейти к **Расчеты с клиентами \> Заказы \> Все заказы на продажу** и создать три одинаковых заказа на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="749ec-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="749ec-115">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="749ec-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="749ec-116">Добавьте строку заказа со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="749ec-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="749ec-117">**Код номенклатуры:** *A0001* (номенклатура, для которой не назначен фильтр **код 4**)</span><span class="sxs-lookup"><span data-stu-id="749ec-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="749ec-118">**Количество:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="749ec-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="749ec-119">Выберите **Запасы \> Резервирование**, а затем на панели операций выберите **резервирование лота** для резервирования строки заказа.</span><span class="sxs-lookup"><span data-stu-id="749ec-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="749ec-120">Запуск заказов на продажу со страницы запуск на склад</span><span class="sxs-lookup"><span data-stu-id="749ec-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="749ec-121">Выполните следующие действия, чтобы переопределить политику консолидации отгрузок в ходе запуска на склад.</span><span class="sxs-lookup"><span data-stu-id="749ec-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="749ec-122">Перейдите на страницу **Управление складом \> Запуск на склад \> Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="749ec-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="749ec-123">В верхней области выберите первый заказ на продажу, созданный для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="749ec-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="749ec-124">Выберите **Добавить**, чтобы добавить строку в запуск на склад.</span><span class="sxs-lookup"><span data-stu-id="749ec-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="749ec-125">Обратите внимание, что политика консолидации отгрузок *по умолчанию* применяется в нижней области.</span><span class="sxs-lookup"><span data-stu-id="749ec-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="749ec-126">В нижней области выберите **выбрать новую политику консолидации отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="749ec-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="749ec-127">Выбор политики, позволяющей выполнить консолидацию с другими открытыми отгрузками той же политики.</span><span class="sxs-lookup"><span data-stu-id="749ec-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="749ec-128">Например, выберите политику *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="749ec-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="749ec-129">Выберите **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="749ec-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="749ec-130">Выберите второй и третий заказы на продажу, созданный для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="749ec-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="749ec-131">Выберите **Добавить**, чтобы добавить строки в запуск на склад.</span><span class="sxs-lookup"><span data-stu-id="749ec-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="749ec-132">Обратите внимание, что политика *по умолчанию* применяется в нижней области.</span><span class="sxs-lookup"><span data-stu-id="749ec-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="749ec-133">Выберите вторую строку, а затем в поле **выберите новую политику консолидации отгрузок** выберите политику *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="749ec-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="749ec-134">Выберите вариант **Запуск на склад** для обеих строк.</span><span class="sxs-lookup"><span data-stu-id="749ec-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="749ec-135">Проверка отгрузок</span><span class="sxs-lookup"><span data-stu-id="749ec-135">Verify the shipments</span></span>

<span data-ttu-id="749ec-136">Должны быть созданы две отгрузки:</span><span class="sxs-lookup"><span data-stu-id="749ec-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="749ec-137">Первая отгрузка содержит две строки и была создана с помощью политики консолидации отгрузок *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="749ec-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="749ec-138">Вторая отгрузка содержит одну строку и была создана с помощью политики консолидации отгрузок *По умолчанию*.</span><span class="sxs-lookup"><span data-stu-id="749ec-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="749ec-139">Чтобы просмотреть созданные отгрузки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="749ec-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="749ec-140">Выберите **Управление складом \> Отгрузки \> Все отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="749ec-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="749ec-141">Найдите и выберите нужную отгрузку.</span><span class="sxs-lookup"><span data-stu-id="749ec-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="749ec-142">В поле **Политика консолидации отгрузок** просмотрите политику консолидации, которая использовалась при создании отгрузки.</span><span class="sxs-lookup"><span data-stu-id="749ec-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="749ec-143">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="749ec-143">Additional resources</span></span>

- [<span data-ttu-id="749ec-144">Политики консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="749ec-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="749ec-145">Настройка политик консолидации отгрузок</span><span class="sxs-lookup"><span data-stu-id="749ec-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
