--- 
title: "Создание мероприятий перемещения для бережливого производства"
description: "Создайте мероприятие перемещения для бережливого производства."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e5f28b26cee2501f1294cd34a495ee925e6b1ba8
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="4f032-103">Создание мероприятий перемещения для бережливого производства</span><span class="sxs-lookup"><span data-stu-id="4f032-103">Create transfer activities for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f032-104">Создайте мероприятие перемещения для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="4f032-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="4f032-105">Обязательные компоненты:</span><span class="sxs-lookup"><span data-stu-id="4f032-105">Prerequisites:</span></span> 

1. <span data-ttu-id="4f032-106">Необходимо создать производственный поток и версию, которые будут неактивны.</span><span class="sxs-lookup"><span data-stu-id="4f032-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="4f032-107">Необходимо создать исходный и конечный склады и местоположения.</span><span class="sxs-lookup"><span data-stu-id="4f032-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="4f032-108">По желанию можно создать пополнение или пополненную производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="4f032-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="4f032-109">Поиск версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="4f032-109">Find the production flow version</span></span>
1. <span data-ttu-id="4f032-110">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="4f032-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="4f032-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4f032-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f032-112">Обратите внимание, что производственный поток должен иметь версию в статусе черновика.</span><span class="sxs-lookup"><span data-stu-id="4f032-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="4f032-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4f032-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="4f032-114">Создание нового мероприятия</span><span class="sxs-lookup"><span data-stu-id="4f032-114">Create a new activity</span></span>
1. <span data-ttu-id="4f032-115">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="4f032-115">Click Activities.</span></span>
    * <span data-ttu-id="4f032-116">Убедитесь, что выбранный производственный поток содержит версию-черновик и выберите эту версию.</span><span class="sxs-lookup"><span data-stu-id="4f032-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="4f032-117">Щелкните "Создание нового мероприятия плана".</span><span class="sxs-lookup"><span data-stu-id="4f032-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="4f032-118">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="4f032-118">Click Next.</span></span>
4. <span data-ttu-id="4f032-119">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4f032-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4f032-120">В поле "Тип мероприятия" выберите "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="4f032-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="4f032-121">В поле "Количество процесса" введите число.</span><span class="sxs-lookup"><span data-stu-id="4f032-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="4f032-122">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="4f032-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="4f032-123">Выбор производственных ячеек</span><span class="sxs-lookup"><span data-stu-id="4f032-123">Select the Work cells</span></span>
1. <span data-ttu-id="4f032-124">В поле "Пополнение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4f032-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4f032-125">Для использования выходного местоположения производственной ячейки как исходного местоположения в мероприятии перемещения выберите производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="4f032-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="4f032-126">То же самое можно сделать с пополненной производственной ячейкой, которая задает целевое местоположение для мероприятия перемещения.</span><span class="sxs-lookup"><span data-stu-id="4f032-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="4f032-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4f032-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="4f032-128">Определение обновлений запасов</span><span class="sxs-lookup"><span data-stu-id="4f032-128">Define the inventory updates</span></span>
1. <span data-ttu-id="4f032-129">В поле "Тип продукта" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="4f032-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="4f032-130">Обратите внимание, что перемещение не изменяет тип продукта.</span><span class="sxs-lookup"><span data-stu-id="4f032-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="4f032-131">Можно переместить готовые продукты или полуфабрикаты (перемещение между двумя мероприятиями производственного потока по возможности потока канбана).</span><span class="sxs-lookup"><span data-stu-id="4f032-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="4f032-132">При перемещении готовых продуктов можно выбрать, приводит ли комплектация или получение к складской проводке.</span><span class="sxs-lookup"><span data-stu-id="4f032-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="4f032-133">Определение местоположения перемещения</span><span class="sxs-lookup"><span data-stu-id="4f032-133">Define the transfer locations</span></span>
1. <span data-ttu-id="4f032-134">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="4f032-134">Click Next.</span></span>
2. <span data-ttu-id="4f032-135">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4f032-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4f032-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4f032-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="4f032-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4f032-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4f032-138">В поле "Местонахождение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4f032-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4f032-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4f032-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4f032-140">В поле "Транспортировка" выберите "Грузоотправитель".</span><span class="sxs-lookup"><span data-stu-id="4f032-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="4f032-141">Возможные варианты: грузоотправитель — организация, управляющая складом отгрузки, получатель — организация, управляющая складом получения, перевозчик — сторонний поставщик.</span><span class="sxs-lookup"><span data-stu-id="4f032-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="4f032-142">Если управляющая организация является поставщиком, для мероприятия перемещения требуется соглашение субподряда.</span><span class="sxs-lookup"><span data-stu-id="4f032-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="4f032-143">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="4f032-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="4f032-144">Определение времени мероприятия</span><span class="sxs-lookup"><span data-stu-id="4f032-144">Define the activity times</span></span>
1. <span data-ttu-id="4f032-145">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4f032-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f032-146">Требуется определение времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4f032-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="4f032-147">Время выполнения используется для расчета затрат и времени пропускной способности заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="4f032-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="4f032-148">Времена выполнения не используются для расчета максимальной мощности и потребления, это рассчитывается временем цикла, производным от задачи версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="4f032-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="4f032-149">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="4f032-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="4f032-150">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4f032-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="4f032-151">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="4f032-151">Select the Time unit.</span></span>
5. <span data-ttu-id="4f032-152">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="4f032-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="4f032-153">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4f032-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f032-154">Время ожидания в очереди является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4f032-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="4f032-155">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="4f032-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="4f032-156">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="4f032-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="4f032-157">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="4f032-157">Select the Time unit.</span></span>
10. <span data-ttu-id="4f032-158">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="4f032-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="4f032-159">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="4f032-159">Click Next.</span></span>
12. <span data-ttu-id="4f032-160">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="4f032-160">Click Finish.</span></span>
13. <span data-ttu-id="4f032-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4f032-161">Close the page.</span></span>


