---
title: Повышение производительности решений электронной отчетности за счет добавления параметризованных источников данных ВЫЧИСЛЯЕМЫЕ ПОЛЯ
description: В этой теме объясняется, как повысить производительность решений электронной отчетности (ER), добавляя параметризированные источники данных ВЫЧИСЛЯЕМЫЕ ПОЛЯ.
author: NickSelin
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 299570d6a94b0f9e7ee7cf490d4c1aeeb86d5716
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749521"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="213c4-103">Повышение производительности решений электронной отчетности за счет добавления параметризованных источников данных ВЫЧИСЛЯЕМЫЕ ПОЛЯ</span><span class="sxs-lookup"><span data-stu-id="213c4-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="213c4-104">В этой теме объясняется, как можно получить [трассировку производительности](trace-execution-er-troubleshoot-perf.md) выполняемых форматов [электронной отчетности (ER)](general-electronic-reporting.md), а затем использовать сведения из этих трассировок для повышения производительности путем настройки параметризированного источника данных **Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="213c4-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="213c4-105">В процессе разработки конфигураций электронной отчетности для создания бизнес-документов определяется метод, используемый для извлечения данных из приложения и ввода их в создаваемые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="213c4-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="213c4-106">При разработке параметризированного источника данных электронной отчетности типа **Вычисляемое поле** можно сократить число вызовов базы данных и значительно сократить время и затраты, связанные со сбором сведений о выполнении формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="213c4-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="213c4-107">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="213c4-107">Prerequisites</span></span>

