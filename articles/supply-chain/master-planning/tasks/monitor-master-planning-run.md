---
title: Мониторинг выполнения сводного планирования
description: В этой теме объясняется, как планировщик производства может определить, выполняется ли в настоящее сводное планирование.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6e7fdd51670ea63efc04e883703f1763955115b
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781927"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="2887a-103">Мониторинг выполнения сводного планирования</span><span class="sxs-lookup"><span data-stu-id="2887a-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="2887a-104">Используйте диаграмму Ганта для наглядного представления хода выполнения сводного планирования</span><span class="sxs-lookup"><span data-stu-id="2887a-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="2887a-105">На странице **Просмотр хода выполнения сводного планирования** можно просмотреть подробные сведения о выполнениях сводного планирования в виде диаграммы Ганта.</span><span class="sxs-lookup"><span data-stu-id="2887a-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="2887a-106">Эти функции могут помочь понять время, потраченное на различные этапы сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="2887a-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="2887a-107">Для текущего активного задания планирования страницу **Просмотр хода выполнения сводного планирования** можно использовать для отслеживания хода выполнения и просмотра предполагаемого оставшегося времени.</span><span class="sxs-lookup"><span data-stu-id="2887a-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="2887a-108">Включение и использование функции визуализации хода выполнения сводного плана</span><span class="sxs-lookup"><span data-stu-id="2887a-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="2887a-109">Для использования этой функции выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2887a-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="2887a-110">В рабочей области **Управление функциями** на вкладке **Создать** выберите **Визуализация хода выполнения сводного планирования** в списке.</span><span class="sxs-lookup"><span data-stu-id="2887a-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="2887a-111">Если эта функция не отображается на вкладке **Создать**, проверьте вкладки **Не включено** и **Все**.</span><span class="sxs-lookup"><span data-stu-id="2887a-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="2887a-112">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="2887a-112">Select **Enable now**.</span></span> <span data-ttu-id="2887a-113">Вместо этого выберите **План**, а затем выберите время, когда необходимо включить функцию.</span><span class="sxs-lookup"><span data-stu-id="2887a-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="2887a-114">На странице **Просмотр хода выполнения сводного планирования** могут отображаться как исторические задания планирования, так и активные задания планирования.</span><span class="sxs-lookup"><span data-stu-id="2887a-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="2887a-115">Для просмотра исторических заданий планирования есть две возможности.</span><span class="sxs-lookup"><span data-stu-id="2887a-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="2887a-116">Перейдите **Сводное планирование \> Настройка \> Планы \> Сводные планы**, а затем на панели операций выберите **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="2887a-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="2887a-117">Выбрав нужное задание, выберите **Запросы**, а затем выберите **Просмотр хода выполнения**.</span><span class="sxs-lookup"><span data-stu-id="2887a-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="2887a-118">Перейдите **Сводное планирование \> Рабочие области \> Сводное планирование**, на плитке сводного планирования выберите **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="2887a-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="2887a-119">Выбрав нужное задание, выберите **Запросы**, а затем выберите **Просмотр хода выполнения**.</span><span class="sxs-lookup"><span data-stu-id="2887a-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="2887a-120">Для просмотра активных заданий планирования есть две возможности.</span><span class="sxs-lookup"><span data-stu-id="2887a-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="2887a-121">Перейдите **Сводное планирование \> Рабочие области \> Сводное планирование**, на панели операций выберите **Незавершенные процессы планирования**.</span><span class="sxs-lookup"><span data-stu-id="2887a-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="2887a-122">Выбрав нужное задание, выберите **Запросы**, а затем выберите **Просмотр хода выполнения**.</span><span class="sxs-lookup"><span data-stu-id="2887a-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="2887a-123">Перейдите **Сводное планирование \> Рабочие области \> Сводное планирование**, на плитке сводного планирования выберите **Просмотр хода выполнения**.</span><span class="sxs-lookup"><span data-stu-id="2887a-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="2887a-124">Выбрав нужное задание, выберите **Запросы**, а затем выберите **Просмотр хода выполнения**.</span><span class="sxs-lookup"><span data-stu-id="2887a-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="2887a-125">Обратите внимание, что активные задания можно просматривать только при обработке задания планирования.</span><span class="sxs-lookup"><span data-stu-id="2887a-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="2887a-126">Анализ задания сводного планирования</span><span class="sxs-lookup"><span data-stu-id="2887a-126">Analyze a master planning job</span></span>

