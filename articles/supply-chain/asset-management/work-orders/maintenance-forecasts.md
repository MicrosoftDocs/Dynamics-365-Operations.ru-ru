---
title: Прогнозы обслуживания
description: В этом разделе описываются прогнозы обслуживания в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875864"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="106d3-103">Прогнозы обслуживания</span><span class="sxs-lookup"><span data-stu-id="106d3-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="106d3-104">При создании заказа на работу создаются задания заказа на работу с соответствующими активами и типами заданий обслуживания.</span><span class="sxs-lookup"><span data-stu-id="106d3-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="106d3-105">При выборе типа задания обслуживания, содержащего прогнозы обслуживания, прогнозы автоматически копируются в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="106d3-106">Можно добавить или удалить строки прогноза в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="106d3-107">Настройка состояния жизненного цикла заказа на работу, соответствующего типа проекта, и правила этапа, связанные с типом проекта, определяют, можно ли добавлять или редактировать строки прогнозов.</span><span class="sxs-lookup"><span data-stu-id="106d3-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="106d3-108">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="106d3-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="106d3-109">Выберите заказ на работу в списке и щелкните **Прогноз**.</span><span class="sxs-lookup"><span data-stu-id="106d3-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="106d3-110">В разделе **Прогноз обслуживания по заказу на работу** отображаются строки прогноза из типа задания обслуживания, выбранного в задании по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="106d3-111">Добавление прогноза времени в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="106d3-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="106d3-112">Выберите задание заказа на работу, в которое необходимо добавить прогноз.</span><span class="sxs-lookup"><span data-stu-id="106d3-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="106d3-113">На экспресс-вкладке **Часы** щелкните **Добавить**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="106d3-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="106d3-114">Выберите категорию в поле **Категория**.</span><span class="sxs-lookup"><span data-stu-id="106d3-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="106d3-115">Вставьте количество прогнозных часов в поле **Часы**.</span><span class="sxs-lookup"><span data-stu-id="106d3-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="106d3-116">В поле **Свойство строки** выберите тип накладных расходов, который будет использоваться в строке.</span><span class="sxs-lookup"><span data-stu-id="106d3-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="106d3-117">Добавление прогноза по номенклатурам в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="106d3-117">Add items forecast to a work order</span></span>

<span data-ttu-id="106d3-118">Существует три способа добавить номенклатуры в прогноз обслуживания по заказу на работу: можно создать строки для номенклатур (запасных частей), не включенных в список запчастей или спецификацию активов, можно выбрать запасные части из списка утвержденных запчастей, а также можно выбрать номенклатуры из спецификации актива.</span><span class="sxs-lookup"><span data-stu-id="106d3-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="106d3-119">Выберите задание заказа на работу, в которое необходимо добавить прогноз.</span><span class="sxs-lookup"><span data-stu-id="106d3-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="106d3-120">Выберите экспресс-вкладку **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="106d3-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="106d3-121">Щелкните **Добавить**, чтобы создать новую строку для запасной части, которая отсутствует в списке запасных частей или в списке спецификации актива.</span><span class="sxs-lookup"><span data-stu-id="106d3-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="106d3-122">Выберите номенклатуру в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="106d3-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="106d3-123">Введите количество в поле **Продаваемое количество** и выберите единицу измерения количества в поле **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="106d3-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="106d3-124">Введите себестоимость и валюту в соответствующие поля и выберите **Свойство строки**.</span><span class="sxs-lookup"><span data-stu-id="106d3-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="106d3-125">Если необходимо изменить список аналитик, отображаемых в строках номенклатуры, щелкните **Запасы** > **Отобразить аналитики**, выберите аналитики и выберите "Да" на переключателе **Сохранить настройку**.</span><span class="sxs-lookup"><span data-stu-id="106d3-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="106d3-126">Если требуется добавить утвержденную запасную часть к прогнозу обслуживания, щелкните **Добавить запасные части**, выберите запчасти, измените связанные сведения, если это необходимо, затем щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="106d3-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="106d3-127">Если необходимо добавить номенклатуры спецификации актива в прогноз, щелкните **Добавить номенклатуры из спецификации**, выберите номенклатуру, измените соответствующие сведения, если требуется, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="106d3-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="106d3-128">Щелкните **Применимость номенклатуры**, если требуется получить обзор того, где в модуле "Управлении активами" используется номенклатура в выбранной строке по отношению к активам, настройкам по умолчанию типа задания обслуживания, запасным частям и заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="106d3-129">Добавление прогноза расходов в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="106d3-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="106d3-130">В этой теме объясняется, как добавить прогноз расходов в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="106d3-131">В левой части формы выберите задание заказа на работу, для которого необходимо добавить прогноз.</span><span class="sxs-lookup"><span data-stu-id="106d3-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="106d3-132">Выберите экспресс-вкладку **Расход**.</span><span class="sxs-lookup"><span data-stu-id="106d3-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="106d3-133">Чтобы создать новую строку, щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="106d3-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="106d3-134">Выберите категорию в поле **Категория**.</span><span class="sxs-lookup"><span data-stu-id="106d3-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="106d3-135">Введите количество в поле **Количество**.</span><span class="sxs-lookup"><span data-stu-id="106d3-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="106d3-136">Вставьте себестоимость, валюты продажи и цены продажи в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="106d3-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="106d3-137">В поле **Свойство строки** выберите тип накладных расходов, который будет использоваться в строке.</span><span class="sxs-lookup"><span data-stu-id="106d3-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="106d3-138">На экспресс-вкладке **Итоговые суммы прогноза по обслуживанию** можно просмотреть обзор количества строк, созданных на каждой вкладке, для выбранного задания заказа на работу и для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="106d3-139">Кроме того, можно просмотреть сумму прогнозируемых рабочих часов для задания заказа на работу и для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="106d3-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Рисунок 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="106d3-141">Автоматическое обновление прогнозов по заказу на работу</span><span class="sxs-lookup"><span data-stu-id="106d3-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="106d3-142">В управлении активами можно автоматически обновлять любые изменения прогнозов по заказам на работу в отношении почасовых затрат, затрат на номенклатуру и расходов, которые были обновлены в других модулях в Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="106d3-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="106d3-143">Это делается для того, чтобы гарантировать, что в прогнозах по заказам на работу всегда используются последние значения себестоимости.</span><span class="sxs-lookup"><span data-stu-id="106d3-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="106d3-144">Также можно выполнить аналогичные обновления для [прогнозов типов заданий обслуживания](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="106d3-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="106d3-145">Щелкните **Управление активами** > **Периодические операции** > **Прогноз** > **Обновить прогноз по заказу на работу**.</span><span class="sxs-lookup"><span data-stu-id="106d3-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="106d3-146">В раскрывающемся диалоговом окне **Обновить прогноз по заказу на работу** можно добавлять выборки по отдельным заказам на работу или заданиям заказов на работу, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="106d3-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="106d3-147">Щелкните **Фильтр**, чтобы выбрать нужные значения.</span><span class="sxs-lookup"><span data-stu-id="106d3-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="106d3-148">Если требуется, можно настроить автоматическое обновление в виде пакетного задания на экспресс-вкладке **Выполнять в фоновом режиме**.</span><span class="sxs-lookup"><span data-stu-id="106d3-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="106d3-149">Щелкните **ОК**, чтобы начать обновление прогноза.</span><span class="sxs-lookup"><span data-stu-id="106d3-149">Click **OK** to start the forecast update.</span></span>


![Рисунок 2](media/07-work-orders.png)

