---
title: Прогнозы обслуживания
description: В этом разделе описываются прогнозы обслуживания в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6428981fcf560c541634d9466695be7bce4cb453
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888961"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="921ae-103">Прогнозы обслуживания</span><span class="sxs-lookup"><span data-stu-id="921ae-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="921ae-104">При создании заказа на работу создаются задания заказа на работу с соответствующими активами и типами заданий обслуживания.</span><span class="sxs-lookup"><span data-stu-id="921ae-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="921ae-105">При выборе типа задания обслуживания, содержащего прогнозы обслуживания, прогнозы автоматически копируются в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="921ae-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="921ae-106">Вы можете добавить строки прогноза в заказ на работу или удалить их из заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="921ae-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="921ae-107">Настройка состояния жизненного цикла заказа на работу, соответствующего типа проекта и правила этапа, связанные с типом проекта, определяют, можно ли добавлять или редактировать строки прогноза.</span><span class="sxs-lookup"><span data-stu-id="921ae-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="921ae-108">Дополнительные сведения о состояниях жизненного цикла заказов на работу и связанных этапах проекта см. в разделе [Прогнозы, заказы на работу и проекты](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="921ae-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="921ae-109">Выберите **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="921ae-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="921ae-110">Выберите заказ на работу в списке, а затем в области действий > вкладка **Заказ на работу** > группа **Проект** выберите **Прогноз**.</span><span class="sxs-lookup"><span data-stu-id="921ae-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="921ae-111">На странице **Прогноз обслуживания по заказу на работу** отображаются строки прогноза из типа задания обслуживания, выбранного в задании по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="921ae-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="921ae-112">Добавление прогноза времени в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="921ae-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="921ae-113">На странице **Прогноз обслуживания заказа на работу** выберите задание заказа на работу, в которое необходимо добавить прогноз.</span><span class="sxs-lookup"><span data-stu-id="921ae-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="921ae-114">На экспресс-вкладке **Часы** выберите **Добавить**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="921ae-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="921ae-115">Выберите категорию в поле **Категория**.</span><span class="sxs-lookup"><span data-stu-id="921ae-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="921ae-116">Введите количество прогнозных часов в поле **Часы**.</span><span class="sxs-lookup"><span data-stu-id="921ae-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="921ae-117">В поле **Свойство строки** выберите тип накладных расходов, который должен использоваться в строке.</span><span class="sxs-lookup"><span data-stu-id="921ae-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="921ae-118">Добавление прогноза по номенклатурам в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="921ae-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="921ae-119">Существует три способа добавления номенклатур в прогноз обслуживания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="921ae-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="921ae-120">Можно создать строки для номенклатур (запасных частей), не включенных в список запасных частей или спецификацию активов (BOM), можно выбрать запасные части из списка утвержденных запчастей или можно выбрать номенклатуры из спецификации актива.</span><span class="sxs-lookup"><span data-stu-id="921ae-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="921ae-121">На странице **Прогноз обслуживания заказа на работу** выберите задание заказа на работу, в которое необходимо добавить прогноз.</span><span class="sxs-lookup"><span data-stu-id="921ae-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="921ae-122">На экспресс-вкладке **Номенклатуры** добавьте номенклатуры к прогнозу обслуживания, используя соответствующий метод.</span><span class="sxs-lookup"><span data-stu-id="921ae-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="921ae-123">Чтобы создать новую строку для запасной части, которая отсутствует в списке запасных частей или в спецификации актива, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="921ae-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="921ae-124">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="921ae-124">Select **Add**.</span></span>
2. <span data-ttu-id="921ae-125">В поле **Код номенклатуры** выберите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="921ae-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="921ae-126">В поле **Количество для продажи** введите количество.</span><span class="sxs-lookup"><span data-stu-id="921ae-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="921ae-127">В поле **Единица** выберите единицу измерения количества.</span><span class="sxs-lookup"><span data-stu-id="921ae-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="921ae-128">В полях **Себестоимость** и **Валюта** введите соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="921ae-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="921ae-129">В поле **свойство строки** выберите свойство строки.</span><span class="sxs-lookup"><span data-stu-id="921ae-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="921ae-130">Чтобы изменить список аналитик, отображаемых в строках номенклатуры, выберите **Запасы** > **Отобразить аналитики**, выберите аналитики и затем установите параметр **Сохранить настройку** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="921ae-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="921ae-131">Чтобы добавить запасную часть из списка утвержденных запасных запчастей, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="921ae-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="921ae-132">Выберите **добавить запасные части**.</span><span class="sxs-lookup"><span data-stu-id="921ae-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="921ae-133">Выберите запасную часть и измените соответствующие сведения, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="921ae-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="921ae-134">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="921ae-134">Select **OK**.</span></span>

<span data-ttu-id="921ae-135">Чтобы добавить номенклатуру из спецификации актива, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="921ae-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="921ae-136">Выберите **Добавить номенклатуры спецификации**.</span><span class="sxs-lookup"><span data-stu-id="921ae-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="921ae-137">Выберите номенклатуру и измените соответствующие сведения, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="921ae-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="921ae-138">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="921ae-138">Select **OK**.</span></span>

<span data-ttu-id="921ae-139">Чтобы получить обзор, показывающий, где используется номенклатура в выбранной строке по отношению к активам, типу задания обслуживания по умолчанию, запасным частям и заказам на работу в "Управлении активами", выберите **Используемая номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="921ae-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="921ae-140">Дополнительные сведения об этом обзоре см. в разделе [Используемая номенклатура](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="921ae-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="921ae-141">Добавление прогноза расходов в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="921ae-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="921ae-142">На странице **Прогноз обслуживания заказа на работу** выберите задание заказа на работу, в которое необходимо добавить прогноз.</span><span class="sxs-lookup"><span data-stu-id="921ae-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="921ae-143">На экспресс-вкладке **Расход** выберите **Добавить**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="921ae-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="921ae-144">Выберите категорию в поле **Категория**.</span><span class="sxs-lookup"><span data-stu-id="921ae-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="921ae-145">В поле **Количество** введите количество.</span><span class="sxs-lookup"><span data-stu-id="921ae-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="921ae-146">Введите соответствующие значения в поля **себестоимость**, **валюты продажи** и **цены продажи**.</span><span class="sxs-lookup"><span data-stu-id="921ae-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="921ae-147">В поле **Свойство строки** выберите тип накладных расходов, который должен использоваться в строке.</span><span class="sxs-lookup"><span data-stu-id="921ae-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="921ae-148">На экспресс-вкладке **Итоговые суммы прогноза по обслуживанию** отображается обзор количества созданных строк, для выбранного задания заказа на работу и для заказа на работу, на каждой экспресс-вкладке.</span><span class="sxs-lookup"><span data-stu-id="921ae-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="921ae-149">Кроме того, можно просмотреть итоговую сумму прогнозируемых рабочих часов для задания заказа на работу и для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="921ae-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="921ae-150">На приведенном ниже рисунке показан пример страницы **Прогноз обслуживания заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="921ae-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Рисунок 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="921ae-152">Автоматическое обновление прогнозов по заказу на работу</span><span class="sxs-lookup"><span data-stu-id="921ae-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="921ae-153">Если почасовые затраты, затраты на номенклатуру и расходы были обновлены в других модулях в Microsoft Dynamics 365 for Finance and Operations, прогнозы по заказам на работу в управлении активами можно автоматически обновлять , чтобы отражать эти изменения.</span><span class="sxs-lookup"><span data-stu-id="921ae-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="921ae-154">Эта возможность помогает гарантировать, что в прогнозах по заказам на работу всегда используются последние значения себестоимости.</span><span class="sxs-lookup"><span data-stu-id="921ae-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="921ae-155">Также можно выполнить аналогичные обновления для [прогнозов типов заданий обслуживания](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="921ae-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="921ae-156">Выберите **Управление активами** > **Периодические операции** > **Прогноз** > **Обновить прогноз по заказу на работу**.</span><span class="sxs-lookup"><span data-stu-id="921ae-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="921ae-157">В диалоговом окне **Обновить прогноз по заказу на работу**, на экспресс-вкладке **Записи для добавления** можно добавлять выборки по отдельным заказам на работу или заданиям заказов на работу, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="921ae-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="921ae-158">Щелкните **Фильтр**, чтобы выбрать соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="921ae-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="921ae-159">На экспресс-вкладке **Выполнять в фоновом режиме** можно настроить автоматическое обновление в виде пакетного задания, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="921ae-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="921ae-160">Выберите **ОК**, чтобы начать обновление прогноза.</span><span class="sxs-lookup"><span data-stu-id="921ae-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="921ae-161">На приведенном ниже рисунке показан пример диалогового окна **Обновить прогноз по заказу на работу**.</span><span class="sxs-lookup"><span data-stu-id="921ae-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Рисунок 2](media/07-work-orders.png)
