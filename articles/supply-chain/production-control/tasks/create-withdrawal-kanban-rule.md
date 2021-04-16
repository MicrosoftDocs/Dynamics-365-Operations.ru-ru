---
title: Создание правила канбана изъятия
description: В этой процедуре показано, как выполнить настройку, необходимую для создания правила канбана изъятия для перемещения материалов в среде бережливого производства.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adbcdbb2d278b25dce1d8c027e66367e9c0930e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828834"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="c04e1-103">Создание правила канбана изъятия</span><span class="sxs-lookup"><span data-stu-id="c04e1-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c04e1-104">В этой процедуре показано, как выполнить настройку, необходимую для создания правила канбана изъятия для перемещения материалов в среде бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="c04e1-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="c04e1-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c04e1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c04e1-106">Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как они подготавливают пополнение нового или измененного материала.</span><span class="sxs-lookup"><span data-stu-id="c04e1-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="c04e1-107">Создать новое правило канбана</span><span class="sxs-lookup"><span data-stu-id="c04e1-107">Create new kanban rule</span></span>
1. <span data-ttu-id="c04e1-108">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="c04e1-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="c04e1-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c04e1-109">Click New.</span></span>
3. <span data-ttu-id="c04e1-110">В поле "Тип" выберите "Изъятие".</span><span class="sxs-lookup"><span data-stu-id="c04e1-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="c04e1-111">Тип "Изъятие" используется для правил канбана для переноса материалов или товаров.</span><span class="sxs-lookup"><span data-stu-id="c04e1-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="c04e1-112">В поле "Первое мероприятие плана" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c04e1-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c04e1-113">Выберите ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="c04e1-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="c04e1-114">Это мероприятие настроено для перемещения компонентов со склада 11, местоположения 11 на склад 12, местоположение 12.</span><span class="sxs-lookup"><span data-stu-id="c04e1-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="c04e1-115">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c04e1-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c04e1-116">Выберите M0007.</span><span class="sxs-lookup"><span data-stu-id="c04e1-116">Select M0007.</span></span>  
6. <span data-ttu-id="c04e1-117">В поле "Время упреждения" введите число.</span><span class="sxs-lookup"><span data-stu-id="c04e1-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="c04e1-118">Например, 60.</span><span class="sxs-lookup"><span data-stu-id="c04e1-118">For example, 60.</span></span>  
7. <span data-ttu-id="c04e1-119">В поле "Единица измерения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c04e1-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="c04e1-120">Например, минуты.</span><span class="sxs-lookup"><span data-stu-id="c04e1-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="c04e1-121">Настройка количеств для канбана</span><span class="sxs-lookup"><span data-stu-id="c04e1-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="c04e1-122">Установите количество по умолчанию равным 5.</span><span class="sxs-lookup"><span data-stu-id="c04e1-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="c04e1-123">Это количество, которое будет передано для каждого канбана.</span><span class="sxs-lookup"><span data-stu-id="c04e1-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="c04e1-124">В поле "Фиксированное количество канбанов" введите "2".</span><span class="sxs-lookup"><span data-stu-id="c04e1-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="c04e1-125">Это сумма канбанов, которые должны быть активными.</span><span class="sxs-lookup"><span data-stu-id="c04e1-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="c04e1-126">В этом случае 2 канбанов передают 5 каждый.</span><span class="sxs-lookup"><span data-stu-id="c04e1-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="c04e1-127">В поле "Минимальная граница оповещения" введите "1".</span><span class="sxs-lookup"><span data-stu-id="c04e1-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="c04e1-128">Используется для того, чтобы отслеживать минимальную сумму полных канбанов, которые должны находиться в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="c04e1-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="c04e1-129">Например, это используется при обзоре количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="c04e1-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="c04e1-130">В поле "Максимальная граница оповещения" введите "2".</span><span class="sxs-lookup"><span data-stu-id="c04e1-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="c04e1-131">Используется для того, чтобы отслеживать максимальную сумму полных канбанов, которые должны находиться в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="c04e1-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="c04e1-132">Например, это используется при обзоре количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="c04e1-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="c04e1-133">Создать канбаны</span><span class="sxs-lookup"><span data-stu-id="c04e1-133">Create kanbans</span></span>
1. <span data-ttu-id="c04e1-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c04e1-134">Click Save.</span></span>
    * <span data-ttu-id="c04e1-135">Правило канбана должно быть сохранено, прежде чем канбаны можно создать.</span><span class="sxs-lookup"><span data-stu-id="c04e1-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="c04e1-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="c04e1-136">Click Add.</span></span>
    * <span data-ttu-id="c04e1-137">Обратите внимание, что нет активных канбанов, поскольку для количества новых канбанов предлагается 2. Это равно значению в поле "Фиксированное количество канбанов".</span><span class="sxs-lookup"><span data-stu-id="c04e1-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="c04e1-138">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c04e1-138">Click Create.</span></span>
    * <span data-ttu-id="c04e1-139">Это создаст два канбана.</span><span class="sxs-lookup"><span data-stu-id="c04e1-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="c04e1-140">Обратите внимание, что 2 канбана, по 5 каждый, были созданы для этого правила канбана изъятия.</span><span class="sxs-lookup"><span data-stu-id="c04e1-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="c04e1-141">Это последний этап в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="c04e1-141">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]