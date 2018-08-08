--- 
title: "Создание правила канбана с помощью события минимального запаса"
description: "Эта процедура рассматривает настройку, необходимую для создания правила канбана с помощью события минимального запаса, чтобы гарантировать, что определенный продукт всегда доступен в определенном местонахождении."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 97975a07d7f0a64a98595cf5dc7c8f572ded9a4d
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="30668-103">Создание правила канбана с помощью события минимального запаса</span><span class="sxs-lookup"><span data-stu-id="30668-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30668-104">Эта процедура рассматривает настройку, необходимую для создания правила канбана с помощью события минимального запаса, чтобы гарантировать, что определенный продукт всегда доступен в определенном местонахождении.</span><span class="sxs-lookup"><span data-stu-id="30668-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="30668-105">Правило канбана создается для перемещения материала в местонахождение, когда уровень запасов опускается ниже 200 шт.</span><span class="sxs-lookup"><span data-stu-id="30668-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="30668-106">В результате обработки события возникновения потребности создаются необходимые канбаны.</span><span class="sxs-lookup"><span data-stu-id="30668-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="30668-107">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="30668-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="30668-108">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="30668-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="30668-109">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="30668-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="30668-110">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="30668-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="30668-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="30668-111">Click New.</span></span>
3. <span data-ttu-id="30668-112">В поле "Тип" выберите "Изъятие".</span><span class="sxs-lookup"><span data-stu-id="30668-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="30668-113">Этот тип используется для создания канбанов перемещения.</span><span class="sxs-lookup"><span data-stu-id="30668-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="30668-114">В поле "Стратегия пополнения" выберите "Событие".</span><span class="sxs-lookup"><span data-stu-id="30668-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="30668-115">Стратегия события используется для создания канбанов перемещения на основе события.</span><span class="sxs-lookup"><span data-stu-id="30668-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="30668-116">Позже в этой процедуре вы активируете канбаны перемещения с помощью пополнения запасов.</span><span class="sxs-lookup"><span data-stu-id="30668-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="30668-117">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30668-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="30668-118">Введите или выберите ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="30668-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="30668-119">Это мероприятие перемещения имеет склад приемки (выпуск) и местонахождение 12. Это означает, что материалы перемещаются в местонахождение 12 на складе 12.</span><span class="sxs-lookup"><span data-stu-id="30668-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="30668-120">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="30668-120">Expand the Details section.</span></span>
7. <span data-ttu-id="30668-121">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30668-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="30668-122">Выберите M0007.</span><span class="sxs-lookup"><span data-stu-id="30668-122">Select M0007.</span></span>  
8. <span data-ttu-id="30668-123">Разверните раздел "События".</span><span class="sxs-lookup"><span data-stu-id="30668-123">Expand the Events section.</span></span>
9. <span data-ttu-id="30668-124">В поле "Событие пополнения запасов" выберите "Партия".</span><span class="sxs-lookup"><span data-stu-id="30668-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="30668-125">В результате создаются канбаны для удовлетворения потребности в материале в связанном местонахождении во время обработки события возникновения потребности.</span><span class="sxs-lookup"><span data-stu-id="30668-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="30668-126">Задание минимального количества для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="30668-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="30668-127">Щелкните для перехода по ссылке в поле "Продукт".</span><span class="sxs-lookup"><span data-stu-id="30668-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="30668-128">Щелкните для перехода по ссылке в поле "Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="30668-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="30668-129">Разверните информационное поле "Изображение продукта".</span><span class="sxs-lookup"><span data-stu-id="30668-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="30668-130">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="30668-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="30668-131">Щелкните "Покрытие номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="30668-131">Click Item coverage.</span></span>
6. <span data-ttu-id="30668-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="30668-132">Click New.</span></span>
7. <span data-ttu-id="30668-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="30668-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="30668-134">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30668-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="30668-135">Задайте склад 12.</span><span class="sxs-lookup"><span data-stu-id="30668-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="30668-136">Задайте минимальное значение "200".</span><span class="sxs-lookup"><span data-stu-id="30668-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="30668-137">Выполнение задания создания события партии</span><span class="sxs-lookup"><span data-stu-id="30668-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="30668-138">Перейдите в раздел "Управление производством" > "Периодические задачи" > "Обработка пакетных заданий канбана" > "Обработка события определения источника потребности".</span><span class="sxs-lookup"><span data-stu-id="30668-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="30668-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30668-139">Click OK.</span></span>
3. <span data-ttu-id="30668-140">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="30668-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="30668-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30668-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30668-142">Выберите правило канбана, созданное ранее.</span><span class="sxs-lookup"><span data-stu-id="30668-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="30668-143">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="30668-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="30668-144">Обратите внимание, что канбан был создан для перемещения необходимого материала на склад 12.</span><span class="sxs-lookup"><span data-stu-id="30668-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  


