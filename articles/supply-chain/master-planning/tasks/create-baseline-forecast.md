---
title: 'Руководство: создание базового прогноза'
description: Планировщик производства может создать базовый прогноз либо путем использования моделей прогнозирования временных рядов, либо путем копирования исторического спроса.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223970"
---
# <a name="guide-create-a-baseline-forecast"></a><span data-ttu-id="5d06e-103">Руководство: создание базового прогноза</span><span class="sxs-lookup"><span data-stu-id="5d06e-103">Guide: Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d06e-104">Планировщик производства может создать базовый прогноз либо путем использования моделей прогнозирования временных рядов, либо путем копирования исторического спроса.</span><span class="sxs-lookup"><span data-stu-id="5d06e-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="5d06e-105">В этой процедуре показано, как скопировать исторический спрос, чтобы создать базовый прогноз для всех продуктов с использованием одного ключа распределения номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5d06e-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span>

## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="5d06e-106">Настройка ключа распределения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="5d06e-106">Set up an item allocation key</span></span>

1. <span data-ttu-id="5d06e-107">Перейдите в раздел **Сводное планирование > Настройка > Группы внутрихолдингового планирования**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-107">Go to **Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="5d06e-108">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="5d06e-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5d06e-109">Например, отфильтруйте поле *Имя* по значению *10*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-109">For example, filter on the *Name* field with a value of *10*.</span></span>
    * <span data-ttu-id="5d06e-110">Прогнозирование спроса выполняется в разных юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="5d06e-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="5d06e-111">Поэтому необходимо настроить все компании, для которых требуется сформировать прогнозы, в виде одной группы внутрихолдингового планирования.</span><span class="sxs-lookup"><span data-stu-id="5d06e-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="5d06e-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5d06e-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5d06e-113">Выберите **Ключи распределения номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-113">Select **Item allocation keys**.</span></span>
    * <span data-ttu-id="5d06e-114">Выберите все ключи распределения номенклатур, для которых требуется создать прогнозы.</span><span class="sxs-lookup"><span data-stu-id="5d06e-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="5d06e-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5d06e-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5d06e-116">Выберите ключ распределения номенклатур D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="5d06e-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="5d06e-117">Выберите **>**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-117">Select **>**.</span></span>
7. <span data-ttu-id="5d06e-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5d06e-118">Close the page.</span></span>
8. <span data-ttu-id="5d06e-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5d06e-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="5d06e-120">Настройка параметров прогнозирования спроса</span><span class="sxs-lookup"><span data-stu-id="5d06e-120">Set up the demand forecasting parameters</span></span>

1. <span data-ttu-id="5d06e-121">Перейдите в раздел **Сводное планирование > Настройка > Прогнозирование спроса > Параметры прогнозирования спроса**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-121">Go to **Master planning > Setup > Demand forecasting > Demand forecasting parameters**.</span></span>
2. <span data-ttu-id="5d06e-122">Разверните раздел **Параметры алгоритма прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-122">Expand the **Forecast algorithm parameters** section.</span></span>
3. <span data-ttu-id="5d06e-123">В поле **Стратегия создания прогноза** выберите **Копировать поверх исторического спроса**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-123">In the **Forecast generation strategy** field, select **Copy over historical demand**.</span></span>
4. <span data-ttu-id="5d06e-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-124">Select **Save**.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="5d06e-125">Создание базового прогноза</span><span class="sxs-lookup"><span data-stu-id="5d06e-125">Create a baseline forecast</span></span>

