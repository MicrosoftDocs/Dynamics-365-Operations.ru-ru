---
title: Проверка производственного потока и версии
description: Эта процедура показывает, как создать новый производственный поток и первую версию для бережливого производства.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae4c5f55d317a99e23ba6e76fc50ddece1e55a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571412"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="31e7c-103">Проверка производственного потока и версии</span><span class="sxs-lookup"><span data-stu-id="31e7c-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31e7c-104">Эта процедура показывает, как создать новый производственный поток и первую версию для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="31e7c-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="31e7c-105">Необходимые условия: должны быть определены производственные параметры для бережливого производства и единицы измерения для времени класса.</span><span class="sxs-lookup"><span data-stu-id="31e7c-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="31e7c-106">Необходимо определить поток создания ценности и производственную группу.</span><span class="sxs-lookup"><span data-stu-id="31e7c-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="31e7c-107">Для ознакомления с принципами производственных потоков и мероприятий см. официальные документы по бережливому производству.</span><span class="sxs-lookup"><span data-stu-id="31e7c-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="31e7c-108">К этой процедуре в демонстрационных данных относится юридическое лицо USMF.</span><span class="sxs-lookup"><span data-stu-id="31e7c-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="31e7c-109">Однако можно использовать и другие юридические лица при условии, что юридическое лицо настроено для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="31e7c-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="31e7c-110">Создание производственного потока</span><span class="sxs-lookup"><span data-stu-id="31e7c-110">Create a production flow</span></span>
1. <span data-ttu-id="31e7c-111">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="31e7c-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="31e7c-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="31e7c-112">Click New.</span></span>
3. <span data-ttu-id="31e7c-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="31e7c-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="31e7c-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="31e7c-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31e7c-115">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="31e7c-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="31e7c-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="31e7c-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="31e7c-117">Поток создания ценности является операционной единицей, которая охватывает все мероприятия и потоки создания ценности потока.</span><span class="sxs-lookup"><span data-stu-id="31e7c-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="31e7c-118">На этом этапе операционные единицы ограничены юридическим лицом и не имеют других функций.</span><span class="sxs-lookup"><span data-stu-id="31e7c-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="31e7c-119">В поле "Производственная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="31e7c-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="31e7c-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="31e7c-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="31e7c-121">Производственные группы позволяют определять материал, трудозатраты и счет НЗП для процесса производства.</span><span class="sxs-lookup"><span data-stu-id="31e7c-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="31e7c-122">Чтобы связать контекст учета с производственным потоком, необходимо выбрать производственную группу.</span><span class="sxs-lookup"><span data-stu-id="31e7c-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="31e7c-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31e7c-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="31e7c-124">Создание версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="31e7c-124">Create a production flow version</span></span>
1. <span data-ttu-id="31e7c-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="31e7c-125">Click Add.</span></span>
2. <span data-ttu-id="31e7c-126">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="31e7c-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="31e7c-127">Можно обновить дату окончания срока действия в любой момент времени, даже для активных версий.</span><span class="sxs-lookup"><span data-stu-id="31e7c-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="31e7c-128">Используйте дату окончания срока действия версии для планирования постепенной замены версии.</span><span class="sxs-lookup"><span data-stu-id="31e7c-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="31e7c-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="31e7c-129">Click OK.</span></span>
4. <span data-ttu-id="31e7c-130">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="31e7c-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="31e7c-131">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="31e7c-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="31e7c-132">Выберите единицу такта.</span><span class="sxs-lookup"><span data-stu-id="31e7c-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="31e7c-133">В поле "Среднее время такта" введите число.</span><span class="sxs-lookup"><span data-stu-id="31e7c-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="31e7c-134">Для управления тактами версии производственного потока определите среднее время такта.</span><span class="sxs-lookup"><span data-stu-id="31e7c-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="31e7c-135">Такт определен как количество за период времени.</span><span class="sxs-lookup"><span data-stu-id="31e7c-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="31e7c-136">В этом примере время такта составляет 0,2 часа на 10 единиц.</span><span class="sxs-lookup"><span data-stu-id="31e7c-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="31e7c-137">Для рабочего времени 8 часов это соответствует ежедневной пропускной способности в 400 единиц.</span><span class="sxs-lookup"><span data-stu-id="31e7c-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="31e7c-138">В поле "Количество в цикле" введите число.</span><span class="sxs-lookup"><span data-stu-id="31e7c-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="31e7c-139">Разверните или сверните раздел "Сведения о версии".</span><span class="sxs-lookup"><span data-stu-id="31e7c-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="31e7c-140">В поле "Минимальное время такта" введите число.</span><span class="sxs-lookup"><span data-stu-id="31e7c-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="31e7c-141">Минимальное время такта должно быть меньше или равно среднему времени такта.</span><span class="sxs-lookup"><span data-stu-id="31e7c-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="31e7c-142">В поле "Максимальное время такта" введите число.</span><span class="sxs-lookup"><span data-stu-id="31e7c-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="31e7c-143">Максимальное время такта должно быть больше или равно среднему времени такта.</span><span class="sxs-lookup"><span data-stu-id="31e7c-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="31e7c-144">Введите количество дней в период для фактического времени цикла</span><span class="sxs-lookup"><span data-stu-id="31e7c-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="31e7c-145">Период для фактического времени цикла — это число дней, из которых суммируются задания по фактической минуте назад для расчета фактического времени цикла.</span><span class="sxs-lookup"><span data-stu-id="31e7c-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="31e7c-146">Значение можно изменить в любое время, и оно используется только для расчета фактического времени цикла.</span><span class="sxs-lookup"><span data-stu-id="31e7c-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="31e7c-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="31e7c-147">Click Save.</span></span>

