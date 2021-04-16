---
title: Устранение неполадок в складских иерархиях резервирования партий или серий
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с иерархиями резервирования, которые используют аналитики партии или серии.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838186"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="56450-103">Устранение неполадок в складских иерархиях резервирования партий или серий</span><span class="sxs-lookup"><span data-stu-id="56450-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56450-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с иерархиями резервирования, которые используют аналитики партии или серии.</span><span class="sxs-lookup"><span data-stu-id="56450-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="56450-105">Дополнительные сведения см. в разделе [Гибкая политика резервирования аналитик на уровне склада](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="56450-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="56450-106">Иерархия резервирования номенклатуры определяет требование аналитик хранения, которые должны быть выполнены, чтобы назначить местоположение для заказа спроса.</span><span class="sxs-lookup"><span data-stu-id="56450-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="56450-107">Эти аналитики могут быть описаны как *аналитики выше местоположения* для всех аналитик, которые должны быть выполнены до назначения местоположения, и *аналитики ниже местоположения* для аналитик, которые могут быть распределены после того, как местоположение было назначено для заказа спроса.</span><span class="sxs-lookup"><span data-stu-id="56450-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="56450-108">Эти иерархии резервирования также называются иерархиями резервирования *партия выше* и *партия ниже* или иерархиями резервирования *серийный выше* и *серийный ниже*.</span><span class="sxs-lookup"><span data-stu-id="56450-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="56450-109">Запасы могут быть успешно распределены только в том случае, если в аналитиках выше местоположения нет разрывов.</span><span class="sxs-lookup"><span data-stu-id="56450-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="56450-110">Например, в иерархии резервирования *партия выше* ожидается, что в заказе спроса будут заданы аналитики **Сайт**, **Склад** и **Номер партии**.</span><span class="sxs-lookup"><span data-stu-id="56450-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="56450-111">Если какие-либо из этих аналитик отсутствуют, процесс распределения завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="56450-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="56450-112">Напротив, в иерархии резервирования *партия ниже* или *серийный ниже* в заказе спроса может быть указан номер партии или серийный номер, но процесс распределения их не требует.</span><span class="sxs-lookup"><span data-stu-id="56450-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="56450-113">Получено следующее сообщение об ошибке: "Для назначения волне в строках загрузки должны быть указаны аналитики, находящийся над местоположением.</span><span class="sxs-lookup"><span data-stu-id="56450-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="56450-114">Чтобы назначить эти аналитики, зарезервируйте и заново создайте строку загрузки."</span><span class="sxs-lookup"><span data-stu-id="56450-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="56450-115">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="56450-115">Issue description</span></span>

<span data-ttu-id="56450-116">При использовании номенклатуры, имеющей иерархию резервирования *партия выше*, команда **Запуск на склад** на странице **Рабочее место планирования загрузки** не работает, если попытаться выпустить загрузку для неполного количества.</span><span class="sxs-lookup"><span data-stu-id="56450-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="56450-117">Выводится это сообщение об ошибке, и работа с частичным количеством не создается.</span><span class="sxs-lookup"><span data-stu-id="56450-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="56450-118">Однако при использовании номенклатуры, имеющей иерархию резервирования *партия ниже*, вы можете выпустить загрузку для частичного количества со страницы **Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="56450-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="56450-119">Причина проблемы</span><span class="sxs-lookup"><span data-stu-id="56450-119">Issue cause</span></span>

<span data-ttu-id="56450-120">Когда аналитика находится над аналитикой **Местоположение** в иерархии резервирования, она должна быть указана до выпуска на склад.</span><span class="sxs-lookup"><span data-stu-id="56450-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="56450-121">Частичные количества не могут быть выпущены, если не указана одна или несколько аналитик, расположенных выше аналитики **Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="56450-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="56450-122">Запрос на автоматическое резервирование для номера партии запускается даже в том случае, если имеются доступные запасы.</span><span class="sxs-lookup"><span data-stu-id="56450-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="56450-123">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="56450-123">Issue description</span></span>

<span data-ttu-id="56450-124">При использовании номенклатуры с иерархией резервирования *партия выше* на складе, для которого не были активированы складские процессы и включено автоматическое резервирование, запрос автоматического резервирования для номера партии отображается даже в том случае, если для комплектации доступна только одна партия.</span><span class="sxs-lookup"><span data-stu-id="56450-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="56450-125">Однако при использовании той же номенклатуры на складе, где включены складские процессы, запрос автоматического резервирования не отображается.</span><span class="sxs-lookup"><span data-stu-id="56450-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="56450-126">Причина проблемы</span><span class="sxs-lookup"><span data-stu-id="56450-126">Issue cause</span></span>

<span data-ttu-id="56450-127">Если иерархия резервирования определена как *партия выше* или *серийный выше*, указанная аналитика (**Номер партии** или **Серийный номер**) всегда должна быть указана в заказах спроса.</span><span class="sxs-lookup"><span data-stu-id="56450-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="56450-128">Складские процессы могут заполнять информацию, если доступна только одна партия или серийный номер.</span><span class="sxs-lookup"><span data-stu-id="56450-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="56450-129">Однако поскольку склад не активирован для складских процессов, пользователь должен всегда указывать все аналитики, находящиеся выше аналитики **Расположение**.</span><span class="sxs-lookup"><span data-stu-id="56450-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="56450-130">Шаблоны слоттинга, которые имеют критерий слота запасов в наличии, не учитывают текущие запасы в наличии для номенклатур, для которых включен учет партий.</span><span class="sxs-lookup"><span data-stu-id="56450-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="56450-131">Дополнительные сведения см. в разделе [Слоттинг на складе](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="56450-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="56450-132">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="56450-132">Issue description</span></span>

<span data-ttu-id="56450-133">Шаблоны слоттинга, которые имеют критерий слота *Запасы в наличии*, не учитывают текущие запасы в наличии для номенклатур *партия выше*.</span><span class="sxs-lookup"><span data-stu-id="56450-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="56450-134">Они учитывают их только в том случае, если номер партии указан в строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="56450-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="56450-135">Однако при использовании номенклатур *партия ниже* текущие запасы в наличии рассматриваются, как ожидается.</span><span class="sxs-lookup"><span data-stu-id="56450-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="56450-136">Причина проблемы</span><span class="sxs-lookup"><span data-stu-id="56450-136">Issue cause</span></span>

<span data-ttu-id="56450-137">Заголовок шаблона слоттинга можно определить для стратегии спроса *Заказано*, *Зарезервировано* или *Выпущено*.</span><span class="sxs-lookup"><span data-stu-id="56450-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="56450-138">Для стратегии спроса *Заказано* действуют те же требования иерархии резервирования, которые применяются для резервирования или выпуска в складских процессах.</span><span class="sxs-lookup"><span data-stu-id="56450-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="56450-139">Таким образом, для номенклатур, имеющих иерархии резервирования *партия-выше* и *серийный-ниже*, в заказе спроса (на продажу или перемещение) должен быть указан номер партии или серийный номер.</span><span class="sxs-lookup"><span data-stu-id="56450-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="56450-140">В качестве альтернативы можно использовать стратегию спроса *Зарезервировано*, чтобы выбрать номер партии или серийный номер, прежде чем будет сгенерирован спрос слоттинга для склада.</span><span class="sxs-lookup"><span data-stu-id="56450-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
