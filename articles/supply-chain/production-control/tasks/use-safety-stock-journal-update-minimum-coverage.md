--- 
title: "Использование журнала резервного запаса для обновления минимального покрытия"
description: "В этой процедуре показано, как рассчитать предложения минимального покрытия на основе статистических проводок, а затем обновить покрытие номенклатуры с учетом предложений."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ad194efd151dab8c8fe5542cb40de2d811fb4b3d
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="1f742-103">Использование журнала резервного запаса для обновления минимального покрытия</span><span class="sxs-lookup"><span data-stu-id="1f742-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f742-104">В этой процедуре показано, как рассчитать предложения минимального покрытия на основе статистических проводок, а затем обновить покрытие номенклатуры с учетом предложений.</span><span class="sxs-lookup"><span data-stu-id="1f742-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="1f742-105">Она выполняется с использованием журнала резервного запаса.</span><span class="sxs-lookup"><span data-stu-id="1f742-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="1f742-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="1f742-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="1f742-107">Эта задача назначена для планировщика производства для поддержки минимального покрытия.</span><span class="sxs-lookup"><span data-stu-id="1f742-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="1f742-108">Создание нового имени журнала резервного запаса</span><span class="sxs-lookup"><span data-stu-id="1f742-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="1f742-109">Перейдите в раздел "Имена журналов резервного запаса".</span><span class="sxs-lookup"><span data-stu-id="1f742-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="1f742-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1f742-110">Click New.</span></span>
3. <span data-ttu-id="1f742-111">В поле "Имя" введите "Материал".</span><span class="sxs-lookup"><span data-stu-id="1f742-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="1f742-112">В поле "Описание" введите "Материал".</span><span class="sxs-lookup"><span data-stu-id="1f742-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="1f742-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1f742-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="1f742-114">Создание журнала резервного запаса</span><span class="sxs-lookup"><span data-stu-id="1f742-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="1f742-115">Перейдите в раздел "Расчет резервного запаса".</span><span class="sxs-lookup"><span data-stu-id="1f742-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="1f742-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1f742-116">Click New.</span></span>
3. <span data-ttu-id="1f742-117">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1f742-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="1f742-118">Выберите наименование созданного журнала резервного запаса, например "Материал".</span><span class="sxs-lookup"><span data-stu-id="1f742-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="1f742-119">Щелкните "Создать строки".</span><span class="sxs-lookup"><span data-stu-id="1f742-119">Click Create lines.</span></span>
5. <span data-ttu-id="1f742-120">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1f742-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="1f742-121">Установите дату "2015-01-02".</span><span class="sxs-lookup"><span data-stu-id="1f742-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="1f742-122">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="1f742-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="1f742-123">Установите дату "2015-12-30".</span><span class="sxs-lookup"><span data-stu-id="1f742-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="1f742-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1f742-124">Click OK.</span></span>
    * <span data-ttu-id="1f742-125">В результате будут созданы строки для аналитик, которые имеют проводки по запасам.</span><span class="sxs-lookup"><span data-stu-id="1f742-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="1f742-126">Подсчет предложений</span><span class="sxs-lookup"><span data-stu-id="1f742-126">Calculate proposal</span></span>
1. <span data-ttu-id="1f742-127">Щелкните "Подсчет предложений".</span><span class="sxs-lookup"><span data-stu-id="1f742-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="1f742-128">Выберите параметр "Использовать средний расход за время упреждения"</span><span class="sxs-lookup"><span data-stu-id="1f742-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="1f742-129">Задайте для множителя значение "10".</span><span class="sxs-lookup"><span data-stu-id="1f742-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="1f742-130">Коэффициент умножения используется для корректировки предложения.</span><span class="sxs-lookup"><span data-stu-id="1f742-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="1f742-131">Поскольку демонстрационные данные имеют только несколько проводок, потребуется задать коэффициент для получения реалистического предложения.</span><span class="sxs-lookup"><span data-stu-id="1f742-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="1f742-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1f742-132">Click OK.</span></span>
    * <span data-ttu-id="1f742-133">Прокрутите вниз, чтобы найти M0002 и M0003.</span><span class="sxs-lookup"><span data-stu-id="1f742-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="1f742-134">Просмотрите столбец "Рассчитанное минимальное количество".</span><span class="sxs-lookup"><span data-stu-id="1f742-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="1f742-135">Обновление минимального количества</span><span class="sxs-lookup"><span data-stu-id="1f742-135">Update minimum quantity</span></span>
1. <span data-ttu-id="1f742-136">В поле "Новое минимальное количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="1f742-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="1f742-137">Обновите новое минимальное количество для соответствия значению в поле "Рассчитанное минимальное количество".</span><span class="sxs-lookup"><span data-stu-id="1f742-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="1f742-138">Если значение "Рассчитанное минимальное количество" равно нулю, можно ввести требуемое будущее значение.</span><span class="sxs-lookup"><span data-stu-id="1f742-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="1f742-139">Например, можно ввести рассчитанное минимальное количество в это поле для M0002 со складом 12.</span><span class="sxs-lookup"><span data-stu-id="1f742-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="1f742-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1f742-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1f742-141">Например, можно выбрать M0002 со складом 12.</span><span class="sxs-lookup"><span data-stu-id="1f742-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="1f742-142">В поле "Новое минимальное количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="1f742-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="1f742-143">Обновите новое минимальное количество для соответствия значению в поле "Рассчитанное минимальное количество".</span><span class="sxs-lookup"><span data-stu-id="1f742-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="1f742-144">Если значение "Рассчитанное минимальное количество" равно нулю, можно ввести требуемое будущее значение.</span><span class="sxs-lookup"><span data-stu-id="1f742-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="1f742-145">Разноска нового минимального количества и проверка результата</span><span class="sxs-lookup"><span data-stu-id="1f742-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="1f742-146">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="1f742-146">Click Post.</span></span>
2. <span data-ttu-id="1f742-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1f742-147">Click OK.</span></span>
3. <span data-ttu-id="1f742-148">Щелкните для перехода по ссылке в поле "Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="1f742-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="1f742-149">Щелкните для перехода по ссылке в поле "Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="1f742-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="1f742-150">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="1f742-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="1f742-151">Щелкните "Покрытие номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="1f742-151">Click Item coverage.</span></span>
    * <span data-ttu-id="1f742-152">Обратите внимание, что минимальное количество было обновлено для отображения нового минимального количества из журнала резервного запаса.</span><span class="sxs-lookup"><span data-stu-id="1f742-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  


