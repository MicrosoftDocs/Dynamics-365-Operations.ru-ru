---
title: Жизненный цикл заказа партии от создания до запуска
description: Эта процедура включает выполнение первой части жизненного цикла заказа партии.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d9ed44c9e05ea815e78ae041234ad61f76d89d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825046"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="2886f-103">Жизненный цикл заказа партии от создания до запуска</span><span class="sxs-lookup"><span data-stu-id="2886f-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2886f-104">Эта процедура включает выполнение первой части жизненного цикла заказа партии.</span><span class="sxs-lookup"><span data-stu-id="2886f-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="2886f-105">От создания, оценки затрат и планирования производственного задания до фактического запуска заказа партии.</span><span class="sxs-lookup"><span data-stu-id="2886f-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="2886f-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="2886f-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="2886f-107">Условиями для запуска процедуры с другим набором данных является выпущенный продукт с активной формулой и версией маршрута.</span><span class="sxs-lookup"><span data-stu-id="2886f-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="2886f-108">Создание заказа партии</span><span class="sxs-lookup"><span data-stu-id="2886f-108">Create a batch order</span></span>
1. <span data-ttu-id="2886f-109">Перейдите в раздел "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="2886f-109">Go to All production orders.</span></span>
2. <span data-ttu-id="2886f-110">Щелкните "Новый заказ партии".</span><span class="sxs-lookup"><span data-stu-id="2886f-110">Click New batch order.</span></span>
3. <span data-ttu-id="2886f-111">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2886f-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="2886f-112">Щелкните Создать.</span><span class="sxs-lookup"><span data-stu-id="2886f-112">Click Create.</span></span>
5. <span data-ttu-id="2886f-113">Используйте экспресс-фильтр для фильтрации поля "Производство" со значением "b".</span><span class="sxs-lookup"><span data-stu-id="2886f-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="2886f-114">Просмотр формулы производства и предполагаемых побочные продуктов</span><span class="sxs-lookup"><span data-stu-id="2886f-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="2886f-115">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="2886f-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="2886f-116">Щелкните Формула.</span><span class="sxs-lookup"><span data-stu-id="2886f-116">Click Formula.</span></span>
3. <span data-ttu-id="2886f-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-117">Close the page.</span></span>
4. <span data-ttu-id="2886f-118">Щелкните Побочные продукты.</span><span class="sxs-lookup"><span data-stu-id="2886f-118">Click Co-products.</span></span>
5. <span data-ttu-id="2886f-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="2886f-120">Оценка заказа партии</span><span class="sxs-lookup"><span data-stu-id="2886f-120">Estimate the batch order</span></span>
1. <span data-ttu-id="2886f-121">Щелкните "Оценка".</span><span class="sxs-lookup"><span data-stu-id="2886f-121">Click Estimate.</span></span>
2. <span data-ttu-id="2886f-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2886f-122">Click OK.</span></span>
3. <span data-ttu-id="2886f-123">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="2886f-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="2886f-124">Щелкните "Просмотреть сведения расчета".</span><span class="sxs-lookup"><span data-stu-id="2886f-124">Click View calculation details.</span></span>
5. <span data-ttu-id="2886f-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="2886f-126">Выпуск заказа партии</span><span class="sxs-lookup"><span data-stu-id="2886f-126">Release the batch order</span></span>
1. <span data-ttu-id="2886f-127">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="2886f-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="2886f-128">Щелкните "Запуск в производство".</span><span class="sxs-lookup"><span data-stu-id="2886f-128">Click Release.</span></span>
3. <span data-ttu-id="2886f-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2886f-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="2886f-130">Планирование производственных заданий</span><span class="sxs-lookup"><span data-stu-id="2886f-130">Schedule production jobs</span></span>
1. <span data-ttu-id="2886f-131">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="2886f-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="2886f-132">Щелкните "Планирование заданий".</span><span class="sxs-lookup"><span data-stu-id="2886f-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="2886f-133">Выберите значение "Нет" в поле "Ограничение по мощности".</span><span class="sxs-lookup"><span data-stu-id="2886f-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="2886f-134">Выберите значение "Нет" в поле "Ограничение по материалам".</span><span class="sxs-lookup"><span data-stu-id="2886f-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="2886f-135">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="2886f-135">Click OK.</span></span>
6. <span data-ttu-id="2886f-136">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="2886f-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="2886f-137">Щелкните "Все задания".</span><span class="sxs-lookup"><span data-stu-id="2886f-137">Click All jobs.</span></span>
8. <span data-ttu-id="2886f-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="2886f-139">Запуск заказа партии</span><span class="sxs-lookup"><span data-stu-id="2886f-139">Start the batch order</span></span>
1. <span data-ttu-id="2886f-140">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="2886f-140">Click Start.</span></span>
2. <span data-ttu-id="2886f-141">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="2886f-141">Click the General tab.</span></span>
3. <span data-ttu-id="2886f-142">В поле "Разнести отборочную накладную" выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="2886f-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="2886f-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2886f-143">Click OK.</span></span>
5. <span data-ttu-id="2886f-144">В области действий щелкните "Показать".</span><span class="sxs-lookup"><span data-stu-id="2886f-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="2886f-145">Щелкните "Лист подбора".</span><span class="sxs-lookup"><span data-stu-id="2886f-145">Click Picking list.</span></span>
7. <span data-ttu-id="2886f-146">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2886f-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2886f-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-147">Close the page.</span></span>
9. <span data-ttu-id="2886f-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-148">Close the page.</span></span>
10. <span data-ttu-id="2886f-149">Щелкните "Карта маршрута".</span><span class="sxs-lookup"><span data-stu-id="2886f-149">Click Route card.</span></span>
11. <span data-ttu-id="2886f-150">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2886f-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2886f-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-151">Close the page.</span></span>
13. <span data-ttu-id="2886f-152">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2886f-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]