<span data-ttu-id="2887a-127">На диаграмме Ганта можно развернуть каждый из следующих процессов планирования, чтобы просмотреть дополнительные сведения о затраченном времени:</span><span class="sxs-lookup"><span data-stu-id="2887a-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="2887a-128">Инициализация</span><span class="sxs-lookup"><span data-stu-id="2887a-128">Initializing</span></span>
- <span data-ttu-id="2887a-129">Удаление и вставка данных</span><span class="sxs-lookup"><span data-stu-id="2887a-129">Deleting and inserting data</span></span>
- <span data-ttu-id="2887a-130">Планирование покрытия</span><span class="sxs-lookup"><span data-stu-id="2887a-130">Coverage planning</span></span>
- <span data-ttu-id="2887a-131">Задержки</span><span class="sxs-lookup"><span data-stu-id="2887a-131">Delays</span></span>
- <span data-ttu-id="2887a-132">Сообщения по действию</span><span class="sxs-lookup"><span data-stu-id="2887a-132">Action messages</span></span>
- <span data-ttu-id="2887a-133">Финализация</span><span class="sxs-lookup"><span data-stu-id="2887a-133">Finalization</span></span>
- <span data-ttu-id="2887a-134">Автоматическое подтверждение</span><span class="sxs-lookup"><span data-stu-id="2887a-134">Auto-firming</span></span>

<span data-ttu-id="2887a-135">Диаграмма Ганта — это полезный инструмент, если необходимо просмотреть результат использования сообщений по действиям.</span><span class="sxs-lookup"><span data-stu-id="2887a-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="2887a-136">Навигация в диаграмме Ганта</span><span class="sxs-lookup"><span data-stu-id="2887a-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="2887a-137">Чтобы развернуть выбранную группу и показать подробные сведения, выберите знак "плюс" (**+**) в представлении в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="2887a-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="2887a-138">Чтобы свернуть выбранную группу, выберите знак "минус" (**–**) в представлении в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="2887a-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="2887a-139">Для навигации можно использовать клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="2887a-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="2887a-140">Для перемещения между строками используйте клавиши **стрелка вверх** и **стрелка вниз**.</span><span class="sxs-lookup"><span data-stu-id="2887a-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="2887a-141">Для развертывания и свертывания групп используйте клавиши **стрелка вправо** и **стрелка влево**.</span><span class="sxs-lookup"><span data-stu-id="2887a-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="2887a-142">Чтобы открыть или закрыть все уровни диаграммы Ганта, выберите **Развернуть все** или **Свернуть все**.</span><span class="sxs-lookup"><span data-stu-id="2887a-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="2887a-143">Чтобы просмотреть связанное время обработки, наведите указатель на задачу.</span><span class="sxs-lookup"><span data-stu-id="2887a-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="2887a-144">(Задачи находятся на самом нижнем уровне диаграммы Ганта.)</span><span class="sxs-lookup"><span data-stu-id="2887a-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="2887a-145">Просмотр дополнительного выполнения сводного планирования для заданий сравнения</span><span class="sxs-lookup"><span data-stu-id="2887a-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="2887a-146">При выборе задания сводного планирования в поле **Показать дополнительное выполнение сводного планирования** можно просмотреть дополнительное выполнение сводного планирования в диаграмме Ганта и сравнить два задания.</span><span class="sxs-lookup"><span data-stu-id="2887a-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="2887a-147">Отображение на уровне спецификации</span><span class="sxs-lookup"><span data-stu-id="2887a-147">BOM-level display</span></span>

