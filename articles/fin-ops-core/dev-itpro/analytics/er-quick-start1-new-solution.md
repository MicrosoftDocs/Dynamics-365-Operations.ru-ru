---
title: Создание нового решения ER для печати пользовательского отчета
description: В этом разделе объясняется, как разработать решение электронной отчетности (ER), чтобы напечатать пользовательский отчет.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90e5381c2d30753e3ad82a38d7361b411f1d7a87
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304401"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="089f5-103">Создание нового решения ER для печати пользовательского отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="089f5-104">В следующих шагах описывается, как пользователь с ролью "системный администратор", "разработчик электронной отчетности" или "функционального консультанта по электронной отчетности" может настроить параметры структуры ER, разработать необходимые конфигурации электронной отчетности для нового решения ER для доступа к данным определенного бизнес-домена и создать пользовательский отчет в формате Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="089f5-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="089f5-105">Эти шаги можно выполнить в компании **USMF**.</span><span class="sxs-lookup"><span data-stu-id="089f5-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="089f5-106">Настройка платформы электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="089f5-107">Настройка параметров ER</span><span class="sxs-lookup"><span data-stu-id="089f5-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="089f5-108">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="089f5-109">Просмотр списка поставщиков конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="089f5-110">Добавление нового поставщика конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="089f5-111">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="089f5-112">Проектирование модели данных для конкретного домена</span><span class="sxs-lookup"><span data-stu-id="089f5-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="089f5-113">Импорт новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="089f5-114">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="089f5-115">Задание имени модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="089f5-116">Добавление полей модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="089f5-117">Завершение разработки модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="089f5-118">Разработка сопоставления модели для настроенной модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="089f5-119">Импорт новой конфигурации сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="089f5-120">Создайте конфигурацию сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="089f5-121">Создание нового компонента сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="089f5-122">Добавление источников данных для доступа к таблицам приложений</span><span class="sxs-lookup"><span data-stu-id="089f5-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="089f5-123">Добавление источников данных для доступа к перечислениям приложений</span><span class="sxs-lookup"><span data-stu-id="089f5-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="089f5-124">Добавление меток ER для создания отчета на определенном языке</span><span class="sxs-lookup"><span data-stu-id="089f5-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="089f5-125">Добавление источника данных для преобразования результатов сравнения значений перечисления с текстовым значением</span><span class="sxs-lookup"><span data-stu-id="089f5-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="089f5-126">Привязка источников данных к полям модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="089f5-127">Завершение разработки сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="089f5-128">Создание шаблона для пользовательского отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="089f5-129">Разработка формата</span><span class="sxs-lookup"><span data-stu-id="089f5-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="089f5-130">Импорт созданной конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="089f5-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="089f5-131">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="089f5-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="089f5-132">Импортируйте шаблон отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="089f5-133">Настройка формата</span><span class="sxs-lookup"><span data-stu-id="089f5-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="089f5-134">Определение привязки данных для заголовка отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="089f5-135">Просмотр источника данных модели</span><span class="sxs-lookup"><span data-stu-id="089f5-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="089f5-136">Привязка элементов формата к полям источника данных</span><span class="sxs-lookup"><span data-stu-id="089f5-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="089f5-137">Выполните созданный формат из ER</span><span class="sxs-lookup"><span data-stu-id="089f5-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="089f5-138">Настройте созданный формат</span><span class="sxs-lookup"><span data-stu-id="089f5-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="089f5-139">Изменение формата для изменения имени созданного документа</span><span class="sxs-lookup"><span data-stu-id="089f5-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="089f5-140">Изменение формата для изменения порядка вопросов</span><span class="sxs-lookup"><span data-stu-id="089f5-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="089f5-141">Выполните измененный формат из ER</span><span class="sxs-lookup"><span data-stu-id="089f5-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="089f5-142">Завершение разработки формата</span><span class="sxs-lookup"><span data-stu-id="089f5-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="089f5-143">Разработка артефактов приложений для вызова разработанного отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="089f5-144">Изменение исходного кода</span><span class="sxs-lookup"><span data-stu-id="089f5-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="089f5-145">Добавление класса контракта данных</span><span class="sxs-lookup"><span data-stu-id="089f5-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="089f5-146">Добавление класса конструктора пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="089f5-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="089f5-147">Добавление класса поставщика данных</span><span class="sxs-lookup"><span data-stu-id="089f5-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="089f5-148">Добавление файла меток</span><span class="sxs-lookup"><span data-stu-id="089f5-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="089f5-149">Добавление класса службы отчетов</span><span class="sxs-lookup"><span data-stu-id="089f5-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="089f5-150">Добавление класса controller отчетов</span><span class="sxs-lookup"><span data-stu-id="089f5-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="089f5-151">Добавление пункта меню</span><span class="sxs-lookup"><span data-stu-id="089f5-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="089f5-152">Добавление пункта меню в меню</span><span class="sxs-lookup"><span data-stu-id="089f5-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="089f5-153">Сборка проекта Visual Studio</span><span class="sxs-lookup"><span data-stu-id="089f5-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="089f5-154">Выполните формат из приложения</span><span class="sxs-lookup"><span data-stu-id="089f5-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="089f5-155">Настройка созданного решения ER</span><span class="sxs-lookup"><span data-stu-id="089f5-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="089f5-156">Изменение сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="089f5-157">Добавление источников данных для доступа к объекту контракта данных</span><span class="sxs-lookup"><span data-stu-id="089f5-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="089f5-158">Добавление источника данных для доступа к записям сопоставления формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="089f5-159">Добавление источника данных для доступа к записи сопоставления формата выполняемого формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="089f5-160">Введите имя выполняемого формата электронной отчетности в модель данных</span><span class="sxs-lookup"><span data-stu-id="089f5-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="089f5-161">Завершение разработки сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="089f5-162">Изменение формата</span><span class="sxs-lookup"><span data-stu-id="089f5-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="089f5-163">Добавление нового элемента формата</span><span class="sxs-lookup"><span data-stu-id="089f5-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="089f5-164">Связывание добавленного элемента формата</span><span class="sxs-lookup"><span data-stu-id="089f5-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="089f5-165">Завершение разработки формата</span><span class="sxs-lookup"><span data-stu-id="089f5-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="089f5-166">Выполните формат из приложения</span><span class="sxs-lookup"><span data-stu-id="089f5-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="089f5-167">Выполните формат из ER</span><span class="sxs-lookup"><span data-stu-id="089f5-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="089f5-168">Настройка назначения формата для предварительного просмотра на экране</span><span class="sxs-lookup"><span data-stu-id="089f5-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="089f5-169">Выполните формат из приложения, чтобы просмотреть его в виде PDF-документа</span><span class="sxs-lookup"><span data-stu-id="089f5-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="089f5-170">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="089f5-170">Additional resources</span></span>](#References)

