---
title: Количество, которое вы пытаетесь обновить, превышает полученное/доставленное количество.
description: При создании отборочной накладной исходящая загрузка содержит количество, которое превышает количество работы, скомплектованное и реверсированное для заказа на продажу.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249163"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="bd432-103">Количество, которое вы пытаетесь обновить, превышает полученное/доставленное количество</span><span class="sxs-lookup"><span data-stu-id="bd432-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="bd432-104">Код ошибки: SYS7676</span><span class="sxs-lookup"><span data-stu-id="bd432-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="bd432-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="bd432-105">Symptoms</span></span>

<span data-ttu-id="bd432-106">При создании отборочной накладной исходящая загрузка содержит количество, которое превышает количество работы, скомплектованное и реверсированное для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="bd432-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="bd432-107">При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="bd432-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="bd432-108">Количество, которое вы пытаетесь обновить, превышает полученное/поставленное количество.</span><span class="sxs-lookup"><span data-stu-id="bd432-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="bd432-109">Поэтому невозможно создать отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="bd432-110">Причина</span><span class="sxs-lookup"><span data-stu-id="bd432-110">Cause</span></span>

<span data-ttu-id="bd432-111">Скомплектованное количество работы не соответствует созданному количеству работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="bd432-112">Например, эта проблема может возникнуть, если количество строки загрузки, созданное количество работы или скомплектованное количество не являются точными.</span><span class="sxs-lookup"><span data-stu-id="bd432-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd432-113">Решение</span><span class="sxs-lookup"><span data-stu-id="bd432-113">Resolution</span></span>

<span data-ttu-id="bd432-114">Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="bd432-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="bd432-115">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="bd432-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="bd432-116">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="bd432-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="bd432-117">Скорректируйте количество в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="bd432-118">Реверсируйте все регистрации комплектации и снова выполните комплектацию.</span><span class="sxs-lookup"><span data-stu-id="bd432-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="bd432-119">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="bd432-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="bd432-120">С помощью следующей процедуры проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="bd432-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="bd432-121">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="bd432-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bd432-122">Выберите загрузку, для которой невозможно создать отгрузку.</span><span class="sxs-lookup"><span data-stu-id="bd432-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="bd432-123">На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="bd432-124">Запишите значение поля **Созданное количество работы**.</span><span class="sxs-lookup"><span data-stu-id="bd432-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="bd432-125">В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="bd432-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="bd432-126">Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="bd432-127">Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.</span><span class="sxs-lookup"><span data-stu-id="bd432-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="bd432-128">Скорректируйте количество в строке загрузки</span><span class="sxs-lookup"><span data-stu-id="bd432-128">Adjust the load line quantity</span></span>

<span data-ttu-id="bd432-129">Используйте следующую процедуру, чтобы скорректировать количество строки загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="bd432-130">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="bd432-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bd432-131">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="bd432-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="bd432-132">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="bd432-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="bd432-133">На вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая вызывает проблему.</span><span class="sxs-lookup"><span data-stu-id="bd432-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="bd432-134">Выберите **Уменьшить скомплектованное количество** для корректировки скомплектованного количества.</span><span class="sxs-lookup"><span data-stu-id="bd432-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="bd432-135">Задайте поле **Уменьшить строку загрузки**, чтобы отразить корректировки в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="bd432-136">Реверсируйте все регистрации комплектации и снова выполните комплектацию</span><span class="sxs-lookup"><span data-stu-id="bd432-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="bd432-137">Если кто-то использовал регистрацию комплектации для закрытия строки загрузки без работы, может возникнуть несоответствие между количеством строки загрузки и скомплектованным количеством.</span><span class="sxs-lookup"><span data-stu-id="bd432-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="bd432-138">В этом случае ручная регистрация комплектации должна быть реверсирована, а комплектация должна быть выполнена с помощью мобильного приложения Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="bd432-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="bd432-139">Используйте следующую процедуру, чтобы реверсировать регистрацию комплектации.</span><span class="sxs-lookup"><span data-stu-id="bd432-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="bd432-140">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы**.</span><span class="sxs-lookup"><span data-stu-id="bd432-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="bd432-141">Выберите заказ на продажу, для которого вы не можете разнести отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="bd432-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="bd432-142">На вкладке **Строки заказа на продажу** выберите строку заказа на продажу, для которого была сделана регистрация комплектации.</span><span class="sxs-lookup"><span data-stu-id="bd432-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="bd432-143">Выберите **Обновить строку \> Комплектация**, чтобы отменить комплектацию номенклатур.</span><span class="sxs-lookup"><span data-stu-id="bd432-143">Select **Update line \> Pick** to unpick the items.</span></span>
