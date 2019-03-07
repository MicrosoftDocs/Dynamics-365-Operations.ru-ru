---
title: Создание субподрядной производственной ячейки для бережливого производства
description: Для моделирования субподрядной работы для бережливого производства необходимо создать производственную ячейку, связанную с поставщиком, выполняющим работу.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "319163"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="e7c45-103">Создание субподрядной производственной ячейки для бережливого производства</span><span class="sxs-lookup"><span data-stu-id="e7c45-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7c45-104">Для моделирования субподрядной работы для бережливого производства необходимо создать производственную ячейку, связанную с поставщиком, выполняющим работу.</span><span class="sxs-lookup"><span data-stu-id="e7c45-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="e7c45-105">Субподрядная производственная ячейка связывается с поставщиком посредством привязки ресурса типа "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="e7c45-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="e7c45-106">Если вы воспроизводите эту запись в демонстрационной компании USMF, вы можете выбрать код счет поставщика 1002 и сайт 1.</span><span class="sxs-lookup"><span data-stu-id="e7c45-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="e7c45-107">Создание ресурса поставщика</span><span class="sxs-lookup"><span data-stu-id="e7c45-107">Create a vendor resource</span></span>
1. <span data-ttu-id="e7c45-108">Перейдите в раздел "Ресурсы".</span><span class="sxs-lookup"><span data-stu-id="e7c45-108">Go to Resources.</span></span>
2. <span data-ttu-id="e7c45-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e7c45-109">Click New.</span></span>
3. <span data-ttu-id="e7c45-110">В поле "Ресурс" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7c45-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="e7c45-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7c45-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e7c45-112">В поле "Тип" выберите "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="e7c45-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="e7c45-113">В поле "Поставщик" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="e7c45-114">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e7c45-114">Create the resource group</span></span>
1. <span data-ttu-id="e7c45-115">Перейдите в раздел "Группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="e7c45-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="e7c45-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e7c45-116">Click New.</span></span>
3. <span data-ttu-id="e7c45-117">В поле "Группа ресурсов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7c45-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="e7c45-118">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7c45-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e7c45-119">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e7c45-120">Выберите сайт, к которому должна относиться производственная ячейка.</span><span class="sxs-lookup"><span data-stu-id="e7c45-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="e7c45-121">В теории сайт может представлять собой отдельный сайт, находящийся под управлением поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7c45-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="e7c45-122">Однако в большинстве случаев субподрядные ресурсы просто выделяются сайту, который заказывает субподрядную работу.</span><span class="sxs-lookup"><span data-stu-id="e7c45-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="e7c45-123">Обратите внимание, что склады получения и выпуска субподрядных производственных ячеек должна находиться на одном и том же сайте.</span><span class="sxs-lookup"><span data-stu-id="e7c45-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="e7c45-124">В поле "Сайт" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7c45-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="e7c45-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="e7c45-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="e7c45-126">Установите или снимите флажок "Производственная ячейка".</span><span class="sxs-lookup"><span data-stu-id="e7c45-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="e7c45-127">В поле "Склад получения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e7c45-128">Выберите склад и местонахождение, используемые для промежуточного размещения материала для производственной ячейки под управлением поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7c45-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="e7c45-129">Во многих случаях склад и местонахождение моделируются путем использования отдельного склада для каждого поставщика и одного местонахождения для каждой производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="e7c45-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="e7c45-130">В поле "Местонахождение получения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e7c45-131">В поле "Склад выхода" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e7c45-132">Определите склад и местонахождение, на которые разносится материал при разноски субподрядных мероприятий производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="e7c45-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="e7c45-133">Склад и местонахождение могут находиться на сайте поставщика, если поставщик отчитывается о заданиях канбана.</span><span class="sxs-lookup"><span data-stu-id="e7c45-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="e7c45-134">Другой вариант — склад и местонахождение могут представлять собой местонахождение получения, связанное со следующим шагом производственного потока.</span><span class="sxs-lookup"><span data-stu-id="e7c45-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="e7c45-135">В поле "Местонахождение выхода" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="e7c45-136">Разверните или сверните раздел "Календари".</span><span class="sxs-lookup"><span data-stu-id="e7c45-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="e7c45-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e7c45-137">Click Add.</span></span>
15. <span data-ttu-id="e7c45-138">В поле "Календарь" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e7c45-139">Свяжите календарь рабочего времени производственной ячейки с группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7c45-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="e7c45-140">Для критических ресурсов рекомендуется определять конкретные календари, представляющие точное рабочее время и связанные с ним мощности производственной ячейки или сайта поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7c45-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="e7c45-141">Разверните или сверните раздел "Ресурсы".</span><span class="sxs-lookup"><span data-stu-id="e7c45-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="e7c45-142">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e7c45-142">Click Add.</span></span>
    * <span data-ttu-id="e7c45-143">Группа субподрядных ресурсов должна иметь связанный ресурс типа "Поставщик", который привязывает группу ресурсов к счету поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7c45-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="e7c45-144">В поле "Ресурсы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e7c45-145">Выберите или введите ресурс поставщика, созданный в предыдущей подзадаче.</span><span class="sxs-lookup"><span data-stu-id="e7c45-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="e7c45-146">Разверните или сверните раздел "Мощность производственной ячейки".</span><span class="sxs-lookup"><span data-stu-id="e7c45-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="e7c45-147">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e7c45-147">Click Add.</span></span>
    * <span data-ttu-id="e7c45-148">Производственная ячейка должна иметь определенную мощность.</span><span class="sxs-lookup"><span data-stu-id="e7c45-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="e7c45-149">В этом примере мы создадим пропускную способность, равную 100 штук в стандартный рабочий день.</span><span class="sxs-lookup"><span data-stu-id="e7c45-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="e7c45-150">В поле "Модель производственного потока" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="e7c45-151">В поле "Период мощности" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="e7c45-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="e7c45-152">В поле "Среднее количество пропускной способности" введите число.</span><span class="sxs-lookup"><span data-stu-id="e7c45-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="e7c45-153">В поле "Единица измерения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e7c45-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="e7c45-154">Разрешить изменение единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="e7c45-154">ResolveChanges the Unit.</span></span>