<span data-ttu-id="089f5-171">В этом примере будет создано новое решение ER для модуля [Анкета](../../../human-resources/hr-learning-questionnaires.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="089f5-172">Новое решение ER позволяет создавать отчеты с помощью листа Microsoft Excel в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="089f5-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="089f5-173">Затем можно создать отчет **Анкета** в формате Excel или PDF, а также создавать существующие отчеты служб SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="089f5-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="089f5-174">Позднее можно изменить новый отчет по запросу.</span><span class="sxs-lookup"><span data-stu-id="089f5-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="089f5-175">Написание кода не требуется.</span><span class="sxs-lookup"><span data-stu-id="089f5-175">No coding is required.</span></span>

1. <span data-ttu-id="089f5-176">Чтобы выполнить существующий отчет, перейдите к **Анкета** \> **Разработка** \> **Отчет "Анкеты"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Выбор пункта меню "Отчет "Анкеты"" в модуле "Анкета" для работы с существующим отчетом SSRS](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="089f5-178">В диалоговом окне **Отчет "Анкеты"** укажите критерии выбора.</span><span class="sxs-lookup"><span data-stu-id="089f5-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="089f5-179">Примените фильтр, чтобы отчет включал только анкету **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Указание критерии выбора в диалоговом окне Отчет "Анкеты".](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="089f5-181">На следующем рисунке показана созданная версия отчета SSRS для анкеты **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Созданный отчет SSRS](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="089f5-183">Настройка платформы электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-183">Configure the ER framework</span></span>

<span data-ttu-id="089f5-184">В качестве пользователя в роли Разработчика электронной отчетности вам необходимо настроить минимальный набор параметров ER, прежде чем можно будет начать использовать платформу электронной отчетности для создания вашего решения электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="089f5-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="089f5-185">Настройка параметров ER</span><span class="sxs-lookup"><span data-stu-id="089f5-185">Configure ER parameters</span></span>

1. <span data-ttu-id="089f5-186">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="089f5-187">В рабочей области **Электронная отчетность** выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="089f5-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="089f5-188">На странице **Параметры электронной отчетности** на вкладке **Общие сведения** задайте для параметра **Включить режим конструктора** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="089f5-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="089f5-189">На вкладке **Вложения** установите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="089f5-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="089f5-190">Задайте поле **Конфигурации** на **Файл** для компании **USMF**.</span><span class="sxs-lookup"><span data-stu-id="089f5-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="089f5-191">Задайте поля **Архив заданий**, **Временный**, **Базовый** и **Другие** на **Файл**.</span><span class="sxs-lookup"><span data-stu-id="089f5-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="089f5-192">Дополнительные сведения о настройке параметров электронной отчетности см. в разделе [Настройка платформы электронной отчетности](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="089f5-193">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="089f5-194">Каждая конфигурация электронной отчетности помечается как принадлежащая поставщику конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="089f5-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="089f5-195">Поэтому перед началом добавления или изменения любых конфигураций электронной отчетности необходимо активировать поставщика конфигурации электронной отчетности в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="089f5-196">Только владелец конфигурации электронной отчетности может редактировать ее.</span><span class="sxs-lookup"><span data-stu-id="089f5-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="089f5-197">Поэтому перед редактированием конфигурации электронной отчетности необходимо активировать соответствующего поставщика конфигурации электронной отчетности в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="089f5-198">Просмотр списка поставщиков конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="089f5-199">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="089f5-200">В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Поставщики конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="089f5-201">На странице **Поставщики конфигурации** каждая запись поставщика конфигурации имеет уникальное имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="089f5-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="089f5-202">Проверьте содержимое данной страницы.</span><span class="sxs-lookup"><span data-stu-id="089f5-202">Review the contents of this page.</span></span> <span data-ttu-id="089f5-203">Если запись для **Litware, Inc.** (`https://www.litware.com`) уже существует, пропустите следующую процедуру, [Добавление нового поставщика конфигурации электронной отчетности](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="089f5-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="089f5-204">Добавление нового поставщика конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="089f5-205">На странице **Поставщики конфигураций** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="089f5-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="089f5-206">В поле **Имя** введите **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="089f5-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="089f5-207">В поле **Интернет-адрес** введите `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="089f5-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="089f5-208">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="089f5-209">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="089f5-210">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="089f5-211">В рабочей области **Электронная отчетность** выберите поставщика конфигурации **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="089f5-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="089f5-212">Выберите **Установить активные**.</span><span class="sxs-lookup"><span data-stu-id="089f5-212">Select **Set active**.</span></span>

<span data-ttu-id="089f5-213">Дополнительные сведения о поставщиках конфигурации электронной отчетности см. в разделе [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="089f5-214">Проектирование модели данных для конкретного домена</span><span class="sxs-lookup"><span data-stu-id="089f5-214">Design a domain-specific data model</span></span>

<span data-ttu-id="089f5-215">Необходимо создать новую конфигурацию ER, которая содержит компонент [модели данных](general-electronic-reporting.md#data-model-and-model-mapping-components) для бизнес-домена **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="089f5-216">Эта модель данных позднее будет использоваться в качестве источника данных при разработке формата ER для создания отчета **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="089f5-217">Выполнив шаги раздела [Импорт новой конфигурации модели данных](#ImportDataModel), можно импортировать требуемую модель данных из предоставленного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="089f5-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="089f5-218">В качестве альтернативы можно выполнить действия, указанные в разделе [Создание новой конфигурации модели данных](#DesignDataModel) для создания этой модели данных "с нуля".</span><span class="sxs-lookup"><span data-stu-id="089f5-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="089f5-219">Импорт новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="089f5-220">Загрузка файла [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) и сохранение его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="089f5-220">Download the [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="089f5-221">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="089f5-222">В рабочей области **Электронная отчетность** выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="089f5-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="089f5-223">На панели действий выберите пункт **Обмен** \> **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="089f5-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="089f5-224">Выберите **Обзор**, затем найдите и выберите файл **Questionnaires model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="089f5-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="089f5-225">Выберите **ОК**, чтобы импортировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="089f5-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="089f5-226">Чтобы продолжить, пропустите следующую процедуру, [создать новую конфигурацию модели данных](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="089f5-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="089f5-227">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="089f5-228">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="089f5-229">В рабочей области **Электронная отчетность** выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="089f5-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="089f5-230">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="089f5-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="089f5-231">В диалоговом окне в раскрывающемся списке в поле **Имя** введите **Модель анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="089f5-232">Выберите **Создать конфигурацию**, чтобы создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="089f5-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="089f5-233">Задание имени модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-233">Name the data model</span></span>

1. <span data-ttu-id="089f5-234">На странице **Конфигурации** в дереве конфигурации выберите **Модель анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="089f5-235">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="089f5-235">Select **Designer**.</span></span>
3. <span data-ttu-id="089f5-236">На странице **конструктор модели данных** на экспресс-вкладке **Общие** в поле **Имя** введите <a name="DataModeName"></a>**Анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="089f5-237">Добавление новых полей модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-237">Add new data model fields</span></span>

1. <span data-ttu-id="089f5-238">На странице **конструктор модели данных** нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="089f5-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="089f5-239">В раскрывающемся диалоговом окне для добавления узла модели данных выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="089f5-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-240">Выберите **Корень модели** в качестве типа нового узла.</span><span class="sxs-lookup"><span data-stu-id="089f5-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="089f5-241">В поле **Имя** введите <a name="RootDefinitionName"></a>**Корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="089f5-242">Чтобы добавить новый узел, выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="089f5-243">Этот корневой дескриптор будет использоваться для предоставления данных для отчета **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="089f5-244">Одна модель данных может иметь несколько дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="089f5-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="089f5-245">Каждый дескриптор может быть указан для одного формата ER, чтобы идентифицировать данные, необходимые для создания отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="089f5-246">Выберите **Создать** вновь, и затем в раскрывающемся диалоговом окне для добавления узла модели данных выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="089f5-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-247">Выберите **дочерний элемент активного узла** в качестве типа нового узла.</span><span class="sxs-lookup"><span data-stu-id="089f5-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="089f5-248">В поле **Имя** введите **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="089f5-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="089f5-249">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="089f5-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="089f5-250">Чтобы добавить новое поле, выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="089f5-251">Это поле требуется для передачи имени текущей компании в отчет ER, в котором эта модель данных используется в качестве источника данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="089f5-252">Выберите **Создать** вновь, и затем в раскрывающемся диалоговом окне для добавления узла модели данных выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="089f5-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-253">Выберите **дочерний элемент активного узла** в качестве типа нового узла.</span><span class="sxs-lookup"><span data-stu-id="089f5-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="089f5-254">В поле **Имя** введите **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="089f5-255">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="089f5-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="089f5-256">Чтобы добавить новое поле, выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="089f5-257">Это поле используется для передачи списка анкет в отчет ER, в котором эта модель данных используется в качестве источника данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="089f5-258">Выберите узел **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="089f5-259">Продолжайте добавлять необходимые поля редактируемой модели данных тем же способом, пока не будет завершена следующая структура модели данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="089f5-260">Путь к полю</span><span class="sxs-lookup"><span data-stu-id="089f5-260">Field path</span></span>                                                    | <span data-ttu-id="089f5-261">Тип данных</span><span class="sxs-lookup"><span data-stu-id="089f5-261">Data type</span></span>   | <span data-ttu-id="089f5-262">Обозначение поля/возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="089f5-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="089f5-263">Корневой</span><span class="sxs-lookup"><span data-stu-id="089f5-263">Root</span></span>                                                          |             | <span data-ttu-id="089f5-264">Опорная точка для запроса данных анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="089f5-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="089f5-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="089f5-266">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-266">String</span></span>      | <span data-ttu-id="089f5-267">Имя текущей компании.</span><span class="sxs-lookup"><span data-stu-id="089f5-267">The name of the current company.</span></span> |
    | <span data-ttu-id="089f5-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="089f5-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="089f5-269">Запись</span><span class="sxs-lookup"><span data-stu-id="089f5-269">Record</span></span>      | <span data-ttu-id="089f5-270">Сведения о выполнении формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-270">Format execution details.</span></span> |
    | <span data-ttu-id="089f5-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="089f5-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="089f5-272">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-272">String</span></span>      | <span data-ttu-id="089f5-273">Имя формата ER, который выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="089f5-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="089f5-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="089f5-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="089f5-275">Список записей</span><span class="sxs-lookup"><span data-stu-id="089f5-275">Record list</span></span> | <span data-ttu-id="089f5-276">Список анкет</span><span class="sxs-lookup"><span data-stu-id="089f5-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="089f5-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="089f5-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="089f5-278">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-278">String</span></span>      | <span data-ttu-id="089f5-279">Статус текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="089f5-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="089f5-281">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-281">String</span></span>      | <span data-ttu-id="089f5-282">Код текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="089f5-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="089f5-284">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-284">String</span></span>      | <span data-ttu-id="089f5-285">Описание текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="089f5-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="089f5-287">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-287">String</span></span>      | <span data-ttu-id="089f5-288">Тип текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="089f5-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="089f5-290">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-290">String</span></span>      | <span data-ttu-id="089f5-291">Числовой порядок текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="089f5-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="089f5-293">Запись</span><span class="sxs-lookup"><span data-stu-id="089f5-293">Record</span></span>      | <span data-ttu-id="089f5-294">Параметры результата текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="089f5-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="089f5-296">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-296">String</span></span>      | <span data-ttu-id="089f5-297">Идентификационный код текущей группы результатов.</span><span class="sxs-lookup"><span data-stu-id="089f5-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="089f5-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="089f5-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="089f5-299">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-299">String</span></span>      | <span data-ttu-id="089f5-300">Описание текущей группы результатов.</span><span class="sxs-lookup"><span data-stu-id="089f5-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="089f5-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="089f5-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="089f5-302">Действующий</span><span class="sxs-lookup"><span data-stu-id="089f5-302">Real</span></span>        | <span data-ttu-id="089f5-303">Максимальное количество баллов, которое можно получить.</span><span class="sxs-lookup"><span data-stu-id="089f5-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="089f5-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="089f5-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="089f5-305">Список записей</span><span class="sxs-lookup"><span data-stu-id="089f5-305">Record list</span></span> | <span data-ttu-id="089f5-306">Список вопросов для текущей анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="089f5-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="089f5-308">Целое число</span><span class="sxs-lookup"><span data-stu-id="089f5-308">Integer</span></span>     | <span data-ttu-id="089f5-309">Порядковый номер текущей коллекции ответов.</span><span class="sxs-lookup"><span data-stu-id="089f5-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="089f5-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="089f5-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="089f5-311">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-311">String</span></span>      | <span data-ttu-id="089f5-312">Идентификационный код текущего вопроса.</span><span class="sxs-lookup"><span data-stu-id="089f5-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="089f5-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="089f5-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="089f5-314">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-314">String</span></span>      | <span data-ttu-id="089f5-315">Флаг, который указывает, должен ли быть дан ответ на текущий вопрос.</span><span class="sxs-lookup"><span data-stu-id="089f5-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="089f5-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="089f5-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="089f5-317">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-317">String</span></span>      | <span data-ttu-id="089f5-318">Флаг, который указывает, является ли текущий вопрос основным.</span><span class="sxs-lookup"><span data-stu-id="089f5-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="089f5-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="089f5-320">Целое число</span><span class="sxs-lookup"><span data-stu-id="089f5-320">Integer</span></span>     | <span data-ttu-id="089f5-321">Порядковый номер текущего вопроса.</span><span class="sxs-lookup"><span data-stu-id="089f5-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="089f5-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="089f5-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="089f5-323">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-323">String</span></span>      | <span data-ttu-id="089f5-324">Текст текущего вопроса.</span><span class="sxs-lookup"><span data-stu-id="089f5-324">The text of the current question.</span></span> |
    | <span data-ttu-id="089f5-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="089f5-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="089f5-326">Список записей</span><span class="sxs-lookup"><span data-stu-id="089f5-326">Record list</span></span> | <span data-ttu-id="089f5-327">Список ответов для текущего вопроса.</span><span class="sxs-lookup"><span data-stu-id="089f5-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="089f5-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="089f5-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="089f5-329">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-329">String</span></span>      | <span data-ttu-id="089f5-330">Флаг, который указывает, является ли текущий ответ верным.</span><span class="sxs-lookup"><span data-stu-id="089f5-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="089f5-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="089f5-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="089f5-332">Действующий</span><span class="sxs-lookup"><span data-stu-id="089f5-332">Real</span></span>        | <span data-ttu-id="089f5-333">Баллы, заработанные при выборе текущего ответа.</span><span class="sxs-lookup"><span data-stu-id="089f5-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="089f5-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="089f5-335">Целое число</span><span class="sxs-lookup"><span data-stu-id="089f5-335">Integer</span></span>     | <span data-ttu-id="089f5-336">Порядковый номер текущего ответа.</span><span class="sxs-lookup"><span data-stu-id="089f5-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="089f5-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="089f5-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="089f5-338">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-338">String</span></span>      | <span data-ttu-id="089f5-339">Текст текущего ответа.</span><span class="sxs-lookup"><span data-stu-id="089f5-339">The text of the current answer.</span></span> |

    <span data-ttu-id="089f5-340">На следующем рисунке показана завершенная редактируемая модель данных на странице **конструктор моделей данных**.</span><span class="sxs-lookup"><span data-stu-id="089f5-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Настроенная модель данных в конструкторе модели данных ER](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="089f5-342">Сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="089f5-342">Save your changes.</span></span>
8. <span data-ttu-id="089f5-343">Закройте страницу **Конструктор модели данных**.</span><span class="sxs-lookup"><span data-stu-id="089f5-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="089f5-344">Завершение создания модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="089f5-345">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-346">На странице **Конфигурации** в дереве конфигурации выберите **Модель анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="089f5-347">На экспресс-вкладке **Версии** выберите версию конфигурации со статусом **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="089f5-348">Выберите **Изменить статус** \> **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="089f5-349">Статус версии 1 этой конфигурации изменяется с **черновик** на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="089f5-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="089f5-350">Версия 1 больше не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="089f5-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="089f5-351">Эта версия содержит настроенную модель данных и может использоваться в качестве основы для других конфигураций ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="089f5-352">Версия 2 этой конфигурации создана и имеет статус **черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="089f5-353">Эту версию можно изменить для корректировки модели данных **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Версии редактируемой конфигурации на странице конфигурации](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="089f5-355">Дополнительные сведения об управлении версиями для конфигураций ER см. в [Обзор электронной отчетности (ER)](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="089f5-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="089f5-356">Настроенная модель данных является абстрактным представлением бизнес-домена **Анкета** и не содержит отношений с артефактами которые относятся к Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="089f5-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="089f5-357">Разработка сопоставления модели для настроенной модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="089f5-358">В качестве пользователя в роли разработчика электронной отчетности необходимо создать новую конфигурацию ER, которая содержит компонент [сопоставления модели](general-electronic-reporting.md#data-model-and-model-mapping-components) для модели данных **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="089f5-359">Так как этот компонент реализует настроенную модель данных для Финансы, она предназначена только для Финансы.</span><span class="sxs-lookup"><span data-stu-id="089f5-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="089f5-360">Необходимо настроить компонент "сопоставление моделей", чтобы указать объекты приложения, которые должны использоваться для заполнения настроенной модели данных данными приложения в среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="089f5-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="089f5-361">Чтобы выполнить эту задачу, необходимо знать информацию о реализации структуры данных в бизнес-домене **Анкета** в Финансы.</span><span class="sxs-lookup"><span data-stu-id="089f5-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="089f5-362">Выполнив шаги раздела [Импорт новой конфигурации сопоставления модели](#ImportModelMapping), можно импортировать требуемую конфигурацию сопоставления модели из предоставленного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="089f5-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="089f5-363">В качестве альтернативы можно выполнить действия, указанные в разделе [Создание новой конфигурации сопоставления модели](#CreateModelMapping) для создания этой сопоставления модели "с нуля".</span><span class="sxs-lookup"><span data-stu-id="089f5-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="089f5-364">Импорт новой конфигурации сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="089f5-365">Загрузка файла [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) и сохранение его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="089f5-365">Download the [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="089f5-366">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="089f5-367">В рабочей области **Электронная отчетность** выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="089f5-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="089f5-368">На панели действий выберите пункт **Обмен** \> **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="089f5-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="089f5-369">Выберите **Обзор**, затем найдите и выберите файл **Questionnaires mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="089f5-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="089f5-370">Выберите **ОК**, чтобы импортировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="089f5-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="089f5-371">Чтобы продолжить, пропустите следующую процедуру, [создать новую конфигурацию сопоставления модели](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="089f5-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="089f5-372">Создайте конфигурацию сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="089f5-373">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-374">На странице **Конфигурации** в дереве конфигурации выберите **Модель анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="089f5-375">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="089f5-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="089f5-376">В раскрывающемся диалоговом окне выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-377">В поле **Создать** выберите **Сопоставление модели, основанное на модели данных Анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="089f5-378">В поле **Имя** введите **Сопоставление анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="089f5-379">В поле **Определение модели данных** выберите определение **Корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="089f5-380">Выберите **Создать конфигурацию**, чтобы создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="089f5-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="089f5-381">Создание нового компонента сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="089f5-382">На странице **Конфигурации** в дереве конфигурации выберите **Сопоставление анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="089f5-383">Выберите **конструктор**, чтобы открыть список сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="089f5-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="089f5-384">Выбор сопоставления **сопоставления анкеты**, которое было автоматически добавлено для определения **Корень**</span><span class="sxs-lookup"><span data-stu-id="089f5-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="089f5-385">Выберите **конструктор**, чтобы начать настройку выбранного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="089f5-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="089f5-386">Для определения **Корень** автоматически добавляется новое сопоставление.</span><span class="sxs-lookup"><span data-stu-id="089f5-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="089f5-387">Это сопоставление имеет направление **В модель**.</span><span class="sxs-lookup"><span data-stu-id="089f5-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="089f5-388">Поэтому это сопоставление может использоваться для заполнения модели данных требуемыми данными.</span><span class="sxs-lookup"><span data-stu-id="089f5-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="089f5-389">Добавление источников данных для доступа к таблицам приложений</span><span class="sxs-lookup"><span data-stu-id="089f5-389">Add data sources to access application tables</span></span>

<span data-ttu-id="089f5-390">Необходимо настроить источники данных для доступа к таблицам приложений, содержащим сведения об анкете.</span><span class="sxs-lookup"><span data-stu-id="089f5-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="089f5-391">На странице **Конструктор сопоставления модели** в области **Типы источников данных** выберите **Dynamics 365 for Operations\\Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="089f5-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="089f5-392">Добавление нового источника данных, который будет использоваться для доступа к таблице KMCollection, в которой каждая запись соответствует одной анкете:</span><span class="sxs-lookup"><span data-stu-id="089f5-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="089f5-393">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-394">В диалоговом окне в поле **Имя** введите **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="089f5-395">В поле **Таблица** введите **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="089f5-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="089f5-396">Для параметра **Запросить запрос** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="089f5-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="089f5-397">После этого можно будет указать параметры [фильтрации](../../fin-ops/get-started/advanced-filtering-query-options.md) для этой таблицы в диалоговом окне системного запроса в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="089f5-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="089f5-398">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="089f5-399">В области **типы источников данных** выберите **Dynamics 365 for Operations\\Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="089f5-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="089f5-400">Добавление нового источника данных, который будет использоваться для доступа к таблице KMQuestion, в которой каждая запись соответствует одному вопросу:</span><span class="sxs-lookup"><span data-stu-id="089f5-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="089f5-401">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-402">В диалоговом окне в поле **Имя** введите **Вопрос**.</span><span class="sxs-lookup"><span data-stu-id="089f5-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="089f5-403">В поле **Таблица** введите **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="089f5-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="089f5-404">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="089f5-405">В области **типы источников данных** выберите **Dynamics 365 for Operations\\Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="089f5-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="089f5-406">Добавление нового источника данных, который будет использоваться для доступа к таблице KMAnswer, в которой каждая запись соответствует одному ответу на вопрос в анкете:</span><span class="sxs-lookup"><span data-stu-id="089f5-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="089f5-407">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-408">В поле **Имя** введите **Ответ**.</span><span class="sxs-lookup"><span data-stu-id="089f5-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="089f5-409">В поле **Таблица** введите **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="089f5-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="089f5-410">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="089f5-411">В области **типы источников данных** выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="089f5-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="089f5-412">Добавьте новое вычисляемое поле, которое будет использоваться для доступа к записи таблицы KMQuestionResultGroup из каждой записи родительской таблицы KMCollection:</span><span class="sxs-lookup"><span data-stu-id="089f5-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="089f5-413">В области **источники данных** выберите **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="089f5-414">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-414">Select **Add**.</span></span>
    3. <span data-ttu-id="089f5-415">В диалоговом окне в поле **Имя** введите **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="089f5-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="089f5-416">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="089f5-417">В [редакторе формул ER](general-electronic-reporting-formula-designer.md)в поле **Формула** введите **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** для использования [пути](er-formula-language.md#Paths) связи "один ко многим" между таблицами KMCollection и KMQuestionResultGroup.</span><span class="sxs-lookup"><span data-stu-id="089f5-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#Paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="089f5-418">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="089f5-419">Нажмите **ОК**, чтобы добавить новый вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="089f5-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="089f5-420">В области **типы источников данных** выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="089f5-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="089f5-421">Добавьте новое вычисляемое поле, которое будет использоваться для доступа к записям вопроса таблицы KMQuestion из каждой записи родительской таблицы KMCollectionQuestion:</span><span class="sxs-lookup"><span data-stu-id="089f5-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="089f5-422">В области **источники данных** выберите **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="089f5-423">Разверните узел **\<отношения**, содержащий связи "один ко многим" с таблицей KMCollection.</span><span class="sxs-lookup"><span data-stu-id="089f5-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="089f5-424">Выберите соответствующую таблицу **KMCollectionQuestion** и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="089f5-425">В диалоговом окне в поле **Имя** введите **\$Вопрос**.</span><span class="sxs-lookup"><span data-stu-id="089f5-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="089f5-426">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="089f5-427">В редакторе формул в поле **Формула** введите **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))**, чтобы вернуть соответствующие записи вопроса из таблицы "KMQuestion.</span><span class="sxs-lookup"><span data-stu-id="089f5-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="089f5-428">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="089f5-429">Нажмите **ОК**, чтобы добавить новый вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="089f5-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="089f5-430">В области **типы источников данных** выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="089f5-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="089f5-431">Добавьте новое вычисляемое поле, которое будет использоваться для доступа к записям ответа таблицы KMAnswer из каждой записи родительской таблицы KMQuestion:</span><span class="sxs-lookup"><span data-stu-id="089f5-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="089f5-432">В области **источники данных** выберите **Анкета.\<Relations.KMCollectionQuestion.\$Вопрос**, а затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="089f5-433">В диалоговом окне в поле **Имя** введите **\$Ответ**.</span><span class="sxs-lookup"><span data-stu-id="089f5-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="089f5-434">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="089f5-435">В редакторе формул в поле **Формула** введите **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)**, чтобы вернуть соответствующие записи ответа из таблицы KMAnswer.</span><span class="sxs-lookup"><span data-stu-id="089f5-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="089f5-436">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="089f5-437">Нажмите **ОК**, чтобы добавить новый вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="089f5-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="089f5-438">В области **типы источников данных** выберите **Dynamics 365 for Operations\\Таблица**.</span><span class="sxs-lookup"><span data-stu-id="089f5-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="089f5-439">Добавление нового источника данных, который будет использоваться для доступа к методам таблицы CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="089f5-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="089f5-440">Обратите внимание, что метод **find()** этой таблицы возвращает запись, представляющую компанию текущего экземпляра Finance, с помощью которой это сопоставление вызывается в контексте.</span><span class="sxs-lookup"><span data-stu-id="089f5-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="089f5-441">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-442">В диалоговом окне в поле **Имя** введите **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="089f5-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="089f5-443">В поле **Таблица** введите **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="089f5-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="089f5-444">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="089f5-445">Добавление источников данных для доступа к перечислениям приложений</span><span class="sxs-lookup"><span data-stu-id="089f5-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="089f5-446">Необходимо настроить источники данных для доступа к перечислениям приложений и сравнить их значения со значениями полей типа **перечисления** в таблицах приложений.</span><span class="sxs-lookup"><span data-stu-id="089f5-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="089f5-447">Результат сравнения должен использоваться для заполнения соответствующих полей модели данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="089f5-448">На странице **Конструктор сопоставления модели** в области **Типы источников данных** выберите **Dynamics 365 for Operations\\Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="089f5-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="089f5-449">Добавление нового источника данных, который будет использоваться для доступа к значениям перечисления **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="089f5-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="089f5-450">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-451">В диалоговом окне в поле **Имя** введите **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="089f5-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="089f5-452">В поле **перечисление** введите **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="089f5-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="089f5-453">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="089f5-454">В области **типы источников данных** выберите **Dynamics 365 for Operations\\Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="089f5-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="089f5-455">Добавление нового источника данных, который будет использоваться для доступа к значениям перечисления **KMCollectionQuestionMode**:</span><span class="sxs-lookup"><span data-stu-id="089f5-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="089f5-456">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-457">В диалоговом окне, в поле **Имя**, введите **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="089f5-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="089f5-458">В поле **перечисление** введите **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="089f5-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="089f5-459">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="089f5-460">Добавление меток ER для создания отчета на определенном языке</span><span class="sxs-lookup"><span data-stu-id="089f5-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="089f5-461">Можно добавить метки ER для настройки некоторых источников данных, чтобы они возвращали значения, которые зависят от языка, определенного в контексте вызова сопоставления модели.</span><span class="sxs-lookup"><span data-stu-id="089f5-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="089f5-462">На странице **Конструктор сопоставления модели** в области **Источники данных** выберите **Ответ**, а затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="089f5-463">Активируйте поле **Метка**.</span><span class="sxs-lookup"><span data-stu-id="089f5-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="089f5-464">Выберите **Перевести**.</span><span class="sxs-lookup"><span data-stu-id="089f5-464">Select **Translate**.</span></span>
4. <span data-ttu-id="089f5-465">В диалоговом окне **Перевод текста** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-466">В поле **Код метки** введите **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="089f5-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="089f5-467">В поле **Текст на языке по умолчанию** введите **Да**.</span><span class="sxs-lookup"><span data-stu-id="089f5-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="089f5-468">Выберите **Перевести**.</span><span class="sxs-lookup"><span data-stu-id="089f5-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="089f5-469">В поле **Код метки** введите **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="089f5-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="089f5-470">В поле **Текст на языке по умолчанию** введите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="089f5-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="089f5-471">Выберите **Перевести**.</span><span class="sxs-lookup"><span data-stu-id="089f5-471">Select **Translate**.</span></span>

5. <span data-ttu-id="089f5-472">Закройте диалоговое окно **Преобразование текста**.</span><span class="sxs-lookup"><span data-stu-id="089f5-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="089f5-473">Выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="089f5-473">Select **Cancel**.</span></span>

![Добавление меток ER для сопоставления редактируемых моделей](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="089f5-475">Метки ER введены только для языка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="089f5-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="089f5-476">Сведения о том, как можно переводить метки ER на другие языки, см. в разделе [Разработка многоязычных отчетов](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="089f5-477">Добавление источника данных для преобразования результатов сравнения значений перечисления с текстовым значением</span><span class="sxs-lookup"><span data-stu-id="089f5-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="089f5-478">Поскольку необходимо несколько раз преобразовать результаты сравнения значений перечислений и текстовых значений для источников отличий, рекомендуется настроить эту логику как единый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="089f5-479">Однако, чтобы сделать этот источник данных пригодным для повторного использования, его необходимо настроить как источник параметризованных данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="089f5-480">Дополнительные сведения см. в [Поддержка параметризованных вызовов источников данных электронной отчетности для рассчитанного типа поля](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="089f5-481">На странице **Конструктор сопоставления модели** в области **Типы источников данных** выберите **Общее\\Пустой контейнер**.</span><span class="sxs-lookup"><span data-stu-id="089f5-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="089f5-482">Добавление нового источника данных контейнера:</span><span class="sxs-lookup"><span data-stu-id="089f5-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="089f5-483">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="089f5-484">В диалоговом окне в поле **Имя** введите **Помощник**.</span><span class="sxs-lookup"><span data-stu-id="089f5-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="089f5-485">Нажмите **ОК**, чтобы добавить новый источник данных контейнера.</span><span class="sxs-lookup"><span data-stu-id="089f5-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="089f5-486">В области **типы источников данных** выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="089f5-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="089f5-487">Добавление нового источника данных:</span><span class="sxs-lookup"><span data-stu-id="089f5-487">Add a new data source:</span></span>

    1. <span data-ttu-id="089f5-488">В области **источники данных** выберите **Помощник**.</span><span class="sxs-lookup"><span data-stu-id="089f5-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="089f5-489">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-489">Select **Add**.</span></span>
    3. <span data-ttu-id="089f5-490">В диалоговом окне, в поле **Имя**, введите **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="089f5-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="089f5-491">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="089f5-492">В редакторе формул выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="089f5-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="089f5-493">Чтобы указать параметры для настроенного выражения, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="089f5-494">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="089f5-494">Select **New**.</span></span>
        2. <span data-ttu-id="089f5-495">В диалоговом окне в поле **Имя** введите **аргумент**.</span><span class="sxs-lookup"><span data-stu-id="089f5-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="089f5-496">В поле **Тип** выберите тип данных **логический**.</span><span class="sxs-lookup"><span data-stu-id="089f5-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="089f5-497">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-497">Select **OK**.</span></span>

    7. <span data-ttu-id="089f5-498">В поле **Формула** введите **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**, чтобы вернуть текст соответствующей метки ER, в зависимости от языка контекста выполнения и значения указанного параметра.</span><span class="sxs-lookup"><span data-stu-id="089f5-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="089f5-499">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="089f5-500">Нажмите **ОК**, чтобы добавить новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-500">Select **OK** to add the new data source.</span></span>

![Настроенное сопоставление модели в конструкторе сопоставления модели ER](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="089f5-502">Привязка источников данных к полям модели данных</span><span class="sxs-lookup"><span data-stu-id="089f5-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="089f5-503">Необходимо привязать настроенные источники данных к полям модели данных, чтобы указать, каким образом модель данных будет заполнена данными приложения в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="089f5-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="089f5-504">На странице **Конструктор сопоставления модели** в области **Модель данных** выберите **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="089f5-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="089f5-505">В области **Источники данных** разверните узел **CompanyInfo** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="089f5-506">Разверните узел **CompanyInfo.find()**, который представляет метод **find()** таблицы CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="089f5-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="089f5-507">Выберите **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="089f5-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="089f5-508">Выберите **Связать** для заполнения названия компании, для которой настроено сопоставление модели в контексте среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="089f5-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="089f5-509">В области **Модель данных** выберите **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="089f5-510">В области **источники данных** выберите **Анкета**, а затем выберите **Связать**, чтобы заполнить записи анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="089f5-511">В области **Модель данных** разверните узел **Анкета** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="089f5-512">В области **Модель данных** выберите **Активный**.</span><span class="sxs-lookup"><span data-stu-id="089f5-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="089f5-513">В области **Модель данных** выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="089f5-514">В поле **Формула** введите **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)**, чтобы заполнить результаты сравнения значений перечислений, зависящих от текста и языка.</span><span class="sxs-lookup"><span data-stu-id="089f5-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="089f5-515">Продолжайте привязывать источники данных к полям модели данных одинаковым образом, пока не получите следующий результат.</span><span class="sxs-lookup"><span data-stu-id="089f5-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="089f5-516">Путь к полю</span><span class="sxs-lookup"><span data-stu-id="089f5-516">Field path</span></span>                                              | <span data-ttu-id="089f5-517">Тип данных</span><span class="sxs-lookup"><span data-stu-id="089f5-517">Data type</span></span>   | <span data-ttu-id="089f5-518">Действие</span><span class="sxs-lookup"><span data-stu-id="089f5-518">Action</span></span> | <span data-ttu-id="089f5-519">Выражение связывания</span><span class="sxs-lookup"><span data-stu-id="089f5-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="089f5-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="089f5-520">CompanyName</span></span>                                             | <span data-ttu-id="089f5-521">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-521">String</span></span>      | <span data-ttu-id="089f5-522">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-522">Bind</span></span>   | <span data-ttu-id="089f5-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="089f5-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="089f5-524">Анкета</span><span class="sxs-lookup"><span data-stu-id="089f5-524">Questionnaire</span></span>                                           | <span data-ttu-id="089f5-525">Список записей</span><span class="sxs-lookup"><span data-stu-id="089f5-525">Record list</span></span> | <span data-ttu-id="089f5-526">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-526">Bind</span></span>   | <span data-ttu-id="089f5-527">Анкета</span><span class="sxs-lookup"><span data-stu-id="089f5-527">Questionnaire</span></span> |
    | <span data-ttu-id="089f5-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="089f5-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="089f5-529">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-529">String</span></span>      | <span data-ttu-id="089f5-530">Редактировать</span><span class="sxs-lookup"><span data-stu-id="089f5-530">Edit</span></span>   | <span data-ttu-id="089f5-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="089f5-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="089f5-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="089f5-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="089f5-533">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-533">String</span></span>      | <span data-ttu-id="089f5-534">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-534">Bind</span></span>   | <span data-ttu-id="089f5-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="089f5-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="089f5-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="089f5-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="089f5-537">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-537">String</span></span>      | <span data-ttu-id="089f5-538">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-538">Bind</span></span>   | <span data-ttu-id="089f5-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="089f5-539">\@.Description</span></span> |
    | <span data-ttu-id="089f5-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="089f5-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="089f5-541">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-541">String</span></span>      | <span data-ttu-id="089f5-542">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-542">Bind</span></span>   | <span data-ttu-id="089f5-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="089f5-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="089f5-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="089f5-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="089f5-545">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-545">String</span></span>      | <span data-ttu-id="089f5-546">Редактировать</span><span class="sxs-lookup"><span data-stu-id="089f5-546">Edit</span></span>   | <span data-ttu-id="089f5-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="089f5-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="089f5-548">EnumAppQuestionOrder.Conditional, "Условный",</span><span class="sxs-lookup"><span data-stu-id="089f5-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="089f5-549">EnumAppQuestionOrder.Random, "Случайно (процент в анкете)",</span><span class="sxs-lookup"><span data-stu-id="089f5-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="089f5-550">EnumAppQuestionOrder.RandomGroup, "Случайно (процент в группах результатов)",</span><span class="sxs-lookup"><span data-stu-id="089f5-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="089f5-551">EnumAppQuestionOrder.Sequence, "Последовательный",</span><span class="sxs-lookup"><span data-stu-id="089f5-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="089f5-552">"")</span><span class="sxs-lookup"><span data-stu-id="089f5-552">"")</span></span> |
    | <span data-ttu-id="089f5-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="089f5-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="089f5-554">Запись</span><span class="sxs-lookup"><span data-stu-id="089f5-554">Record</span></span>      |        | |
    | <span data-ttu-id="089f5-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="089f5-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="089f5-556">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-556">String</span></span>      | <span data-ttu-id="089f5-557">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-557">Bind</span></span>   | <span data-ttu-id="089f5-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="089f5-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="089f5-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="089f5-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="089f5-560">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-560">String</span></span>      | <span data-ttu-id="089f5-561">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-561">Bind</span></span>   | <span data-ttu-id="089f5-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="089f5-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="089f5-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="089f5-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="089f5-564">Действующий</span><span class="sxs-lookup"><span data-stu-id="089f5-564">Real</span></span>        | <span data-ttu-id="089f5-565">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-565">Bind</span></span>   | <span data-ttu-id="089f5-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="089f5-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="089f5-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="089f5-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="089f5-568">Список записей</span><span class="sxs-lookup"><span data-stu-id="089f5-568">Record list</span></span> | <span data-ttu-id="089f5-569">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-569">Bind</span></span>   | <span data-ttu-id="089f5-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="089f5-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="089f5-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="089f5-572">Целое число</span><span class="sxs-lookup"><span data-stu-id="089f5-572">Integer</span></span>     | <span data-ttu-id="089f5-573">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-573">Bind</span></span>   | <span data-ttu-id="089f5-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="089f5-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="089f5-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="089f5-576">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-576">String</span></span>      | <span data-ttu-id="089f5-577">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-577">Bind</span></span>   | <span data-ttu-id="089f5-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="089f5-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="089f5-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="089f5-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="089f5-580">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-580">String</span></span>      | <span data-ttu-id="089f5-581">Редактировать</span><span class="sxs-lookup"><span data-stu-id="089f5-581">Edit</span></span>   | <span data-ttu-id="089f5-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="089f5-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="089f5-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="089f5-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="089f5-584">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-584">String</span></span>      | <span data-ttu-id="089f5-585">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-585">Bind</span></span>   | <span data-ttu-id="089f5-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="089f5-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="089f5-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="089f5-588">Целое число</span><span class="sxs-lookup"><span data-stu-id="089f5-588">Integer</span></span>     | <span data-ttu-id="089f5-589">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-589">Bind</span></span>   | <span data-ttu-id="089f5-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="089f5-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="089f5-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="089f5-592">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-592">String</span></span>      | <span data-ttu-id="089f5-593">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-593">Bind</span></span>   | <span data-ttu-id="089f5-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="089f5-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="089f5-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="089f5-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="089f5-596">Список записей</span><span class="sxs-lookup"><span data-stu-id="089f5-596">Record list</span></span> | <span data-ttu-id="089f5-597">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-597">Bind</span></span>   | <span data-ttu-id="089f5-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="089f5-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="089f5-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="089f5-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="089f5-600">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-600">String</span></span>      | <span data-ttu-id="089f5-601">Редактировать</span><span class="sxs-lookup"><span data-stu-id="089f5-601">Edit</span></span>   | <span data-ttu-id="089f5-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="089f5-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="089f5-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="089f5-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="089f5-604">Действующий</span><span class="sxs-lookup"><span data-stu-id="089f5-604">Real</span></span>        | <span data-ttu-id="089f5-605">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-605">Bind</span></span>   | <span data-ttu-id="089f5-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="089f5-606">\@.point</span></span> |
    | <span data-ttu-id="089f5-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="089f5-608">Целое число</span><span class="sxs-lookup"><span data-stu-id="089f5-608">Integer</span></span>     | <span data-ttu-id="089f5-609">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-609">Bind</span></span>   | <span data-ttu-id="089f5-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="089f5-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="089f5-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="089f5-612">Строка</span><span class="sxs-lookup"><span data-stu-id="089f5-612">String</span></span>      | <span data-ttu-id="089f5-613">Связать</span><span class="sxs-lookup"><span data-stu-id="089f5-613">Bind</span></span>   | <span data-ttu-id="089f5-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="089f5-614">\@.text</span></span> |

    <span data-ttu-id="089f5-615">На следующем рисунке показано конечное состояние настроенного сопоставления модели на странице **конструктор сопоставления моделей**.</span><span class="sxs-lookup"><span data-stu-id="089f5-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Полностью настроенное сопоставление модели в конструкторе сопоставления модели ER](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="089f5-617">Сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="089f5-617">Save your changes.</span></span>
8. <span data-ttu-id="089f5-618">Закройте страницу **Конструктор сопоставления модели**.</span><span class="sxs-lookup"><span data-stu-id="089f5-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="089f5-619">Завершение разработки сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="089f5-620">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-621">На странице **Конфигурации** в дереве конфигурации выберите **Сопоставление анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="089f5-622">На экспресс-вкладке **Версии** выберите версию конфигурации со статусом **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="089f5-623">Выберите **Изменить статус** \> **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="089f5-624">Статус версии 1.1 этой конфигурации изменяется с **черновик** на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="089f5-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="089f5-625">Версия 1.1 больше не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="089f5-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="089f5-626">Эта версия содержит настроенное сопоставление модели и может использоваться в качестве основы для других конфигураций ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="089f5-627">Версия 1.2 этой конфигурации создана и имеет статус **черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="089f5-628">Эту версию можно изменить для корректировки конфигурации **Сопоставление анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Версии редактируемой конфигурации ER на странице конфигурации](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="089f5-630">Настроенное сопоставление модели — это предназначенная для Финансы реализация модели абстрактных данных, которая представляет собой бизнес-домен **анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="089f5-631">Создание шаблона для пользовательского отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-631">Design a template for a custom report</span></span>

<span data-ttu-id="089f5-632">Платформа ER использует предопределенные шаблоны для создания отчетов в форматах Microsoft Office (книги Excel или документы Word).</span><span class="sxs-lookup"><span data-stu-id="089f5-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="089f5-633">В процессе создания обязательного отчета шаблон заполняется необходимыми данными в соответствии с настроенным потоком данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="089f5-634">Поэтому сначала необходимо создать шаблон для пользовательского отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="089f5-635">Этот шаблон должен быть создан в качестве рабочей книги Excel, структура которого представляет макет пользовательского отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="089f5-636">Необходимо присвоить имя каждому объекту Excel, который планируется заполнить требуемыми данными.</span><span class="sxs-lookup"><span data-stu-id="089f5-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="089f5-637">Загрузка файла [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) и сохранение его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="089f5-637">Download the [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="089f5-638">Откройте файл в Excel и проверьте структуру книги.</span><span class="sxs-lookup"><span data-stu-id="089f5-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="089f5-639">Как показано на следующем рисунке, загруженный шаблон предназначен для печати указанных анкет, которые представляют вопросы анкеты вместе с соответствующими ответами.</span><span class="sxs-lookup"><span data-stu-id="089f5-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Шаблон Excel для печати указанных анкет](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="089f5-641">В этот шаблон были добавлены имена Excel для заполнения сведений анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="089f5-642">Для просмотра имен Excel можно использовать Диспетчер имен.</span><span class="sxs-lookup"><span data-stu-id="089f5-642">You can use Name Manager to review the Excel names.</span></span>

![Использование диспетчера имен для просмотра имен Excel в предоставленном шаблоне Excel](./media/er-quick-start1-template-names.png)

<span data-ttu-id="089f5-644">Метки отчетов были добавлены в виде фиксированного текста на английском языке.</span><span class="sxs-lookup"><span data-stu-id="089f5-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="089f5-645">Можно заменить метки отчетов новыми именами Excel, которые заполняют этикетки текстом, зависящим от языка, используя [метки](#AddMmLabels) формата ER, как и в случае выражений, зависящих от языка, в настроенном сопоставлении модели.</span><span class="sxs-lookup"><span data-stu-id="089f5-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="089f5-646">В этом случае метки ER должны быть добавлены в редактируемый формат ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="089f5-647">Как показано на следующем рисунке, для включения разбиения по страницам в Excel был указан пользовательский заголовок отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Пользовательский заголовок отчета в предоставленном шаблоне Excel](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="089f5-649">Разработка формата</span><span class="sxs-lookup"><span data-stu-id="089f5-649">Design a format</span></span>

<span data-ttu-id="089f5-650">В качестве пользователя в роли функционального консультанта по электронной отчетности необходимо создать новую конфигурацию ER, которая содержит компонент [формата](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="089f5-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="089f5-651">Необходимо настроить компонент формата, чтобы указать, как будет заполнен шаблон отчета обязательными данными в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="089f5-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="089f5-652">Выполнив шаги раздела [Импорт конфигурации созданного формата](#FormatImport), можно импортировать требуемый формат из предоставленного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="089f5-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="089f5-653">В качестве альтернативы можно выполнить действия, указанные в разделе [Создание новой конфигурации формата](#FormatCreate) для создания этой формата "с нуля".</span><span class="sxs-lookup"><span data-stu-id="089f5-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="089f5-654">Импорт созданной конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="089f5-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="089f5-655">Загрузка файла [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) и сохранение его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="089f5-655">Download the [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="089f5-656">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="089f5-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="089f5-657">В рабочей области **Электронная отчетность** выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="089f5-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="089f5-658">На панели действий выберите пункт **Обмен** \> **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="089f5-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="089f5-659">Выберите **Обзор**, затем найдите и выберите файл **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="089f5-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="089f5-660">Выберите **ОК**, чтобы импортировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="089f5-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="089f5-661">Чтобы продолжить, пропустите следующую процедуру, [создать новую конфигурацию формата](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="089f5-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="089f5-662">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="089f5-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="089f5-663">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-664">На странице **Конфигурации** в дереве конфигурации выберите **Модель анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="089f5-665">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="089f5-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="089f5-666">В раскрывающемся диалоговом окне выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-667">В поле **Создать** выберите **Формат, основанное на модели данных Анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="089f5-668">В поле **Имя** введите **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="089f5-669">В поле **Версия модели данных** выберите **1**.</span><span class="sxs-lookup"><span data-stu-id="089f5-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="089f5-670">При выборе определенной версии базовой модели данных структура соответствующей версии модели данных будет представлена в виде структуры источника данных **модели** в созданном формате.</span><span class="sxs-lookup"><span data-stu-id="089f5-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="089f5-671">Данное поле можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="089f5-671">You can leave this field blank.</span></span> <span data-ttu-id="089f5-672">В этом случае структура **черновой** версии модели данных будет представлена в виде структуры источника данных **модели** в созданном формате.</span><span class="sxs-lookup"><span data-stu-id="089f5-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="089f5-673">Затем можно откорректировать модель и сразу увидеть изменения в своем формате.</span><span class="sxs-lookup"><span data-stu-id="089f5-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="089f5-674">Такой подход может повысить эффективность разработки решения ER при настройке одновременно модели данных, сопоставления модели и формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="089f5-675">При выборе определенной версии базовой модели данных можно переключаться на использование **черновой** версии позже при запуске редактирования формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="089f5-676">В поле **Определение модели данных** выберите определение **Корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="089f5-677">Выберите **Создать конфигурацию**, чтобы создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="089f5-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="089f5-678">Импортируйте шаблон отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-678">Import a report template</span></span>

1. <span data-ttu-id="089f5-679">На странице **Конфигурации** в дереве конфигурации выберите **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="089f5-680">Чтобы начать настройку пользовательского формата, выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="089f5-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="089f5-681">На странице **Конструктор форматов** в области действий выберите **Импорт** \> **Импорт из Excel**.</span><span class="sxs-lookup"><span data-stu-id="089f5-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="089f5-682">В диалоговом окне выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-683">Выберите **Добавить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="089f5-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="089f5-684">Найдите и выберите локально сохраненный файл **Questionnaires report template.xslx** и нажмите кнопку **открыть**.</span><span class="sxs-lookup"><span data-stu-id="089f5-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="089f5-685">Выберите **ОК**, чтобы импортировать шаблон.</span><span class="sxs-lookup"><span data-stu-id="089f5-685">Select **OK** to import the template.</span></span>

    ![Импортирование шаблона отчета](./media/er-quick-start1-template-import.png)

<span data-ttu-id="089f5-687">Элемент формата **Excel\\File** автоматически добавляется к редактируемому формату как корневой элемент.</span><span class="sxs-lookup"><span data-stu-id="089f5-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="089f5-688">Кроме того, элемент формата **Excel\\Range** или **Excel\\Cell** автоматически добавляется для каждого распознаваемого имени Excel импортированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="089f5-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="089f5-689">Формат **Excel\\Header**, в котором имеется вложенный элемент **Строка**, автоматически добавляется для отображения настроек заголовка импортированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="089f5-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Структура формата, которая включает автоматически добавленные элементы в конструкторе операций ER](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="089f5-691">Настройка формата</span><span class="sxs-lookup"><span data-stu-id="089f5-691">Configure a format</span></span>

1. <span data-ttu-id="089f5-692">На странице **конструктор формата** в дереве формата выберите корневой элемент **Excel**.</span><span class="sxs-lookup"><span data-stu-id="089f5-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="089f5-693">На вкладке **Формат** в правой части страницы в поле **Имя** введите <a name="AddFormatRootElement"></a>**отчет**.</span><span class="sxs-lookup"><span data-stu-id="089f5-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="089f5-694">В поле **Выбор языка** выберите **Пользовательские предпочтения**, чтобы выполнить отчет в выбранном пользователем языке.</span><span class="sxs-lookup"><span data-stu-id="089f5-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="089f5-695">В поле **Предпочтения языкового стандарта** выберите **Пользовательские предпочтения**, чтобы выполнить отчет в выбранном пользователем языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="089f5-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="089f5-696">Сведения об указании языков и региональных параметров для процесса ER см. в разделе [Разработка многоязычных отчетов](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Настройка параметров языка и региональных параметров для созданного отчета в конструкторе операций ER](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="089f5-698">В дереве формата разверните корневой узел, а затем выберите **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="089f5-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="089f5-699">На вкладке **Формат** в поле **направление репликации** выберите **Без репликации**, так как для одной анкеты не предполагается наличие нескольких групп результатов.</span><span class="sxs-lookup"><span data-stu-id="089f5-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Определение направления репликации для элементов формата диапазона в конструкторе операции ER](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="089f5-701">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="089f5-702">Определение привязки данных для заголовка отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-702">Define the data binding for a report title</span></span>

<span data-ttu-id="089f5-703">Необходимо указать привязку данных для элемента формата, который используется для заполнения заголовка созданного отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="089f5-704">На странице **Конструктор форматов** на вкладке **сопоставление** справа выберите элемент **Report\\ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="089f5-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="089f5-705">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="089f5-706">В редакторе формул выберите **Перевести**.</span><span class="sxs-lookup"><span data-stu-id="089f5-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="089f5-707">В диалоговом окне **Перевод текста** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="089f5-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="089f5-708">В поле **Код метки** введите **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="089f5-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="089f5-709">В поле **Текст на языке по умолчанию** введите **Отчет "Анкеты"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="089f5-710">Выберите **Перевести**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="089f5-711">Выберите **перевести**, чтобы закрыть диалоговое окно **Перевод текста**.</span><span class="sxs-lookup"><span data-stu-id="089f5-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="089f5-712">Закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-712">Close the formula editor.</span></span>

    ![Настройка привязки для заполнения заголовка созданного отчета](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="089f5-714">Этот метод можно использовать для создания любых других меток, зависящих от языка текущего шаблона.</span><span class="sxs-lookup"><span data-stu-id="089f5-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="089f5-715">Сведения о том, как можно перевести метки одной конфигурации ER на все поддерживаемые языки, см. в разделе [Разработка многоязычных отчетов](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="089f5-716">Просмотр источника данных модели</span><span class="sxs-lookup"><span data-stu-id="089f5-716">Review model data source</span></span>

1. <span data-ttu-id="089f5-717">На странице **конструктор формата** на вкладке **Сопоставление** выберите источник данных <a name="ModelDSName"></a>**модель**, представляющий базовую модель данных для этого формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="089f5-718">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="089f5-718">Select **Edit**.</span></span>
3. <span data-ttu-id="089f5-719">Просмотрите сведения в диалоговом окне **Свойства источника данных**.</span><span class="sxs-lookup"><span data-stu-id="089f5-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="089f5-720">Этот источник данных представляет версию 1 компонента модели данных **анкеты**, которая находится в конфигурации ER **Модель Анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Свойства источника данных модели в конструкторе операций электронной отчетности](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="089f5-722">Привязка элементов формата к полям источника данных</span><span class="sxs-lookup"><span data-stu-id="089f5-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="089f5-723">Чтобы указать способ заполнения шаблона в среде выполнения, необходимо связать каждый элемент формата, связанный с соответствующим именем Excel, с одним полем источника данных этого формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="089f5-724">На странице **конструктор формата** в дереве формата выберите элемент формата **Report\\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="089f5-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="089f5-725">На вкладке **Сопоставление** выберите поле источника данных **model.CompanyName** типа **строка**.</span><span class="sxs-lookup"><span data-stu-id="089f5-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="089f5-726">Выберите **Связать** для ввода названия компании в шаблон.</span><span class="sxs-lookup"><span data-stu-id="089f5-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="089f5-727">В дереве формата выберите элемент **Report\\Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="089f5-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="089f5-728">На вкладке **Сопоставление** выберите поле источника данных **model.Questionnaire** типа **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="089f5-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="089f5-729">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="089f5-729">Select **Bind**.</span></span>
7. <span data-ttu-id="089f5-730">Выберите **Показать сведения** для просмотра сведений об элементах формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="089f5-731">Элемент формата диапазона **анкета** настраивается как реплицируемый по вертикали.</span><span class="sxs-lookup"><span data-stu-id="089f5-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="089f5-732">При привязке к источнику данных типа **списка записей** соответствующий диапазон **анкета** шаблона Excel повторяется для каждой записи связанного источника данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Привязка элемента формата диапазона Анкета к соответствующим источникам данных Список записей в конструкторе операций ER](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="089f5-734">Поскольку диапазон **анкета** шаблона Excel определяется между строками с 5 по 14, эти строки повторяются для каждой отчетной анкеты.</span><span class="sxs-lookup"><span data-stu-id="089f5-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Строки в шаблоне Excel, которые будут повторяться в сформированном отчете для каждой записи источников данных Список записей](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="089f5-736">Настройте аналогичные привязки для остальных элементов формата, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="089f5-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="089f5-737">В этой таблице информация в столбце "путь источника данных" предполагает, что функция ER [относительный путь](relative-path-data-bindings-er-models-format.md) включена.</span><span class="sxs-lookup"><span data-stu-id="089f5-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="089f5-738">Путь к элементу формата</span><span class="sxs-lookup"><span data-stu-id="089f5-738">Format element path</span></span>                                      | <span data-ttu-id="089f5-739">Путь иcточника данных</span><span class="sxs-lookup"><span data-stu-id="089f5-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="089f5-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="089f5-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="089f5-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="089f5-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="089f5-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="089f5-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="089f5-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="089f5-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="089f5-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="089f5-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="089f5-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="089f5-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="089f5-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="089f5-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="089f5-747">**\@.Active**, где **\@** это **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="089f5-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="089f5-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="089f5-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="089f5-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="089f5-749">**\@.Code**</span></span> |
    | <span data-ttu-id="089f5-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="089f5-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="089f5-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="089f5-751">**\@.Description**</span></span> |
    | <span data-ttu-id="089f5-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="089f5-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="089f5-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="089f5-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="089f5-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="089f5-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="089f5-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="089f5-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="089f5-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="089f5-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="089f5-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="089f5-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="089f5-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="089f5-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="089f5-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="089f5-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="089f5-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="089f5-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="089f5-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="089f5-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="089f5-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="089f5-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="089f5-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="089f5-763">**\@.Question**</span></span> |
    | <span data-ttu-id="089f5-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="089f5-765">**\@.CollectionSequenceNumber**, где **\@** это **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="089f5-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="089f5-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="089f5-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="089f5-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="089f5-767">**\@.Id**</span></span> |
    | <span data-ttu-id="089f5-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="089f5-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="089f5-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="089f5-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="089f5-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="089f5-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="089f5-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="089f5-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="089f5-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="089f5-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="089f5-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="089f5-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="089f5-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="089f5-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="089f5-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="089f5-775">**\@.Text**</span></span> |
    | <span data-ttu-id="089f5-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="089f5-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="089f5-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="089f5-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="089f5-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="089f5-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="089f5-779">**\@.CorrectAnswer**, где **\@** это **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="089f5-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="089f5-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="089f5-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="089f5-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="089f5-781">**\@.Points**</span></span> |
    | <span data-ttu-id="089f5-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="089f5-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="089f5-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="089f5-783">**\@.Text**</span></span> |

9. <span data-ttu-id="089f5-784">Закончив, выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="089f5-785">На следующем рисунке показано конечное состояние настроенных привязок данных на странице **конструктор формата**.</span><span class="sxs-lookup"><span data-stu-id="089f5-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Настроенные привязи данных в конструкторе операций ER](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="089f5-787">Вся коллекция указанных источников данных и привязок представляет компонент сопоставления формата для настроенного формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="089f5-788">Это сопоставление формата вызывается при выполнении настроенного формата для создания отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="089f5-789">Выполните созданный формат из ER</span><span class="sxs-lookup"><span data-stu-id="089f5-789">Run a designed format from ER</span></span>

<span data-ttu-id="089f5-790">Теперь можно запустить созданный формат для целей тестирования на странице **конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="089f5-791">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-792">На странице **Конфигурации** в дереве конфигураций разверните **Модель анкеты**, и затем выберите **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="089f5-793">Выберите **конструктор** для версии формата, имеющей статус **черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="089f5-794">На странице **Конструктор формата** выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="089f5-795">В диалоговом окне **Параметры ER** на экспресс-вкладке **Включаемые записи** настройте параметры фильтрации таким образом, чтобы включалась только анкета **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="089f5-796">Выберите **ОК**, чтобы подтвердить параметр фильтрации.</span><span class="sxs-lookup"><span data-stu-id="089f5-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="089f5-797">Выберите **OK**, чтобы выполнить отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="089f5-798">Просмотрите созданный отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-798">Review the generated report.</span></span>

<span data-ttu-id="089f5-799">По [умолчанию](electronic-reporting-destinations.md#default-behavior), созданный отчет доставляется в виде файла Excel, который можно загрузить.</span><span class="sxs-lookup"><span data-stu-id="089f5-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="089f5-800">На следующем рисунке показаны две страницы созданного отчета в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="089f5-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Пример созданного отчета в формате Excel, страница 1](./media/er-quick-start1-report1a.png)

![Пример созданного отчета в формате Excel, страница 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="089f5-803">Настройте созданный формат</span><span class="sxs-lookup"><span data-stu-id="089f5-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="089f5-804">Изменение формата для изменения имени созданного документа</span><span class="sxs-lookup"><span data-stu-id="089f5-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="089f5-805">По умолчанию созданный документ называется с использованием псевдонима текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="089f5-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="089f5-806">Изменяя формат, можно изменить это поведение, чтобы имя созданного документа основывалось на пользовательской логике.</span><span class="sxs-lookup"><span data-stu-id="089f5-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="089f5-807">Например, имя созданного документа может основываться на текущих дате и времени сеанса и на заголовке отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="089f5-808">На странице **Конструктор формата** выберите корневого элемента **Отчет**.</span><span class="sxs-lookup"><span data-stu-id="089f5-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="089f5-809">На вкладке **Сопоставление** выберите **редактировать имя файла**.</span><span class="sxs-lookup"><span data-stu-id="089f5-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="089f5-810">В поле **Формула** введите **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="089f5-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="089f5-811">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="089f5-812">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="089f5-813">Изменение формата для изменения порядка вопросов</span><span class="sxs-lookup"><span data-stu-id="089f5-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="089f5-814">Вопросы в сформированном отчете неправильно упорядочены.</span><span class="sxs-lookup"><span data-stu-id="089f5-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="089f5-815">Заказ можно изменить, изменив формат.</span><span class="sxs-lookup"><span data-stu-id="089f5-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="089f5-816">На странице **Конструктор формата** выберите корневого элемента **Отчет**.</span><span class="sxs-lookup"><span data-stu-id="089f5-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="089f5-817">На вкладке **Сопоставление** в дереве формата разверните **Report\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="089f5-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Элемент формата вопроса типа диапазона в конструкторе операции ER](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="089f5-819">На вкладке **Сопоставление** выберите **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="089f5-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="089f5-820">Выберите **Добавить** \> **Функции\\вычисляемое поле**, а затем в поле **имя** введите **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="089f5-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="089f5-821">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="089f5-822">В редакторе формул в поле **Формула** введите **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** для упорядочения списка вопросов по текущей анкете по порядковому номеру заказа.</span><span class="sxs-lookup"><span data-stu-id="089f5-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="089f5-823">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="089f5-824">Нажмите кнопку **ОК**, чтобы завершить ввод нового вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="089f5-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="089f5-825">На вкладке **Сопоставление** выберите **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="089f5-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="089f5-826">В дереве формата выберите **Excel\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="089f5-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="089f5-827">Выберите **Связать**, а затем подтвердите, что текущий путь **model.Questionnaire.Questions** заменяется новым путем **model.Questionnaire.OrderedQuestions** во всех привязках вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="089f5-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="089f5-828">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-828">Select **Save**.</span></span>

![Привязка элемента формата вопроса к настроенному источнику данных OrderedQuestions в конструкторе операций ER](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="089f5-830">Выполните измененный формат из ER</span><span class="sxs-lookup"><span data-stu-id="089f5-830">Run a modified format from ER</span></span>

<span data-ttu-id="089f5-831">Теперь для целей тестирования можно запустить измененный формат из платформы ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="089f5-832">На странице **Конструктор формата** выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="089f5-833">В диалоговом окне **Параметры ER** на экспресс-вкладке **Включаемые записи** настройте параметры фильтрации таким образом, чтобы включалась только анкета **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="089f5-834">Выберите **ОК**, чтобы подтвердить параметр фильтрации.</span><span class="sxs-lookup"><span data-stu-id="089f5-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="089f5-835">Выберите **OK**, чтобы выполнить отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="089f5-836">Просмотрите созданный отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-836">Review the generated report.</span></span>

<span data-ttu-id="089f5-837">На следующем рисунке показан созданный отчет в формате Excel, в котором вопросы правильно упорядочены.</span><span class="sxs-lookup"><span data-stu-id="089f5-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Сформированный отчет в формате Excel, в котором правильно упорядочены вопросы](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="089f5-839">Завершение разработки формата</span><span class="sxs-lookup"><span data-stu-id="089f5-839">Complete the format design</span></span>

1. <span data-ttu-id="089f5-840">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-841">На странице **Конфигурации** в дереве конфигураций разверните **Модель анкеты**, и затем выберите **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="089f5-842">На экспресс-вкладке **Версии** выберите версию конфигурации со статусом **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="089f5-843">Выберите **Изменить статус** \> **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="089f5-844">Статус версии 1.1 этой конфигурации изменяется с **черновик** на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="089f5-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="089f5-845">Версия 1.1 больше не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="089f5-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="089f5-846">Эта версия содержит настроенный формат и может использоваться для печати пользовательского отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="089f5-847">Версия 1.2 этой конфигурации создана и имеет статус **черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="089f5-848">Эту версию можно изменить для корректировки формата вашего отчета **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Редактируемая конфигурация электронной отчетности на странице конфигурации](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="089f5-850">Настроенный формат является макетом отчета **Анкета** и не содержит связей с артефактами, предназначенными только для Финансы.</span><span class="sxs-lookup"><span data-stu-id="089f5-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="089f5-851">Разработка артефактов приложений для вызова созданного отчета</span><span class="sxs-lookup"><span data-stu-id="089f5-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="089f5-852">Пользователь, работающий в роли системного администратора, должен разработать новую логику, чтобы настроенный формат ER можно было вызывать из пользовательского интерфейса приложения для создания пользовательского отчета.</span><span class="sxs-lookup"><span data-stu-id="089f5-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="089f5-853">В настоящее время в ER не предусмотрена возможность настройки этого типа логики.</span><span class="sxs-lookup"><span data-stu-id="089f5-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="089f5-854">Поэтому требуются некоторые технологические работы.</span><span class="sxs-lookup"><span data-stu-id="089f5-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="089f5-855">Чтобы разработать новую логику, необходимо развернуть топологию, которая поддерживает непрерывную сборку.</span><span class="sxs-lookup"><span data-stu-id="089f5-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="089f5-856">Дополнительные сведения см. в разделе [Развертывание топологий, которые поддерживают непрерывное построение и автоматизацию тестирования](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="089f5-857">Кроме того, необходим доступ к среде разработки для этой топологии.</span><span class="sxs-lookup"><span data-stu-id="089f5-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="089f5-858">Дополнительные сведения о доступном API электронной отчетности см. в разделе [API платформы электронной отчетности](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="089f5-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="089f5-859">Изменение исходного кода</span><span class="sxs-lookup"><span data-stu-id="089f5-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="089f5-860">Добавление класса контракта данных</span><span class="sxs-lookup"><span data-stu-id="089f5-860">Add a data contract class</span></span>

<span data-ttu-id="089f5-861">Добавьте новый класс **QuestionnairesErReportContract** в проект Microsoft Visual Studio и создайте код, который определяет контракт данных, который должен использоваться для выполнения настроенного формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="089f5-862">Добавление класса конструктора пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="089f5-862">Add a UI builder class</span></span>

<span data-ttu-id="089f5-863">Добавьте новый класс **QuestionnairesErReportUIBuilder** в проект Visual Studio и напишите код для создания диалогового окна среды выполнения, которое будет использоваться для поиска кода сопоставления формата для формата ER, который должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="089f5-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="089f5-864">Предоставленный код выполняет поиск только в тех форматах ER, которые содержат источник данных типа **модели данных** , относящегося к модели данных **[Анкеты](#DataModeName)** с использованием определения **[Корень](#RootDefinitionName)**.</span><span class="sxs-lookup"><span data-stu-id="089f5-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="089f5-865">Кроме того, можно использовать точки интеграции ER для фильтрации форматов ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="089f5-866">Дополнительные сведения см. в [API для отображения поиска сопоставления формата](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="089f5-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="089f5-867">Добавление класса поставщика данных</span><span class="sxs-lookup"><span data-stu-id="089f5-867">Add a data provider class</span></span>

<span data-ttu-id="089f5-868">Добавьте новый класс **QuestionnairesErReportDP** в проект Visual Studio и напишите код, который вводит поставщика данных, который должен использоваться для выполнения настроенного формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="089f5-869">Предоставленный код включает только контракт данных для этого поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="089f5-870">Добавление файла меток</span><span class="sxs-lookup"><span data-stu-id="089f5-870">Add a labels file</span></span>

<span data-ttu-id="089f5-871">Добавьте новый файл меток **QuestionnairesErReportLabels\_en-US** в проект Visual Studio и укажите следующие метки для новых ресурсов пользовательского интерфейса:</span><span class="sxs-lookup"><span data-stu-id="089f5-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="089f5-872">Метка **\@QuestionnairesReport** для нового пункта меню, которая содержит следующий текст на американском английском (en-US): **Отчет "Анкеты" (на платформе ER)**</span><span class="sxs-lookup"><span data-stu-id="089f5-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="089f5-873">Метка **\@QuestionnairesReportBatchJobDescription** для заголовка пакетного задания, если выбранный формат ER запланирован на выполнение в виде пакетного задания</span><span class="sxs-lookup"><span data-stu-id="089f5-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="089f5-874">Добавление класса службы отчетов</span><span class="sxs-lookup"><span data-stu-id="089f5-874">Add a report service class</span></span>

<span data-ttu-id="089f5-875">Добавьте новый класс **QuestionnairesErReportService** в свой проект Visual Studio и напишите код, который вызывает формат ER, идентифицирует его по коду сопоставления формата и предоставляет контракт данных в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="089f5-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="089f5-876">Если необходимо использовать формат ER, который использует данные приложений, необходимо настроить источник данных типа **модели данных**, в сопоставлении формата.</span><span class="sxs-lookup"><span data-stu-id="089f5-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="089f5-877">Этот источник данных ссылается на определенную часть указанной модели данных, используя одно определение корня.</span><span class="sxs-lookup"><span data-stu-id="089f5-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="089f5-878">При выполнении формата ER он вызывает этот источник данных для получения соответствующего сопоставления модели ER, которое настроено для данной модели и определения корня.</span><span class="sxs-lookup"><span data-stu-id="089f5-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="089f5-879">Все сведения, которые могут быть подготовлены в исходном коде и магазине в рамках контракта данных, можно передавать в выполняемый формат ER с помощью сопоставления модели ER с этим типом.</span><span class="sxs-lookup"><span data-stu-id="089f5-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="089f5-880">В сопоставлении модели ER необходимо настроить источник данных типа **объекта**, относящегося к классу **[QuestionnairesErReportContract](#DataContractClass)**.</span><span class="sxs-lookup"><span data-stu-id="089f5-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="089f5-881">Чтобы определить сопоставление модели, необходимо указать источник данных, вызывающий это сопоставление модели.</span><span class="sxs-lookup"><span data-stu-id="089f5-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="089f5-882">В указанном коде — это источник данных, указанный константой **ERModelDataSourceName**, которая имеет значение **[модели](#ModelDSName)**.</span><span class="sxs-lookup"><span data-stu-id="089f5-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="089f5-883">Чтобы определить источник данных, используемый для предоставления контракта данных в сопоставлении модели, необходимо указать имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="089f5-884">В указанном коде — это имя, указанный константой **ParametersDataSourceName**, которая имеет значение <a name="DataContractDSName"></a>**RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="089f5-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="089f5-885">В новой среде может потребоваться обновление метаданных ER таким образом, чтобы класс данного типа был доступен в конструкторе сопоставления моделей ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="089f5-886">Дополнительные сведения см. в разделе [Настройка платформы электронной отчетности](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="089f5-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="089f5-887">Добавление класса controller отчетов</span><span class="sxs-lookup"><span data-stu-id="089f5-887">Add a report controller class</span></span>

<span data-ttu-id="089f5-888">Добавьте новый класс **QuestionnairesErReportController** в проект Visual Studio и напишите код, который запускает формат ER в синхронном режиме или в пакетном режиме, согласно предпочтениям, в диалоговом окне, созданном на основе логики предоставленного класса **QuestionnairesErReportUIBuilder**.</span><span class="sxs-lookup"><span data-stu-id="089f5-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="089f5-889">Добавление пункта меню</span><span class="sxs-lookup"><span data-stu-id="089f5-889">Add a menu item</span></span>

<span data-ttu-id="089f5-890">Добавьте новый пункт меню **QuestionnairesErReport** в проект Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="089f5-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="089f5-891">В свойстве **объекта** этот пункт меню относится к классу **QuestionnairesErReportController** и используется для указания разрешения пользователя для выбора и выполнения формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="089f5-892">В свойстве **Метка** этот пункт меню относится к метке **\@QuestionnairesReport**, которая была создана ранее, так что правильный текст представлен в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="089f5-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="089f5-893">Добавление пункта меню в меню</span><span class="sxs-lookup"><span data-stu-id="089f5-893">Add a menu item to a menu</span></span>

<span data-ttu-id="089f5-894">Добавьте существующее меню **KM** в проект Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="089f5-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="089f5-895">В это меню необходимо добавить новую номенклатуру **QuestionnairesErReport** типа **Выпуск**.</span><span class="sxs-lookup"><span data-stu-id="089f5-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="089f5-896">Эта номенклатура должна ссылаться на пункт меню **QuestionnairesErReport**, который описан в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="089f5-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="089f5-897">Сборка проекта Visual Studio</span><span class="sxs-lookup"><span data-stu-id="089f5-897">Build a Visual Studio project</span></span>

<span data-ttu-id="089f5-898">Соберите проект, чтобы сделать новый пункт доступным для пользователей.</span><span class="sxs-lookup"><span data-stu-id="089f5-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="089f5-899">Выполните формат из приложения</span><span class="sxs-lookup"><span data-stu-id="089f5-899">Run a format from the application</span></span>

1. <span data-ttu-id="089f5-900">Перейдите к **Анкета** \> **Разработка** \> **Отчет "Анкеты" (на платформе ER)**.</span><span class="sxs-lookup"><span data-stu-id="089f5-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Выбор пункта меню "Отчет "Анкеты" (на платформе ER) в модуле "Анкета" для выполнения настроенного формата ER](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="089f5-902">В диалоговом окне в поле **сопоставление формата** выберите **Отчет "Анкеты"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="089f5-903">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-903">Select **OK**.</span></span>
4. <span data-ttu-id="089f5-904">В диалоговом окне **Параметры электронной отчетности** на экспресс-вкладке **Включаемые записи** настройте параметры фильтрации таким образом, чтобы включалась только анкета **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="089f5-905">Выберите **ОК**, чтобы подтвердить параметр фильтрации.</span><span class="sxs-lookup"><span data-stu-id="089f5-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="089f5-906">Выберите **OK**, чтобы выполнить отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-906">Select **OK** to run the report.</span></span>

    ![Указание критерии выбора в диалоговом окне электронной отчетности](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="089f5-908">Просмотрите созданный отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="089f5-909">Настройка созданного решения ER</span><span class="sxs-lookup"><span data-stu-id="089f5-909">Tune a designed ER solution</span></span>

<span data-ttu-id="089f5-910">Можно изменить настроенное решение ER таким образом, чтобы оно использовало класс поставщика данных, который был создан для доступа к сведениям о выполняемом формате электронной отчетности, и таким образом, и чтобы оно вводило имя этого формата ER в созданный отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="089f5-911">Изменение сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="089f5-912">Добавление источников данных для доступа к объекту контракта данных</span><span class="sxs-lookup"><span data-stu-id="089f5-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="089f5-913">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-914">На странице **Конфигурации** в дереве конфигураций разверните **Модель анкеты**, и затем выберите **Сопоставление анкеты**.</span><span class="sxs-lookup"><span data-stu-id="089f5-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="089f5-915">Выберите **конструктор**, чтобы открыть страницу **Сопоставление модели и источника данных**.</span><span class="sxs-lookup"><span data-stu-id="089f5-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="089f5-916">Выберите **конструктор**, чтобы открыть выбранное сопоставление в конструкторе сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="089f5-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="089f5-917">На странице **Конструктор сопоставления модели** в области **Типы источников данных** выберите **Dynamics 365 for Operations\\Объект**.</span><span class="sxs-lookup"><span data-stu-id="089f5-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="089f5-918">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="089f5-919">В диалоговом окне в поле **Имя** введите **[RunTimeParameters](#DataContractDSName)**, как определено в исходном коде класса **QuestionnairesErReportService**.</span><span class="sxs-lookup"><span data-stu-id="089f5-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="089f5-920">В поле **Класс** введите **[QuestionnairesErReportContract](#DataContractClass)**, которые были кодированы ранее.</span><span class="sxs-lookup"><span data-stu-id="089f5-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="089f5-921">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-921">Select **OK**.</span></span>
10. <span data-ttu-id="089f5-922">Разверните **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="089f5-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="089f5-923">Добавленный источник данных содержит информацию о коде записи для сопоставления формата запуска ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Добавлен источник данных в конструкторе сопоставления модели ER](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="089f5-925">Добавление источника данных для доступа к записям сопоставления формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="089f5-926">Продолжайте редактировать выбранное сопоставление модели путем добавления источника данных для доступа к записям сопоставления формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="089f5-927">На странице **Конструктор сопоставления модели** в области **Типы источников данных** выберите **Dynamics 365 for Operations\\Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="089f5-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="089f5-928">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="089f5-929">В диалоговом окне в поле **Имя** введите **ER1**.</span><span class="sxs-lookup"><span data-stu-id="089f5-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="089f5-930">В поле **Таблица** введите **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="089f5-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="089f5-931">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="089f5-932">Добавление источника данных для доступа к записи сопоставления формата выполняемого формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="089f5-933">Продолжайте редактировать выбранное сопоставление модели путем добавления источника данных для доступа к записи сопоставления формата для выполняемого формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="089f5-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="089f5-934">На странице **Конструктор сопоставления модели** в области **Типы источников данных** выберите **Функции\\Вычисляемое поле**.</span><span class="sxs-lookup"><span data-stu-id="089f5-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="089f5-935">В области **источники данных** выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="089f5-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="089f5-936">В диалоговом окне в поле **Имя** введите **ER2**.</span><span class="sxs-lookup"><span data-stu-id="089f5-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="089f5-937">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="089f5-938">В редакторе формул в поле **Формула** введите **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="089f5-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="089f5-939">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="089f5-940">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="089f5-941">Введите имя выполняемого формата электронной отчетности в модель данных</span><span class="sxs-lookup"><span data-stu-id="089f5-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="089f5-942">Продолжайте изменять выбранное сопоставление модели таким образом, чтобы в модель данных вводилось имя текущего формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="089f5-943">На странице **Конструктор сопоставления модели** в области **Модель данных** разверните **ExecutionContext**, а затем выберите **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="089f5-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="089f5-944">В области **модель данных** выберите **Изменить**, чтобы настроить привязку данных для поля выбранной модели данных.</span><span class="sxs-lookup"><span data-stu-id="089f5-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="089f5-945">В редакторе формул в поле **Формула** введите **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="089f5-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="089f5-946">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="089f5-947">Поскольку используется поле **FormatName**, настроенное сопоставление модели теперь предоставляет имя формата ER, который вызывает сопоставление модели во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="089f5-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Привязка поля модели данных к методу добавленного источника данных в конструкторе сопоставления модели ER](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="089f5-949">Завершение разработки сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="089f5-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="089f5-950">На странице **конструктора сопоставления модели** нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="089f5-951">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="089f5-951">Close the page.</span></span>
3. <span data-ttu-id="089f5-952">Закройте страницу сопоставлений моделей.</span><span class="sxs-lookup"><span data-stu-id="089f5-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="089f5-953">На странице **конфигурации** в дереве конфигурации убедитесь, что конфигурация **Сопоставление анкеты** все еще выбрана.</span><span class="sxs-lookup"><span data-stu-id="089f5-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="089f5-954">Затем, на экспресс-вкладке **Версии** выберите версию конфигурации со статусом **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="089f5-955">Выберите **Изменить статус** \> **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="089f5-956">Статус версии 1.2 этой конфигурации изменяется с **черновик** на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="089f5-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="089f5-957">Версия 1.2 больше не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="089f5-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="089f5-958">Эта версия содержит настроенное сопоставление модели и может использоваться в качестве основы для других конфигураций ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="089f5-959">Версия 1.3 этой конфигурации создана и имеет статус **черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="089f5-960">Эту версию можно изменить для корректировки сопоставления модели **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="089f5-961">Изменение формата</span><span class="sxs-lookup"><span data-stu-id="089f5-961">Modify a format</span></span>

<span data-ttu-id="089f5-962">Можно изменить настроенный формат ER так, чтобы имя отображалось в нижнем колонтитуле отчета, созданного при выполнении формата ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="089f5-963">Добавление нового элемента формата</span><span class="sxs-lookup"><span data-stu-id="089f5-963">Add a new format element</span></span>

1. <span data-ttu-id="089f5-964">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-965">На странице **Конфигурации** в дереве конфигураций разверните **Модель анкеты**, и затем выберите **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="089f5-966">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="089f5-966">Select **Designer**.</span></span>
4. <span data-ttu-id="089f5-967">На странице **Конструктор формата** выберите корневого элемента **Отчет**.</span><span class="sxs-lookup"><span data-stu-id="089f5-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="089f5-968">Выберите **Добавить**, чтобы добавить новый вложенный элемент формата для выбранного корневого элемента **Отчет**.</span><span class="sxs-lookup"><span data-stu-id="089f5-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="089f5-969">Выберите **Excel\\Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="089f5-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="089f5-970">В поле **Имя** введите **Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="089f5-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="089f5-971">Выберите **Отчет\Нижний колонтитул** и затем щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="089f5-972">Выберите **Текст\\Строка**.</span><span class="sxs-lookup"><span data-stu-id="089f5-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="089f5-973">Связывание добавленного элемента формата</span><span class="sxs-lookup"><span data-stu-id="089f5-973">Bind the added format element</span></span>

1. <span data-ttu-id="089f5-974">На странице **Конструктор форматов** на вкладке **сопоставление** в дереве формата, для активного элемента **Нижний колонтитул\\Строка** выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="089f5-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="089f5-975">В редакторе формул в поле **Формула** введите **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="089f5-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="089f5-976">Выберите **Сохранить** и закройте редактор формул.</span><span class="sxs-lookup"><span data-stu-id="089f5-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="089f5-977">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-977">Select **Save**.</span></span>

<span data-ttu-id="089f5-978">Настроенный формат был изменен таким образом, что его имя будет введено в нижнем колонтитуле созданного отчета с использованием элемента **Нижний колонтитул\\Строка**.</span><span class="sxs-lookup"><span data-stu-id="089f5-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Добавление элемента формата нижнего колонтитула к настроенному формату в конструкторе операций ER](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="089f5-980">Завершение разработки формата</span><span class="sxs-lookup"><span data-stu-id="089f5-980">Complete the format design</span></span>

1. <span data-ttu-id="089f5-981">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="089f5-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="089f5-982">На странице **конфигурации** в дереве конфигурации убедитесь, что конфигурация **Отчет "Анкета"** все еще выбрана.</span><span class="sxs-lookup"><span data-stu-id="089f5-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="089f5-983">Затем, на экспресс-вкладке **Версии** выберите версию конфигурации со статусом **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="089f5-984">Выберите **Изменить статус** \> **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="089f5-985">Статус версии 1.2 этой конфигурации изменяется с **черновик** на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="089f5-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="089f5-986">Версия 1.2 больше не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="089f5-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="089f5-987">Эта версия содержит настроенную формат и может использоваться в качестве основы для других конфигураций ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="089f5-988">Версия 1.3 этой конфигурации создана и имеет статус **черновик**.</span><span class="sxs-lookup"><span data-stu-id="089f5-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="089f5-989">Эту версию можно изменить для корректировки отчета **Анкета**.</span><span class="sxs-lookup"><span data-stu-id="089f5-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="089f5-990">Выполните формат из приложения</span><span class="sxs-lookup"><span data-stu-id="089f5-990">Run a format from the application</span></span>

1. <span data-ttu-id="089f5-991">Перейдите к **Анкета** \> **Разработка** \> **Отчет "Анкеты" (на платформе ER)**.</span><span class="sxs-lookup"><span data-stu-id="089f5-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="089f5-992">В диалоговом окне в поле **сопоставление формата** выберите **Отчет "Анкеты"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="089f5-993">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-993">Select **OK**.</span></span>
4. <span data-ttu-id="089f5-994">В диалоговом окне **Параметры ER** на экспресс-вкладке **Включаемые записи** настройте параметры фильтрации таким образом, чтобы включалась только анкета **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="089f5-995">Выберите **ОК**, чтобы подтвердить параметр фильтрации.</span><span class="sxs-lookup"><span data-stu-id="089f5-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="089f5-996">Выберите **OK**, чтобы выполнить отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="089f5-997">Просмотрите созданный отчет в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="089f5-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="089f5-998">Обратите внимание, что нижний колонтитул созданного отчета содержит имя формата ER, который был использован при его создании.</span><span class="sxs-lookup"><span data-stu-id="089f5-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Созданный отчет в формате Excel](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="089f5-1000">Выполните формат из ER</span><span class="sxs-lookup"><span data-stu-id="089f5-1000">Run a format from ER</span></span>

1. <span data-ttu-id="089f5-1001">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="089f5-1002">На странице **Конфигурации** в дереве конфигураций разверните **Модель анкеты**, и затем выберите **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="089f5-1003">В области действий выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="089f5-1004">В диалоговом окне **Параметры электронной отчетности** на экспресс-вкладке **Включаемые записи** настройте параметры фильтрации таким образом, чтобы включалась только анкета **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="089f5-1005">Выберите **ОК**, чтобы подтвердить параметр фильтрации.</span><span class="sxs-lookup"><span data-stu-id="089f5-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="089f5-1006">Выберите **OK**, чтобы выполнить отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="089f5-1007">Просмотрите созданный отчет в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="089f5-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="089f5-1008">Обратите внимание, что нижний колонтитул созданного отчета не содержит имени формата ER, использованного при создании, поскольку объект контракта данных не был передан в выполняемое сопоставление модели при вызове из формата ER, выполняемого из ER.</span><span class="sxs-lookup"><span data-stu-id="089f5-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="089f5-1009">Настройка назначения формата для предварительного просмотра на экране</span><span class="sxs-lookup"><span data-stu-id="089f5-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="089f5-1010">Перейдите в раздел **Управление организацией** \> **Электронная отчетность** \> **Место назначения электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="089f5-1011">На странице **Место назначения электронной отчетности** добавьте запись назначения для настроенного формата ER **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="089f5-1012">На экспресс-вкладке **Назначение файла** настройте **экран** [назначение](er-destination-type-screen.md) для компонента формата **отчет**, который был [добавлен](#AddFormatRootElement) в качестве корневого элемента настроенного формата ER **Отчет "Анкета"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="089f5-1013">На экспресс-вкладке **Параметры преобразования PDF** настройте назначение, чтобы преобразовать отчет в [Формат PDF](electronic-reporting-destinations.md#OutputConversionToPDF), в котором используется **Альбомная** ориентация страницы.</span><span class="sxs-lookup"><span data-stu-id="089f5-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Настройка пользовательского назначения экрана для формата ER на странице назначения электронной отчетности](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="089f5-1015">Выполните формат из приложения, чтобы просмотреть его в виде PDF-документа</span><span class="sxs-lookup"><span data-stu-id="089f5-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="089f5-1016">Перейдите к **Анкета** \> **Разработка** \> **Отчет "Анкеты" (на платформе ER)**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="089f5-1017">В диалоговом окне в поле **сопоставление формата** выберите **Отчет "Анкеты"**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="089f5-1018">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1018">Select **OK**.</span></span>
4. <span data-ttu-id="089f5-1019">В диалоговом окне **Параметры электронной отчетности** на экспресс-вкладке **Включаемые записи** настройте параметры фильтрации таким образом, чтобы включалась только анкета **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="089f5-1020">Выберите **ОК**, чтобы подтвердить параметр фильтрации.</span><span class="sxs-lookup"><span data-stu-id="089f5-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="089f5-1021">Обратите внимание, что на экспресс-вкладке **назначения** поле **Вывод** имеет значение **экран**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="089f5-1022">Если необходимо изменить настроенное назначение, выберите **изменить**.</span><span class="sxs-lookup"><span data-stu-id="089f5-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Диалоговое окно выполнения отчета ER, в котором можно изменить настроенное назначение](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="089f5-1024">Выберите **OK**, чтобы выполнить отчет.</span><span class="sxs-lookup"><span data-stu-id="089f5-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="089f5-1025">Просмотрите созданный отчет в формате PDF.</span><span class="sxs-lookup"><span data-stu-id="089f5-1025">Review the generated report in PDF format.</span></span>

    ![Предварительный просмотр на экране созданного отчета в формате PDF](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="089f5-1027">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="089f5-1027">Additional resources</span></span>

- [<span data-ttu-id="089f5-1028">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="089f5-1029">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="089f5-1030">Разработка многоязычных отчетов</span><span class="sxs-lookup"><span data-stu-id="089f5-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="089f5-1031">API платформы электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="089f5-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="089f5-1032">Функция CASE</span><span class="sxs-lookup"><span data-stu-id="089f5-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="089f5-1033">Функция CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="089f5-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="089f5-1034">Функция DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="089f5-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="089f5-1035">Функция FILTER</span><span class="sxs-lookup"><span data-stu-id="089f5-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="089f5-1036">Функция FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="089f5-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="089f5-1037">Функция FORMAT</span><span class="sxs-lookup"><span data-stu-id="089f5-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="089f5-1038">Функция IF</span><span class="sxs-lookup"><span data-stu-id="089f5-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="089f5-1039">Функция ORDERBY</span><span class="sxs-lookup"><span data-stu-id="089f5-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="089f5-1040">Функция SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="089f5-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
