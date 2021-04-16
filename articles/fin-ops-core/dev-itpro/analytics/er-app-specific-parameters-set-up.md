---
title: Настройка параметров формата ER для юридического лица
description: В этом разделе объясняется, как настроить параметры формата электронной отчетности (ER) для юридического лица.
author: NickSelin
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 4003208a1f02db134bbec1ecf90c1cdd2973e67f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751162"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="83d7c-103">Настройка параметров формата ER для юридического лица</span><span class="sxs-lookup"><span data-stu-id="83d7c-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="83d7c-104">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="83d7c-104">Prerequisites</span></span>

<span data-ttu-id="83d7c-105">Для выполнения этих шагов необходимо сначала выполнить шаги в разделе [Настройка форматов ER для использования параметров, указанных для юридического лица](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="83d7c-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="83d7c-106">Чтобы выполнить примеры в этом разделе, необходимо иметь доступ к Microsoft Dynamics 365 Finance (Finance) для одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="83d7c-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="83d7c-107">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="83d7c-107">Electronic reporting developer</span></span>
- <span data-ttu-id="83d7c-108">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="83d7c-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="83d7c-109">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="83d7c-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="83d7c-110">Импорт конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="83d7c-110">Import ER configurations</span></span>

1.  <span data-ttu-id="83d7c-111">Выполните вход в свою среду.</span><span class="sxs-lookup"><span data-stu-id="83d7c-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="83d7c-112">В панели мониторинга по умолчанию выберите **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="83d7c-113">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="83d7c-114">Импортируйте в текущий экземпляр Finance конфигурации, которые были экспортированы из Regulatory Configuration Service (RCS) во время выполнения шагов, описанных в разделе [Настройка форматов ER для использования параметров, указанных для юридического лица](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="83d7c-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="83d7c-115">Выполните следующие шаги для каждой конфигурации электронной отчетности (ER) в следующем порядке: модель данных, сопоставление моделей и форматы.</span><span class="sxs-lookup"><span data-stu-id="83d7c-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="83d7c-116">Выберите **Exchange \> Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="83d7c-117">Выберите **Обзор**, чтобы выбрать файл для требуемой конфигурации ER в формате XML.</span><span class="sxs-lookup"><span data-stu-id="83d7c-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="83d7c-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-118">Select **OK**.</span></span>
    
    <span data-ttu-id="83d7c-119">На следующем рисунке показаны конфигурации, которые должны получиться после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="83d7c-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Страница конфигураций электронной отчетности](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="83d7c-121">Настройка параметров компании DEMF</span><span class="sxs-lookup"><span data-stu-id="83d7c-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="83d7c-122">Структуру ER можно использовать для настройки параметров приложения для формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="83d7c-123">Выберите юридическое лицо **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="83d7c-124">В дереве конфигураций выберите формат **Формат для изучения поиска данных LE**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="83d7c-125">В области действий на вкладке **Конфигурации** в группе **Параметры для конкретного приложения** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![Страница импорта параметров для конкретного приложения ER](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="83d7c-127">На странице параметры **Параметры для конкретного приложения** можно настроить правила для источника данных **Выбор** в формате **Формат для изучения поиска данных LE**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="83d7c-128">Если базовый формат ER будет содержать несколько источников данных типа **Поиск**, необходимо выбрать нужный источник данных на экспресс-вкладке **Поиск**, прежде чем можно будет начать настройку набора правил для источника данных.</span><span class="sxs-lookup"><span data-stu-id="83d7c-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="83d7c-129">Для каждого источника данных можно настроить отдельные правила для каждой версии выбранного формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="83d7c-130">Полный набор правил для всех источников данных поиска, доступных в выбранной версии базового формата ER, используется для настройки параметров для конкретного приложения в формате ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="83d7c-131">Выберите версию **1.1.1** формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="83d7c-132">На экспресс- вкладке **Условия** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="83d7c-133">В поле **Код** новой записи выберите стрелку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="83d7c-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="83d7c-134">Поиск представляет собой список налоговых кодов для выбора.</span><span class="sxs-lookup"><span data-stu-id="83d7c-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="83d7c-135">Этот список возвращается источником данных **Model.Data.Tax**, который был настроен в основном формате ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="83d7c-136">Так как этот источник данных содержит поле **Имя**, в поиске отображается имя каждого налогового кода.</span><span class="sxs-lookup"><span data-stu-id="83d7c-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![Страница импорта параметров для конкретного приложения ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="83d7c-138">Выберите налоговый код **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="83d7c-139">В поле **Результат поиска** новой записи выберите стрелку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="83d7c-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="83d7c-140">При поиске представлен список значений для перечисления формата TaxationLevel format для выбора.</span><span class="sxs-lookup"><span data-stu-id="83d7c-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="83d7c-141">Обратите внимание, что если выбран немецкий язык как предпочитаемый язык для пользователя, выполнившего вход, метки значений будут отображаться в поиске на немецком языке при условии, что они были переведены в основном формате ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="83d7c-142">Кроме того, если метка источника данных поиска была переведена, эта метка появится на предпочтительном языке пользователя на вкладке **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![Страница импорта параметров для конкретного приложения ER](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="83d7c-144">Выбор значения **Обычное налогообложение**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="83d7c-145">При добавлении этой записи определяется следующее правило: каждый раз, когда запрашивается источник данных поиска **Выбор** и налоговый код **VAT19** передается в качестве аргумента, в качестве запрошенного уровня налогообложения будет возвращено **Обычное налогообложение**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="83d7c-146">Выберите **Добавить**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83d7c-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="83d7c-147">В поле **Код** выберите налоговый код **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="83d7c-148">В поле **Результат поиска** выберите значение **Обычное налогообложение**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="83d7c-149">Снова выберите **Добавить**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83d7c-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="83d7c-150">В поле **Код** выберите налоговый код **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="83d7c-151">В поле **Результат поиска** выберите значение **Сокращенное налогообложение**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="83d7c-152">Снова выберите **Добавить**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83d7c-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="83d7c-153">В поле **Код** выберите налоговый код **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="83d7c-154">В поле **Результат поиска** выберите значение **Сокращенное налогообложение**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="83d7c-155">Снова выберите **Добавить**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83d7c-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="83d7c-156">В поле **Код** выберите налоговый код **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="83d7c-157">В поле **Результат поиска** выберите значение **Нет налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="83d7c-158">Снова выберите **Добавить**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83d7c-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="83d7c-159">В поле **Код** выберите налоговый код **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="83d7c-160">В поле **Результат поиска** выберите значение **Нет налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="83d7c-161">Снова выберите **Добавить**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83d7c-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="83d7c-162">В поле **Код** выберите параметр **\*Нет налогообложения\***.</span><span class="sxs-lookup"><span data-stu-id="83d7c-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="83d7c-163">В поле **Результат поиска** выберите значение **Другое**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="83d7c-164">При добавлении этой последней записи определяется следующее правило: каждый раз, когда запрашивается налоговый код, передаваемый в качестве аргумента, не удовлетворяет какому-либо предыдущему правилу, в качестве запрошенного уровня налогообложения будет возвращено **Другое**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![Страница импорта параметров для конкретного приложения ER](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="83d7c-166">В поле **Состояние** выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="83d7c-167">При выполнении версии формата ER со статусом **Завершено** или **Общие** этот набор правил должен находиться в состоянии **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="83d7c-168">В противном случае выполнение базового формата ER будет прервано, когда формат пытается загрузить данные из этого набора правил во время выполнения источника данных поиска **Выбор**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="83d7c-169">При выполнении версии формата ER со статусом **Черновик** базовый формат ER имеет доступ к этому набору правил независимо от его состояния.</span><span class="sxs-lookup"><span data-stu-id="83d7c-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="83d7c-170">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-170">Select **Save**.</span></span>
18. <span data-ttu-id="83d7c-171">Закройте страницу **Параметры для конкретного приложения**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="83d7c-172">Выполните формат ER в компании DEMF</span><span class="sxs-lookup"><span data-stu-id="83d7c-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="83d7c-173">В дереве конфигураций выберите формат **Формат для изучения поиска данных LE**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="83d7c-174">В области действий выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="83d7c-175">В появившемся диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="83d7c-176">Загрузите созданный отчет и сохраните его локально.</span><span class="sxs-lookup"><span data-stu-id="83d7c-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="83d7c-177">Обратите внимание, что в созданном отчете сводка налогового кода **InVAT7** была помещена на уровень **Сокращенное**, а суммарные данные кодов **VAT19** и **InVA19** помещены на уровне **Обычное**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="83d7c-178">Это поведение определяется конфигурацией в наборе правил, зависящем от юридического лица.</span><span class="sxs-lookup"><span data-stu-id="83d7c-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="83d7c-179">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="83d7c-180">Выберите налоговый код **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="83d7c-181">В области действий на вкладке **Код налога** в группе **Запросы** выберите **Разнесенный налог** для просмотра информации о значении налога и примененной налоговой ставки для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="83d7c-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Страница разнесенного налога](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="83d7c-183">Закройте страницу "Разнесенные налоги".</span><span class="sxs-lookup"><span data-stu-id="83d7c-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="83d7c-184">Настройка параметров компании USMF</span><span class="sxs-lookup"><span data-stu-id="83d7c-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="83d7c-185">Выберите юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="83d7c-186">Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="83d7c-187">В дереве конфигураций разверните элемент **Модель данных для изучения параметризованных вызовов**, раскройте элемент **Формат для изучения параметризованных вызовов** и выберите формат **Формат для изучения поиска данных LE**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="83d7c-188">В области действий на вкладке **Конфигурации** в группе **Параметры для конкретного приложения** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="83d7c-189">Выберите версию **1.1.1** выбранного формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="83d7c-190">На экспресс- вкладке **Условия** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="83d7c-191">В поле **Код** новой записи выберите стрелку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="83d7c-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="83d7c-192">Теперь поиск отображает список налоговых кодов для налога компании **USMF** для выбора.</span><span class="sxs-lookup"><span data-stu-id="83d7c-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![Страница импорта параметров для конкретного приложения ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="83d7c-194">Выберите налоговый код **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="83d7c-195">В поле **Результат поиска** новой записи выберите значение **Нет налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="83d7c-196">Снова выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-196">Select **Add** again.</span></span>
11. <span data-ttu-id="83d7c-197">В поле **Код** новой записи выберите параметр **\*Нет налогообложения\***.</span><span class="sxs-lookup"><span data-stu-id="83d7c-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="83d7c-198">В поле **Результат поиска** новой записи выберите значение **Обычное налогообложение**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="83d7c-199">В поле **Состояние** выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="83d7c-200">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-200">Select **Save**.</span></span>

    ![Страница импорта параметров для конкретного приложения ER](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="83d7c-202">Закройте страницу **Параметры для конкретного приложения**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="83d7c-203">Выполните формат ER в компании USMF</span><span class="sxs-lookup"><span data-stu-id="83d7c-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="83d7c-204">В дереве конфигураций выберите формат **Формат для изучения поиска данных LE**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="83d7c-205">В области действий выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="83d7c-206">В появившемся диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="83d7c-207">Загрузите созданный отчет и сохраните его локально.</span><span class="sxs-lookup"><span data-stu-id="83d7c-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="83d7c-208">В созданном отчете обратите внимание, что теперь вы повторно использовали один и тот же формат ER для другого юридического лица, но не внесли никакие изменения в формат ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="83d7c-209">Использование параметров, зависимых от юридического лица</span><span class="sxs-lookup"><span data-stu-id="83d7c-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="83d7c-210">Параметры экспорта</span><span class="sxs-lookup"><span data-stu-id="83d7c-210">Export parameters</span></span>

1.  <span data-ttu-id="83d7c-211">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="83d7c-212">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="83d7c-213">В дереве конфигураций выберите формат **Формат для изучения поиска данных LE**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="83d7c-214">В области действий на вкладке **Конфигурации** в группе **Параметры для конкретного приложения** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="83d7c-215">Выберите версию **1.1.1** формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="83d7c-216">На панели операций выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="83d7c-217">Загрузите созданный файл и сохраните его локально.</span><span class="sxs-lookup"><span data-stu-id="83d7c-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="83d7c-218">Настроенный набор параметров приложения был экспортирован как файл XML.</span><span class="sxs-lookup"><span data-stu-id="83d7c-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="83d7c-219">Параметры импорта</span><span class="sxs-lookup"><span data-stu-id="83d7c-219">Import parameters</span></span>

1.  <span data-ttu-id="83d7c-220">Выберите версию **1.1.2** формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="83d7c-221">На панели операций выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="83d7c-222">Выберите **Да** для подтверждения того, что вы хотите перезаписать существующие параметры для конкретного приложения для данной версии формата.</span><span class="sxs-lookup"><span data-stu-id="83d7c-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="83d7c-223">Нажмите **Обзор**, чтобы найти файл, содержащий экспортированные параметры приложения для версии **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="83d7c-224">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-224">Select **OK**.</span></span>

    <span data-ttu-id="83d7c-225">Версия **1.1.2** формата ER теперь имеет те же параметры, что и приложение, первоначально настроенное для версии **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="83d7c-226">Обратите внимание, что зависящие от приложения параметры формата ER зависят от юридического лица.</span><span class="sxs-lookup"><span data-stu-id="83d7c-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="83d7c-227">Для повторного использования параметров, связанных с приложением, которые были настроены для одного юридического лица, в другом юридическом лице, необходимо экспортировать их, а затем импортировать их после того, как вы войдете в другую компанию.</span><span class="sxs-lookup"><span data-stu-id="83d7c-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="83d7c-228">Этот подход можно также использовать для переноса формата ER, относящегося к параметрам конкретного приложения, которые первоначально были настроены в одном экземпляре Finance в другом экземпляре Finance.</span><span class="sxs-lookup"><span data-stu-id="83d7c-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="83d7c-229">Имейте в виду, что при настройке параметров конкретного приложения для одной версии формата ER и импорте более поздней версии того же формата в текущий экземпляр Finance существующие параметры для конкретного приложения не будут применены к импортируемой версии.</span><span class="sxs-lookup"><span data-stu-id="83d7c-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="83d7c-230">Также имейте в виду, что при выборе файла для импорта структура параметров конкретного приложения в этом файле сравнивается со структурой соответствующего источника данных типа **Поиск** в формате ER, выбранном для импорта.</span><span class="sxs-lookup"><span data-stu-id="83d7c-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="83d7c-231">Импорт выполняется, когда структура каждого параметра конкретного приложения совпадает со структурой соответствующего источника данных в формате ER, выбранном для импорта.</span><span class="sxs-lookup"><span data-stu-id="83d7c-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="83d7c-232">Если структуры не соответствуют друг другу, выводится предупреждающее сообщение о том, что импорт выполнить невозможно.</span><span class="sxs-lookup"><span data-stu-id="83d7c-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="83d7c-233">Если принудительно выполнить импорт, то существующие параметры для конкретного приложения для выбранного формата ER будут очищены, и их необходимо настроить с начала.</span><span class="sxs-lookup"><span data-stu-id="83d7c-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="83d7c-234">Отношение между параметрами конкретного приложения и форматом ER</span><span class="sxs-lookup"><span data-stu-id="83d7c-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="83d7c-235">Связь между форматом ER и его параметрами, зависящими от приложения, устанавливается с помощью уникального идентификационного кода формата ER, зависящего от экземпляра, для формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="83d7c-236">Таким образом, при удалении формата ER из Finance параметры конкретного приложения, настроенные для формата ER, хранятся в текущем экземпляре Finance.</span><span class="sxs-lookup"><span data-stu-id="83d7c-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="83d7c-237">Они могут быть доступны при повторном импорте базового формата ER в данный экземпляр Finance.</span><span class="sxs-lookup"><span data-stu-id="83d7c-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="83d7c-238">Доступ к параметрам, относящимся к приложению, при помощи структуры ER</span><span class="sxs-lookup"><span data-stu-id="83d7c-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="83d7c-239">В предыдущем примере для доступа к параметрам в формате ER, связанных с приложением, используется структура ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="83d7c-240">Такой подход не позволяет ограничить доступ к параметрам конкретного приложения для заданного формата ER.</span><span class="sxs-lookup"><span data-stu-id="83d7c-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="83d7c-241">Если необходимо применять такие ограничения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83d7c-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="83d7c-242">Либо используйте существующий элемент меню **ERSolutionAppSpecificParametersDesigner**, либо реализуйте свой собственный элемент меню **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Страница Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="83d7c-244">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="83d7c-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="83d7c-245">Создайте новую кнопку пункта меню и свяжите ее с соответствующей записью их таблицы **ERSolutionTable**, задав для свойства **Источник данных** значение **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="83d7c-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Страница Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="83d7c-247">Создайте простую кнопку и переопределите метод **Нажато**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="83d7c-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="83d7c-248">Используя этот подход, можно указать уникальный код решения (определяемый через значение **GUID**), чтобы разрешить доступ к параметрам конкретного приложения только определенного формата ER и последующих копий, которые были получены из него.</span><span class="sxs-lookup"><span data-stu-id="83d7c-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="83d7c-249">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="83d7c-249">Additional resources</span></span>

[<span data-ttu-id="83d7c-250">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="83d7c-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="83d7c-251">Настройка форматов ER для использования параметров, указанных для юридического лица</span><span class="sxs-lookup"><span data-stu-id="83d7c-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]