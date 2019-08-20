---
title: Создание мероприятий процесса для бережливого производства
description: Создайте мероприятие процесса для бережливого производства.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 609a7872bd2388291aed88c0eb260b4a64d06391
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838615"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="c99fe-103">Создание мероприятий процесса для бережливого производства</span><span class="sxs-lookup"><span data-stu-id="c99fe-103">Create process activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c99fe-104">Создайте мероприятие процесса для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="c99fe-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="c99fe-105">Обязательные компоненты:</span><span class="sxs-lookup"><span data-stu-id="c99fe-105">Prerequisites:</span></span> 

1. <span data-ttu-id="c99fe-106">Необходимо создать производственный поток и версию, которые будут неактивны.</span><span class="sxs-lookup"><span data-stu-id="c99fe-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="c99fe-107">Необходимо создать производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="c99fe-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="c99fe-108">Поиск версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="c99fe-108">Find the production flow version</span></span>
1. <span data-ttu-id="c99fe-109">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="c99fe-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c99fe-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c99fe-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c99fe-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c99fe-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="c99fe-112">Создание нового мероприятия</span><span class="sxs-lookup"><span data-stu-id="c99fe-112">Create a new activity</span></span>
1. <span data-ttu-id="c99fe-113">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="c99fe-113">Click Activities.</span></span>
    * <span data-ttu-id="c99fe-114">Убедитесь, что выбранный производственный поток содержит версию-черновик и выберите эту версию.</span><span class="sxs-lookup"><span data-stu-id="c99fe-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="c99fe-115">Щелкните "Создание нового мероприятия плана".</span><span class="sxs-lookup"><span data-stu-id="c99fe-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="c99fe-116">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="c99fe-116">Click Next.</span></span>
4. <span data-ttu-id="c99fe-117">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c99fe-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c99fe-118">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c99fe-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c99fe-119">Обратите внимание, что имя должно быть уникальным для данного производственного потока для всех версий.</span><span class="sxs-lookup"><span data-stu-id="c99fe-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="c99fe-120">В поле "Количество процесса" введите число.</span><span class="sxs-lookup"><span data-stu-id="c99fe-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="c99fe-121">Обратите внимание, что независимо от того, какое количество задания будет обработано, это минимальное количество на задание для расчета трудовых затрат.</span><span class="sxs-lookup"><span data-stu-id="c99fe-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="c99fe-122">Если количества для задания отличаются от этого количества, то будет создано отклонение стоимости.</span><span class="sxs-lookup"><span data-stu-id="c99fe-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="c99fe-123">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="c99fe-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="c99fe-124">Выбор производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="c99fe-124">Select the work cell</span></span>
1. <span data-ttu-id="c99fe-125">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c99fe-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c99fe-126">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c99fe-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="c99fe-127">Определение обновлений запасов</span><span class="sxs-lookup"><span data-stu-id="c99fe-127">Define the inventory updates</span></span>
1. <span data-ttu-id="c99fe-128">Установите или снимите флажок "Обновление запасов в наличии при поступлении".</span><span class="sxs-lookup"><span data-stu-id="c99fe-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="c99fe-129">Если значение "Обновление запасов в наличии" — "Нет", можно определить мероприятие для получения полуфабриката (мероприятие не достигает следующего уровня спецификации).</span><span class="sxs-lookup"><span data-stu-id="c99fe-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="c99fe-130">Можно также выбрать потребление полуфабрикатов.</span><span class="sxs-lookup"><span data-stu-id="c99fe-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="c99fe-131">Определение мероприятий комплектации</span><span class="sxs-lookup"><span data-stu-id="c99fe-131">Define the picking activities</span></span>
1. <span data-ttu-id="c99fe-132">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="c99fe-132">Click Next.</span></span>
2. <span data-ttu-id="c99fe-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c99fe-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c99fe-134">Мероприятия комплектации по умолчанию создается для исходного местоположения выбранной производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="c99fe-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="c99fe-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="c99fe-135">Click Add.</span></span>
    * <span data-ttu-id="c99fe-136">Можно создать дополнительные мероприятия комплектации для конкретных продуктов, которые не указаны в исходном мероприятии производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="c99fe-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="c99fe-137">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c99fe-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c99fe-138">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c99fe-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="c99fe-139">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c99fe-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c99fe-140">С этим определением все материалы, потребленные в мероприятии комплектуются из исходного склада и местоположения по умолчанию за исключением номенклатуры, которая определена во втором мероприятии комплектации.</span><span class="sxs-lookup"><span data-stu-id="c99fe-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="c99fe-141">Эта номенклатура будет скомплектована из других склада и местоположения.</span><span class="sxs-lookup"><span data-stu-id="c99fe-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="c99fe-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c99fe-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c99fe-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c99fe-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c99fe-144">Установите или удалите флажок "Зарегистрировать отходы".</span><span class="sxs-lookup"><span data-stu-id="c99fe-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="c99fe-145">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="c99fe-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="c99fe-146">Определение времени мероприятия</span><span class="sxs-lookup"><span data-stu-id="c99fe-146">Define the activity times</span></span>
1. <span data-ttu-id="c99fe-147">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c99fe-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c99fe-148">Требуется определение времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c99fe-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="c99fe-149">Время выполнения используется для расчета затрат и времени пропускной способности заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="c99fe-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="c99fe-150">Времена выполнения не используются для расчета максимальной мощности и потребления, это рассчитывается временем цикла, производным от задачи версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="c99fe-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="c99fe-151">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="c99fe-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="c99fe-152">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c99fe-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="c99fe-153">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="c99fe-153">Select the Time unit.</span></span>
5. <span data-ttu-id="c99fe-154">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="c99fe-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="c99fe-155">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c99fe-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c99fe-156">Время ожидания в очереди является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c99fe-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="c99fe-157">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="c99fe-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="c99fe-158">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c99fe-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="c99fe-159">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="c99fe-159">Select the Time unit.</span></span>
10. <span data-ttu-id="c99fe-160">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="c99fe-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="c99fe-161">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="c99fe-161">Click Next.</span></span>
12. <span data-ttu-id="c99fe-162">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="c99fe-162">Click Finish.</span></span>
13. <span data-ttu-id="c99fe-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c99fe-163">Close the page.</span></span>

