---
title: Создание правила канбана события строки спецификации
description: Эта задача рассматривает настройку, необходимую для создания правила канбана событий, чтобы обеспечить поставку для строк производственной спецификации в смешанной среде бережливого и классического производства.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 698b7af3bc8e2146aaf86fb5e04dd123ea6d5153
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435762"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="7e3db-103">Создание правила канбана события строки спецификации</span><span class="sxs-lookup"><span data-stu-id="7e3db-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e3db-104">Эта задача рассматривает настройку, необходимую для создания правила канбана событий, чтобы обеспечить поставку для строк производственной спецификации в смешанной среде бережливого и классического производства.</span><span class="sxs-lookup"><span data-stu-id="7e3db-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="7e3db-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="7e3db-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7e3db-106">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта.</span><span class="sxs-lookup"><span data-stu-id="7e3db-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="7e3db-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="7e3db-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="7e3db-108">Перейдите в раздел "Управление производством" > "Периодические задачи" > "Расчет количества канбанов" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="7e3db-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="7e3db-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7e3db-109">Click New.</span></span>
3. <span data-ttu-id="7e3db-110">В поле "Тип" выберите "Изъятие".</span><span class="sxs-lookup"><span data-stu-id="7e3db-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="7e3db-111">Тип "Изъятие" используется для создания канбанов перемещения.</span><span class="sxs-lookup"><span data-stu-id="7e3db-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="7e3db-112">В поле "Стратегия пополнения" выберите "Событие".</span><span class="sxs-lookup"><span data-stu-id="7e3db-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="7e3db-113">Стратегия события выбирается для создания перемещения канбанов на основе события.</span><span class="sxs-lookup"><span data-stu-id="7e3db-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="7e3db-114">Далее в руководстве по задаче мы вызовем его, оценив производственный заказ.</span><span class="sxs-lookup"><span data-stu-id="7e3db-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="7e3db-115">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7e3db-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7e3db-116">Введите или выберите ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="7e3db-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="7e3db-117">Это мероприятие перемещения имеет склад приемки (выпуск) и местоположение 12. Это означает, что материал перемещается в местоположение 12 на складе 12.</span><span class="sxs-lookup"><span data-stu-id="7e3db-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="7e3db-118">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="7e3db-118">Expand the Details section.</span></span>
7. <span data-ttu-id="7e3db-119">В поле "Продукт" введите или выберите M0001.</span><span class="sxs-lookup"><span data-stu-id="7e3db-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="7e3db-120">Разверните раздел "События".</span><span class="sxs-lookup"><span data-stu-id="7e3db-120">Expand the Events section.</span></span>
9. <span data-ttu-id="7e3db-121">В поле "Событие строки спецификации" выберите "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="7e3db-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="7e3db-122">Если в поле события строки спецификации задано значение "Автоматически", канбан будет создан для удовлетворения потребности в материале для строк спецификации производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7e3db-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="7e3db-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7e3db-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="7e3db-124">Создание и изменение нового производственного заказа</span><span class="sxs-lookup"><span data-stu-id="7e3db-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="7e3db-125">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="7e3db-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="7e3db-126">Щелкните "Новый производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="7e3db-126">Click New production order.</span></span>
3. <span data-ttu-id="7e3db-127">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7e3db-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7e3db-128">Введите или выберите "L0001".</span><span class="sxs-lookup"><span data-stu-id="7e3db-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="7e3db-129">Мы используем номенклатуру L0001, так как номенклатура M0001 включена в спецификацию для номенклатуры L0001.</span><span class="sxs-lookup"><span data-stu-id="7e3db-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="7e3db-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7e3db-130">Click Create.</span></span>
5. <span data-ttu-id="7e3db-131">В списке перейдите по ссылке в строке L0001.</span><span class="sxs-lookup"><span data-stu-id="7e3db-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="7e3db-132">Щелкните "Спецификация".</span><span class="sxs-lookup"><span data-stu-id="7e3db-132">Click BOM.</span></span>
7. <span data-ttu-id="7e3db-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7e3db-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="7e3db-134">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="7e3db-134">Click Edit.</span></span>
9. <span data-ttu-id="7e3db-135">В поле "Тип строки" выберите "Фиксированное снабжение".</span><span class="sxs-lookup"><span data-stu-id="7e3db-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="7e3db-136">Фиксированное снабжение выбирается для активации создания поставки канбана.</span><span class="sxs-lookup"><span data-stu-id="7e3db-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="7e3db-137">Выберите значение "Нет" в поле "Потребление ресурса".</span><span class="sxs-lookup"><span data-stu-id="7e3db-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="7e3db-138">Если снять флажок "Потребление ресурса", можно изменить склад.</span><span class="sxs-lookup"><span data-stu-id="7e3db-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="7e3db-139">Разверните раздел "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="7e3db-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="7e3db-140">В поле "Склад" введите "12".</span><span class="sxs-lookup"><span data-stu-id="7e3db-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="7e3db-141">Для склада задано значение 12, так как он является складом выпуска для мероприятия изъятия.</span><span class="sxs-lookup"><span data-stu-id="7e3db-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="7e3db-142">В поле "Местонахождение" введите "12".</span><span class="sxs-lookup"><span data-stu-id="7e3db-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="7e3db-143">Для местонахождения задано значение 12, так как оно является местонахождением выпуска для мероприятия изъятия.</span><span class="sxs-lookup"><span data-stu-id="7e3db-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="7e3db-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7e3db-144">Close the page.</span></span>
15. <span data-ttu-id="7e3db-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7e3db-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="7e3db-146">Оценка производственного заказа и просмотр созданного канбана</span><span class="sxs-lookup"><span data-stu-id="7e3db-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="7e3db-147">Щелкните "Оценка".</span><span class="sxs-lookup"><span data-stu-id="7e3db-147">Click Estimate.</span></span>
    * <span data-ttu-id="7e3db-148">Оценка производственного заказа активирует создание связанного канбана на поставку номенклатуры M0001.</span><span class="sxs-lookup"><span data-stu-id="7e3db-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="7e3db-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="7e3db-149">Click OK.</span></span>
3. <span data-ttu-id="7e3db-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7e3db-150">Close the page.</span></span>
4. <span data-ttu-id="7e3db-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7e3db-151">Close the page.</span></span>
5. <span data-ttu-id="7e3db-152">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="7e3db-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="7e3db-153">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7e3db-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7e3db-154">Выберите правило канбана события, созданное для номенклатуры M0001.</span><span class="sxs-lookup"><span data-stu-id="7e3db-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="7e3db-155">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="7e3db-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="7e3db-156">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7e3db-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7e3db-157">Обратите внимание, что канбан создан на поставку M0001 для оценки производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="7e3db-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="7e3db-158">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="7e3db-158">This is the last step!</span></span>  

