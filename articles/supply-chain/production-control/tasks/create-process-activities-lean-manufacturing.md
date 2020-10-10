---
title: Создание мероприятий процесса для бережливого производства
description: Создайте мероприятие процесса для бережливого производства.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb8068012453fd4a8b06dea8cc8e5067d6968fe3
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826607"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="eddfc-103">Создание мероприятий процесса для бережливого производства</span><span class="sxs-lookup"><span data-stu-id="eddfc-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eddfc-104">Создайте мероприятие процесса для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="eddfc-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="eddfc-105">Обязательные компоненты:</span><span class="sxs-lookup"><span data-stu-id="eddfc-105">Prerequisites:</span></span> 

1. <span data-ttu-id="eddfc-106">Необходимо создать производственный поток и версию, которые будут неактивны.</span><span class="sxs-lookup"><span data-stu-id="eddfc-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="eddfc-107">Необходимо создать производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="eddfc-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="eddfc-108">Поиск версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="eddfc-108">Find the production flow version</span></span>
1. <span data-ttu-id="eddfc-109">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="eddfc-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="eddfc-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eddfc-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eddfc-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="eddfc-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="eddfc-112">Создание нового мероприятия</span><span class="sxs-lookup"><span data-stu-id="eddfc-112">Create a new activity</span></span>
1. <span data-ttu-id="eddfc-113">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="eddfc-113">Click Activities.</span></span>
    * <span data-ttu-id="eddfc-114">Убедитесь, что выбранный производственный поток содержит версию-черновик и выберите эту версию.</span><span class="sxs-lookup"><span data-stu-id="eddfc-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="eddfc-115">Щелкните "Создание нового мероприятия плана".</span><span class="sxs-lookup"><span data-stu-id="eddfc-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="eddfc-116">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="eddfc-116">Click Next.</span></span>
4. <span data-ttu-id="eddfc-117">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eddfc-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="eddfc-118">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eddfc-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eddfc-119">Обратите внимание, что имя должно быть уникальным для данного производственного потока для всех версий.</span><span class="sxs-lookup"><span data-stu-id="eddfc-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="eddfc-120">В поле "Количество процесса" введите число.</span><span class="sxs-lookup"><span data-stu-id="eddfc-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="eddfc-121">Обратите внимание, что независимо от того, какое количество задания будет обработано, это минимальное количество на задание для расчета трудовых затрат.</span><span class="sxs-lookup"><span data-stu-id="eddfc-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="eddfc-122">Если количества для задания отличаются от этого количества, то будет создано отклонение стоимости.</span><span class="sxs-lookup"><span data-stu-id="eddfc-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="eddfc-123">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="eddfc-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="eddfc-124">Выбор производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="eddfc-124">Select the work cell</span></span>
1. <span data-ttu-id="eddfc-125">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="eddfc-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="eddfc-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="eddfc-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="eddfc-127">Определение обновлений запасов</span><span class="sxs-lookup"><span data-stu-id="eddfc-127">Define the inventory updates</span></span>
1. <span data-ttu-id="eddfc-128">Установите или снимите флажок "Обновление запасов в наличии при поступлении".</span><span class="sxs-lookup"><span data-stu-id="eddfc-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="eddfc-129">Если значение "Обновление запасов в наличии" — "Нет", можно определить мероприятие для получения полуфабриката (мероприятие не достигает следующего уровня спецификации).</span><span class="sxs-lookup"><span data-stu-id="eddfc-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="eddfc-130">Можно также выбрать потребление полуфабрикатов.</span><span class="sxs-lookup"><span data-stu-id="eddfc-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="eddfc-131">Определение мероприятий комплектации</span><span class="sxs-lookup"><span data-stu-id="eddfc-131">Define the picking activities</span></span>
1. <span data-ttu-id="eddfc-132">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="eddfc-132">Click Next.</span></span>
2. <span data-ttu-id="eddfc-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eddfc-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="eddfc-134">Мероприятия комплектации по умолчанию создается для исходного местоположения выбранной производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="eddfc-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="eddfc-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="eddfc-135">Click Add.</span></span>
    * <span data-ttu-id="eddfc-136">Можно создать дополнительные мероприятия комплектации для конкретных продуктов, которые не указаны в исходном мероприятии производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="eddfc-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="eddfc-137">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eddfc-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="eddfc-138">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eddfc-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="eddfc-139">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="eddfc-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="eddfc-140">С этим определением все материалы, потребленные в мероприятии комплектуются из исходного склада и местоположения по умолчанию за исключением номенклатуры, которая определена во втором мероприятии комплектации.</span><span class="sxs-lookup"><span data-stu-id="eddfc-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="eddfc-141">Эта номенклатура будет скомплектована из других склада и местоположения.</span><span class="sxs-lookup"><span data-stu-id="eddfc-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="eddfc-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eddfc-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="eddfc-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="eddfc-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="eddfc-144">Установите или удалите флажок "Зарегистрировать отходы".</span><span class="sxs-lookup"><span data-stu-id="eddfc-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="eddfc-145">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="eddfc-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="eddfc-146">Определение времени мероприятия</span><span class="sxs-lookup"><span data-stu-id="eddfc-146">Define the activity times</span></span>
1. <span data-ttu-id="eddfc-147">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eddfc-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eddfc-148">Требуется определение времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="eddfc-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="eddfc-149">Время выполнения используется для расчета затрат и времени пропускной способности заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="eddfc-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="eddfc-150">Времена выполнения не используются для расчета максимальной мощности и потребления, это рассчитывается временем цикла, производным от задачи версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="eddfc-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="eddfc-151">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="eddfc-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="eddfc-152">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eddfc-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="eddfc-153">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="eddfc-153">Select the Time unit.</span></span>
5. <span data-ttu-id="eddfc-154">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="eddfc-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="eddfc-155">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eddfc-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eddfc-156">Время ожидания в очереди является необязательным.</span><span class="sxs-lookup"><span data-stu-id="eddfc-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="eddfc-157">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="eddfc-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="eddfc-158">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eddfc-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="eddfc-159">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="eddfc-159">Select the Time unit.</span></span>
10. <span data-ttu-id="eddfc-160">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="eddfc-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="eddfc-161">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="eddfc-161">Click Next.</span></span>
12. <span data-ttu-id="eddfc-162">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="eddfc-162">Click Finish.</span></span>
13. <span data-ttu-id="eddfc-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eddfc-163">Close the page.</span></span>

