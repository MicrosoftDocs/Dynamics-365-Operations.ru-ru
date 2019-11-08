---
title: Поддержка параметризованных вызовов источников данных электронной отчетности для типа вычисляемого поля
description: В этом разделе приводятся сведения об использовании типов вычисляемых полей для источников данных электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550092"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="5585c-103">Поддержка параметризованных вызовов источников данных электронной отчетности для типа вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5585c-104">В этой теме объясняется, как создать источник данных для электронной отчетности (ER) с помощью типа **Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="5585c-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="5585c-105">Этот источник данных может содержать выражение электронной отчетности, которое при исполнении может управляться значениями аргументов параметров, которые настроены в привязке, вызывающей этот источник данных.</span><span class="sxs-lookup"><span data-stu-id="5585c-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="5585c-106">Настраивая параметризованные вызовы такого источника данных, можно повторно использовать один источник данных во многих привязках, что позволяет сократить общее число источников данных, которые должны быть настроены в сопоставлениях модели ER или в форматах ER.</span><span class="sxs-lookup"><span data-stu-id="5585c-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="5585c-107">Это также упрощает настроенный компонент ER, что снижает затраты на обслуживание и затраты на их использование другими потребителями.</span><span class="sxs-lookup"><span data-stu-id="5585c-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5585c-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="5585c-108">Prerequisites</span></span>
<span data-ttu-id="5585c-109">Чтобы завершить примеры из этой темы необходимы следующие возможности доступа:</span><span class="sxs-lookup"><span data-stu-id="5585c-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="5585c-110">Доступ к одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="5585c-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="5585c-111">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="5585c-112">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5585c-113">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="5585c-113">System administrator</span></span>

- <span data-ttu-id="5585c-114">Доступ к службам Regulatory Configuration Service (RCS), которые были настроены для того же клиента, что и Finance and Operations, для одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="5585c-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="5585c-115">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="5585c-116">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5585c-117">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="5585c-117">System administrator</span></span>

