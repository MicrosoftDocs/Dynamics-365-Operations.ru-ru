--- 
title: "Создание правила канбана события строки спецификации"
description: "Эта задача рассматривает настройку, необходимую для создания правила канбана событий, чтобы обеспечить поставку для строк производственной спецификации в смешанной среде бережливого и классического производства."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.openlocfilehash: 4168a515f5bc1b69a24aac616aba7e447ccda11a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="d96ba-103">Создание правила канбана события строки спецификации</span><span class="sxs-lookup"><span data-stu-id="d96ba-103">Create a BOM line event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d96ba-104">Эта задача рассматривает настройку, необходимую для создания правила канбана событий, чтобы обеспечить поставку для строк производственной спецификации в смешанной среде бережливого и классического производства.</span><span class="sxs-lookup"><span data-stu-id="d96ba-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="d96ba-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d96ba-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="d96ba-106">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта.</span><span class="sxs-lookup"><span data-stu-id="d96ba-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="d96ba-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="d96ba-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="d96ba-108">Перейдите в раздел "Управление производством" > "Периодические задачи" > "Расчет количества канбанов" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="d96ba-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="d96ba-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d96ba-109">Click New.</span></span>
3. <span data-ttu-id="d96ba-110">В поле "Тип" выберите "Изъятие".</span><span class="sxs-lookup"><span data-stu-id="d96ba-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="d96ba-111">Тип "Изъятие" используется для создания канбанов перемещения.</span><span class="sxs-lookup"><span data-stu-id="d96ba-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="d96ba-112">В поле "Стратегия пополнения" выберите "Событие".</span><span class="sxs-lookup"><span data-stu-id="d96ba-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="d96ba-113">Стратегия события выбирается для создания перемещения канбанов на основе события.</span><span class="sxs-lookup"><span data-stu-id="d96ba-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="d96ba-114">Далее в руководстве по задаче мы вызовем его, оценив производственный заказ.</span><span class="sxs-lookup"><span data-stu-id="d96ba-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="d96ba-115">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d96ba-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="d96ba-116">Введите или выберите ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="d96ba-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="d96ba-117">Это мероприятие перемещения имеет склад приемки (выпуск) и местоположение 12. Это означает, что материал перемещается в местоположение 12 на складе 12.</span><span class="sxs-lookup"><span data-stu-id="d96ba-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="d96ba-118">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="d96ba-118">Expand the Details section.</span></span>
7. <span data-ttu-id="d96ba-119">В поле "Продукт" введите или выберите M0001.</span><span class="sxs-lookup"><span data-stu-id="d96ba-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="d96ba-120">Разверните раздел "События".</span><span class="sxs-lookup"><span data-stu-id="d96ba-120">Expand the Events section.</span></span>
9. <span data-ttu-id="d96ba-121">В поле "Событие строки спецификации" выберите "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="d96ba-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="d96ba-122">Если в поле события строки спецификации задано значение "Автоматически", канбан будет создан для удовлетворения потребности в материале для строк спецификации производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d96ba-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="d96ba-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d96ba-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="d96ba-124">Создание и изменение нового производственного заказа</span><span class="sxs-lookup"><span data-stu-id="d96ba-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="d96ba-125">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="d96ba-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="d96ba-126">Щелкните "Новый производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="d96ba-126">Click New production order.</span></span>
3. <span data-ttu-id="d96ba-127">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d96ba-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="d96ba-128">Введите или выберите "L0001".</span><span class="sxs-lookup"><span data-stu-id="d96ba-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="d96ba-129">Мы используем номенклатуру L0001, так как номенклатура M0001 включена в спецификацию для номенклатуры L0001.</span><span class="sxs-lookup"><span data-stu-id="d96ba-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="d96ba-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d96ba-130">Click Create.</span></span>
5. <span data-ttu-id="d96ba-131">В списке перейдите по ссылке в строке L0001.</span><span class="sxs-lookup"><span data-stu-id="d96ba-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="d96ba-132">Щелкните "Спецификация".</span><span class="sxs-lookup"><span data-stu-id="d96ba-132">Click BOM.</span></span>
7. <span data-ttu-id="d96ba-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d96ba-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d96ba-134">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d96ba-134">Click Edit.</span></span>
9. <span data-ttu-id="d96ba-135">В поле "Тип строки" выберите "Фиксированное снабжение".</span><span class="sxs-lookup"><span data-stu-id="d96ba-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="d96ba-136">Фиксированное снабжение выбирается для активации создания поставки канбана.</span><span class="sxs-lookup"><span data-stu-id="d96ba-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="d96ba-137">Выберите значение "Нет" в поле "Потребление ресурса".</span><span class="sxs-lookup"><span data-stu-id="d96ba-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="d96ba-138">Если снять флажок "Потребление ресурса", можно изменить склад.</span><span class="sxs-lookup"><span data-stu-id="d96ba-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="d96ba-139">Разверните раздел "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="d96ba-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="d96ba-140">В поле "Склад" введите "12".</span><span class="sxs-lookup"><span data-stu-id="d96ba-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="d96ba-141">Для склада задано значение 12, так как он является складом выпуска для мероприятия изъятия.</span><span class="sxs-lookup"><span data-stu-id="d96ba-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="d96ba-142">В поле "Местонахождение" введите "12".</span><span class="sxs-lookup"><span data-stu-id="d96ba-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="d96ba-143">Для местонахождения задано значение 12, так как оно является местонахождением выпуска для мероприятия изъятия.</span><span class="sxs-lookup"><span data-stu-id="d96ba-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="d96ba-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d96ba-144">Close the page.</span></span>
15. <span data-ttu-id="d96ba-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d96ba-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="d96ba-146">Оценка производственного заказа и просмотр созданного канбана</span><span class="sxs-lookup"><span data-stu-id="d96ba-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="d96ba-147">Щелкните "Оценка".</span><span class="sxs-lookup"><span data-stu-id="d96ba-147">Click Estimate.</span></span>
    * <span data-ttu-id="d96ba-148">Оценка производственного заказа активирует создание связанного канбана на поставку номенклатуры M0001.</span><span class="sxs-lookup"><span data-stu-id="d96ba-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="d96ba-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d96ba-149">Click OK.</span></span>
3. <span data-ttu-id="d96ba-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d96ba-150">Close the page.</span></span>
4. <span data-ttu-id="d96ba-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d96ba-151">Close the page.</span></span>
5. <span data-ttu-id="d96ba-152">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="d96ba-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="d96ba-153">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d96ba-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d96ba-154">Выберите правило канбана события, созданное для номенклатуры M0001.</span><span class="sxs-lookup"><span data-stu-id="d96ba-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="d96ba-155">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="d96ba-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="d96ba-156">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d96ba-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d96ba-157">Обратите внимание, что канбан создан на поставку M0001 для оценки производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d96ba-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="d96ba-158">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="d96ba-158">This is the last step!</span></span>  


