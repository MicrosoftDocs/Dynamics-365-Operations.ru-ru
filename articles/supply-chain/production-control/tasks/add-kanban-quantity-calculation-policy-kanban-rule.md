--- 
title: "Добавление политики расчета количества канбанов в правило канбана"
description: "Эта процедура заключается в создании политики вычисления количества канбанов и добавлении ее к правилу канбана для оптимизации размера и количества канбанов."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7ca576210d5978383c91b6274f78028121efedbb
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="7c7ce-103">Добавление политики расчета количества канбанов в правило канбана</span><span class="sxs-lookup"><span data-stu-id="7c7ce-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c7ce-104">Эта процедура заключается в создании политики вычисления количества канбанов и добавлении ее к правилу канбана для оптимизации размера и количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="7c7ce-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7c7ce-106">Эта процедура предназначена для менеджера потока создания ценности.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="7c7ce-107">Эта процедура является предварительным условием для создания процедуры "Расчет предложений количества канбанов".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="7c7ce-108">Создание политики расчета количества канбанов</span><span class="sxs-lookup"><span data-stu-id="7c7ce-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="7c7ce-109">Перейдите в раздел "Управление производством" > "Периодические задачи" > "Расчет количества канбанов" > "Политики расчета количества канбанов".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="7c7ce-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-110">Click New.</span></span>
3. <span data-ttu-id="7c7ce-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7c7ce-112">Например, введите Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="7c7ce-113">В поле "Сводный план" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7c7ce-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c7ce-115">Выберите StaticPlan, чтобы рассчитать спрос.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="7c7ce-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7c7ce-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-117">Click Save.</span></span>
8. <span data-ttu-id="7c7ce-118">В поле "Минимальное количество канбанов" введите "1".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="7c7ce-119">Это дополнительное количество канбанов, включаемое в расчет количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="7c7ce-120">Установите коэффициент безопасности равным 1.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="7c7ce-121">Это коэффициент, используемый для расчета дополнительного количества резервного запаса.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="7c7ce-122">В поле "Дни перед" введите "30".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="7c7ce-123">Это число дней перед датой расчета количества канбанов, включаемое в расчет спроса.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="7c7ce-124">В поле "Дни до" введите "30".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="7c7ce-125">Это число дней после даты расчета количества канбанов, включаемое в расчет спроса.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="7c7ce-126">Формула, используемая для расчета, показана с фактическими значениями.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="7c7ce-127">Например, количество канбанов = ((средний ежедневный спрос x время упреждения x 2,00) / количество продукта на единицу обработки) + 1</span><span class="sxs-lookup"><span data-stu-id="7c7ce-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="7c7ce-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="7c7ce-129">Добавление политики расчета количества канбанов к правилу канбана</span><span class="sxs-lookup"><span data-stu-id="7c7ce-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="7c7ce-130">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="7c7ce-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c7ce-132">Выберите для этой процедуры правило канбана 000020.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="7c7ce-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7c7ce-134">Переключите развертывание раздела "Политики расчета количества канбанов".</span><span class="sxs-lookup"><span data-stu-id="7c7ce-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="7c7ce-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-135">Click Add.</span></span>
    * <span data-ttu-id="7c7ce-136">Добавьте политику расчета количества канбанов, созданную в предыдущей подзадаче.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="7c7ce-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="7c7ce-138">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7c7ce-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7c7ce-140">Выберите политику Speaker2016, созданную в предыдущей подзадаче.</span><span class="sxs-lookup"><span data-stu-id="7c7ce-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  


