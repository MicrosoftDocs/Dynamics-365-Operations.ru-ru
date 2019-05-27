---
title: Создание правила канбана события продаж
description: Эта процедура описывает настройку, необходимую для создания правила канбана, которое запускается во время создания заказа на продажу.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573075"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="dc24b-103">Создание правила канбана события продаж</span><span class="sxs-lookup"><span data-stu-id="dc24b-103">Create a sales event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc24b-104">Эта процедура описывает настройку, необходимую для создания правила канбана, которое запускается во время создания заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="dc24b-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="dc24b-105">Правило канбана событий пополняет требования, созданные из строк заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="dc24b-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="dc24b-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="dc24b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dc24b-107">Это предназначено для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта.</span><span class="sxs-lookup"><span data-stu-id="dc24b-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="dc24b-108">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="dc24b-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="dc24b-109">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="dc24b-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="dc24b-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="dc24b-110">Click New.</span></span>
3. <span data-ttu-id="dc24b-111">В поле "Стратегия пополнения" выберите "Событие".</span><span class="sxs-lookup"><span data-stu-id="dc24b-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="dc24b-112">Выбор событие означает, что правило канбана запускается событием, например, созданием строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="dc24b-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="dc24b-113">Это применяется к областям, где каждый канбан должен покрывать определенный спрос.</span><span class="sxs-lookup"><span data-stu-id="dc24b-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="dc24b-114">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="dc24b-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="dc24b-115">Выберите окончательную сборку.</span><span class="sxs-lookup"><span data-stu-id="dc24b-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="dc24b-116">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="dc24b-116">Expand the Details section.</span></span>
6. <span data-ttu-id="dc24b-117">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="dc24b-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="dc24b-118">Выберите L0050.</span><span class="sxs-lookup"><span data-stu-id="dc24b-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="dc24b-119">Определение события</span><span class="sxs-lookup"><span data-stu-id="dc24b-119">Define an event</span></span>
1. <span data-ttu-id="dc24b-120">Разверните раздел "События".</span><span class="sxs-lookup"><span data-stu-id="dc24b-120">Expand the Events section.</span></span>
2. <span data-ttu-id="dc24b-121">В поле "Событие продажи" выберите "Автоматическое".</span><span class="sxs-lookup"><span data-stu-id="dc24b-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="dc24b-122">При выборе события продаж "автоматическое" это правило канбана будет запускаться автоматически, когда строка продаж будет соответствовать местоположению продукта и поступления.</span><span class="sxs-lookup"><span data-stu-id="dc24b-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="dc24b-123">В этой процедуре это продукт L0050 на складе 13.</span><span class="sxs-lookup"><span data-stu-id="dc24b-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="dc24b-124">Установите минимальное количество событий "50".</span><span class="sxs-lookup"><span data-stu-id="dc24b-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="dc24b-125">С минимальным количеством события 50 правило канбана будет только запускаться событиями с количеством 50 или больше.</span><span class="sxs-lookup"><span data-stu-id="dc24b-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="dc24b-126">Разверните раздел "Производственный поток".</span><span class="sxs-lookup"><span data-stu-id="dc24b-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="dc24b-127">Обратите внимание, что местоположение поступления находится на складе 13.</span><span class="sxs-lookup"><span data-stu-id="dc24b-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="dc24b-128">Это означает, что это правило канбана будет запускаться для этого местоположения.</span><span class="sxs-lookup"><span data-stu-id="dc24b-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="dc24b-129">В этом примере строка продажи для продукта L0050, с количеством 50 или больше, на складе 13 запустит это правило канбана.</span><span class="sxs-lookup"><span data-stu-id="dc24b-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="dc24b-130">Создание строки продажи для запуска правила канбана события</span><span class="sxs-lookup"><span data-stu-id="dc24b-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="dc24b-131">Перейдите в раздел "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="dc24b-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="dc24b-132">Предупреждение отображается, когда правило канбана сохраняется; это означает, что канбаны будут созданы в реальном времени во время создания заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="dc24b-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="dc24b-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="dc24b-133">Click New.</span></span>
3. <span data-ttu-id="dc24b-134">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="dc24b-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="dc24b-135">Например, выберите US-003.</span><span class="sxs-lookup"><span data-stu-id="dc24b-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="dc24b-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dc24b-136">Click OK.</span></span>
5. <span data-ttu-id="dc24b-137">В поле "Код номенклатуры" введите "L0050".</span><span class="sxs-lookup"><span data-stu-id="dc24b-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="dc24b-138">В поле "Сайт" введите "1".</span><span class="sxs-lookup"><span data-stu-id="dc24b-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="dc24b-139">Выберите сайт 1, поскольку склад 13 находится на сайте 1.</span><span class="sxs-lookup"><span data-stu-id="dc24b-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="dc24b-140">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="dc24b-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="dc24b-141">Задайте склад 13.</span><span class="sxs-lookup"><span data-stu-id="dc24b-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="dc24b-142">В поле "Количество" укажите "75".</span><span class="sxs-lookup"><span data-stu-id="dc24b-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="dc24b-143">Введите количество 50 или больше для запуска созданного правила канбана.</span><span class="sxs-lookup"><span data-stu-id="dc24b-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="dc24b-144">Проверка, что канбан создан</span><span class="sxs-lookup"><span data-stu-id="dc24b-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="dc24b-145">Щелкните "Продукт и поставки".</span><span class="sxs-lookup"><span data-stu-id="dc24b-145">Click Product and supply.</span></span>
2. <span data-ttu-id="dc24b-146">Щелкните "Просмотр дерева информации об источниках потребности".</span><span class="sxs-lookup"><span data-stu-id="dc24b-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="dc24b-147">Обратите внимание, что создается канбан с тем же количеством, что и в строке продажи.</span><span class="sxs-lookup"><span data-stu-id="dc24b-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="dc24b-148">Можно также просмотреть расходы на материалы, необходимые для производства L0050.</span><span class="sxs-lookup"><span data-stu-id="dc24b-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="dc24b-149">Это последний этап в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="dc24b-149">This is the last step in this procedure.</span></span>  

