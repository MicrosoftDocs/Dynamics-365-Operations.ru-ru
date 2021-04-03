---
title: Поддержка параметризованных вызовов источников данных электронной отчетности для типа вычисляемого поля
description: В этом разделе приводятся сведения об использовании типов вычисляемых полей для источников данных электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
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
ms.openlocfilehash: 1c2c13cd3f165826e0d5b5ac901ffa61895301e7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569209"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="a6dd2-103">Поддержка параметризованных вызовов источников данных электронной отчетности для типа вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6dd2-104">В этой теме объясняется, как создать источник данных для электронной отчетности (ER) с помощью типа **Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="a6dd2-105">Этот источник данных может содержать выражение электронной отчетности, которое при исполнении может управляться значениями аргументов параметров, которые настроены в привязке, вызывающей этот источник данных.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="a6dd2-106">Настраивая параметризованные вызовы такого источника данных, можно повторно использовать один источник данных во многих привязках, что позволяет сократить общее число источников данных, которые должны быть настроены в сопоставлениях модели ER или в форматах ER.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="a6dd2-107">Это также упрощает настроенный компонент ER, что снижает затраты на обслуживание и затраты на их использование другими потребителями.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a6dd2-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a6dd2-108">Prerequisites</span></span>
<span data-ttu-id="a6dd2-109">Чтобы завершить примеры из этой темы необходимы следующие возможности доступа:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="a6dd2-110">Доступ к одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="a6dd2-111">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="a6dd2-112">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a6dd2-113">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="a6dd2-113">System administrator</span></span>

- <span data-ttu-id="a6dd2-114">Доступ к службам Regulatory Configuration Services (RCS), которые были настроены для того же клиента, что и Finance and Operations, для одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="a6dd2-115">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="a6dd2-116">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a6dd2-117">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="a6dd2-117">System administrator</span></span>

