---
title: Отчет «Сравнение хранилища цен номенклатур»
description: Узнайте, как создать отчет «Сравнение хранилища цен номенклатур» и затем просмотреть и/или экспортировать результат.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6554aec1991080f4a14aedb3440ff3dfd32e9b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983982"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="cafe8-103">Отчет «Сравнение хранилища цен номенклатур»</span><span class="sxs-lookup"><span data-stu-id="cafe8-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cafe8-104">В этом разделе объясняется, как выполнить отчет **Сравнение хранилища цен номенклатур** и сделать результат доступным в цифровом виде либо как интерактивную страницу в Dynamics 365 Supply Chain Management, либо в виде экспортированного документа в любом из нескольких форматов.</span><span class="sxs-lookup"><span data-stu-id="cafe8-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="cafe8-105">При просмотре отчета в браузере столбцы и агрегированные балансы динамически корректируются в зависимости от настроенного макета.</span><span class="sxs-lookup"><span data-stu-id="cafe8-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="cafe8-106">Можно сортировать результаты, фильтровать их, детализировать данные и т. д.</span><span class="sxs-lookup"><span data-stu-id="cafe8-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="cafe8-107">Результаты отчета хранятся в информационном объекте **Сравнить цены номенклатур**, что позволяет фильтровать и экспортировать результаты в формате CSV или Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cafe8-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="cafe8-108">Отчет **Сравнение хранилища цен номенклатур** полезен в тех случаях, когда результат содержит много строк.</span><span class="sxs-lookup"><span data-stu-id="cafe8-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="cafe8-109">Например, результат будет содержать много строк, если в версии учета затрат имеется более 40000 номенклатур, содержащих ожидающие цены номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="cafe8-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="cafe8-110">Включить Сравнение хранилища цен номенклатур</span><span class="sxs-lookup"><span data-stu-id="cafe8-110">Enable compare item prices storage</span></span>

<span data-ttu-id="cafe8-111">Прежде чем использовать эту функцию, необходимо включить ее в системе.</span><span class="sxs-lookup"><span data-stu-id="cafe8-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="cafe8-112">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения их при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cafe8-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="cafe8-113">В этой статье функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cafe8-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="cafe8-114">**Модуль** — Управление затратами</span><span class="sxs-lookup"><span data-stu-id="cafe8-114">**Module** - Cost management</span></span>
- <span data-ttu-id="cafe8-115">**Имя функции** — Сравнение хранилища цен номенклатур</span><span class="sxs-lookup"><span data-stu-id="cafe8-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="cafe8-116">Создать отчет «Сравнение хранилища цен номенклатур»</span><span class="sxs-lookup"><span data-stu-id="cafe8-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="cafe8-117">Выполните следующие действия, чтобы создать и сохранить отчет **Сравнение хранилища цен номенклатур**:</span><span class="sxs-lookup"><span data-stu-id="cafe8-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="cafe8-118">Перейти к **Управление затратами > Запросы и отчеты > Отчеты о заранее определенных затратах > Сравнение хранилища цен номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="cafe8-119">Выберите **Создать**, чтобы открыть панель **Сравнить цены номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="cafe8-120">Настройте следующие параметры, чтобы определить, какие цены необходимо сравнить в отчете:</span><span class="sxs-lookup"><span data-stu-id="cafe8-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="cafe8-121">На экспресс-вкладке **параметры** присвойте отчету уникальное **имя** и используйте поля в разделах **Ожидающие сравниваемые цены** и **Цены, используемые для сравнения**, чтобы определить, какие цены и даты требуется сравнить.</span><span class="sxs-lookup"><span data-stu-id="cafe8-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="cafe8-122">На экспресс-вкладке **Записи для добавления** настройте фильтры и ограничения, чтобы определить, какие данные должны быть включены в отчет.</span><span class="sxs-lookup"><span data-stu-id="cafe8-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="cafe8-123">На экспресс-вкладке **Выполнять в фоновом режиме** настройте способ и частоту создания отчета.</span><span class="sxs-lookup"><span data-stu-id="cafe8-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="cafe8-124">Этот отчет всегда выполняется как часть пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="cafe8-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="cafe8-125">Нажмите кнопку **ОК**, чтобы применить настройки и закрыть панель.</span><span class="sxs-lookup"><span data-stu-id="cafe8-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="cafe8-126">После завершения пакетного задания оно будет указано на странице **Сравнение хранилища цен номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="cafe8-127">Возможно, потребуется обновить страницу, чтобы просмотреть отчет.</span><span class="sxs-lookup"><span data-stu-id="cafe8-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="cafe8-128">Знакомство с отчетом «Сравнение хранилища цен номенклатур»</span><span class="sxs-lookup"><span data-stu-id="cafe8-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="cafe8-129">После создания отчета его можно просмотреть и изучить в любое время следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cafe8-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="cafe8-130">Перейти к **Управление затратами > Запросы и отчеты > Отчеты о заранее определенных затратах > Сравнение хранилища цен номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="cafe8-131">Выберите отчет из списка.</span><span class="sxs-lookup"><span data-stu-id="cafe8-131">Select a report from the list.</span></span>