<span data-ttu-id="2887a-148">Уровни спецификации (BOM) отображаются по-разному для планирования покрытия, задержек, действий и утверждений.</span><span class="sxs-lookup"><span data-stu-id="2887a-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="2887a-149">**Планирование покрытия** — уровни BOM отображаются ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="2887a-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="2887a-150">Они вычисляются сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="2887a-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="2887a-151">**Пример:** уровень BOM 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="2887a-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="2887a-152">**Задержки** — уровни BOM отображаются как уровни BOM планирования покрытия, умноженные на –1.</span><span class="sxs-lookup"><span data-stu-id="2887a-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="2887a-153">(Иными словами, они имеют отрицательное значение.)</span><span class="sxs-lookup"><span data-stu-id="2887a-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="2887a-154">**Пример:** уровень BOM –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="2887a-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="2887a-155">**Сообщение по действию** — уровни BOM отображаются ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="2887a-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="2887a-156">Они вычисляются сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="2887a-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="2887a-157">**Пример:** уровень BOM 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="2887a-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="2887a-158">**Автоматическое подтверждение** — уровни BOM отображаются как 999 минус уровень BOM планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="2887a-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="2887a-159">**Пример:** уровень BOM 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="2887a-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="2887a-160">В приведенной ниже таблице представлена сводная информация о поведении.</span><span class="sxs-lookup"><span data-stu-id="2887a-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="2887a-161">Показанный уровень BOM</span><span class="sxs-lookup"><span data-stu-id="2887a-161">BOM level that is shown</span></span> | <span data-ttu-id="2887a-162">Готовая номенклатура</span><span class="sxs-lookup"><span data-stu-id="2887a-162">End item</span></span> | <span data-ttu-id="2887a-163">Субкомпонент</span><span class="sxs-lookup"><span data-stu-id="2887a-163">Subcomponent</span></span> | <span data-ttu-id="2887a-164">Сырье</span><span class="sxs-lookup"><span data-stu-id="2887a-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="2887a-165">Планирование покрытия</span><span class="sxs-lookup"><span data-stu-id="2887a-165">Coverage planning</span></span> | <span data-ttu-id="2887a-166">0</span><span class="sxs-lookup"><span data-stu-id="2887a-166">0</span></span> | <span data-ttu-id="2887a-167">1</span><span class="sxs-lookup"><span data-stu-id="2887a-167">1</span></span> | <span data-ttu-id="2887a-168">2</span><span class="sxs-lookup"><span data-stu-id="2887a-168">2</span></span> |
| <span data-ttu-id="2887a-169">Задержки</span><span class="sxs-lookup"><span data-stu-id="2887a-169">Delays</span></span> | <span data-ttu-id="2887a-170">0</span><span class="sxs-lookup"><span data-stu-id="2887a-170">0</span></span> | <span data-ttu-id="2887a-171">–1</span><span class="sxs-lookup"><span data-stu-id="2887a-171">–1</span></span> | <span data-ttu-id="2887a-172">–2</span><span class="sxs-lookup"><span data-stu-id="2887a-172">–2</span></span> |
| <span data-ttu-id="2887a-173">Сообщение по действию</span><span class="sxs-lookup"><span data-stu-id="2887a-173">Action message</span></span> | <span data-ttu-id="2887a-174">0</span><span class="sxs-lookup"><span data-stu-id="2887a-174">0</span></span> | <span data-ttu-id="2887a-175">1</span><span class="sxs-lookup"><span data-stu-id="2887a-175">1</span></span> | <span data-ttu-id="2887a-176">2</span><span class="sxs-lookup"><span data-stu-id="2887a-176">2</span></span> |
| <span data-ttu-id="2887a-177">Автоматическое подтверждение</span><span class="sxs-lookup"><span data-stu-id="2887a-177">Auto-firming</span></span> | <span data-ttu-id="2887a-178">999</span><span class="sxs-lookup"><span data-stu-id="2887a-178">999</span></span> | <span data-ttu-id="2887a-179">998</span><span class="sxs-lookup"><span data-stu-id="2887a-179">998</span></span> | <span data-ttu-id="2887a-180">997</span><span class="sxs-lookup"><span data-stu-id="2887a-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="2887a-181">Визуализация хода выполнения</span><span class="sxs-lookup"><span data-stu-id="2887a-181">Visualize progress</span></span>

<span data-ttu-id="2887a-182">При просмотре выполняющегося задания сводного планирования ход выполнения показан цветами на диаграмме Ганта.</span><span class="sxs-lookup"><span data-stu-id="2887a-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="2887a-183">К примеру следующие цвета применяются к синей теме.</span><span class="sxs-lookup"><span data-stu-id="2887a-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="2887a-184">Для других цветовых тем цвета будут отличаться.</span><span class="sxs-lookup"><span data-stu-id="2887a-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="2887a-185">**Темно-синий** — завершенные задачи планирования.</span><span class="sxs-lookup"><span data-stu-id="2887a-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="2887a-186">**Оранжевый** — выполняемая в данный момент задача.</span><span class="sxs-lookup"><span data-stu-id="2887a-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="2887a-187">**Светло-голубой** — оценка для оставшихся задач.</span><span class="sxs-lookup"><span data-stu-id="2887a-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="2887a-188">Цвет отображается только на самом нижнем уровне в диаграмме Ганта.</span><span class="sxs-lookup"><span data-stu-id="2887a-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="2887a-189">Выберите **Развернуть все**, чтобы просмотреть все задачи в задании сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="2887a-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="2887a-190">Оценка оставшихся задач основана на исторических заданиях сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="2887a-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="2887a-191">Выполнение сводного планирования и отслеживание времени обработки</span><span class="sxs-lookup"><span data-stu-id="2887a-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="2887a-192">В панели мониторинга по умолчанию выберите **Сводное планирование**.</span><span class="sxs-lookup"><span data-stu-id="2887a-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="2887a-193">В поле **План** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2887a-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="2887a-194">Выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="2887a-194">Select **Run**.</span></span>
1. <span data-ttu-id="2887a-195">Установите для параметра **Отслеживать время обработки** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2887a-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="2887a-196">В поле **Количество потоков** введите число.</span><span class="sxs-lookup"><span data-stu-id="2887a-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="2887a-197">На экспресс-вкладке **Записи для добавления** выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="2887a-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="2887a-198">В сетке выберите строку, в которой в поле **Поле** задано как **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="2887a-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="2887a-199">В поле **Критерии** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2887a-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="2887a-200">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2887a-200">Select **OK**.</span></span>