<span data-ttu-id="a6dd2-118">Кроме того, необходимо загрузить следующие файлы и сохранить их локально.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="a6dd2-119">**Содержание**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-119">**Content**</span></span>                           | <span data-ttu-id="a6dd2-120">**Имя файла**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a6dd2-121">Пример конфигурации модели данных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="a6dd2-122">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="a6dd2-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="a6dd2-123">Пример конфигурации метаданных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="a6dd2-124">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="a6dd2-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="a6dd2-125">Пример конфигурации сопоставления модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="a6dd2-126">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a6dd2-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a6dd2-127">Пример конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="a6dd2-128">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a6dd2-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="a6dd2-129">Вход в экземпляр RCS</span><span class="sxs-lookup"><span data-stu-id="a6dd2-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="a6dd2-130">В этой примере вам предстоит создать конфигурацию для демонстрационной компании Litware, Inc. Сначала в RCS необходимо выполнить шаги в процедуре [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a6dd2-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="a6dd2-131">В панели мониторинга по умолчанию выберите **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="a6dd2-132">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a6dd2-133">Импортируйте загруженные конфигурации в RCS в следующей последовательности: модель данных, метаданные, сопоставление модели, формат.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="a6dd2-134">Выполните следующие шаги для каждой конфигурации ER:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="a6dd2-135">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="a6dd2-136">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a6dd2-137">Выберите **Обзор**, затем выберите требуемую конфигурацию ER в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="a6dd2-138">Выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="a6dd2-139">Предварительный просмотр предоставленного решения ER</span><span class="sxs-lookup"><span data-stu-id="a6dd2-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="a6dd2-140">Предварительный просмотр сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="a6dd2-140">Review model mapping</span></span>

1. <span data-ttu-id="a6dd2-141">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="a6dd2-142">Выберите **Сопоставление для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="a6dd2-143">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-143">Select **Designer**.</span></span>
4. <span data-ttu-id="a6dd2-144">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="a6dd2-145">Это сопоставление модели ER предназначено для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="a6dd2-146">Извлечение списка налоговых кодов (источник данных **Tax**), расположенных в таблице **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="a6dd2-147">Извлечение списка налоговых проводок (источник данных **Trans**), расположенных в таблице **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="a6dd2-148">Группировка списка извлеченных проводок (источник данных **Gr**) по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="a6dd2-149">Расчет для сгруппированных проводок следующих агрегированных значений для налогового кода:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="a6dd2-150">Сумма значений налоговой базы.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="a6dd2-151">Сумма значений налога.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-151">Sum of tax values.</span></span>
            - <span data-ttu-id="a6dd2-152">Минимальное значение примененной налоговой ставки.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="a6dd2-153">Сопоставление модели в этой конфигурации реализует базовую модель данных для любого из форматов ER, созданных для этой модели и выполняемых в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="a6dd2-154">В результате содержимое источников данных **Tax** и **Gr** предоставляется для форматов ER, таких как абстрактные источники данных.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Страница конструктора сопоставления модели, на которой отображаются источники данных Tax и Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="a6dd2-156">Закройте страницу **Конструктор сопоставления модели**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="a6dd2-157">Закройте страницу **Сопоставление модели**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="a6dd2-158">Предварительный просмотр формата</span><span class="sxs-lookup"><span data-stu-id="a6dd2-158">Review format</span></span>

1. <span data-ttu-id="a6dd2-159">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="a6dd2-160">Выберите **Формат для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="a6dd2-161">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-161">Select **Designer**.</span></span> <span data-ttu-id="a6dd2-162">Этот формат ER предназначен для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="a6dd2-163">Создание налоговой декларации в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="a6dd2-164">Представление следующих уровней налогообложения в налоговой декларации: обычный, уменьшенный и нет.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="a6dd2-165">Представление нескольких сведений на каждом уровне налогообложения, имеющем различное количество сведений на каждом уровне.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Страница конструктора форматов](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="a6dd2-167">Выберите **Сопоставление**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="a6dd2-168">Разверните элементы **Модель**, **Данные** и **Сводка**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="a6dd2-169">Вычисляемое поле **Model.Data.Summary.Level** содержит выражение, которое возвращает код уровня налогообложения (**Обычный**, **Пониженный**, **Нет** или **Другой**) в виде текстового значения для любого налогового кода, которое может быть извлечено из источника данных **Model.Data.Summary** во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Страница конструктора форматов, в которой показаны подробные сведения о модели данных для изучения параметризованных вызовов](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="a6dd2-171">Разверните элемент **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="a6dd2-172">Разверните элемент **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="a6dd2-173">Источник данных **Model**.**Data2.Summary2** настроен для группирования сведений проводок источника данных **Model.Data.Summary** по уровню налогообложения (возвращается вычисляемым полем **Model.Data.Summary.Level**) и вычисления агрегированных значений.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Страница конструктора форматов, в которой показаны подробные сведения об источнике данных Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="a6dd2-175">Просмотрите вычисляемые поля **Model**.**Data2.Level1**, **Model**.**Data2.Level2** и **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="a6dd2-176">Эти вычисляемые поля используются для фильтрации списка записей **Model**.**Data2.Summary2** и возврата только тех записей, которые представляют конкретный уровень налогообложения.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="a6dd2-177">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="a6dd2-178">Создание производного формата</span><span class="sxs-lookup"><span data-stu-id="a6dd2-178">Create a derived format</span></span>
<span data-ttu-id="a6dd2-179">Можно улучшить предоставленный формат, добавив одно вычисляемое поле для фильтрации необходимого уровня налогообложения вместо использования существующих трех полей: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** и **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="a6dd2-180">Требуемый уровень налогообложения можно указать в месте, где будет вызвано это новое вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="a6dd2-181">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="a6dd2-182">Выберите **Формат для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="a6dd2-183">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="a6dd2-184">Выберите **Производное от имени: формат для изучения параметризованных вызовов, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="a6dd2-185">В поле **Имя** введите **Формат для изучения параметризованных вызовов (настраиваемый)**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="a6dd2-186">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="a6dd2-187">Настройка параметризованного вычисляемого поля, которое возвращает список записей</span><span class="sxs-lookup"><span data-stu-id="a6dd2-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="a6dd2-188">Начало добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="a6dd2-189">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-189">Select **Designer**.</span></span>
2. <span data-ttu-id="a6dd2-190">Чтобы развернуть все элементы форматирования, выберите **Развернуть/свернуть**/</span><span class="sxs-lookup"><span data-stu-id="a6dd2-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="a6dd2-191">Выберите **Сопоставление**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="a6dd2-192">Разверните элемент **Model**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="a6dd2-193">Выберите элемент **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="a6dd2-194">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-194">Select **Add**.</span></span>
7. <span data-ttu-id="a6dd2-195">Выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="a6dd2-196">В поле **Имя** введите **Уровни**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="a6dd2-197">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="a6dd2-198">Определение параметра для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="a6dd2-199">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="a6dd2-200">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-200">Select **New**.</span></span>
3. <span data-ttu-id="a6dd2-201">В поле **Имя** введите **Уровень налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="a6dd2-202">В поле **Тип** выберите **String**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="a6dd2-203">Для указания типа аргумента параметра могут использоваться только примитивные типы данных.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="a6dd2-204">Таким образом, для этой цели нельзя использовать типы **Список записей**, **Запись** и **Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="a6dd2-205">Максимальное число параметров, которые могут быть указаны для одного вычисляемого поля, равно 8.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Список источников данных параметров](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="a6dd2-207">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-207">Select **OK**.</span></span>

<span data-ttu-id="a6dd2-208">При добавлении этого параметра указывается условие, которое должно выполняться для вызова этого вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="a6dd2-209">При вызове этого вычисляемого поля необходимо указать аргумент параметра **Уровень налогообложения** как значение в формате **String**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="a6dd2-210">Убедитесь, что параметры определены только для тех вычисляемых полей, которые находятся в контейнере (**Список записей**, **Запись** или **Контейнер**).</span><span class="sxs-lookup"><span data-stu-id="a6dd2-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="a6dd2-211">Настроенный параметр доступен в списке источников данных для этого вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="a6dd2-212">Можно добавить параметр в настроенное выражение, выбрав **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Поле источника данных](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="a6dd2-214">Определение выражения для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="a6dd2-215">В поле **Формула** введите:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="a6dd2-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="a6dd2-217">Выберите параметр **Уровень налогообложения** в списке источников данных.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="a6dd2-218">Выберите **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="a6dd2-219">В поле **Формула** завершите выражение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="a6dd2-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Уровень налогообложения')**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="a6dd2-221">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-221">Select **Save**.</span></span>

    ![Сведения о поле источника данных](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="a6dd2-223">Закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="a6dd2-224">Завершение добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="a6dd2-225">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-225">Select **OK**.</span></span>

<span data-ttu-id="a6dd2-226">На странице **Конструктор форматов** настроенное параметризованное вычисляемое поле **Уровни** требует наличия аргумента типа **String**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Развернутый список уровней вычисляемых полей](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="a6dd2-228">Использование настроенного вычисляемого поля для привязки элементов форматирования</span><span class="sxs-lookup"><span data-stu-id="a6dd2-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="a6dd2-229">Выберите **Model.Data2.Levels**, чтобы выбрать настроенное вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="a6dd2-230">Выберите элемент форматирования **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="a6dd2-231">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-231">Select **Bind**.</span></span>
4. <span data-ttu-id="a6dd2-232">Выберите **Да**, чтобы подтвердить замену текущего источника данных, **Level1**, новым источником данных, **Levels**, во всех вложенных элементах форматирования выбранного элемента форматирования.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="a6dd2-233">Примененная привязка была создана в виде вызова параметризованного вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="a6dd2-234">По умолчанию имя связанного элемента форматирования используется в качестве аргумента для параметризованного вычисляемого поля при следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="a6dd2-235">В вычисляемом поле настроено использование одного параметра.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="a6dd2-236">Тип данных этого параметра определен как **String**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="a6dd2-237">Если имя связанного элемента форматирования не заполнено, в применяемой привязке используется имя источника данных этого элемента.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="a6dd2-238">Выберите элемент форматирования **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="a6dd2-239">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-239">Select **Bind**.</span></span>
7. <span data-ttu-id="a6dd2-240">Выберите **Да**, чтобы подтвердить замену текущего источника данных, **Level2**, новым источником данных, **Levels**, во всех вложенных элементах форматирования в выбранном элементе форматирования.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="a6dd2-241">Выберите элемент форматирования **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="a6dd2-242">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-242">Select **Bind**.</span></span>
10. <span data-ttu-id="a6dd2-243">Выберите **Да**, чтобы подтвердить замену текущего источника данных, **Level3**, новым источником данных, **Levels**, во всех вложенных элементах форматирования в выбранном элементе форматирования.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="a6dd2-244">При указании аргумента параметризованного вычисляемого поля для элемента XML, представляющего уровень налогообложения ( например, **Model.Data2.Levels("Пониженный")** как текстовое значение), нет необходимости выполнять те же действия для вложенных XML-атрибутов — их привязки автоматически наследуют значение аргумента, определенного на родительском уровне (**Model.Data2.Levels.aggregated.Base**, а не **Model.Data2.Levels("Пониженный").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="a6dd2-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="a6dd2-245">Рекуррентные вызовы любого параметризованного вычисляемого поля не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="a6dd2-246">Можно выбрать **Изменить формулу** и изменить применяемый по умолчанию аргумент параметризованного вычисляемого поля в выбранной привязке.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="a6dd2-247">Если этот аргумент отсутствует, он может вызвать ошибки во время выполнения — пользователи получают уведомление о такой ситуации, когда проверяется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Уведомление о предупреждении проверки](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="a6dd2-249">Настройка параметризованного вычисляемого поля для возвращения записи</span><span class="sxs-lookup"><span data-stu-id="a6dd2-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="a6dd2-250">Когда параметризованное вычисляемое поле возвращает запись, необходимо обеспечить привязку отдельных полей данной записи к элементам форматирования.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="a6dd2-251">В таких случаях родительская привязка, содержащая значение аргумента для вызова параметризованного вычисляемого поля, не будет представлена — это значение должно быть определено в привязке одного поля записи.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="a6dd2-252">Начало добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="a6dd2-253">Выберите элемент **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="a6dd2-254">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-254">Select **Add**.</span></span>
3. <span data-ttu-id="a6dd2-255">Выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="a6dd2-256">В поле **Имя** введите **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="a6dd2-257">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="a6dd2-258">Определение параметра для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="a6dd2-259">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="a6dd2-260">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-260">Select **New**.</span></span>
3. <span data-ttu-id="a6dd2-261">В поле **Имя** введите **Уровень налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="a6dd2-262">В поле **Тип** выберите **String**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="a6dd2-263">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="a6dd2-264">Определение выражения для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="a6dd2-265">В поле **Формула** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="a6dd2-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="a6dd2-267">Выберите параметр **Уровень налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="a6dd2-268">Выберите **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="a6dd2-269">В поле **Формула** добавьте **'Уровень налогообложения'))** к тому, что было введено на шаге 1, чтобы завершить выражение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="a6dd2-270">**FIRSTORNULL(\@.Levels('Уровень налогообложения'))**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="a6dd2-271">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-271">Select **Save**.</span></span>
6. <span data-ttu-id="a6dd2-272">Закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="a6dd2-273">Завершение добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="a6dd2-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="a6dd2-274">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="a6dd2-275">Использование настроенного вычисляемого поля для привязки элементов форматирования</span><span class="sxs-lookup"><span data-stu-id="a6dd2-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="a6dd2-276">Разверните **Model.Data2.LevelRecord**, чтобы выбрать настроенное вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="a6dd2-277">Разверните контейнер **Model.Data2.LevelRecord.aggregated** настроенного вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="a6dd2-278">Выберите поле **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="a6dd2-279">Выберите элемент форматирования **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="a6dd2-280">Выберите **Отменить связь**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="a6dd2-281">Выберите элемент форматирования **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="a6dd2-282">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-282">Select **Bind**.</span></span>
8. <span data-ttu-id="a6dd2-283">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="a6dd2-284">Измените выражение на **Model.Data2.LevelRecord("Нет").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Обновленное выражение](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="a6dd2-286">Удаление вычисляемых полей, которые не используются</span><span class="sxs-lookup"><span data-stu-id="a6dd2-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="a6dd2-287">Выберите **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="a6dd2-288">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-288">Select **Delete**.</span></span>
3. <span data-ttu-id="a6dd2-289">Выберите **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="a6dd2-290">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-290">Select **Delete**.</span></span>
5. <span data-ttu-id="a6dd2-291">Выберите **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="a6dd2-292">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-292">Select **Delete**.</span></span>
7. <span data-ttu-id="a6dd2-293">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="a6dd2-294">Вы повторно использовали одно и то же вычисляемое поле **Model.Data2.Levels** несколько раз в привязках формата.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="a6dd2-295">Гораздо проще использовать и сопровождать одно вычисляемое поле вместо того, чтобы делать это для нескольких аналогичных полей.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="a6dd2-296">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="a6dd2-297">Завершение измененной версии производного формата</span><span class="sxs-lookup"><span data-stu-id="a6dd2-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="a6dd2-298">На экспресс-вкладке **Версии** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="a6dd2-299">Выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="a6dd2-300">Экспорт завершенной версии производного формата</span><span class="sxs-lookup"><span data-stu-id="a6dd2-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="a6dd2-301">Выберите формат **Формат для изучения параметризованных вызовов (настраиваемый)** в дереве конфигураций.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="a6dd2-302">На экспресс-вкладке **Версии** выберите завершенную версию 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="a6dd2-303">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="a6dd2-304">Выберите **Экспорт в виде XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="a6dd2-305">Сохраните загруженную конфигурацию локально, в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="a6dd2-306">Проверка форматов ER</span><span class="sxs-lookup"><span data-stu-id="a6dd2-306">Test ER formats</span></span> 
<span data-ttu-id="a6dd2-307">Можно выполнить исходный и улучшенный форматы электронной отчетности, чтобы убедиться, что настроенные параметризованные вычисляемые поля работают правильно.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="a6dd2-308">Импорт конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a6dd2-308">Import ER configurations</span></span>
<span data-ttu-id="a6dd2-309">Можно импортировать проверенные конфигурации из RCS, используя репозиторий ER типа **RCS**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="a6dd2-310">Если вы уже выполнили эти шаги в разделе [Импорт конфигураций электронной отчетности (ER) из служб нормативных конфигураций (RCS)](rcs-download-configurations.md), используйте настроенный репозиторий ER, чтобы импортировать конфигурации, описанные ранее в этом разделе, в вашу среду.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="a6dd2-311">В противном случае выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="a6dd2-312">Выберите компанию **DEMF** и на панели мониторинга по умолчанию выберите **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="a6dd2-313">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a6dd2-314">Импортируйте конфигурации из центра загрузки Майкрософт в следующей последовательности: модель данных, сопоставление модели, формат.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="a6dd2-315">Выполните следующие шаги для каждой конфигурации ER:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="a6dd2-316">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="a6dd2-317">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a6dd2-318">Выберите **Обзор**, чтобы выбрать требуемую конфигурацию ER в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="a6dd2-319">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-319">Select **OK**.</span></span>

4. <span data-ttu-id="a6dd2-320">Импортируйте экспортированную из RCS завершенную версию 1.1.1 формата **Формат для изучения параметризованных вызовов (настраиваемый)**:</span><span class="sxs-lookup"><span data-stu-id="a6dd2-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="a6dd2-321">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="a6dd2-322">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a6dd2-323">Выберите **Обзор**, чтобы выбрать локально сохраненный файл **Формат для изучения параметризованных вызовов (настраиваемый)** в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="a6dd2-324">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="a6dd2-325">Выполнение форматов ER</span><span class="sxs-lookup"><span data-stu-id="a6dd2-325">Run ER formats</span></span>

1. <span data-ttu-id="a6dd2-326">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="a6dd2-327">Выберите **Формат для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="a6dd2-328">Выберите **Выполнить** на самой верхней ленте.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="a6dd2-329">Сохраните локально созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="a6dd2-330">Выберите элемент **Формат для изучения параметризованных вызовов (настраиваемый)**.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="a6dd2-331">Выберите **Выполнить** на самой верхней ленте.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="a6dd2-332">Сохраните созданные выходные данные локально.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="a6dd2-333">Сравните содержимое созданных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6dd2-334">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a6dd2-334">Additional resources</span></span>

- [<span data-ttu-id="a6dd2-335">Конструктор формул в электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="a6dd2-336">Повышение производительности решений электронной отчетности за счет добавления параметризованных источников данных ВЫЧИСЛЯЕМЫЕ ПОЛЯ</span><span class="sxs-lookup"><span data-stu-id="a6dd2-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]