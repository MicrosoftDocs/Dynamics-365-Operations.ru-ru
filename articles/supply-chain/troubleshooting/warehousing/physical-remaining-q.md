---
title: Физическое оставшееся количество в единице не должно быть нулевым
description: При создании отборочной накладной данные, которые поставляются в нее, имеют ненулевое количество запасов, но нулевое количество продаж.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248800"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="e4024-103">Физическое оставшееся количество в единице не должно быть нулевым</span><span class="sxs-lookup"><span data-stu-id="e4024-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="e4024-104">Код ошибки: SYS19591</span><span class="sxs-lookup"><span data-stu-id="e4024-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="e4024-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="e4024-105">Symptoms</span></span>

<span data-ttu-id="e4024-106">При создании отборочной накладной данные, которые поставляются в нее, имеют ненулевое количество запасов, но нулевое количество продаж.</span><span class="sxs-lookup"><span data-stu-id="e4024-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="e4024-107">При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="e4024-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="e4024-108">Физический остаток по складу в ед. изм. учета %1 должен быть отличен от нуля.</span><span class="sxs-lookup"><span data-stu-id="e4024-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="e4024-109">Поэтому невозможно создать отборочную накладную для загрузки.</span><span class="sxs-lookup"><span data-stu-id="e4024-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e4024-110">Причина</span><span class="sxs-lookup"><span data-stu-id="e4024-110">Cause</span></span>

<span data-ttu-id="e4024-111">Система оценивает физическое оставшееся количество в единице измерения складского учета и физическое оставшееся количество в единице отгрузки.</span><span class="sxs-lookup"><span data-stu-id="e4024-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="e4024-112">Если система обнаружит, что физическое оставшееся количество в единице отгрузки составляет 0 (ноль), но физическое оставшееся количество в единице измерения складского учета не равно 0, вы не можете создать отборочную накладную.</span><span class="sxs-lookup"><span data-stu-id="e4024-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="e4024-113">Например, эта проблема может возникнуть, если единица измерения продажи и единица измерения складского учета для номенклатуры отличаются, а конверсия между единицами не является точной.</span><span class="sxs-lookup"><span data-stu-id="e4024-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4024-114">Решение</span><span class="sxs-lookup"><span data-stu-id="e4024-114">Resolution</span></span>

<span data-ttu-id="e4024-115">Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="e4024-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="e4024-116">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="e4024-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="e4024-117">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="e4024-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="e4024-118">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без проблем округления.</span><span class="sxs-lookup"><span data-stu-id="e4024-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="e4024-119">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.</span><span class="sxs-lookup"><span data-stu-id="e4024-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="e4024-120">Убедитесь, что единица измерения складского учета меньше единицы измерения продажи.</span><span class="sxs-lookup"><span data-stu-id="e4024-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="e4024-121">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="e4024-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="e4024-122">С помощью следующей процедуры проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="e4024-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="e4024-123">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="e4024-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e4024-124">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="e4024-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e4024-125">На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.</span><span class="sxs-lookup"><span data-stu-id="e4024-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="e4024-126">Запишите значение поля **Созданное количество работы**.</span><span class="sxs-lookup"><span data-stu-id="e4024-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="e4024-127">В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="e4024-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="e4024-128">Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="e4024-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="e4024-129">Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.</span><span class="sxs-lookup"><span data-stu-id="e4024-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="e4024-130">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без проблем округления.</span><span class="sxs-lookup"><span data-stu-id="e4024-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="e4024-131">С помощью следующей процедуры проверьте строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без проблем округления.</span><span class="sxs-lookup"><span data-stu-id="e4024-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="e4024-132">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="e4024-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e4024-133">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="e4024-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="e4024-134">На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="e4024-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="e4024-135">На вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает перепоставку.</span><span class="sxs-lookup"><span data-stu-id="e4024-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="e4024-136">Выберите **Уменьшить скомплектованное количество** для корректировки скомплектованного количества.</span><span class="sxs-lookup"><span data-stu-id="e4024-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="e4024-137">На вкладке  **Сведения строки** выберите **Заказ**.</span><span class="sxs-lookup"><span data-stu-id="e4024-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="e4024-138">В поле **Количество** установите значение для скомплектованного количества (то есть значение в поле **Созданное количество работы**), чтобы можно было продолжить создание отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="e4024-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="e4024-139">Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.</span><span class="sxs-lookup"><span data-stu-id="e4024-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="e4024-140">С помощью следующей процедуры проверьте строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.</span><span class="sxs-lookup"><span data-stu-id="e4024-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="e4024-141">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="e4024-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e4024-142">Выберите загрузку, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="e4024-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="e4024-143">На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая вызывает проблему.</span><span class="sxs-lookup"><span data-stu-id="e4024-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="e4024-144">Запишите значение полей **Количество** и **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="e4024-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="e4024-145">Перейдите в раздел **Управление организацией \> Единицы \> Единицы**.</span><span class="sxs-lookup"><span data-stu-id="e4024-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="e4024-146">Выберите единицу, для которой не может быть создана отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="e4024-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="e4024-147">При необходимости скорректируйте значение в поле **Десятичная точность**.</span><span class="sxs-lookup"><span data-stu-id="e4024-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="e4024-148">Убедитесь, что единица измерения складского учета меньше единицы измерения продажи.</span><span class="sxs-lookup"><span data-stu-id="e4024-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="e4024-149">Убедитесь, что единица измерения складского учета меньше единицы измерения продажи.</span><span class="sxs-lookup"><span data-stu-id="e4024-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="e4024-150">Рассмотрите перенастройку единицы измерения для номенклатуры по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="e4024-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
