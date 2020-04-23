---
title: Создание мероприятий перемещения для бережливого производства
description: Создайте мероприятие перемещения для бережливого производства.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae31cca96825665f9482b4523b66586415504b65
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210809"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="73038-103">Создание мероприятий перемещения для бережливого производства</span><span class="sxs-lookup"><span data-stu-id="73038-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73038-104">Создайте мероприятие перемещения для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="73038-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="73038-105">Обязательные компоненты:</span><span class="sxs-lookup"><span data-stu-id="73038-105">Prerequisites:</span></span> 

1. <span data-ttu-id="73038-106">Необходимо создать производственный поток и версию, которые будут неактивны.</span><span class="sxs-lookup"><span data-stu-id="73038-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="73038-107">Необходимо создать исходный и конечный склады и местоположения.</span><span class="sxs-lookup"><span data-stu-id="73038-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="73038-108">По желанию можно создать пополнение или пополненную производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="73038-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="73038-109">Поиск версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="73038-109">Find the production flow version</span></span>
1. <span data-ttu-id="73038-110">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="73038-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="73038-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="73038-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="73038-112">Обратите внимание, что производственный поток должен иметь версию в статусе черновика.</span><span class="sxs-lookup"><span data-stu-id="73038-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="73038-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="73038-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="73038-114">Создание нового мероприятия</span><span class="sxs-lookup"><span data-stu-id="73038-114">Create a new activity</span></span>
1. <span data-ttu-id="73038-115">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="73038-115">Click Activities.</span></span>
    * <span data-ttu-id="73038-116">Убедитесь, что выбранный производственный поток содержит версию-черновик и выберите эту версию.</span><span class="sxs-lookup"><span data-stu-id="73038-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="73038-117">Щелкните "Создание нового мероприятия плана".</span><span class="sxs-lookup"><span data-stu-id="73038-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="73038-118">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="73038-118">Click Next.</span></span>
4. <span data-ttu-id="73038-119">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73038-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="73038-120">В поле "Тип мероприятия" выберите "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="73038-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="73038-121">В поле "Количество процесса" введите число.</span><span class="sxs-lookup"><span data-stu-id="73038-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="73038-122">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="73038-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="73038-123">Выбор производственных ячеек</span><span class="sxs-lookup"><span data-stu-id="73038-123">Select the Work cells</span></span>
1. <span data-ttu-id="73038-124">В поле "Пополнение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="73038-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="73038-125">Для использования выходного местоположения производственной ячейки как исходного местоположения в мероприятии перемещения выберите производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="73038-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="73038-126">То же самое можно сделать с пополненной производственной ячейкой, которая задает целевое местоположение для мероприятия перемещения.</span><span class="sxs-lookup"><span data-stu-id="73038-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="73038-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="73038-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="73038-128">Определение обновлений запасов</span><span class="sxs-lookup"><span data-stu-id="73038-128">Define the inventory updates</span></span>
1. <span data-ttu-id="73038-129">В поле "Тип продукта" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="73038-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="73038-130">Обратите внимание, что перемещение не изменяет тип продукта.</span><span class="sxs-lookup"><span data-stu-id="73038-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="73038-131">Можно переместить готовые продукты или полуфабрикаты (перемещение между двумя мероприятиями производственного потока по возможности потока канбана).</span><span class="sxs-lookup"><span data-stu-id="73038-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="73038-132">При перемещении готовых продуктов можно выбрать, приводит ли комплектация или получение к складской проводке.</span><span class="sxs-lookup"><span data-stu-id="73038-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="73038-133">Определение местоположения перемещения</span><span class="sxs-lookup"><span data-stu-id="73038-133">Define the transfer locations</span></span>
1. <span data-ttu-id="73038-134">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="73038-134">Click Next.</span></span>
2. <span data-ttu-id="73038-135">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="73038-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="73038-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="73038-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="73038-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="73038-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="73038-138">В поле "Местонахождение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="73038-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="73038-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="73038-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="73038-140">В поле "Транспортировка" выберите "Грузоотправитель".</span><span class="sxs-lookup"><span data-stu-id="73038-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="73038-141">Возможные варианты: грузоотправитель — организация, управляющая складом отгрузки, получатель — организация, управляющая складом получения, перевозчик — сторонний поставщик.</span><span class="sxs-lookup"><span data-stu-id="73038-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="73038-142">Если управляющая организация является поставщиком, для мероприятия перемещения требуется соглашение субподряда.</span><span class="sxs-lookup"><span data-stu-id="73038-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="73038-143">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="73038-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="73038-144">Определение времени мероприятия</span><span class="sxs-lookup"><span data-stu-id="73038-144">Define the activity times</span></span>
1. <span data-ttu-id="73038-145">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="73038-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="73038-146">Требуется определение времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="73038-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="73038-147">Время выполнения используется для расчета затрат и времени пропускной способности заданий канбана.</span><span class="sxs-lookup"><span data-stu-id="73038-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="73038-148">Времена выполнения не используются для расчета максимальной мощности и потребления, это рассчитывается временем цикла, производным от задачи версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="73038-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="73038-149">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="73038-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="73038-150">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73038-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="73038-151">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="73038-151">Select the Time unit.</span></span>
5. <span data-ttu-id="73038-152">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="73038-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="73038-153">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="73038-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="73038-154">Время ожидания в очереди является необязательным.</span><span class="sxs-lookup"><span data-stu-id="73038-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="73038-155">В поле "Время" введите число.</span><span class="sxs-lookup"><span data-stu-id="73038-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="73038-156">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="73038-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="73038-157">Выберите единицу времени.</span><span class="sxs-lookup"><span data-stu-id="73038-157">Select the Time unit.</span></span>
10. <span data-ttu-id="73038-158">В поле "На количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="73038-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="73038-159">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="73038-159">Click Next.</span></span>
12. <span data-ttu-id="73038-160">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="73038-160">Click Finish.</span></span>
13. <span data-ttu-id="73038-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="73038-161">Close the page.</span></span>

