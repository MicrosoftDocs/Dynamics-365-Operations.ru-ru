---
title: Определение последовательности производственных заданий для непрерывного производства
description: В этой процедуре используются краски в качестве примера, чтобы показать, как определить последовательность спланированных заказов в соответствии с приоритетом по цвету и размеру упаковки.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e064f55ed451d44f58e60ba0aa722166981c129
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "312263"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="16d0a-103">Определение последовательности производственных заданий для непрерывного производства</span><span class="sxs-lookup"><span data-stu-id="16d0a-103">Sequence production jobs for process manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16d0a-104">В этой процедуре используются краски в качестве примера, чтобы показать, как определить последовательность спланированных заказов в соответствии с приоритетом по цвету и размеру упаковки.</span><span class="sxs-lookup"><span data-stu-id="16d0a-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="16d0a-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USPI.</span><span class="sxs-lookup"><span data-stu-id="16d0a-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="16d0a-106">Эта процедура предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="16d0a-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="16d0a-107">Выполнение сводного планирования для USPI</span><span class="sxs-lookup"><span data-stu-id="16d0a-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="16d0a-108">Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Выполнить" > "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="16d0a-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="16d0a-109">В поле "Сводный план" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="16d0a-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="16d0a-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="16d0a-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="16d0a-111">Выберите MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="16d0a-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="16d0a-112">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="16d0a-112">Click OK.</span></span>
    * <span data-ttu-id="16d0a-113">В результате начнется сводное планирование, включая процесс последовательности.</span><span class="sxs-lookup"><span data-stu-id="16d0a-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="16d0a-114">Этот процесс может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="16d0a-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="16d0a-115">Просмотр спланированных заказов для краски</span><span class="sxs-lookup"><span data-stu-id="16d0a-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="16d0a-116">Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="16d0a-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="16d0a-117">Разверните информационное поле "Сведения о номенклатуре".</span><span class="sxs-lookup"><span data-stu-id="16d0a-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="16d0a-118">Разверните информационное поле "Сведения о плане".</span><span class="sxs-lookup"><span data-stu-id="16d0a-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="16d0a-119">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="16d0a-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="16d0a-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="16d0a-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="16d0a-121">Выберите MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="16d0a-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="16d0a-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="16d0a-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="16d0a-123">В экспресс-фильтре по полю "Код номенклатуры" выберите значение "P300".</span><span class="sxs-lookup"><span data-stu-id="16d0a-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="16d0a-124">Разблокируйте прокрутку справа, чтобы просмотреть дату заказа и дату поставки.</span><span class="sxs-lookup"><span data-stu-id="16d0a-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="16d0a-125">Обратите внимание, что дата заказа этих номенклатур имеет значение "Сегодня", а даты доставки для спланированных заказов не упорядочены по приоритету цвета и размера упаковки, как показано в наименовании продукта.</span><span class="sxs-lookup"><span data-stu-id="16d0a-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="16d0a-126">Можно навести указатель мыши на код номенклатуры, чтобы просмотреть наименование и приоритет продукта.</span><span class="sxs-lookup"><span data-stu-id="16d0a-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="16d0a-127">Упорядочение спланированных заказов для краски</span><span class="sxs-lookup"><span data-stu-id="16d0a-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="16d0a-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="16d0a-128">Close the page.</span></span>
2. <span data-ttu-id="16d0a-129">Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Упорядоченные плановые заказы".</span><span class="sxs-lookup"><span data-stu-id="16d0a-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="16d0a-130">Разверните информационное поле "Сведения о номенклатуре".</span><span class="sxs-lookup"><span data-stu-id="16d0a-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="16d0a-131">Разверните информационное поле "Сведения о плане".</span><span class="sxs-lookup"><span data-stu-id="16d0a-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="16d0a-132">Примечание. Здесь можно увидеть, что дата и время начала спланированных заказов упорядочены по цвету и размеру упаковки в пределах периода в 28 дней.</span><span class="sxs-lookup"><span data-stu-id="16d0a-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="16d0a-133">Эти периоды определяются номером в поле "Кампания".</span><span class="sxs-lookup"><span data-stu-id="16d0a-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="16d0a-134">Форма упорядоченного планового заказа действует как типовая форма спланированного заказа, и планировщик производства может утвердить спланированные заказы здесь.</span><span class="sxs-lookup"><span data-stu-id="16d0a-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="16d0a-135">Пометьте все строки.</span><span class="sxs-lookup"><span data-stu-id="16d0a-135">Mark all rows.</span></span>
6. <span data-ttu-id="16d0a-136">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="16d0a-136">Click Accept.</span></span>
    * <span data-ttu-id="16d0a-137">В результате будут обновлены спланированные заказы с выбранным действием последовательности "Отложить" или "Ускорение".</span><span class="sxs-lookup"><span data-stu-id="16d0a-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="16d0a-138">Проверка последовательности спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="16d0a-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="16d0a-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="16d0a-139">Close the page.</span></span>
2. <span data-ttu-id="16d0a-140">Перейдите в раздел "Сводное планирование" > "Сводное планирование" > "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="16d0a-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="16d0a-141">Разверните информационное поле "Сведения о номенклатуре".</span><span class="sxs-lookup"><span data-stu-id="16d0a-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="16d0a-142">Разверните информационное поле "Сведения о плане".</span><span class="sxs-lookup"><span data-stu-id="16d0a-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="16d0a-143">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="16d0a-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="16d0a-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="16d0a-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="16d0a-145">Выберите MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="16d0a-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="16d0a-146">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="16d0a-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="16d0a-147">В экспресс-фильтре по полю "Код номенклатуры" выберите значение "P300".</span><span class="sxs-lookup"><span data-stu-id="16d0a-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="16d0a-148">Обратите внимание, что заказы теперь упорядочены в соответствии с приоритетом по цвету и размеру и спланированные заказы запускаются на самую раннюю дату заказа и дату поставки.</span><span class="sxs-lookup"><span data-stu-id="16d0a-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="16d0a-149">Проверьте столбец "Дата заказа" или "Дата начала" в информационном поле "Сведения о плане".</span><span class="sxs-lookup"><span data-stu-id="16d0a-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

