---
title: Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы
description: Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301313"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="9051e-103">Невозможно подтвердить отгрузку, так как номенклатуры не были скомплектованы</span><span class="sxs-lookup"><span data-stu-id="9051e-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="9051e-104">Код ошибки: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="9051e-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="9051e-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="9051e-105">Symptoms</span></span>

<span data-ttu-id="9051e-106">При попытке подтвердить отгрузку система выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="9051e-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="9051e-107">Некоторые из номенклатур, которые требуются для загрузки %1, еще не скомплектованы и не перемещены в местонахождение конечной отгрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="9051e-108">Поэтому невозможно подтвердить отгрузку для загрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="9051e-109">Причина</span><span class="sxs-lookup"><span data-stu-id="9051e-109">Cause</span></span>

<span data-ttu-id="9051e-110">Невозможно подтвердить загрузку в ее текущем состоянии, так как могут существовать следующие условия:</span><span class="sxs-lookup"><span data-stu-id="9051e-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="9051e-111">Связанная работа еще не скомплектована и не перемещена в конечную ячейку отгрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="9051e-112">Скомплектованное количество работы не соответствует созданному количеству работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="9051e-113">При использовании контейнеров шаблонов волны настроена директива местонахождения с местоположением упаковки в качестве окончательного местоположения отгрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="9051e-114">Решение</span><span class="sxs-lookup"><span data-stu-id="9051e-114">Resolution</span></span>

<span data-ttu-id="9051e-115">Загрузка или отгрузка в данный момент находится в состоянии, когда подтверждение отгрузки завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="9051e-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="9051e-116">Для решения продляемы необходимо выполнить одну или несколько из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="9051e-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="9051e-117">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="9051e-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="9051e-118">Отмените коды работы, которые были созданы для местоположения упаковки в качестве окончательного местоположения отгрузки, перенастройте директиву местоположения и повторно выпустите загрузку.</span><span class="sxs-lookup"><span data-stu-id="9051e-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="9051e-119">Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="9051e-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="9051e-120">С помощью следующей процедуры проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.</span><span class="sxs-lookup"><span data-stu-id="9051e-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="9051e-121">Выберите **Управление складом \> Загрузки \> Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="9051e-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="9051e-122">Выберите загрузку, для которой невозможно подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="9051e-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="9051e-123">На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="9051e-124">Запишите значение поля **Созданное количество работы**.</span><span class="sxs-lookup"><span data-stu-id="9051e-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="9051e-125">В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="9051e-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="9051e-126">Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="9051e-127">Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.</span><span class="sxs-lookup"><span data-stu-id="9051e-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="9051e-128">Отмените коды работы, которые были созданы для местоположения упаковки в качестве окончательного местоположения отгрузки, перенастройте директиву местоположения и повторно выпустите загрузку.</span><span class="sxs-lookup"><span data-stu-id="9051e-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="9051e-129">Используйте следующую процедуру, чтобы отменить коды работ, которые имеют местоположение упаковки, заданное как окончательное местоположение отгрузки с автоматической контейнеризацией.</span><span class="sxs-lookup"><span data-stu-id="9051e-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="9051e-130">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="9051e-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="9051e-131">Откроется диалоговое окно **Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="9051e-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="9051e-132">В поле **Код работы** укажите код работы, которую необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="9051e-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="9051e-133">Выбранный код работы должен иметь значение **Статус работы** *Открыто*, *В работе*, *Отменено*, *Объединено* или *Закрыто*.</span><span class="sxs-lookup"><span data-stu-id="9051e-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="9051e-134">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9051e-134">Select **OK**.</span></span>
1. <span data-ttu-id="9051e-135">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="9051e-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="9051e-136">Повторите эту процедуру для других кодов работ по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9051e-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="9051e-137">Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="9051e-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="9051e-138">Следующая процедура используется для перенастройки директиву местоположения, чтобы она не использовала местоположение упаковки в качестве окончательного местоположения отгрузки, когда автоматическая контейнеризация настроена для шаблона волн.</span><span class="sxs-lookup"><span data-stu-id="9051e-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="9051e-139">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="9051e-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="9051e-140">В поле **Тип заказа на работу** выберите *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="9051e-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="9051e-141">Выберите директиву местоположения, которую вы используете для автоматической контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="9051e-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="9051e-142">На панели экспресс-вкладки **Действия директивы для места хранения** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="9051e-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="9051e-143">В диалоговом окне редактора запросов на вкладке **Диапазон** найдите строку, где **Поле** задано как *Профиль местонахождения*, и убедитесь, что в поле **Критерии** для этой строки не указан профиль местоположения, у которого **Тип местоположения** — *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="9051e-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="9051e-144">Измените поле **Критерии** так, чтобы скорректировать место окончательного размещения.</span><span class="sxs-lookup"><span data-stu-id="9051e-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="9051e-145">Используйте следующую процедуру, чтобы повторно выпустить загрузку и создать коды работ, используя правильное окончательные местоположение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="9051e-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="9051e-146">Перейдите в раздел **Управление складом \> Загрузки \> Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="9051e-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="9051e-147">В разделе **Загрузки** найдите загрузку, которую необходимо выпустить.</span><span class="sxs-lookup"><span data-stu-id="9051e-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="9051e-148">На панели инструментов раздела **Загрузки** выберите **Выпуск \> Выпуск на склад**, чтобы выпустить выбранную загрузку на склад.</span><span class="sxs-lookup"><span data-stu-id="9051e-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="9051e-149">Повторите эту процедуру для других загрузок по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9051e-149">Repeat this procedure for the other loads as needed.</span></span>
