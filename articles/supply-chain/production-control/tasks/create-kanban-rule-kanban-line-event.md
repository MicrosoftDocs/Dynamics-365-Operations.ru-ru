---
title: Создание правила канбана с помощью события строки канбана
description: В ходе этой процедуры создается правило канбана с помощью настройки события строки канбана для запуска получения данных из мероприятия обработки.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bff5f16c1911739a29d50c546c3c2a9ab85c2371
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "350236"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="eb76b-103">Создание правила канбана с помощью события строки канбана</span><span class="sxs-lookup"><span data-stu-id="eb76b-103">Create a kanban rule using a kanban line event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb76b-104">В ходе этой процедуры создается правило канбана с помощью настройки события строки канбана для запуска получения данных из мероприятия обработки.</span><span class="sxs-lookup"><span data-stu-id="eb76b-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="eb76b-105">Правило канбана запускается для мероприятия обработки канбана с количеством, которое больше или равно 25 для каждого мероприятия.</span><span class="sxs-lookup"><span data-stu-id="eb76b-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="eb76b-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="eb76b-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="eb76b-107">Эта задача предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство нового или измененного продукта в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="eb76b-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="eb76b-108">Создание правила канбана</span><span class="sxs-lookup"><span data-stu-id="eb76b-108">Create a kanban rule</span></span>
1. <span data-ttu-id="eb76b-109">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="eb76b-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="eb76b-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eb76b-110">Click New.</span></span>
3. <span data-ttu-id="eb76b-111">В поле "Стратегия пополнения" выберите "Событие".</span><span class="sxs-lookup"><span data-stu-id="eb76b-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="eb76b-112">В результате канбаны будут созданы непосредственно из спроса.</span><span class="sxs-lookup"><span data-stu-id="eb76b-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="eb76b-113">Эта процедура используется для настройки правил, определяющих сценарий производства под заказ.</span><span class="sxs-lookup"><span data-stu-id="eb76b-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="eb76b-114">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb76b-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="eb76b-115">Введите или выберите SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="eb76b-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="eb76b-116">Первое мероприятие производственного правила канбана должно представлять собой мероприятие процесса в производственном потоке.</span><span class="sxs-lookup"><span data-stu-id="eb76b-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="eb76b-117">При выборе мероприятия даты срока действия мероприятия копируются в даты срока действия правила канбана.</span><span class="sxs-lookup"><span data-stu-id="eb76b-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="eb76b-118">Разверните раздел "Сведения".</span><span class="sxs-lookup"><span data-stu-id="eb76b-118">Expand the Details section.</span></span>
6. <span data-ttu-id="eb76b-119">В поле "Продукт" введите "L0001".</span><span class="sxs-lookup"><span data-stu-id="eb76b-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="eb76b-120">Разверните раздел "События".</span><span class="sxs-lookup"><span data-stu-id="eb76b-120">Expand the Events section.</span></span>
8. <span data-ttu-id="eb76b-121">В поле "Событие строки канбана" выберите "Автоматически".</span><span class="sxs-lookup"><span data-stu-id="eb76b-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="eb76b-122">В результате создаются канбаны событий по запросу.</span><span class="sxs-lookup"><span data-stu-id="eb76b-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="eb76b-123">Это поле используется для настройки правил канбана, которые пополняют материалы, необходимые для расположенного ниже в цепочке мероприятия обработки.</span><span class="sxs-lookup"><span data-stu-id="eb76b-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="eb76b-124">При выборе значения "Автоматически" канбаны событий создаются со спросом.</span><span class="sxs-lookup"><span data-stu-id="eb76b-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="eb76b-125">Эту настройку рекомендуется использовать, если вы ожидаете выполнять производство в тот же день.</span><span class="sxs-lookup"><span data-stu-id="eb76b-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="eb76b-126">Установите минимальное количество событий "25".</span><span class="sxs-lookup"><span data-stu-id="eb76b-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="eb76b-127">Канбаны событий создаются, если количество спроса больше или равно количеству в этом поле.</span><span class="sxs-lookup"><span data-stu-id="eb76b-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="eb76b-128">Это полезно, если нужно произвести количество по заказу меньше количества в этом поле на одном виде оборудования и больше количества в этом поле на другом виде оборудования.</span><span class="sxs-lookup"><span data-stu-id="eb76b-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="eb76b-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eb76b-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="eb76b-130">Создание заказа на продажу и активация цепочки канбана</span><span class="sxs-lookup"><span data-stu-id="eb76b-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="eb76b-131">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="eb76b-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="eb76b-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eb76b-132">Click New.</span></span>
3. <span data-ttu-id="eb76b-133">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb76b-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="eb76b-134">Выберите счет клиента US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="eb76b-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="eb76b-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="eb76b-135">Click OK.</span></span>
5. <span data-ttu-id="eb76b-136">В поле "Код номенклатуры" введите "L0001".</span><span class="sxs-lookup"><span data-stu-id="eb76b-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="eb76b-137">L0001 — это номенклатура, для которой создано правило канбана.</span><span class="sxs-lookup"><span data-stu-id="eb76b-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="eb76b-138">В поле "Количество" укажите "27".</span><span class="sxs-lookup"><span data-stu-id="eb76b-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="eb76b-139">Поскольку 27 превышает минимальное количество равное 25 в правиле канбана, будет активирован канбан события.</span><span class="sxs-lookup"><span data-stu-id="eb76b-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="eb76b-140">В поле "Сайт" введите "1".</span><span class="sxs-lookup"><span data-stu-id="eb76b-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="eb76b-141">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb76b-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="eb76b-142">Выберите склад 13.</span><span class="sxs-lookup"><span data-stu-id="eb76b-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="eb76b-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eb76b-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="eb76b-144">Просмотр канбан, созданного правилом канбана</span><span class="sxs-lookup"><span data-stu-id="eb76b-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="eb76b-145">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="eb76b-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="eb76b-146">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eb76b-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eb76b-147">Разверните раздел "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="eb76b-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="eb76b-148">Обратите внимание, что канбан для 27 был создан для обработки мероприятия на основе созданного правила канбана.</span><span class="sxs-lookup"><span data-stu-id="eb76b-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="eb76b-149">Это последний шаг.</span><span class="sxs-lookup"><span data-stu-id="eb76b-149">This is the last step.</span></span>  

