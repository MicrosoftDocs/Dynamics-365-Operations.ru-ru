---
title: Внесение ручных корректировок в базовый прогноз
description: В этом разделе поясняется, как внести корректировки в базовый прогноз вручную и просмотреть подробные сведения о прогнозе.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dc5d1812fa926216a75b6fc4e3cf820ccc3ef6d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978159"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="4e659-103">Внесение ручных корректировок в базовый прогноз</span><span class="sxs-lookup"><span data-stu-id="4e659-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e659-104">В этом разделе поясняется, как внести корректировки в базовый прогноз вручную и просмотреть подробные сведения о прогнозе.</span><span class="sxs-lookup"><span data-stu-id="4e659-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="4e659-105">Прежде чем внести ручные корректировки, важно понять несколько моментов о разных страницах.</span><span class="sxs-lookup"><span data-stu-id="4e659-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="4e659-106">Сетка на странице "Скорректированный прогноз спроса"</span><span class="sxs-lookup"><span data-stu-id="4e659-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="4e659-107">Страница **Скорректированный прогноз спроса** включает сетку следующей структуры.</span><span class="sxs-lookup"><span data-stu-id="4e659-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="4e659-108">В первом столбце показаны номенклатуры, ключи распределения номенклатуры, компании и так далее, для которых был создан прогноз.</span><span class="sxs-lookup"><span data-stu-id="4e659-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="4e659-109">Подзаголовок страницы содержит описание текущих аналитик прогноза, которые отображаются в сетке.</span><span class="sxs-lookup"><span data-stu-id="4e659-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="4e659-110">Например, если подзаголовок страницы — **Компания / Объект / Ключ распределения номенклатуры** и один из заголовков строки в сетке — **USMF / 1 / D\_Alloc**, в этой строке показан прогноз для компании USMF, объект 1, и ключ распределения номенклатур **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="4e659-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="4e659-111">Последующие столбцы представляют периоды прогноза, для которых был создан прогноз.</span><span class="sxs-lookup"><span data-stu-id="4e659-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="4e659-112">Каждый заголовок столбца — первая дата периода прогноза, отображаемого в соответствующем столбце.</span><span class="sxs-lookup"><span data-stu-id="4e659-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="4e659-113">Значения в ячейках представляют прогноз для одной номенклатуры, ключа распределения номенклатур и так далее, для конкретного периода прогноза.</span><span class="sxs-lookup"><span data-stu-id="4e659-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="4e659-114">Суммирование и отмена суммирования прогноза</span><span class="sxs-lookup"><span data-stu-id="4e659-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="4e659-115">Подзаголовок страницы показывает уровень суммирования прогноза.</span><span class="sxs-lookup"><span data-stu-id="4e659-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="4e659-116">Например, если подзаголовок страницы **Компания / Объект / Ключ распределения / Код номенклатуры / Цвет / Размер / Конфигурация / Стиль**, суммирование прогноза отсутствует, и прогноз показан на уровне номенклатуры и ее аналитик.</span><span class="sxs-lookup"><span data-stu-id="4e659-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="4e659-117">Чтобы изменить суммирование, воспользуйтесь страницей **Изменить аналитики прогноза**, которую можно открыть из меню приложения.</span><span class="sxs-lookup"><span data-stu-id="4e659-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="4e659-118">Чтобы изменить прогноз, щелкните любую доступную ячейку и введите скорректированное значение прогноза.</span><span class="sxs-lookup"><span data-stu-id="4e659-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="4e659-119">Отредактированная ячейка сразу выделяется жирным шрифтом, чтобы показать, что отображаемый прогноз — это не прогноз, созданный сервисом прогнозирования спроса, а прогноз, скорректированный вручную.</span><span class="sxs-lookup"><span data-stu-id="4e659-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="4e659-120">Если изменить суммирование, чтобы на странице отображалось больше суммированных данных, можно воспользоваться страницей **Строки прогноза спроса** и посмотреть отдельные строки прогноза, составляющие суммированный прогноз.</span><span class="sxs-lookup"><span data-stu-id="4e659-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="4e659-121">Например, вы создали прогноз на уровне номенклатуры, но вы знаете, что спрос на эту номенклатуру будет расти по всем объектам из-за рекламной акции или другого похожего мероприятия.</span><span class="sxs-lookup"><span data-stu-id="4e659-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="4e659-122">В этом случае можно задать суммирование **Компания / Ключ распределения номенклатуры / Номенклатура** на странице **Изменение аналитик прогноза**.</span><span class="sxs-lookup"><span data-stu-id="4e659-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="4e659-123">Можно скорректировать глобальный прогноз для номенклатуры по всем объектам в сетке **Скорректированный прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="4e659-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="4e659-124">Чтобы увидеть результат изменений на всех объектах, откройте страницу **Строки прогноза спроса**.</span><span class="sxs-lookup"><span data-stu-id="4e659-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="4e659-125">На этой странице вы увидите одну строку для номенклатуры по каждому объекту, скорректированное количество прогноза и исходное количество прогноза.</span><span class="sxs-lookup"><span data-stu-id="4e659-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="4e659-126">Если регулировка прогнозируемого количества выполняется на сводном уровне, система использует взвешенное распределение для распространения изменения между строками, которые формируют суммирование.</span><span class="sxs-lookup"><span data-stu-id="4e659-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="4e659-127">Можно также внести корректировки вручную на странице **Строки прогноза спроса**, изменив значение **Общее количество** или ячейки **Количество** в сетке отмены суммирования.</span><span class="sxs-lookup"><span data-stu-id="4e659-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="4e659-128">Просмотр подробных сведений о прогнозе</span><span class="sxs-lookup"><span data-stu-id="4e659-128">Viewing details of the forecast</span></span>
<span data-ttu-id="4e659-129">Можно открыть страницу **Сведения о прогнозе спроса**, чтобы просмотреть дополнительную информацию о прогнозе.</span><span class="sxs-lookup"><span data-stu-id="4e659-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="4e659-130">На странице **Сведения о прогнозе спроса** показаны следующие сведения в графическом и табличном форматах.</span><span class="sxs-lookup"><span data-stu-id="4e659-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="4e659-131">Спрос за прошлые периоды, на котором основываются текущие прогнозные предположения.</span><span class="sxs-lookup"><span data-stu-id="4e659-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="4e659-132">Текущий прогноз, используемый в сводном планировании.</span><span class="sxs-lookup"><span data-stu-id="4e659-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="4e659-133">Новые значения прогноза спроса и суммы, на которые они были скорректированы вручную.</span><span class="sxs-lookup"><span data-stu-id="4e659-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="4e659-134">Интервал доверия для прогнозируемых значений.</span><span class="sxs-lookup"><span data-stu-id="4e659-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="4e659-135">Модель прогноза, которая использовалась для создания прогноза.</span><span class="sxs-lookup"><span data-stu-id="4e659-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="4e659-136">При просмотре суммированных данных вы увидите список всех методов, использованных для всех суммированных временных серий.</span><span class="sxs-lookup"><span data-stu-id="4e659-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="4e659-137">Внутренняя модельная точность (MAPE).</span><span class="sxs-lookup"><span data-stu-id="4e659-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="4e659-138">Дополнительные сведения о точности прогноза см. в разделе [Мониторинг точности прогноза](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="4e659-138">For more information about forecast accuracy, see [Monitor forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="4e659-139">**Примечания.**</span><span class="sxs-lookup"><span data-stu-id="4e659-139">**Notes:**</span></span>