<span data-ttu-id="5585c-118">С помощью [центра загрузки Microsoft](https://go.microsoft.com/fwlink/?linkid=874684) загрузите сжатый файл (ZIP) **Поддержка параметризованных вызовов источников данных электронной отчетности для типа вычисляемого поля**.</span><span class="sxs-lookup"><span data-stu-id="5585c-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="5585c-119">Он содержит следующие конфигурации ER, которые необходимо извлечь и сохранить локально.</span><span class="sxs-lookup"><span data-stu-id="5585c-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="5585c-120">**Содержание**</span><span class="sxs-lookup"><span data-stu-id="5585c-120">**Content**</span></span>                           | <span data-ttu-id="5585c-121">**Имя файла**</span><span class="sxs-lookup"><span data-stu-id="5585c-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5585c-122">Пример конфигурации модели данных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="5585c-123">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="5585c-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="5585c-124">Пример конфигурации метаданных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="5585c-125">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="5585c-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="5585c-126">Пример конфигурации сопоставления модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="5585c-127">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="5585c-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="5585c-128">Пример конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-128">Sample ER format configuration</span></span>        | <span data-ttu-id="5585c-129">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="5585c-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="5585c-130">Вход в экземпляр RCS</span><span class="sxs-lookup"><span data-stu-id="5585c-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="5585c-131">В этой примере вам предстоит создать конфигурацию для демонстрационной компании Litware, Inc. Сначала в RCS необходимо выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5585c-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="5585c-132">В панели мониторинга по умолчанию выберите **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="5585c-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="5585c-133">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5585c-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="5585c-134">Импортируйте загруженные конфигурации в RCS в следующей последовательности: модель данных, метаданные, сопоставление модели, формат.</span><span class="sxs-lookup"><span data-stu-id="5585c-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="5585c-135">Выполните следующие шаги для каждой конфигурации ER:</span><span class="sxs-lookup"><span data-stu-id="5585c-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="5585c-136">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="5585c-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5585c-137">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="5585c-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5585c-138">Выберите **Обзор**, затем выберите требуемую конфигурацию ER в формате XML.</span><span class="sxs-lookup"><span data-stu-id="5585c-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="5585c-139">Выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="5585c-140">Предварительный просмотр предоставленного решения ER</span><span class="sxs-lookup"><span data-stu-id="5585c-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="5585c-141">Предварительный просмотр сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="5585c-141">Review model mapping</span></span>

1. <span data-ttu-id="5585c-142">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5585c-143">Выберите **Сопоставление для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5585c-144">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="5585c-144">Select **Designer**.</span></span>
4. <span data-ttu-id="5585c-145">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="5585c-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="5585c-146">Это сопоставление модели ER предназначено для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="5585c-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="5585c-147">Извлечение списка налоговых кодов (источник данных **Tax**), расположенных в таблице **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="5585c-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="5585c-148">Извлечение списка налоговых проводок (источник данных **Trans**), расположенных в таблице **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="5585c-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="5585c-149">Группировка списка извлеченных проводок (источник данных **Gr**) по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="5585c-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="5585c-150">Расчет для сгруппированных проводок следующих агрегированных значений для налогового кода:</span><span class="sxs-lookup"><span data-stu-id="5585c-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="5585c-151">Сумма значений налоговой базы.</span><span class="sxs-lookup"><span data-stu-id="5585c-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="5585c-152">Сумма значений налога.</span><span class="sxs-lookup"><span data-stu-id="5585c-152">Sum of tax values.</span></span>
        - <span data-ttu-id="5585c-153">Минимальное значение примененной налоговой ставки.</span><span class="sxs-lookup"><span data-stu-id="5585c-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="5585c-154">Сопоставление модели в этой конфигурации реализует базовую модель данных для любого из форматов ER, созданных для этой модели и выполняемых в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5585c-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="5585c-155">В результате содержимое источников данных **Tax** и **Gr** предоставляется для форматов ER, таких как абстрактные источники данных.</span><span class="sxs-lookup"><span data-stu-id="5585c-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Страница конструктора сопоставления модели, на которой отображаются источники данных Tax и Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="5585c-157">Закройте страницу **Конструктор сопоставления модели**.</span><span class="sxs-lookup"><span data-stu-id="5585c-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="5585c-158">Закройте страницу **Сопоставление модели**.</span><span class="sxs-lookup"><span data-stu-id="5585c-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="5585c-159">Предварительный просмотр формата</span><span class="sxs-lookup"><span data-stu-id="5585c-159">Review format</span></span>

1. <span data-ttu-id="5585c-160">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5585c-161">Выберите **Формат для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5585c-162">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="5585c-162">Select **Designer**.</span></span> <span data-ttu-id="5585c-163">Этот формат ER предназначен для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="5585c-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="5585c-164">Создание налоговой декларации в формате XML.</span><span class="sxs-lookup"><span data-stu-id="5585c-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="5585c-165">Представление следующих уровней налогообложения в налоговой декларации: обычный, уменьшенный и нет.</span><span class="sxs-lookup"><span data-stu-id="5585c-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="5585c-166">Представление нескольких сведений на каждом уровне налогообложения, имеющем различное количество сведений на каждом уровне.</span><span class="sxs-lookup"><span data-stu-id="5585c-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Страница конструктора форматов](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="5585c-168">Выберите **Сопоставление**.</span><span class="sxs-lookup"><span data-stu-id="5585c-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="5585c-169">Разверните элементы **Модель**, **Данные** и **Сводка**.</span><span class="sxs-lookup"><span data-stu-id="5585c-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="5585c-170">Вычисляемое поле **Model.Data.Summary.Level** содержит выражение, которое возвращает код уровня налогообложения (**Обычный**, **Пониженный**, **Нет** или **Другой**) в виде текстового значения для любого налогового кода, которое может быть извлечено из источника данных **Model.Data.Summary** во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="5585c-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Страница конструктора форматов, в которой показаны подробные сведения о модели данных для изучения параметризованных вызовов](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="5585c-172">Разверните элемент **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="5585c-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="5585c-173">Разверните элемент **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="5585c-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="5585c-174">Источник данных **Model**.**Data2.Summary2** настроен для группирования сведений проводок источника данных **Model.Data.Summary** по уровню налогообложения (возвращается вычисляемым полем **Model.Data.Summary.Level**) и вычисления агрегированных значений.</span><span class="sxs-lookup"><span data-stu-id="5585c-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Страница конструктора форматов, в которой показаны подробные сведения об источнике данных Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="5585c-176">Просмотрите вычисляемые поля **Model**.**Data2.Level1**, **Model**.**Data2.Level2** и **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="5585c-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="5585c-177">Эти вычисляемые поля используются для фильтрации списка записей **Model**.**Data2.Summary2** и возврата только тех записей, которые представляют конкретный уровень налогообложения.</span><span class="sxs-lookup"><span data-stu-id="5585c-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="5585c-178">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="5585c-179">Создание производного формата</span><span class="sxs-lookup"><span data-stu-id="5585c-179">Create a derived format</span></span>
<span data-ttu-id="5585c-180">Можно улучшить предоставленный формат, добавив одно вычисляемое поле для фильтрации необходимого уровня налогообложения вместо использования существующих трех полей: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** и **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="5585c-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="5585c-181">Требуемый уровень налогообложения можно указать в месте, где будет вызвано это новое вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="5585c-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="5585c-182">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5585c-183">Выберите **Формат для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5585c-184">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="5585c-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="5585c-185">Выберите **Производное от имени: формат для изучения параметризованных вызовов, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="5585c-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="5585c-186">В поле **Имя** введите **Формат для изучения параметризованных вызовов (настраиваемый)**.</span><span class="sxs-lookup"><span data-stu-id="5585c-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="5585c-187">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="5585c-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="5585c-188">Настройка параметризованного вычисляемого поля, которое возвращает список записей</span><span class="sxs-lookup"><span data-stu-id="5585c-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="5585c-189">Начало добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="5585c-190">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="5585c-190">Select **Designer**.</span></span>
2. <span data-ttu-id="5585c-191">Чтобы развернуть все элементы форматирования, выберите **Развернуть/свернуть**/</span><span class="sxs-lookup"><span data-stu-id="5585c-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="5585c-192">Выберите **Сопоставление**.</span><span class="sxs-lookup"><span data-stu-id="5585c-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="5585c-193">Разверните элемент **Model**.</span><span class="sxs-lookup"><span data-stu-id="5585c-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="5585c-194">Выберите элемент **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="5585c-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="5585c-195">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-195">Select **Add**.</span></span>
7. <span data-ttu-id="5585c-196">Выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="5585c-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="5585c-197">В поле **Имя** введите **Уровни**.</span><span class="sxs-lookup"><span data-stu-id="5585c-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="5585c-198">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="5585c-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="5585c-199">Определение параметра для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="5585c-200">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="5585c-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="5585c-201">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5585c-201">Select **New**.</span></span>
3. <span data-ttu-id="5585c-202">В поле **Имя** введите **Уровень налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="5585c-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="5585c-203">В поле **Тип** выберите **String**.</span><span class="sxs-lookup"><span data-stu-id="5585c-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="5585c-204">Для указания типа аргумента параметра могут использоваться только примитивные типы данных.</span><span class="sxs-lookup"><span data-stu-id="5585c-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="5585c-205">Таким образом, для этой цели нельзя использовать типы **Список записей**, **Запись** и **Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="5585c-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="5585c-206">Максимальное число параметров, которые могут быть указаны для одного вычисляемого поля, равно 8.</span><span class="sxs-lookup"><span data-stu-id="5585c-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Список источников данных параметров](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="5585c-208">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-208">Select **OK**.</span></span>

<span data-ttu-id="5585c-209">При добавлении этого параметра указывается условие, которое должно выполняться для вызова этого вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="5585c-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="5585c-210">При вызове этого вычисляемого поля необходимо указать аргумент параметра **Уровень налогообложения** как значение в формате **String**.</span><span class="sxs-lookup"><span data-stu-id="5585c-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="5585c-211">Убедитесь, что параметры определены только для тех вычисляемых полей, которые находятся в контейнере (**Список записей**, **Запись** или **Контейнер**).</span><span class="sxs-lookup"><span data-stu-id="5585c-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="5585c-212">Настроенный параметр доступен в списке источников данных для этого вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="5585c-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="5585c-213">Можно добавить параметр в настроенное выражение, выбрав **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="5585c-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Поле источника данных](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="5585c-215">Определение выражения для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="5585c-216">В поле **Формула** введите:</span><span class="sxs-lookup"><span data-stu-id="5585c-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="5585c-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="5585c-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="5585c-218">Выберите параметр **Уровень налогообложения** в списке источников данных.</span><span class="sxs-lookup"><span data-stu-id="5585c-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="5585c-219">Выберите **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="5585c-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="5585c-220">В поле **Формула** завершите выражение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5585c-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="5585c-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Уровень налогообложения'**</span><span class="sxs-lookup"><span data-stu-id="5585c-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="5585c-222">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-222">Select **Save**.</span></span>

    ![Сведения о поле источника данных](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="5585c-224">Закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="5585c-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="5585c-225">Завершение добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="5585c-226">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-226">Select **OK**.</span></span>

<span data-ttu-id="5585c-227">На странице **Конструктор форматов** настроенное параметризованное вычисляемое поле **Уровни** требует наличия аргумента типа **String**.</span><span class="sxs-lookup"><span data-stu-id="5585c-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Развернутый список уровней вычисляемых полей](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="5585c-229">Использование настроенного вычисляемого поля для привязки элементов форматирования</span><span class="sxs-lookup"><span data-stu-id="5585c-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="5585c-230">Выберите **Model.Data2.Levels**, чтобы выбрать настроенное вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="5585c-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="5585c-231">Выберите элемент форматирования **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="5585c-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="5585c-232">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="5585c-232">Select **Bind**.</span></span>
4. <span data-ttu-id="5585c-233">Выберите **Да**, чтобы подтвердить замену текущего источника данных, **Level1**, новым источником данных, **Levels**, во всех вложенных элементах форматирования выбранного элемента форматирования.</span><span class="sxs-lookup"><span data-stu-id="5585c-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="5585c-234">Примененная привязка была создана в виде вызова параметризованного вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="5585c-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="5585c-235">По умолчанию имя связанного элемента форматирования используется в качестве аргумента для параметризованного вычисляемого поля при следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="5585c-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="5585c-236">В вычисляемом поле настроено использование одного параметра.</span><span class="sxs-lookup"><span data-stu-id="5585c-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="5585c-237">Тип данных этого параметра определен как **String**.</span><span class="sxs-lookup"><span data-stu-id="5585c-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="5585c-238">Если имя связанного элемента форматирования не заполнено, в применяемой привязке используется имя источника данных этого элемента.</span><span class="sxs-lookup"><span data-stu-id="5585c-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="5585c-239">Выберите элемент форматирования **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="5585c-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="5585c-240">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="5585c-240">Select **Bind**.</span></span>
7. <span data-ttu-id="5585c-241">Выберите **Да**, чтобы подтвердить замену текущего источника данных, **Level2**, новым источником данных, **Levels**, во всех вложенных элементах форматирования в выбранном элементе форматирования.</span><span class="sxs-lookup"><span data-stu-id="5585c-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="5585c-242">Выберите элемент форматирования **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="5585c-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="5585c-243">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="5585c-243">Select **Bind**.</span></span>
10. <span data-ttu-id="5585c-244">Выберите **Да**, чтобы подтвердить замену текущего источника данных, **Level3**, новым источником данных, **Levels**, во всех вложенных элементах форматирования в выбранном элементе форматирования.</span><span class="sxs-lookup"><span data-stu-id="5585c-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="5585c-245">При указании аргумента параметризованного вычисляемого поля для элемента XML, представляющего уровень налогообложения ( например, **Model.Data2.Levels("Пониженный")** как текстовое значение), нет необходимости выполнять те же действия для вложенных XML-атрибутов — их привязки автоматически наследуют значение аргумента, определенного на родительском уровне (**Model.Data2.Levels.aggregated.Base**, а не **Model.Data2.Levels("Пониженный").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="5585c-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="5585c-246">Рекуррентные вызовы любого параметризованного вычисляемого поля не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5585c-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="5585c-247">Можно выбрать **Изменить формулу** и изменить применяемый по умолчанию аргумент параметризованного вычисляемого поля в выбранной привязке.</span><span class="sxs-lookup"><span data-stu-id="5585c-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="5585c-248">Если этот аргумент отсутствует, он может вызвать ошибки во время выполнения — пользователи получают уведомление о такой ситуации, когда проверяется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="5585c-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Уведомление о предупреждении проверки](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="5585c-250">Настройка параметризованного вычисляемого поля для возвращения записи</span><span class="sxs-lookup"><span data-stu-id="5585c-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="5585c-251">Когда параметризованное вычисляемое поле возвращает запись, необходимо обеспечить привязку отдельных полей данной записи к элементам форматирования.</span><span class="sxs-lookup"><span data-stu-id="5585c-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="5585c-252">В таких случаях родительская привязка, содержащая значение аргумента для вызова параметризованного вычисляемого поля, не будет представлена — это значение должно быть определено в привязке одного поля записи.</span><span class="sxs-lookup"><span data-stu-id="5585c-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="5585c-253">Начало добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="5585c-254">Выберите элемент **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="5585c-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="5585c-255">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-255">Select **Add**.</span></span>
3. <span data-ttu-id="5585c-256">Выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="5585c-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="5585c-257">В поле **Имя** введите **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="5585c-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="5585c-258">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="5585c-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="5585c-259">Определение параметра для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="5585c-260">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="5585c-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="5585c-261">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5585c-261">Select **New**.</span></span>
3. <span data-ttu-id="5585c-262">В поле **Имя** введите **Уровень налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="5585c-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="5585c-263">В поле **Тип** выберите **String**.</span><span class="sxs-lookup"><span data-stu-id="5585c-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="5585c-264">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="5585c-265">Определение выражения для добавления вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="5585c-266">В поле **Формула** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="5585c-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="5585c-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="5585c-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="5585c-268">Выберите параметр **Уровень налогообложения**.</span><span class="sxs-lookup"><span data-stu-id="5585c-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="5585c-269">Выберите **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="5585c-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="5585c-270">В поле **Формула** добавьте **'Уровень налогообложения'))** к тому, что было введено на шаге 1, чтобы завершить выражение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5585c-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="5585c-271">**FIRSTORNULL(\@.Levels('Уровень налогообложения'))**</span><span class="sxs-lookup"><span data-stu-id="5585c-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="5585c-272">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-272">Select **Save**.</span></span>
6. <span data-ttu-id="5585c-273">Закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="5585c-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="5585c-274">Завершение добавления нового вычисляемого поля</span><span class="sxs-lookup"><span data-stu-id="5585c-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="5585c-275">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="5585c-276">Использование настроенного вычисляемого поля для привязки элементов форматирования</span><span class="sxs-lookup"><span data-stu-id="5585c-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="5585c-277">Разверните **Model.Data2.LevelRecord**, чтобы выбрать настроенное вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="5585c-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="5585c-278">Разверните контейнер **Model.Data2.LevelRecord.aggregated** настроенного вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="5585c-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="5585c-279">Выберите поле **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="5585c-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="5585c-280">Выберите элемент форматирования **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="5585c-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="5585c-281">Выберите **Отменить связь**.</span><span class="sxs-lookup"><span data-stu-id="5585c-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="5585c-282">Выберите элемент форматирования **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="5585c-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="5585c-283">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="5585c-283">Select **Bind**.</span></span>
8. <span data-ttu-id="5585c-284">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="5585c-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="5585c-285">Измените выражение на **Model.Data2.LevelRecord("Нет").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="5585c-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Обновленное выражение](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="5585c-287">Удаление вычисляемых полей, которые не используются</span><span class="sxs-lookup"><span data-stu-id="5585c-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="5585c-288">Выберите **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="5585c-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="5585c-289">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-289">Select **Delete**.</span></span>
3. <span data-ttu-id="5585c-290">Выберите **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="5585c-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="5585c-291">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-291">Select **Delete**.</span></span>
5. <span data-ttu-id="5585c-292">Выберите **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="5585c-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="5585c-293">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-293">Select **Delete**.</span></span>
7. <span data-ttu-id="5585c-294">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5585c-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5585c-295">Вы повторно использовали одно и то же вычисляемое поле **Model.Data2.Levels** несколько раз в привязках формата.</span><span class="sxs-lookup"><span data-stu-id="5585c-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="5585c-296">Гораздо проще использовать и сопровождать одно вычисляемое поле вместо того, чтобы делать это для нескольких аналогичных полей.</span><span class="sxs-lookup"><span data-stu-id="5585c-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="5585c-297">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="5585c-298">Завершение измененной версии производного формата</span><span class="sxs-lookup"><span data-stu-id="5585c-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="5585c-299">На экспресс-вкладке **Версии** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="5585c-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="5585c-300">Выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="5585c-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="5585c-301">Экспорт завершенной версии производного формата</span><span class="sxs-lookup"><span data-stu-id="5585c-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="5585c-302">Выберите формат **Формат для изучения параметризованных вызовов (настраиваемый)** в дереве конфигураций.</span><span class="sxs-lookup"><span data-stu-id="5585c-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="5585c-303">На экспресс-вкладке **Версии** выберите завершенную версию 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="5585c-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="5585c-304">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="5585c-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="5585c-305">Выберите **Экспорт в виде XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="5585c-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="5585c-306">Сохраните загруженную конфигурацию локально, в формате XML.</span><span class="sxs-lookup"><span data-stu-id="5585c-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="5585c-307">Проверка форматов ER</span><span class="sxs-lookup"><span data-stu-id="5585c-307">Test ER formats</span></span> 
<span data-ttu-id="5585c-308">Можно выполнить исходный и улучшенный форматы электронной отчетности, чтобы убедиться, что настроенные параметризованные вычисляемые поля работают правильно.</span><span class="sxs-lookup"><span data-stu-id="5585c-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="5585c-309">Импорт конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-309">Import ER configurations</span></span>
<span data-ttu-id="5585c-310">Можно импортировать проверенные конфигурации из RCS, используя репозиторий ER типа **RCS**.</span><span class="sxs-lookup"><span data-stu-id="5585c-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="5585c-311">Если вы уже выполнили эти шаги в разделе [Импорт конфигураций электронной отчетности из служб нормативных конфигураций (RCS)](rcs-download-configurations.md), используйте настроенный репозиторий ER, чтобы импортировать конфигурации, описанные ранее в этом разделе, в вашу среду.</span><span class="sxs-lookup"><span data-stu-id="5585c-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="5585c-312">В противном случае выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5585c-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="5585c-313">Выберите компанию **DEMF** и на панели мониторинга по умолчанию выберите **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="5585c-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="5585c-314">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5585c-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="5585c-315">Импортируйте конфигурации из центра загрузки Майкрософт в следующей последовательности: модель данных, сопоставление модели, формат.</span><span class="sxs-lookup"><span data-stu-id="5585c-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="5585c-316">Выполните следующие шаги для каждой конфигурации ER:</span><span class="sxs-lookup"><span data-stu-id="5585c-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="5585c-317">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="5585c-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5585c-318">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="5585c-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5585c-319">Выберите **Обзор**, чтобы выбрать требуемую конфигурацию ER в формате XML.</span><span class="sxs-lookup"><span data-stu-id="5585c-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="5585c-320">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-320">Select **OK**.</span></span>

4. <span data-ttu-id="5585c-321">Импортируйте экспортированную из RCS завершенную версию 1.1.1 формата **Формат для изучения параметризованных вызовов (настраиваемый)**:</span><span class="sxs-lookup"><span data-stu-id="5585c-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="5585c-322">Выберите **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="5585c-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="5585c-323">Выберите **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="5585c-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="5585c-324">Выберите **Обзор**, чтобы выбрать локально сохраненный файл **Формат для изучения параметризованных вызовов (настраиваемый)** в формате XML.</span><span class="sxs-lookup"><span data-stu-id="5585c-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="5585c-325">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5585c-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="5585c-326">Выполнение форматов ER</span><span class="sxs-lookup"><span data-stu-id="5585c-326">Run ER formats</span></span>

1. <span data-ttu-id="5585c-327">В дереве конфигурации разверните содержимое пункта **Модели для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="5585c-328">Выберите **Формат для изучения параметризованных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="5585c-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="5585c-329">Выберите **Выполнить** на самой верхней ленте.</span><span class="sxs-lookup"><span data-stu-id="5585c-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="5585c-330">Сохраните локально созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="5585c-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="5585c-331">Выберите элемент **Формат для изучения параметризованных вызовов (настраиваемый)**.</span><span class="sxs-lookup"><span data-stu-id="5585c-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="5585c-332">Выберите **Выполнить** на самой верхней ленте.</span><span class="sxs-lookup"><span data-stu-id="5585c-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="5585c-333">Сохраните созданные выходные данные локально.</span><span class="sxs-lookup"><span data-stu-id="5585c-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="5585c-334">Сравните содержимое созданных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5585c-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5585c-335">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5585c-335">Additional resources</span></span>
[<span data-ttu-id="5585c-336">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="5585c-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