1. <span data-ttu-id="cafe8-132">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="cafe8-132">Do one of the following:</span></span>

    - <span data-ttu-id="cafe8-133">Выберите **Обзор**, чтобы получить обзор результатов отчета.</span><span class="sxs-lookup"><span data-stu-id="cafe8-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="cafe8-134">Выберите **Просмотреть сведения** для получения подробного представления отчета</span><span class="sxs-lookup"><span data-stu-id="cafe8-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="cafe8-135">После открытия выбранного представления вы можете сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="cafe8-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="cafe8-136">Выберите практически любой заголовок столбца для сортировки или отсортируйте таблицы по значениям в этом столбце, так же как и в случае большинства стандартных форм в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cafe8-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="cafe8-137">Примечание: невозможно отсортировать или отфильтровать столбец **Чистое изменение цены %**, поскольку это вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="cafe8-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="cafe8-138">Выберите **Отображение аналитики**, чтобы открыть область, в которой можно выбрать столбец аналитики для включения в форму.</span><span class="sxs-lookup"><span data-stu-id="cafe8-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="cafe8-139">Установите **Сохранить настройки** на значение **Да**, если вы хотите сохранить эти параметры, чтобы они сохранялись при следующем открытии отчета.</span><span class="sxs-lookup"><span data-stu-id="cafe8-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="cafe8-140">Нажмите кнопку **ОК**, чтобы применить настройки и закрыть.</span><span class="sxs-lookup"><span data-stu-id="cafe8-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="cafe8-141">Выберите любую строку в форме, а затем выберите **Просмотреть сведения** для просмотра дополнительных сведений о выбранной номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="cafe8-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="cafe8-142">Вы сможете детализировать данные отсюда.</span><span class="sxs-lookup"><span data-stu-id="cafe8-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="cafe8-143">Выберите любую строку в форме, а затем выберите **Просмотреть таблицу диаграмм сравнения** для просмотра интерактивного графического представления результатов относительно их связи с выбранной номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="cafe8-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="cafe8-144">Можно ознакомиться с результатами, выбирая различные графические элементы в диаграмме и условных обозначениях диаграммы.</span><span class="sxs-lookup"><span data-stu-id="cafe8-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="cafe8-145">Выберите любую строку в форме, а затем выберите **Просмотреть сведения расчета** для просмотра дополнительных сведений о расчетах, связанных с выбранной номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="cafe8-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="cafe8-146">Вы сможете детализировать данные отсюда.</span><span class="sxs-lookup"><span data-stu-id="cafe8-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="cafe8-147">Экспорт отчета «Сравнение хранилища цен номенклатур»</span><span class="sxs-lookup"><span data-stu-id="cafe8-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="cafe8-148">Каждый созданный отчет сохраняется в информационный объекте **Сравнить цены номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="cafe8-149">Можно использовать стандартные функции управления данными Supply Chain Management, чтобы экспортировать данные из этого объекта в любой поддерживаемый формат данных, включая CSV или Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cafe8-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="cafe8-150">В следующем примере показано, как экспортировать отчет о **Сравнение хранилища цен номенклатур**:</span><span class="sxs-lookup"><span data-stu-id="cafe8-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="cafe8-151">Перейдите в раздел **Администрирование системы > Рабочие области > Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="cafe8-152">Нажмите кнопку **Экспорт** в разделе **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="cafe8-153">Откроется страница **экспорт**, которая будет использоваться для настройки задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="cafe8-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="cafe8-154">Начните с присвоения заданию **Имя группы**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="cafe8-155">В разделе **Выбранные объекты** выберите **Добавить объект**, чтобы открыть диалоговое окно, в котором можно настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cafe8-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="cafe8-156">**Имя объекта** — выберите **Сравнить цены номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="cafe8-157">**Формат целевых данных** — выберите формат, в который необходимо экспортировать данные.</span><span class="sxs-lookup"><span data-stu-id="cafe8-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="cafe8-158">Выберите **Добавить**, чтобы добавить новую строку, а затем нажмите кнопку **Закрыть**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cafe8-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="cafe8-159">Обычно вы экспортируете один отчет за раз.</span><span class="sxs-lookup"><span data-stu-id="cafe8-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="cafe8-160">Для этого настройте **фильтр** для строки, только что добавленной в область **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="cafe8-161">Это позволяет определить, какие отчеты из объекта **Сравнить цены номенклатур** будут включены в экспорт.</span><span class="sxs-lookup"><span data-stu-id="cafe8-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="cafe8-162">Настройка следующих параметров фильтра для экспорта одного отчета:</span><span class="sxs-lookup"><span data-stu-id="cafe8-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="cafe8-163">На вкладке **диапазон** выберите **добавить**, чтобы добавить новую строку.</span><span class="sxs-lookup"><span data-stu-id="cafe8-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="cafe8-164">Установите **Таблица** на **Сравнить цены номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="cafe8-165">Установите **производная таблица** на **Сравнить цены номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="cafe8-166">Установите **поле** в поле, по которому необходимо выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="cafe8-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="cafe8-167">Обычно используется **Имя выполнения** или **Время выполнения**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="cafe8-168">Задайте **критерию** значение из выбранного поля, которое необходимо найти (имя отчета или время создания отчета).</span><span class="sxs-lookup"><span data-stu-id="cafe8-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="cafe8-169">При необходимости добавьте строки в таблицу **диапазон** до тех пор, пока не будет найден необходимый отчет.</span><span class="sxs-lookup"><span data-stu-id="cafe8-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="cafe8-170">Нажмите кнопку **ОК**, чтобы сохранить настройки и закрыть.</span><span class="sxs-lookup"><span data-stu-id="cafe8-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="cafe8-171">Для сохранения настроек экспорта выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cafe8-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="cafe8-172">Откройте вкладку **Параметры экспорта** и выберите **Экспортировать**, чтобы создать файл экспорта.</span><span class="sxs-lookup"><span data-stu-id="cafe8-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="cafe8-173">Будет открыта страница **Сводка по выполнению**, в которой можно увидеть статус задания экспорта и список экспортированных объектов.</span><span class="sxs-lookup"><span data-stu-id="cafe8-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="cafe8-174">Выберите объект **Сравнить цены номенклатур**, указанный в области **Статус обработки объекта**, а затем выберите **Загрузить файл**, чтобы загрузить данные, экспортированные из этого объекта.</span><span class="sxs-lookup"><span data-stu-id="cafe8-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="cafe8-175">Дополнительные сведения об использовании управления данными для экспорта данных см. в разделе [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="cafe8-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
