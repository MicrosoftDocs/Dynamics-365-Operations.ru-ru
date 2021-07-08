---
title: Количество превышает процент недопоставки при создании отборочной накладной
description: При создании отборочной накладной исходящая загрузка содержит количество, превышающее процент недопоставки.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249158"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="78560-103">Количество превышает процент недопоставки при создании отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="78560-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="78560-104">Код ошибки: SYS24921</span><span class="sxs-lookup"><span data-stu-id="78560-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="78560-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="78560-105">Symptoms</span></span>

<span data-ttu-id="78560-106">При создании отборочной накладной исходящая загрузка содержит количество, превышающее процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="78560-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="78560-107">При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="78560-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="78560-108">Величина недопоставки по строке составляет %1 процентов. Допустимая недопоставка - %2 процентов.</span><span class="sxs-lookup"><span data-stu-id="78560-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="78560-109">Поэтому невозможно создать отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="78560-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="78560-110">Причина</span><span class="sxs-lookup"><span data-stu-id="78560-110">Cause</span></span>

<span data-ttu-id="78560-111">Скомплектованное количество для загрузки или отгрузки меньше заказанного количества и не находится в пределах процента недопоставки.</span><span class="sxs-lookup"><span data-stu-id="78560-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="78560-112">Решение</span><span class="sxs-lookup"><span data-stu-id="78560-112">Resolution</span></span>

<span data-ttu-id="78560-113">Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="78560-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="78560-114">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="78560-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="78560-115">Скорректируйте процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="78560-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="78560-116">Реверсируйте и внесите коррективы.</span><span class="sxs-lookup"><span data-stu-id="78560-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="78560-117">Скорректируйте процент недопоставки</span><span class="sxs-lookup"><span data-stu-id="78560-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="78560-118">Используйте следующую процедуру, чтобы скорректировать процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="78560-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="78560-119">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы**.</span><span class="sxs-lookup"><span data-stu-id="78560-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="78560-120">Выберите заказ на продажу, для которого вы не можете разнести отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="78560-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="78560-121">На вкладке **Строки заказа на продажу** выберите строку заказа на продажу для номенклатуры, которая превышает процент недопоставки.</span><span class="sxs-lookup"><span data-stu-id="78560-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="78560-122">На вкладке  **Сведения строки** выберите **Доставка**.</span><span class="sxs-lookup"><span data-stu-id="78560-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="78560-123">В поле **Недопоставка** задайте в качестве значения большее процентное значение, которое было скомплектовано по количеству загрузки, чтобы можно было продолжить создание отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="78560-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="78560-124">Реверсируйте и внесите коррективы</span><span class="sxs-lookup"><span data-stu-id="78560-124">Reverse and make adjustments</span></span>

<span data-ttu-id="78560-125">Реверсируйте все, что было разнесено для загрузки (например, отборочная накладная, подтверждение отгрузки и работа), внесите корректировки заказа на продажу, повторно выпустите заказ на склад и завершите процедуру отгрузки.</span><span class="sxs-lookup"><span data-stu-id="78560-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="78560-126">Используйте следующую процедуру, чтобы отменить отборочную накладную.</span><span class="sxs-lookup"><span data-stu-id="78560-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="78560-127">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="78560-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="78560-128">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Отмена отборочных накладных**.</span><span class="sxs-lookup"><span data-stu-id="78560-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="78560-129">Используйте следующую процедуру, чтобы отменить подтверждение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="78560-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="78560-130">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="78560-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="78560-131">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="78560-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="78560-132">Для реверсирования работы используется следующая процедура.</span><span class="sxs-lookup"><span data-stu-id="78560-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="78560-133">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="78560-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="78560-134">В области действий на вкладке **Загрузки** в группе **Работа** выберите **Реверсировать работу**.</span><span class="sxs-lookup"><span data-stu-id="78560-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
