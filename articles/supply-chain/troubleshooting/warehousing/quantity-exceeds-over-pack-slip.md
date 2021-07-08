---
title: Количество превышает процент перепоставки при создании отборочной накладной
description: При создании отборочной накладной исходящая загрузка содержит количество, превышающее процент перепоставки.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249160"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="0414d-103">Количество превышает процент перепоставки при создании отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="0414d-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="0414d-104">Код ошибки: SYS24920</span><span class="sxs-lookup"><span data-stu-id="0414d-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="0414d-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="0414d-105">Symptoms</span></span>

<span data-ttu-id="0414d-106">При создании отборочной накладной исходящая загрузка содержит количество, превышающее процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="0414d-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="0414d-107">При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="0414d-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="0414d-108">Величина перепоставки по строке составляет %1 процентов. Допустимая перепоставка - %2 процентов.</span><span class="sxs-lookup"><span data-stu-id="0414d-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="0414d-109">Поэтому невозможно создать отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="0414d-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0414d-110">Причина</span><span class="sxs-lookup"><span data-stu-id="0414d-110">Cause</span></span>

<span data-ttu-id="0414d-111">Скомплектованное количество для загрузки или отгрузки больше заказанного количества и не находится в пределах процента перепоставки.</span><span class="sxs-lookup"><span data-stu-id="0414d-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="0414d-112">Решение</span><span class="sxs-lookup"><span data-stu-id="0414d-112">Resolution</span></span>

<span data-ttu-id="0414d-113">Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="0414d-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="0414d-114">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="0414d-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="0414d-115">Скорректируйте количество в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="0414d-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="0414d-116">Скорректируйте процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="0414d-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="0414d-117">Реверсируйте и внесите коррективы.</span><span class="sxs-lookup"><span data-stu-id="0414d-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="0414d-118">Скорректируйте количество в строке загрузки</span><span class="sxs-lookup"><span data-stu-id="0414d-118">Adjust the load line quantity</span></span>

<span data-ttu-id="0414d-119">Используйте следующую процедуру, чтобы скорректировать количество строки загрузки.</span><span class="sxs-lookup"><span data-stu-id="0414d-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="0414d-120">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="0414d-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0414d-121">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="0414d-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0414d-122">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="0414d-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="0414d-123">На вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="0414d-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="0414d-124">Выберите **Уменьшить скомплектованное количество** для корректировки скомплектованного количества.</span><span class="sxs-lookup"><span data-stu-id="0414d-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="0414d-125">На вкладке  **Сведения строки** выберите **Заказ**.</span><span class="sxs-lookup"><span data-stu-id="0414d-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="0414d-126">В поле **Количество** установите значение для скомплектованного количества (то есть значение в поле **Созданное количество работы**), чтобы можно было продолжить создание отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="0414d-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="0414d-127">Скорректируйте процент перепоставки</span><span class="sxs-lookup"><span data-stu-id="0414d-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="0414d-128">Используйте следующую процедуру, чтобы скорректировать процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="0414d-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="0414d-129">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы**.</span><span class="sxs-lookup"><span data-stu-id="0414d-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="0414d-130">Выберите заказ на продажу, для которого вы не можете разнести отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="0414d-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="0414d-131">На вкладке **Строки заказа на продажу** выберите строку заказа на продажу для номенклатуры, которая превышает процент перепоставки.</span><span class="sxs-lookup"><span data-stu-id="0414d-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="0414d-132">На вкладке  **Сведения строки** выберите **Доставка**.</span><span class="sxs-lookup"><span data-stu-id="0414d-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="0414d-133">В поле **Перепоставка** задайте в качестве значения большее процентное значение, которое было скомплектовано по количеству загрузки, чтобы можно было продолжить создание отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="0414d-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="0414d-134">Реверсируйте и внесите коррективы</span><span class="sxs-lookup"><span data-stu-id="0414d-134">Reverse and make adjustments</span></span>

<span data-ttu-id="0414d-135">Реверсируйте все, что было разнесено для загрузки (например, отборочная накладная, подтверждение отгрузки и работа), внесите корректировки заказа на продажу, повторно выпустите заказ на склад и завершите процедуру отгрузки.</span><span class="sxs-lookup"><span data-stu-id="0414d-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="0414d-136">Используйте следующую процедуру, чтобы отменить отборочную накладную.</span><span class="sxs-lookup"><span data-stu-id="0414d-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="0414d-137">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="0414d-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0414d-138">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Отмена отборочных накладных**.</span><span class="sxs-lookup"><span data-stu-id="0414d-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="0414d-139">Используйте следующую процедуру, чтобы отменить подтверждение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="0414d-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="0414d-140">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="0414d-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0414d-141">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="0414d-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="0414d-142">Для реверсирования работы используется следующая процедура.</span><span class="sxs-lookup"><span data-stu-id="0414d-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="0414d-143">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="0414d-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0414d-144">В области действий на вкладке **Загрузки** в группе **Работа** выберите **Реверсировать работу**.</span><span class="sxs-lookup"><span data-stu-id="0414d-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