1. <span data-ttu-id="5d06e-126">Перейдите в раздел **Сводное планирование > Прогнозирование > Прогнозирование спроса > Сгенерировать статистический базовый прогноз**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-126">Go to **Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast**.</span></span>
2. <span data-ttu-id="5d06e-127">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="5d06e-127">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5d06e-128">Если заказы на продажу начинаются с 1 января 2015 г., введите эту дату.</span><span class="sxs-lookup"><span data-stu-id="5d06e-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="5d06e-129">Если в противном случае введите самую раннюю дату заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="5d06e-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="5d06e-130">В поле **Дата окончания** введите дату.</span><span class="sxs-lookup"><span data-stu-id="5d06e-130">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="5d06e-131">Введите последнюю дату заказов на продажу, например *2015-03-31*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-131">Enter the last date of your sales orders, for example *2015-03-31*.</span></span>  
4. <span data-ttu-id="5d06e-132">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="5d06e-132">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5d06e-133">Введите *2015-04-01*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-133">Enter *2015-04-01*.</span></span> <span data-ttu-id="5d06e-134">Эта дата будет автоматически вычислена как дата начала следующего периода прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="5d06e-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="5d06e-135">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-135">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="5d06e-136">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-136">Select **Filter**.</span></span>
7. <span data-ttu-id="5d06e-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5d06e-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5d06e-138">Отметьте строку, где **Поле** = *Группа внутрихолдингового планирования*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-138">Mark the row where **Field** = *Intercompany planning group*.</span></span>  
8. <span data-ttu-id="5d06e-139">В поле **Критерии** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5d06e-139">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="5d06e-140">Введите группу внутрихолдингового планирования (например, *10*), которая использовалась в первой задаче.</span><span class="sxs-lookup"><span data-stu-id="5d06e-140">Type the intercompany planning group (for example, *10*) that you used in the first task.</span></span>  
9. <span data-ttu-id="5d06e-141">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5d06e-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5d06e-142">Выберите строку, где **Поле** = *Ключ распределения номенклатур*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-142">Select the row where **Field** = *Item allocation key*.</span></span>  
10. <span data-ttu-id="5d06e-143">В поле **Критерии** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5d06e-143">In the **Criteria** field, type a value.</span></span>
11. <span data-ttu-id="5d06e-144">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-144">Select **OK**.</span></span>
12. <span data-ttu-id="5d06e-145">Разверните раздел **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-145">Expand the **Advanced parameters** section.</span></span>
13. <span data-ttu-id="5d06e-146">В поле **Период прогноза** выберите *Месяц*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-146">In the **Forecast bucket** field, select *Month*.</span></span>
14. <span data-ttu-id="5d06e-147">В поле **Горизонт прогноза** введите *3*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-147">In the **Forecast horizon** field, enter *3*.</span></span>
15. <span data-ttu-id="5d06e-148">В поле **Временная граница блокировки** введите значение *1*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-148">In the **Freeze time fence** field, enter *1*.</span></span>
16. <span data-ttu-id="5d06e-149">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-149">Select **OK**.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="5d06e-150">Визуализация прогноза спроса</span><span class="sxs-lookup"><span data-stu-id="5d06e-150">Visualize the demand forecast</span></span>

1. <span data-ttu-id="5d06e-151">Перейдите в раздел **Сводное планирование > Прогнозирование > Прогнозирование спроса > Скорректированный прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-151">Go to **Master planning > Forecasting > Demand forecasting > Adjusted demand forecast**.</span></span>
2. <span data-ttu-id="5d06e-152">В таблице агрегированного представления выберите ячейку в строке 1, столбце 2.</span><span class="sxs-lookup"><span data-stu-id="5d06e-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="5d06e-153">Это второй месяц, для которого вы создали прогноз.</span><span class="sxs-lookup"><span data-stu-id="5d06e-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="5d06e-154">Установите **QtyCell** в значение *400*.</span><span class="sxs-lookup"><span data-stu-id="5d06e-154">Set **QtyCell** to *400*.</span></span>
    * <span data-ttu-id="5d06e-155">Введите в ячейке число, отличное от спрогнозированного, — например, 400.</span><span class="sxs-lookup"><span data-stu-id="5d06e-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="5d06e-156">Вы внесли вручную корректировку в прогноз.</span><span class="sxs-lookup"><span data-stu-id="5d06e-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="5d06e-157">Обратите внимание на графическое указание на следующем шаге.</span><span class="sxs-lookup"><span data-stu-id="5d06e-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="5d06e-158">Выберите **Сведения о строке прогноза**.</span><span class="sxs-lookup"><span data-stu-id="5d06e-158">Select **Forecast line details**.</span></span>
    * <span data-ttu-id="5d06e-159">На этой странице можно просмотреть значения точности, исторический спрос и прогноз.</span><span class="sxs-lookup"><span data-stu-id="5d06e-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="5d06e-160">Также можно внести изменения в прогноз.</span><span class="sxs-lookup"><span data-stu-id="5d06e-160">You can make changes to the forecast as well.</span></span>  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]