- <span data-ttu-id="213c4-108">Чтобы выполнить примеры в этом разделе, необходимо иметь доступ к одной из следующих [ролей](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="213c4-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="213c4-109">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="213c4-110">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="213c4-111">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="213c4-111">System administrator</span></span>

- <span data-ttu-id="213c4-112">Компания должна иметь значение **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="213c4-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="213c4-113">Выполните действия в [Приложении 1](#appendix1) этой темы, чтобы загрузить компоненты образца решения электронной отчетности Microsoft, необходимые для выполнения примеров из этой темы.</span><span class="sxs-lookup"><span data-stu-id="213c4-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="213c4-114">Следуйте шагам, изложенным в [Приложении 2](#appendix2) данной темы, для настройки минимального набора параметров электронной отчетности, необходимого для использования платформы электронной отчетности, чтобы повысить производительность образца решения электронной отчетности Microsoft.</span><span class="sxs-lookup"><span data-stu-id="213c4-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="213c4-115">Импорт примера решения электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-115">Import the sample ER solution</span></span>

<span data-ttu-id="213c4-116">Представьте, что вы должны разработать решение электронной отчетности для создания нового отчета, отображающего проводки по поставщику.</span><span class="sxs-lookup"><span data-stu-id="213c4-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="213c4-117">В настоящее время на странице **Проводки по поставщику** можно найти проводки для выбранного поставщика (перейдите по пути **Расчеты с поставщиками** \> **Поставщики** \> **Все поставщики**, выберите поставщика, затем на панели операций на вкладке **Поставщик** в группе **Проводки** выберите **Проводки**).</span><span class="sxs-lookup"><span data-stu-id="213c4-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="213c4-118">Однако необходимо иметь вместе все проводки по поставщику в одном электронном документе в формате XML.</span><span class="sxs-lookup"><span data-stu-id="213c4-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="213c4-119">Это решение будет состоять из нескольких конфигураций ER, которые содержат требуемую модель данных, сопоставление моделей и компоненты формата.</span><span class="sxs-lookup"><span data-stu-id="213c4-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="213c4-120">Первым шагом является импорт образца решения электронной отчетности для создания отчета о проводках по поставщику.</span><span class="sxs-lookup"><span data-stu-id="213c4-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="213c4-121">Выполните вход в экземпляр Microsoft Dynamics 365 Finance, который был подготовлен для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="213c4-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="213c4-122">В этой теме вам предстоит создать и изменить конфигурации для демонстрационной компании **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="213c4-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="213c4-123">Убедитесь, что данный поставщик конфигурации был добавлен в ваш экземпляр Finance и отмечен как активный.</span><span class="sxs-lookup"><span data-stu-id="213c4-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="213c4-124">Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="213c4-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="213c4-125">В рабочей области **Электронная отчетность** выберите плитку **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="213c4-126">На странице **Конфигурации** импортируйте конфигурации электронной отчетности, загруженные в качестве необходимого компонента в Finance, в следующем порядке: модель данных, сопоставление моделей, формат.</span><span class="sxs-lookup"><span data-stu-id="213c4-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="213c4-127">Для каждой конфигурации выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="213c4-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="213c4-128">На панели действий выберите пункт **Обмен** \> **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="213c4-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="213c4-129">Выберите **Обзор** и выберите соответствующий файл для конфигурации электронной отчетности в формате XML.</span><span class="sxs-lookup"><span data-stu-id="213c4-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="213c4-130">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-130">Select **OK**.</span></span>

![Импортированные конфигурации на странице конфигураций](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="213c4-132">Проверка примера решения электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="213c4-133">Просмотр сопоставления моделей</span><span class="sxs-lookup"><span data-stu-id="213c4-133">Review the model mapping</span></span>

1. <span data-ttu-id="213c4-134">На странице **Конфигурации** в дереве конфигураций разверните **Модель улучшения производительности** и выберите **Сопоставление улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="213c4-135">В области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="213c4-136">На странице **Сопоставление модели и источника данных** в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="213c4-137">Это сопоставление модели электронной отчетности предназначено для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="213c4-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="213c4-138">Получите список проводок по поставщику, которые хранятся в таблице VendTrans (источник данных **Trans**).</span><span class="sxs-lookup"><span data-stu-id="213c4-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="213c4-139">Для каждой проводки выберите из таблицы VendTable запись поставщика, для которой была разнесена проводка (источник данных **\#Vend**).</span><span class="sxs-lookup"><span data-stu-id="213c4-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="213c4-140">Источник данных **\#Vend** настроен для получения соответствующей записи поставщика с помощью существующего отношения "многие к одному" **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="213c4-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="213c4-141">Сопоставление модели в этой конфигурации реализует базовую модель данных для любого из форматов электронной отчетности, созданных для этой модели и выполняемых в Finance.</span><span class="sxs-lookup"><span data-stu-id="213c4-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="213c4-142">Таким образом, содержимое источника данных **Trans** предоставляется для форматов электронной отчетности, таких как абстрактные источники данных **модели**.</span><span class="sxs-lookup"><span data-stu-id="213c4-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Источник данных Trans на странице конструктора сопоставления модели](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="213c4-144">Закройте страницу **Конструктор сопоставления модели**.</span><span class="sxs-lookup"><span data-stu-id="213c4-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="213c4-145">Закройте страницу **Сопоставление модели и источника данных**.</span><span class="sxs-lookup"><span data-stu-id="213c4-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="213c4-146">Предварительный просмотр формата</span><span class="sxs-lookup"><span data-stu-id="213c4-146">Review format</span></span>

1. <span data-ttu-id="213c4-147">На странице **Конфигурации** в дереве конфигураций разверните **Модель улучшения производительности** и выберите **Формат улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="213c4-148">В области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="213c4-149">На странице **Конструктор формата** на вкладке **Сопоставление** выберите **Свернуть/Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="213c4-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="213c4-150">Разверните элементы **Модель**, **Данные** и **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="213c4-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="213c4-151">Этот формат электронной отчетности предназначен для создания отчета о проводках по поставщику в формате XML.</span><span class="sxs-lookup"><span data-stu-id="213c4-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Источники данных формата и сконфигурированные привязки элементов форматирования на странице конструктора форматов](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="213c4-153">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="213c4-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="213c4-154">Запуск примера решения электронной отчетности для трассировки выполнения</span><span class="sxs-lookup"><span data-stu-id="213c4-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="213c4-155">Представьте, что вы завершили разработку первой версии решения электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="213c4-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="213c4-156">Теперь необходимо проверить решение в вашем экземпляре Finance и проанализировать производительность выполнения.</span><span class="sxs-lookup"><span data-stu-id="213c4-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="213c4-157">Включение трассировки производительности электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="213c4-158">Выберите компанию **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="213c4-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="213c4-159">Следуйте указаниям в разделе [Включение трассировки производительности электронной отчетности](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace), чтобы создать трассировку производительности при выполнении формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="213c4-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Диалоговое окно параметров пользователя](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="213c4-161">Выполнение формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-161">Run the ER format</span></span>

1. <span data-ttu-id="213c4-162">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="213c4-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="213c4-163">На странице **Конфигурации** в дереве конфигураций выберите пункт **Формат улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="213c4-164">В области действий выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="213c4-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="213c4-165">Используйте трассировку производительности для анализа производительности сопоставления моделей</span><span class="sxs-lookup"><span data-stu-id="213c4-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="213c4-166">На странице **Конфигурации** в дереве конфигураций выберите пункт **Сопоставление улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="213c4-167">В области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="213c4-168">На странице **Сопоставления модели** в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="213c4-169">На странице **Конструктор сопоставления модели** в области действий выберите **Трассировка производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="213c4-170">Выберите последнюю созданную трассировку, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="213c4-171">Новые сведения теперь доступны для некоторых элементов источника данных в текущем сопоставлении модели:</span><span class="sxs-lookup"><span data-stu-id="213c4-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="213c4-172">Фактическое время, потраченное на получение данных с использованием источника данных</span><span class="sxs-lookup"><span data-stu-id="213c4-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="213c4-173">То же время, выраженное в процентах от общего времени, затраченного на выполнение всего сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="213c4-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Сведения о времени выполнения на странице конструктора сопоставления моделей](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="213c4-175">Сетка **Статистика производительности** показывает, что источник данных **Trans** обращается к таблице VendTrans один раз.</span><span class="sxs-lookup"><span data-stu-id="213c4-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="213c4-176">Значение **\[265\]\[Q:265\]** источника данных **Trans** указывает на то, что проводки по поставщику 265 были извлечены из таблицы приложения и возвращены в модель данных.</span><span class="sxs-lookup"><span data-stu-id="213c4-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="213c4-177">Сетка **Статистика производительности** также показывает, что сопоставление текущей модели дублирует запросы базы данных во время выполнения источника данных **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="213c4-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="213c4-178">Это дублирование происходит по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="213c4-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="213c4-179">Таблица поставщика вызывается два раза для каждой из 265 прошедших итерацию проводок по поставщику, что дает общее количество вызовов 530:</span><span class="sxs-lookup"><span data-stu-id="213c4-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="213c4-180">Один вызов выполняется для ввода номера счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="213c4-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="213c4-181">Один вызов выполняется для ввода имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="213c4-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="213c4-182">Таблица поставщиков вызывается для каждой итерации проводки по поставщику, даже если выбранные проводки были разнесены только для пяти поставщиков.</span><span class="sxs-lookup"><span data-stu-id="213c4-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="213c4-183">Из 530 вызовов 525 являются дубликатами.</span><span class="sxs-lookup"><span data-stu-id="213c4-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="213c4-184">На следующем рисунке показано полученное сообщение о повторяющихся вызовах (запросах базы данных).</span><span class="sxs-lookup"><span data-stu-id="213c4-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Сообщение о дубликатах запросов базы данных на странице конструктора сопоставления модели](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="213c4-186">Общее время выполнения сопоставления модели (приблизительно восемь секунд); обратите внимание на то, что более 80 процентов (примерно шесть секунд) было потрачено на получение значений из таблицы приложений VendTable.</span><span class="sxs-lookup"><span data-stu-id="213c4-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="213c4-187">Этот процент слишком велик для двух атрибутов пяти поставщиков, в сравнении с объемом информации из таблицы приложения VendTrans.</span><span class="sxs-lookup"><span data-stu-id="213c4-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="213c4-188">Для уменьшения числа вызовов, выполняемых для получения сведений о поставщике для каждой проводки, и для повышения производительности сопоставления моделей можно использовать кэширование для источника данных **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="213c4-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="213c4-189">Источник данных **Trans\\\#Vend** будет кэширован в области текущей проводки источника данных **Trans** во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="213c4-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="213c4-190">При кэшировании источника данных **\#Vend** уменьшается число дубликатов вызовов с 525 до 260, но дублирование не устраняется полностью.</span><span class="sxs-lookup"><span data-stu-id="213c4-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="213c4-191">Для полного устранения дублирования можно настроить новый параметризованный источник данных типа **Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="213c4-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="213c4-192">Улучшите сопоставление модели на основе информации из трассировки выполнения</span><span class="sxs-lookup"><span data-stu-id="213c4-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="213c4-193">Изменение логики сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="213c4-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="213c4-194">Выполните следующие действия, чтобы использовать кэширование и источник данных типа **Вычисляемое поле**, чтобы предотвратить дублирование вызовов к базе данных.</span><span class="sxs-lookup"><span data-stu-id="213c4-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="213c4-195">На странице **Конфигурации** в дереве конфигураций выберите пункт **Сопоставление улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="213c4-196">В области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="213c4-197">На странице **Сопоставления модели** в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="213c4-198">На странице **Конструктор сопоставления моделей** выполните следующие шаги, чтобы добавить источник данных типа **Записи таблицы** для доступа к записям в таблице приложения VendTable:</span><span class="sxs-lookup"><span data-stu-id="213c4-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="213c4-199">В области **Типы источников данных** разверните **Dynamics 365 for Operations** и выберите **Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="213c4-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="213c4-200">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="213c4-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="213c4-201">В диалоговом окне в поле **Имя** введите **Vend**.</span><span class="sxs-lookup"><span data-stu-id="213c4-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="213c4-202">В поле **Таблица** введите **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="213c4-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="213c4-203">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-203">Select **OK**.</span></span>

5. <span data-ttu-id="213c4-204">Можно параметризировать вызовы к источникам данных типа **Вычисляемое поле** только в том случае, если эти источники данных находятся в контейнере.</span><span class="sxs-lookup"><span data-stu-id="213c4-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="213c4-205">Таким образом, необходимо выполнить следующие действия, чтобы добавить источник данных типа **Пустой контейнер** для хранения нового параметризованного источника данных типа **Вычисляемое поле**:</span><span class="sxs-lookup"><span data-stu-id="213c4-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="213c4-206">В области **Типы источников данных** разверните **Общие** и выберите **Пустой контейнер**.</span><span class="sxs-lookup"><span data-stu-id="213c4-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="213c4-207">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="213c4-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="213c4-208">В диалоговом окне в поле **Имя** введите **Box**.</span><span class="sxs-lookup"><span data-stu-id="213c4-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="213c4-209">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-209">Select **OK**.</span></span>

    ![Источник данных Box на странице конструктора сопоставления модели](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="213c4-211">Выполните следующие действия, чтобы добавить параметризованный источник данных типа **Вычисляемое поле**:</span><span class="sxs-lookup"><span data-stu-id="213c4-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="213c4-212">В области **Источники данных** выберите **Box**.</span><span class="sxs-lookup"><span data-stu-id="213c4-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="213c4-213">В области **Типы источников данных** раскройте **Функции** и выберите элемент **Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="213c4-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="213c4-214">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="213c4-214">Select **Add**.</span></span>
    4. <span data-ttu-id="213c4-215">В диалоговом окне в поле **Имя** введите **Vend**.</span><span class="sxs-lookup"><span data-stu-id="213c4-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="213c4-216">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="213c4-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="213c4-217">На странице **Конструктор формул** выберите **Параметры**, чтобы указать параметры, которые должны быть предоставлены при вызове этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="213c4-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="213c4-218">В диалоговом окне **Параметры** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="213c4-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="213c4-219">В поле **Имя** введите **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="213c4-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="213c4-220">В поле **Тип** выберите **String**.</span><span class="sxs-lookup"><span data-stu-id="213c4-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="213c4-221">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-221">Select **OK**.</span></span>
    11. <span data-ttu-id="213c4-222">В поле **Формула** введите **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="213c4-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="213c4-223">Выберите **Сохранить**, затем закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="213c4-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="213c4-224">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="213c4-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="213c4-225">Чтобы пометить добавленный источник данных как кэшируемый во время выполнения, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="213c4-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="213c4-226">В области **Источники данных** выберите **Box\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="213c4-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="213c4-227">Выберите **Кэш**.</span><span class="sxs-lookup"><span data-stu-id="213c4-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="213c4-228">Источник данных **Box\\Vend** будет кэширован в области всех проводок по поставщикам источника данных **Trans** во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="213c4-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="213c4-229">Выполните следующие шаги для обновления вложенного источника данных **Trans\\\#Vend**, чтобы в нем использовался источник данных **Box\\Vend**:</span><span class="sxs-lookup"><span data-stu-id="213c4-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="213c4-230">В области **Источники данных** разверните **Trans**.</span><span class="sxs-lookup"><span data-stu-id="213c4-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="213c4-231">Выберите источник данных **Trans\\\#Vend**, затем выберите **Правка** \> **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="213c4-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="213c4-232">На странице **Конструктор формул** в поле **Формула** введите **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="213c4-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="213c4-233">Выберите **Сохранить**, затем закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="213c4-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="213c4-234">Выберите **ОК**, чтобы завершить изменения в выбранном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="213c4-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="213c4-235">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="213c4-235">Select **Save**.</span></span>

    ![Источник данных Vend на странице конструктора сопоставления модели](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="213c4-237">Закройте страницу **Конструктор сопоставления модели**.</span><span class="sxs-lookup"><span data-stu-id="213c4-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="213c4-238">Закройте страницу **Сопоставления модели**.</span><span class="sxs-lookup"><span data-stu-id="213c4-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="213c4-239">Выполните измененную версию сопоставления модели ER</span><span class="sxs-lookup"><span data-stu-id="213c4-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="213c4-240">На странице **Конфигурации** на экспресс-вкладке **Версии** выберите версию **1.2** конфигурации **Сопоставление улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="213c4-241">Выберите **Изменить статус** \> **Завершено**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="213c4-242">Запуск измененного решения электронной отчетности для трассировки выполнения</span><span class="sxs-lookup"><span data-stu-id="213c4-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="213c4-243">Повторите шаги в разделе [Выполнение формата электронной отчетности](#run-format) ранее в этой теме, чтобы создать новую трассировку производительности.</span><span class="sxs-lookup"><span data-stu-id="213c4-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="213c4-244">Используйте трассировку производительности для анализа корректировок сопоставления моделей</span><span class="sxs-lookup"><span data-stu-id="213c4-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="213c4-245">На странице **Конфигурации** в дереве конфигураций выберите пункт **Сопоставление улучшения производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="213c4-246">В области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="213c4-247">На странице **Сопоставления модели** в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="213c4-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="213c4-248">На странице **Конструктор сопоставления модели** в области действий выберите **Трассировка производительности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="213c4-249">Выберите последнюю созданную трассировку, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="213c4-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="213c4-250">Обратите внимание, что изменения, внесенные в сопоставление модели, исключают повторяющиеся запросы к базе данных.</span><span class="sxs-lookup"><span data-stu-id="213c4-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="213c4-251">Также уменьшилось число обращений к таблицам базы данных и источникам данных для данного сопоставления модели.</span><span class="sxs-lookup"><span data-stu-id="213c4-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Сведения о трассировке на странице 1 конструктора сопоставления модели](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="213c4-253">Общее время выполнения сократилось примерно в 20 раз (с примерно 8 секунд до 400 миллисекунд).</span><span class="sxs-lookup"><span data-stu-id="213c4-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="213c4-254">Поэтому производительность всего решения электронной отчетности улучшилась.</span><span class="sxs-lookup"><span data-stu-id="213c4-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Сведения о трассировке на странице 2 конструктора сопоставления модели](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="213c4-256">Приложение 1. Загрузка компонентов образца решения электронной отчетности Microsoft</span><span class="sxs-lookup"><span data-stu-id="213c4-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="213c4-257">Необходимо загрузить следующие файлы и сохранить их локально.</span><span class="sxs-lookup"><span data-stu-id="213c4-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="213c4-258">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="213c4-258">File</span></span>                                        | <span data-ttu-id="213c4-259">Содержимое</span><span class="sxs-lookup"><span data-stu-id="213c4-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="213c4-260">Модель улучшения производительности.версия.1</span><span class="sxs-lookup"><span data-stu-id="213c4-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="213c4-261">Пример конфигурации модели данных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="213c4-262">Сопоставление улучшения производительности.версия.1.1</span><span class="sxs-lookup"><span data-stu-id="213c4-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="213c4-263">Пример конфигурации сопоставления модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="213c4-264">Формат улучшения производительности.версия.1.1</span><span class="sxs-lookup"><span data-stu-id="213c4-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="213c4-265">Пример конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="213c4-266">Приложение 2. Настройка платформы электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="213c4-267">Прежде чем можно будет начать пользоваться платформой электронной отчетности с целью повышения производительности образца решения электронной отчетности Microsoft, необходимо настроить минимальный набор параметров электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="213c4-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="213c4-268">Настройка параметров ER</span><span class="sxs-lookup"><span data-stu-id="213c4-268">Configure ER parameters</span></span>

1. <span data-ttu-id="213c4-269">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="213c4-270">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="213c4-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="213c4-271">На странице **Параметры электронной отчетности** на вкладке **Общие сведения** задайте для параметра **Включить режим конструктора** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="213c4-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="213c4-272">На вкладке **Вложения** установите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="213c4-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="213c4-273">В поле **Конфигурации** выберите тип **Файл** для компании **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="213c4-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="213c4-274">В полях **Архив заданий**, **Временная**, **Базовый** и **Другие** выберите тип **Файл**.</span><span class="sxs-lookup"><span data-stu-id="213c4-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="213c4-275">Дополнительные сведения о настройке параметров электронной отчетности см. в разделе [Настройка платформы электронной отчетности](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="213c4-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="213c4-276">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="213c4-277">Каждая добавленная конфигурация электронной отчетности помечается как принадлежащая поставщику конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="213c4-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="213c4-278">Для этой цели используется поставщик конфигурации электронной отчетности, который активирован в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="213c4-279">Поэтому перед началом добавления или изменения конфигураций электронной отчетности необходимо активировать поставщика конфигурации электронной отчетности в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="213c4-280">Только владелец конфигурации электронной отчетности может редактировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="213c4-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="213c4-281">Поэтому перед редактированием конфигурации электронной отчетности необходимо активировать соответствующего поставщика конфигурации электронной отчетности в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="213c4-282">Просмотр списка поставщиков конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="213c4-283">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="213c4-284">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите **Поставщики конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="213c4-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="213c4-285">На странице **Таблица поставщиков конфигураций** каждая запись поставщика имеет уникальное имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="213c4-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="213c4-286">Проверьте содержимое данной страницы.</span><span class="sxs-lookup"><span data-stu-id="213c4-286">Review the contents of this page.</span></span> <span data-ttu-id="213c4-287">Если запись для **Litware, Inc.** уже существует, пропустите следующую процедуру, [Добавление нового поставщика конфигурации электронной отчетности](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="213c4-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="213c4-288">Добавление нового поставщика конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="213c4-289">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="213c4-290">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите **Поставщики конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="213c4-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="213c4-291">На странице **Поставщики конфигураций** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="213c4-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="213c4-292">В поле **Имя** введите **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="213c4-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="213c4-293">В поле **Интернет-адрес** введите `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="213c4-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="213c4-294">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="213c4-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="213c4-295">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="213c4-296">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="213c4-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="213c4-297">На странице **Конфигурации локализации** в разделе **Поставщики конфигураций** выберите плитку **Litware, Inc.**, затем выберите **Установить активные**.</span><span class="sxs-lookup"><span data-stu-id="213c4-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="213c4-298">Дополнительные сведения о поставщиках конфигурации электронной отчетности см. в разделе [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="213c4-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="213c4-299">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="213c4-299">Additional resources</span></span>

- [<span data-ttu-id="213c4-300">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="213c4-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="213c4-301">Трассировка выполнения форматов электронной отчетности для устранения неполадок, связанных с производительностью</span><span class="sxs-lookup"><span data-stu-id="213c4-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="213c4-302">Поддержка параметризованных вызовов источников данных электронной отчетности для типа вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="213c4-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]