-   <span data-ttu-id="4e659-140">Если вы включите **Выбор модели прогноза в сведениях прогноза спроса** в управлении функциями, вы сможете выбрать модели прогноза, которые будут включены, для исторического прогноза, на странице **сведений о прогнозе спроса**.</span><span class="sxs-lookup"><span data-stu-id="4e659-140">If you enable **Forecast model selection on Demand forecast details** from Feature management, you will be able to select the forecast models to be include, for the historical forecast, on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="4e659-141">Интервал доверия, который появляется в разделе **Прогноз** страницы, представляет разницу между верхним лимитом интервала доверия и нижним лимитом интервала доверия.</span><span class="sxs-lookup"><span data-stu-id="4e659-141">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="4e659-142">Для просмотра значений верхнего и нижнего лимитов наведите указатель на таблицу в разделе **Графическое представление спроса за прошлые периоды и прогноза**.</span><span class="sxs-lookup"><span data-stu-id="4e659-142">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="4e659-143">Если используется Microsoft Azure Machine Learning для прогнозирования спроса, можно задать процент уровня доверия, который должен иметь созданный прогноз.</span><span class="sxs-lookup"><span data-stu-id="4e659-143">If you use the Demand forecasting Microsoft Azure Machine Learning, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="4e659-144">Интервал доверия состоит из диапазона значений, которые функционируют в качестве достоверных оценок прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="4e659-144">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="4e659-145">Уровень доверия 95 процентов показывает, что имеется 5-процентный риск того, что прогноз спроса окажется за пределами диапазона интервала доверия.</span><span class="sxs-lookup"><span data-stu-id="4e659-145">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="4e659-146">Можно также вносить корректировки в прогноз вручную на странице **Сведения о прогнозе спроса**, изменяя значения в строке **Прогноз** в разделе **Прогноз**.</span><span class="sxs-lookup"><span data-stu-id="4e659-146">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4e659-147">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e659-147">Additional resources</span></span>
--------

[<span data-ttu-id="4e659-148">Отслеживание точности прогноза</span><span class="sxs-lookup"><span data-stu-id="4e659-148">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="4e659-149">Создание статистического базового прогноза</span><span class="sxs-lookup"><span data-stu-id="4e659-149">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



