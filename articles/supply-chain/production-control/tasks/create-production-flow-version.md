--- 
title: "Создание версии производственного потока"
description: "В этой процедуре рассматривается создание новой версии производственного потока."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8903e618a35e66742b5c2ebcb5b6f0da3853fcaf
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="1442c-103">Создание версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="1442c-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1442c-104">В этой процедуре рассматривается создание новой версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="1442c-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="1442c-105">Для этой процедуры необходимо определить параметры производства для бережливого производства и единицы измерения для времени класса.</span><span class="sxs-lookup"><span data-stu-id="1442c-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="1442c-106">Необходимо также определить поток создания ценности и производственную группу.</span><span class="sxs-lookup"><span data-stu-id="1442c-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="1442c-107">Для получения дополнительных сведений о производственных потоках и мероприятиях в бережливом производстве см. официальные документы по бережливому производству для Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="1442c-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="1442c-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="1442c-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="1442c-109">Создание производственного потока</span><span class="sxs-lookup"><span data-stu-id="1442c-109">Create a production flow</span></span>
1. <span data-ttu-id="1442c-110">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="1442c-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="1442c-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1442c-111">Click New.</span></span>
3. <span data-ttu-id="1442c-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1442c-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1442c-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1442c-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1442c-114">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="1442c-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1442c-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1442c-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1442c-116">Выберите операционную единицу потока создания ценности типа.</span><span class="sxs-lookup"><span data-stu-id="1442c-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="1442c-117">Поток создания ценности является операционной единицей, которая охватывает все мероприятия и потоки создания ценности потока.</span><span class="sxs-lookup"><span data-stu-id="1442c-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="1442c-118">На этом этапе операционные единицы ограничены юридическим лицом и не имеют других функций.</span><span class="sxs-lookup"><span data-stu-id="1442c-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="1442c-119">В поле "Производственная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="1442c-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1442c-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1442c-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1442c-121">Выберите производственную группу для производственного потока.</span><span class="sxs-lookup"><span data-stu-id="1442c-121">Select a production group for the production flow.</span></span> <span data-ttu-id="1442c-122">Производственные группы позволяют определять материал, трудозатраты и счет НЗП для процесса производства.</span><span class="sxs-lookup"><span data-stu-id="1442c-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="1442c-123">Чтобы связать контекст учета с производственным потоком, необходимо выбрать производственную группу.</span><span class="sxs-lookup"><span data-stu-id="1442c-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="1442c-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1442c-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="1442c-125">Создание версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="1442c-125">Create a production flow version</span></span>
1. <span data-ttu-id="1442c-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="1442c-126">Click Add.</span></span>
2. <span data-ttu-id="1442c-127">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="1442c-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="1442c-128">При необходимости определите дату окончания срока действия для версии.</span><span class="sxs-lookup"><span data-stu-id="1442c-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="1442c-129">Можно обновить ее в любой момент времени, даже для активных версий.</span><span class="sxs-lookup"><span data-stu-id="1442c-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="1442c-130">Ее можно использовать для планирования постепенной замены версии.</span><span class="sxs-lookup"><span data-stu-id="1442c-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="1442c-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1442c-131">Click OK.</span></span>
4. <span data-ttu-id="1442c-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1442c-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="1442c-133">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="1442c-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="1442c-134">Разрешить изменения единицы такта.</span><span class="sxs-lookup"><span data-stu-id="1442c-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="1442c-135">В поле "Среднее время такта" введите число.</span><span class="sxs-lookup"><span data-stu-id="1442c-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="1442c-136">Определите среднее время такта версии.</span><span class="sxs-lookup"><span data-stu-id="1442c-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="1442c-137">Для управления тактами версии производственного потока определите среднее время такта.</span><span class="sxs-lookup"><span data-stu-id="1442c-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="1442c-138">Такт определен как количество за период времени.</span><span class="sxs-lookup"><span data-stu-id="1442c-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="1442c-139">В примере время такта составляет 0,2 часа на 10 единиц.</span><span class="sxs-lookup"><span data-stu-id="1442c-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="1442c-140">Для рабочего времени 8 часов это соответствует ежедневной пропускной способности в 400 единиц.</span><span class="sxs-lookup"><span data-stu-id="1442c-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="1442c-141">В поле "Количество в цикле" введите число.</span><span class="sxs-lookup"><span data-stu-id="1442c-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="1442c-142">Определите количество на цикл, связанный со среднем временем такта.</span><span class="sxs-lookup"><span data-stu-id="1442c-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="1442c-143">Переключите развертывание раздела "Сведения о версии".</span><span class="sxs-lookup"><span data-stu-id="1442c-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="1442c-144">В поле "Минимальное время такта" введите число.</span><span class="sxs-lookup"><span data-stu-id="1442c-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="1442c-145">Определите минимальное время такта.</span><span class="sxs-lookup"><span data-stu-id="1442c-145">Define the minimum takt time.</span></span> <span data-ttu-id="1442c-146">Минимальное время такта должно быть меньше или равно среднему времени такта.</span><span class="sxs-lookup"><span data-stu-id="1442c-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="1442c-147">В поле "Максимальное время такта" введите число.</span><span class="sxs-lookup"><span data-stu-id="1442c-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="1442c-148">Максимальное время такта должно быть больше или равно среднему времени такта.</span><span class="sxs-lookup"><span data-stu-id="1442c-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="1442c-149">Введите число в поле "Период для фактического времени цикла (дни)".</span><span class="sxs-lookup"><span data-stu-id="1442c-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="1442c-150">Введите количество дней в период для фактического времени цикла.</span><span class="sxs-lookup"><span data-stu-id="1442c-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="1442c-151">Период для фактического времени цикла — это число дней, из которых суммируются задания по фактической минуте назад для расчета фактического времени цикла.</span><span class="sxs-lookup"><span data-stu-id="1442c-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="1442c-152">Значение можно изменить в любое время, и оно используется только для расчета фактического времени цикла.</span><span class="sxs-lookup"><span data-stu-id="1442c-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="1442c-153">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1442c-153">Click Save.</span></span>


