---
title: Скомплектованного количества недостаточно во время создания отборочной накладной
description: При создании отборочной накладной исходящая загрузка содержит скомплектованное количество, которое не соответствует созданному количеству работы в строке загрузки.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249162"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="cffad-103">Скомплектованного количества недостаточно во время создания отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="cffad-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="cffad-104">Код ошибки: SYS54073</span><span class="sxs-lookup"><span data-stu-id="cffad-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="cffad-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="cffad-105">Symptoms</span></span>

<span data-ttu-id="cffad-106">При создании отборочной накладной исходящая загрузка содержит скомплектованное количество, которое не соответствует созданному количеству работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="cffad-107">При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="cffad-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="cffad-108">Поскольку скомплектовано всего %1, недостаточно обновить %2, при том чтобы осталось %3.</span><span class="sxs-lookup"><span data-stu-id="cffad-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="cffad-109">Поэтому невозможно создать отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="cffad-110">Причина</span><span class="sxs-lookup"><span data-stu-id="cffad-110">Cause</span></span>

<span data-ttu-id="cffad-111">Невозможно создать отборочную накладную в ее текущем состоянии, так как могут существовать следующие условия:</span><span class="sxs-lookup"><span data-stu-id="cffad-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="cffad-112">Связанная работа еще не скомплектована и не перемещена в конечную ячейку отгрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="cffad-113">Скомплектованное количество работы не соответствует созданному количеству работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="cffad-114">Количество в строке загрузки, количество созданной работы и скомплектованное количество не соответствуют.</span><span class="sxs-lookup"><span data-stu-id="cffad-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="cffad-115">Решение</span><span class="sxs-lookup"><span data-stu-id="cffad-115">Resolution</span></span>

<span data-ttu-id="cffad-116">Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="cffad-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="cffad-117">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="cffad-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="cffad-118">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="cffad-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="cffad-119">Скорректируйте количество в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="cffad-120">Реверсируйте все регистрации комплектации и снова выполните комплектацию.</span><span class="sxs-lookup"><span data-stu-id="cffad-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="cffad-121">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="cffad-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="cffad-122">С помощью следующей процедуры проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="cffad-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="cffad-123">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="cffad-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cffad-124">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="cffad-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cffad-125">На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="cffad-126">Запишите значение поля **Созданное количество работы**.</span><span class="sxs-lookup"><span data-stu-id="cffad-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="cffad-127">В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="cffad-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="cffad-128">Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="cffad-129">Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.</span><span class="sxs-lookup"><span data-stu-id="cffad-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="cffad-130">Скорректируйте количество в строке загрузки</span><span class="sxs-lookup"><span data-stu-id="cffad-130">Adjust the load line quantity</span></span>

<span data-ttu-id="cffad-131">Используйте следующую процедуру, чтобы скорректировать количество строки загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="cffad-132">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="cffad-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cffad-133">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="cffad-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cffad-134">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="cffad-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="cffad-135">На вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая вызывает проблему.</span><span class="sxs-lookup"><span data-stu-id="cffad-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="cffad-136">Выберите **Уменьшить скомплектованное количество** для корректировки скомплектованного количества.</span><span class="sxs-lookup"><span data-stu-id="cffad-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="cffad-137">Задайте поле **Уменьшить строку загрузки**, чтобы отразить корректировки в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="cffad-138">Реверсируйте все регистрации комплектации и снова выполните комплектацию</span><span class="sxs-lookup"><span data-stu-id="cffad-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="cffad-139">Проблема может возникнуть из-за того, что кто-то использовал регистрацию комплектации, чтобы закрыть строку загрузки без работы.</span><span class="sxs-lookup"><span data-stu-id="cffad-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="cffad-140">В этом случае ручная регистрация комплектации должна быть реверсирована, а комплектация должна быть выполнена с помощью мобильного приложения Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="cffad-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="cffad-141">Используйте следующую процедуру, чтобы реверсировать регистрацию комплектации.</span><span class="sxs-lookup"><span data-stu-id="cffad-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="cffad-142">Перейдите в раздел **Расчеты с клиентами \> Заказы \> Все заказы**.</span><span class="sxs-lookup"><span data-stu-id="cffad-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="cffad-143">Выберите заказ на продажу, для которого вы не можете разнести отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="cffad-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="cffad-144">На вкладке **Строки заказа на продажу** выберите строку заказа на продажу, для которого была сделана регистрация комплектации.</span><span class="sxs-lookup"><span data-stu-id="cffad-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="cffad-145">Выберите **Обновить строку \> Комплектация**, чтобы отменить комплектацию номенклатур.</span><span class="sxs-lookup"><span data-stu-id="cffad-145">Select **Update line \> Pick** to unpick the items.</span></span>
