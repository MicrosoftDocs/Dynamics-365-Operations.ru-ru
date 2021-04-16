---
title: Подавлять элементы управления содержимым Word в сформированных отчетах
description: В этой теме объясняется, как настроить формат электронной отчетности (ER) для создания отчетов в виде файлов Microsoft Word, в которых элементы управления содержимым подавлены.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753612"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="0d6e1-103">Подавлять элементы управления содержимым Word в сформированных отчетах</span><span class="sxs-lookup"><span data-stu-id="0d6e1-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d6e1-104">Чтобы создавать отчеты как документы Microsoft Word, необходимо разработать шаблон для отчетов в качестве документа Word.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="0d6e1-105">Этот шаблон должен содержать элементы управления содержимым Word в качестве заполнителей для данных, которые будут заполнены во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="0d6e1-106">Чтобы использовать документ Word, созданный в качестве шаблона для ваших отчетов, можно [настроить](er-design-configuration-word.md) новое [решение](er-quick-start1-new-solution.md) [электронной отчетности (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="0d6e1-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="0d6e1-107">Решение должно включать [конфигурацию](general-electronic-reporting.md#Configuration) электронной отчетности, которая содержит компонент [формата](general-electronic-reporting.md#FormatComponentOutbound) электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="0d6e1-108">Этот формат электронной отчетности должен быть настроен на использование шаблона, разработанного для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="0d6e1-109">В версии Dynamics 365 Finance 10.0.6 или более поздней можно настроить формулы в формате электронной отчетности, чтобы подавить некоторые элементы управления содержимым Word в создаваемых документах.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="0d6e1-110">Следующие шаги описывают, как пользователь, назначенный для роли "системный администратор" или "Консультант по функциональным возможностям электронной отчетности", может настроить формат ER, который создает отчеты как файлы Word, и подавляет некоторые элементы управления содержимым в созданных отчетах, которые были настроены с помощью шаблона Word.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="0d6e1-111">Эти шаги можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d6e1-112">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="0d6e1-112">Prerequisites</span></span>

<span data-ttu-id="0d6e1-113">Для выполнения этих действий необходимо сначала выполнить шаги из следующих проводников по задачам:</span><span class="sxs-lookup"><span data-stu-id="0d6e1-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="0d6e1-114">Разработка конфигурации для создания отчетов в формате OPENXML</span><span class="sxs-lookup"><span data-stu-id="0d6e1-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="0d6e1-115">Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="0d6e1-116">После выполнения шагов этих проводников по задачам подготавливаются следующие номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="0d6e1-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="0d6e1-117">Формат ER **Пример отчета о листе**, настроенный для создания документа в формате Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="0d6e1-118">Версия [черновик](general-electronic-reporting.md#component-versioning) формата ER **Пример отчета о листе**, помеченного как **Исполняемая**</span><span class="sxs-lookup"><span data-stu-id="0d6e1-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="0d6e1-119">**Электронный** метод платежей, настроенный на использование формата ER **Пример отчета о листе** для обработки платежей поставщикам</span><span class="sxs-lookup"><span data-stu-id="0d6e1-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="0d6e1-120">Необходимо также загрузить и сохранить следующий шаблон для примера отчета:</span><span class="sxs-lookup"><span data-stu-id="0d6e1-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="0d6e1-121">Связанный шаблон 2 отчета о платежах (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="0d6e1-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="0d6e1-122">Проверка загруженного шаблона Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="0d6e1-123">В классическом приложении Word откройте файл шаблона **SampleVendPaymDocReportBounded2.docx**, который был загружен ранее.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="0d6e1-124">Убедитесь, что файл шаблона содержит раздел "Сводка", в котором показаны итоговые суммы платежа для каждого кода валюты, который был удовлетворен в обработанных платежах.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="0d6e1-125">Раздел "Сводка" располагается в отдельной таблице документа Word.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="0d6e1-126">Первая строка этой таблицы содержит заголовки столбцов таблицы в качестве заголовка раздела.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="0d6e1-127">Во второй строке этой таблицы содержится повторяющийся элемент управления содержимым в качестве сведений о разделе.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="0d6e1-128">Этот элемент управления содержимым отображается в поле **SummaryLines** пользовательской XML-части **отчета**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="0d6e1-129">На основе этого сопоставления элемент управления содержимым связывается с элементом **SummaryLines** для редактируемого формата ER.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d6e1-130">Повторяющийся элемент управления содержимым помечается ключом **SummaryLines**, совпадающим с полем пользовательской XML-части, которой он сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Макет шаблона Word](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="0d6e1-132">Выбор существующей конфигурации отчета электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="0d6e1-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="0d6e1-133">Для следующих шагов вы будете повторно использовать существующую конфигурацию ER, которая была настроена при выполнении шагов, описанных ранее в разделе проводников по задачам.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="0d6e1-134">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0d6e1-135">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="0d6e1-136">На странице **Конфигурации** в дереве конфигураций разверните **Модель платежа**, затем выберите **Пример отчета о листе**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="0d6e1-137">Выберите **конструктор**, чтобы изменить черновую версию выбранного формата ER.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="0d6e1-138">Замена текущего шаблона на новый шаблон</span><span class="sxs-lookup"><span data-stu-id="0d6e1-138">Replace the current template with the new template</span></span>

<span data-ttu-id="0d6e1-139">В настоящее время файл SampleVendPaymDocReportBounded.docx используется как шаблон для создания выходных данных в формате Word.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="0d6e1-140">На следующих шагах вы замените этот шаблон Word новым шаблоном Word, SampleVendPaymDocReportBounded2.docx, который загрузили ранее.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="0d6e1-141">На странице **Конструктор форматов** выберите **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="0d6e1-142">На странице **Вложения** выберите **Удалить**, чтобы удалить существующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="0d6e1-143">Выберите **Да**, чтобы подтвердить удаление.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="0d6e1-144">Выберите **Создать** \> **Файл**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="0d6e1-145">Выберите **Обзор**, найдите и выберите файл **SampleVendPaymDocReportBounded2.docx**, загруженный ранее.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="0d6e1-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-146">Select **OK**.</span></span>
7. <span data-ttu-id="0d6e1-147">Закройте страницу **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="0d6e1-148">На странице **Конструктор форматов** в поле **Шаблон** введите или выберите файл **SampleVendPaymDocReportBounded2.docx**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="0d6e1-149">Выполните формат для создания выходных данных Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="0d6e1-150">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="0d6e1-151">На странице **Платежи поставщикам** на вкладке **Список** выберите все платежи.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="0d6e1-152">Выберите **Статус платежа** \> **Нет**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="0d6e1-153">Выберите **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="0d6e1-154">В поле **Способ оплаты** выберите **Электронный**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="0d6e1-155">В поле **Банковский счет** выберите **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="0d6e1-156">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-156">Select **OK**.</span></span>
8. <span data-ttu-id="0d6e1-157">В диалоговом окне **параметров электронной отчетности** нажмите кнопку **ОК** и проанализируйте созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Платежи для обработки на странице платежей поставщикам](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="0d6e1-159">Выходные данные представлены в формате Word и содержат раздел "Сводка".</span><span class="sxs-lookup"><span data-stu-id="0d6e1-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="0d6e1-160">Настройка редактируемого формата для подавления раздела сводки</span><span class="sxs-lookup"><span data-stu-id="0d6e1-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="0d6e1-161">Если необходимо подавлять раздел сводки в созданном документе на основе запроса пользователя, запустившего данный формат ER, необходимо изменить формат файла ER.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="0d6e1-162">Перейдите в раздел **Администрирование организации** \> **Рабочие области** \> **Электронная отчетность** и откройте черновую версию формата ER для редактирования.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="0d6e1-163">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="0d6e1-164">На странице **Конфигурации** в дереве конфигураций разверните **Модель платежа** \> **Пример отчета о листе**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="0d6e1-165">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-165">Select **Designer**.</span></span>
5. <span data-ttu-id="0d6e1-166">На странице **конструктор форматов** разверните **Word** и выберите **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="0d6e1-167">На вкладке **Сопоставление** добавьте новый источник данных для запроса пользователю во время выполнения, следует ли подавлять раздел сводки:</span><span class="sxs-lookup"><span data-stu-id="0d6e1-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="0d6e1-168">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="0d6e1-169">В диалоговом окне **Добавить источник данных** выберите **Общее\Параметр ввода пользователя**, чтобы открыть диалоговое окно **Свойства источника данных параметра пользовательского ввода**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="0d6e1-170">В поле **Имя** введите **uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="0d6e1-171">В поле **Метка** введите **подавление раздела сводки**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="0d6e1-172">В поле **имя типа данных операций** выберите или введите **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="0d6e1-173">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-173">Select **OK**.</span></span>

7. <span data-ttu-id="0d6e1-174">Добавить новый источник данных типа перечисления приложения **NoYes**:</span><span class="sxs-lookup"><span data-stu-id="0d6e1-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="0d6e1-175">Выберите **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="0d6e1-176">В диалоговом окне **Добавить источник данных** выберите **Dynamics 365 for Operations\Перечисление**, чтобы открыть диалоговое окно **Свойства источника данных "перечисление"**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="0d6e1-177">В поле **Имя** введите **enumNoYes**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="0d6e1-178">В поле **Метка** введите **Параметры подавления**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="0d6e1-179">В поле **имя типа данных операций** выберите или введите **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="0d6e1-180">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-180">Select **OK**.</span></span>

8. <span data-ttu-id="0d6e1-181">Для выбранного элемента формата **SummaryLines** настройте формулу, чтобы указать, когда следует подавлять элемент управления содержимым Word, связанный с выбранным элементом форматирования:</span><span class="sxs-lookup"><span data-stu-id="0d6e1-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="0d6e1-182">На вкладке **Сопоставление** в разделе **Удаленный** выберите **Изменить**, чтобы открыть страницу **[конструктор формул](general-electronic-reporting-formula-designer.md)**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="0d6e1-183">В поле **Формула** введите формулу `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="0d6e1-184">Выберите **Сохранить**, затем закройте страницу **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0d6e1-185">Эта формула будет применена к созданному документу **после запуска всех остальных элементов форматирования**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="0d6e1-186">Чтобы применить эту формулу, в созданном документе найден элемент управления содержимым Word, помеченный как элемент формата, для которого настроена формула (в данном случае **SummaryLines**).</span><span class="sxs-lookup"><span data-stu-id="0d6e1-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="0d6e1-187">Затем этот элемент управления содержимым полностью удаляется вместе со строкой в таблице Word, в которой он содержится.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="0d6e1-188">Строка сведений из раздела сводки удаляется из созданного документа.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="0d6e1-189">Во время разработки можно настроить формулу **Удаленный** для элемента форматирования, даже если в шаблоне Word нет элемента управления, который используется в качестве тега, совпадающего с именем элемента формата, для которого настроено свойство **Удаленный**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="0d6e1-190">При проверке формата во время разработки появляется [предупреждение](er-components-inspections.md#i14) об этой несогласованности.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="0d6e1-191">Во время выполнения создается исключение, если ни один из элементов управления в шаблоне Word не используется в теге, совпадающем с именем элемента формата, для которого настроено свойство **Удаленный**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="0d6e1-192">На вкладке **Сопоставление** в области **Удаленный** установите для параметра **С родительским** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0d6e1-193">Необходимо установить для этого параметра значение **Да**, чтобы удалить всю таблицу слов в качестве родительского объекта строки, содержащей сведения о разделе сводки.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="0d6e1-194">Если для этого параметра установить значение **нет**, строка заголовка раздела останется в созданном документе.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="0d6e1-195">Для сохранения изменений в изменяемом формате выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Созданные выходные данные в формате Word](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="0d6e1-197">Выполните измененный формат для создания выходных данных Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="0d6e1-198">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="0d6e1-199">Выберите журнал платежей, который был создан, а затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="0d6e1-200">На странице **Платежи поставщикам** выберите все строки, а затем выберите **статус оплаты** \> **нет**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="0d6e1-201">Выберите **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="0d6e1-202">В поле **Способ оплаты** выберите **Электронный**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="0d6e1-203">В поле **Банковский счет** выберите **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="0d6e1-204">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-204">Select **OK**.</span></span>
8. <span data-ttu-id="0d6e1-205">В диалоговом окне **Параметры электронной отчетности** в поле **подавление раздела сводки** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="0d6e1-206">Нажмите кнопку **ОК** и проанализируйте созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-206">Select **OK**, and analyze the generated output.</span></span>

    ![Созданные выходные данные в формате Word](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="0d6e1-208">Обратите внимание, что выходные данные не содержат раздел "Сводка", так как он был подавлен.</span><span class="sxs-lookup"><span data-stu-id="0d6e1-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d6e1-209">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0d6e1-209">Additional resources</span></span>

- [<span data-ttu-id="0d6e1-210">Разработка конфигурации для создания отчетов в формате OPENXML</span><span class="sxs-lookup"><span data-stu-id="0d6e1-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="0d6e1-211">Разработка конфигураций электронной отчетности для создания отчетов в формате Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="0d6e1-212">Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word</span><span class="sxs-lookup"><span data-stu-id="0d6e1-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="0d6e1-213">Проверка настроенного компонента электронной отчетности для предотвращения неполадок среды выполнения</span><span class="sxs-lookup"><span data-stu-id="0d6e1-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]