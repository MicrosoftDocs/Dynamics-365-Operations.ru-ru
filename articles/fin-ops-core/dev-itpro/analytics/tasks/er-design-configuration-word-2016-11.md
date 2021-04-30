---
title: Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word
description: В этой теме описывается, как форматы отчетов, предназначенные для создания отчетов в виде рабочих книг Excel, можно настроить для создания отчетов в виде документов Word.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4cd4a390782936a74977ac2aef3790aa8ac1af
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891703"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="a4a3c-103">Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word</span><span class="sxs-lookup"><span data-stu-id="a4a3c-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4a3c-104">Для создания отчетов в виде документов Microsoft Word можно [настроить](../er-design-configuration-word.md) новый [формат](../general-electronic-reporting.md#FormatComponentOutbound) [электронной отчетности (ER)](../general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="a4a3c-105">Кроме того, можно повторно использовать формат электронной отчетности, который изначально был создан для создания отчетов в виде книг Excel.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="a4a3c-106">В этом случае шаблон Excel необходимо заменить шаблоном Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="a4a3c-107">Следующие процедуры показывают, как пользователь в роли системного администратора или роли разработчика электронной отчетности может настроить формат электронной отчетности для создания отчетов в виде файлов Word путем повторного использования формата электронной отчетности, созданного для формирования отчетов в виде файлов Excel.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="a4a3c-108">Эти процедуры можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a4a3c-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a4a3c-109">Prerequisites</span></span>

<span data-ttu-id="a4a3c-110">Для выполнения этих процедур необходимо сначала выполнить шаги из руководства по задаче [Разработка конфигурации для создания отчетов в формате OPENXML](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="a4a3c-111">Необходимо также загрузить и локально сохранить следующие шаблоны для примера отчета:</span><span class="sxs-lookup"><span data-stu-id="a4a3c-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="a4a3c-112">Шаблон отчета платежей (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="a4a3c-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="a4a3c-113">Связанный шаблон отчета о платежах (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="a4a3c-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="a4a3c-114">Эти процедуры предназначены для функции, которая была добавлена в Dynamics 365 for Operations версии 1611 (ноябрь 2016 года).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="a4a3c-115">Выбор существующей конфигурации отчета электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a4a3c-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="a4a3c-116">В Dynamics 365 Finance перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="a4a3c-117">Убедитесь, что поставщик конфигураций **Litware, Inc.** выбран как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="a4a3c-118">Если это не так, выполните шаги, указанные в разделе [Создание поставщиков конфигураций и пометка их как активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="a4a3c-119">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="a4a3c-120">Вы будете повторно использовать существующую конфигурацию электронной отчетности, которая была создана для создания выходных данных отчета в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="a4a3c-121">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**, затем выберите **Пример отчета о листе**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4a3c-122">Черновую версию выбранного формата электронной отчетности можно редактировать на экспресс-вкладке **Версии**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="a4a3c-123">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-123">Select **Designer**.</span></span>
6. <span data-ttu-id="a4a3c-124">На странице **Конструктор форматов** обратите внимание, что заголовок корневого элемента формата показывает, что в данный момент используется шаблон Excel.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Выбор существующей конфигурации](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="a4a3c-126">Проверка загруженного шаблона Word</span><span class="sxs-lookup"><span data-stu-id="a4a3c-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="a4a3c-127">В классическом приложении Word откройте файл шаблона **SampleVendPaymDocReport.docx**, который был загружен ранее.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="a4a3c-128">Проверьте, что шаблон содержит только макет документа, который требуется создать как выходные данные электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Макет шаблона Word в классическом приложении](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="a4a3c-130">Замена шаблона Excel шаблоном Word и добавление пользовательской XML-части</span><span class="sxs-lookup"><span data-stu-id="a4a3c-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="a4a3c-131">В настоящее время документ Excel используется как шаблон для создания выходных данных в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="a4a3c-132">Вы замените этот шаблон файлом шаблоном Word SampleVendPaymDocReport.docx, который загрузили ранее.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="a4a3c-133">Вы также расширите шаблон Word путем добавления пользовательской XML-части.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="a4a3c-134">В Finance на странице **Конструктор форматов** на вкладке **Формат** выберите **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="a4a3c-135">На странице **Вложения** выберите **Удалить**, чтобы удалить существующий шаблон Excel.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="a4a3c-136">Выберите **Да**, чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="a4a3c-137">Выберите **Создать** \> **Файл**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4a3c-138">Необходимо выбрать тип документа, который был [настроен](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) в параметрах электронной отчетности для хранения шаблонов форматов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="a4a3c-139">Выберите **Обзор**, затем найдите и выберите файл **SampleVendPaymDocReport.docx**, загруженный ранее.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="a4a3c-140">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-140">Select **OK**.</span></span>
6. <span data-ttu-id="a4a3c-141">Закройте страницу **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="a4a3c-142">На странице **Конструктор форматов** в поле **Шаблон** введите или выберите файл **SampleVendPaymDocReport.docx**, который будет использоваться для шаблона Word вместо шаблона Excel, который использовался ранее.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="a4a3c-143">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-143">Select **Save**.</span></span>

    <span data-ttu-id="a4a3c-144">В дополнение к сохранению изменений конфигурации действие **Сохранить** также обновит присоединенный шаблон Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="a4a3c-145">Иерархическая структура созданного формата добавляется в приложенный документ Word в качестве новой пользовательской XML-части с именем **Отчет**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="a4a3c-146">Присоединенный шаблон Word содержит макет документа, который будет создаваться как выходные данные электронной отчетности, и структуру данных, которую электронная отчетность введет в этот шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="a4a3c-147">Обратите внимание, что заголовок корневого элемента формата показывает, что в данный момент используется шаблон Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Замена шаблона Excel шаблоном Word и добавление пользовательской XML-части](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="a4a3c-149">На вкладке **Формат** выберите **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="a4a3c-150">Теперь можно сопоставать элементы пользовательской XML-части **Отчет** с элементами управления содержимым документа Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="a4a3c-151">Если вы знакомы с процессом разработки документов Word в виде форм, которые содержат [элементы управления содержимым](/office/client-developer/word/content-controls-in-word), сопоставленные с элементами [пользовательских XML-частей](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), выполните все шаги в следующей процедуре для создания документа.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="a4a3c-152">Дополнительные сведения см. в разделе [Создание форм, которые пользователи заполняют или печатают в Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="a4a3c-153">В противном случае пропустите следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="a4a3c-154">Получение документа Word с пользовательской XML-частью и сопоставление данных</span><span class="sxs-lookup"><span data-stu-id="a4a3c-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="a4a3c-155">В Finance на странице **Вложения** выберите **Открыть**, чтобы загрузить выбранный шаблон из Finance и сохранить его локально как документ Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="a4a3c-156">В классическом приложении Word откройте только что загруженный документ.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="a4a3c-157">На вкладке **Разработчик** выберите **Область сопоставления XML**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4a3c-158">Если вкладка **Разработчик** не отображается на ленте, настройте ленту для ее добавления.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="a4a3c-159">В области **Сопоставление XML** в поле **Пользовательская XML-часть** выберите пользовательскую XML-часть **Отчет**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="a4a3c-160">Сопоставьте элементы выбранной пользовательской XML-части **Отчет** с элементами управления содержимым документа Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="a4a3c-161">Сохраните обновленный документ Word локально как **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="a4a3c-162">Просмотр шаблона Word, где пользовательская XML-часть сопоставлена с элементами управления содержимым</span><span class="sxs-lookup"><span data-stu-id="a4a3c-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="a4a3c-163">В классическом приложении Word откройте файл шаблона **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="a4a3c-164">Проверьте, что шаблон содержит макет документа, который требуется создать как выходные данные электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="a4a3c-165">Элементы управления содержимым, которые используются в качестве заполнителей для данных, которые будут введены электронной отчетностью в этот шаблон в ходе выполнения, основаны на сопоставлениях, настроенных между элементами пользовательской XML-части **Отчет** и элементами управления содержимым документа Word.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Предварительный просмотр шаблона Word в классическом приложении](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="a4a3c-167">Отправка шаблона Word, где пользовательская XML-часть сопоставлена с элементами управления содержимым</span><span class="sxs-lookup"><span data-stu-id="a4a3c-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="a4a3c-168">В Finance на странице **Вложения** выберите **Удалить**, чтобы удалить шаблон Word, который не содержит сопоставлений между элементами пользовательской XML-части **Отчет** и элементами управления содержимым.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="a4a3c-169">Выберите **Да**, чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="a4a3c-170">Выберите **Создать** \> **Файл**, чтобы добавить новый файл шаблона, содержащий сопоставления между элементами пользовательской XML-части **Отчет** и элементами управления содержимым.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4a3c-171">Необходимо выбрать тип документа, который был [настроен](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) в параметрах электронной отчетности для хранения шаблонов форматов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="a4a3c-172">Выберите **Обзор**, затем найдите и выберите файл **SampleVendPaymDocReportBounded.docx**, который вы загрузили или подготовили, выполнив процедуру, описанную в разделе [Получение документа Word с пользовательской XML-частью и сопоставление данных](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="a4a3c-173">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-173">Select **OK**.</span></span>
5. <span data-ttu-id="a4a3c-174">Закройте страницу **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="a4a3c-175">На странице **Конструктор форматов** в поле **Шаблон** выберите только что загруженный документ.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="a4a3c-176">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-176">Select **Save**.</span></span>
8. <span data-ttu-id="a4a3c-177">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="a4a3c-178">Отметка настроенного формата как готового к запуску</span><span class="sxs-lookup"><span data-stu-id="a4a3c-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="a4a3c-179">Чтобы выполнить черновую версию редактируемого формата, необходимо сделать ее [пригодной к запуску](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="a4a3c-180">В Finance на странице **Конфигурации** в области действий на вкладке **Конфигурации** в группе **Дополнительные параметры** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="a4a3c-181">В диалоговом окне **Параметры пользователя** установите для параметра **Параметры выполнения** значение **Да**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="a4a3c-182">При необходимости выберите **Правка**, чтобы сделать текущую страницу редактируемой.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="a4a3c-183">Для текущей выбранной конфигурации **Пример отчета о листе**, установите для параметра **Выполнить черновик** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="a4a3c-184">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="a4a3c-185">Выполнение формата для создания выходных данных в формате Word</span><span class="sxs-lookup"><span data-stu-id="a4a3c-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="a4a3c-186">В Finance перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="a4a3c-187">В журнале платежей, который был введен ранее, выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="a4a3c-188">На странице **Платежи поставщикам** выберите все строки в сетке.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="a4a3c-189">Выберите **Статус платежа** \> **Нет**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-189">Select **Payment status** \> **None**.</span></span>

    ![Платежи для обработки на странице платежей поставщикам](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="a4a3c-191">На панели операций выберите **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="a4a3c-192">В появившемся диалоговом окне выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a4a3c-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="a4a3c-193">В поле **Способ оплаты** выберите **Электронный**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="a4a3c-194">В поле **Банковский счет** выберите **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="a4a3c-195">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-195">Select **OK**.</span></span>

7. <span data-ttu-id="a4a3c-196">В диалоговом окне **Параметры электронной отчетности** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="a4a3c-197">Созданные выходные данные представлены в формате Word и содержат сведения об обработанных платежах.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="a4a3c-198">Проанализируйте созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-198">Analyze the generated output.</span></span>

    ![Созданные выходные данные в формате Word](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="a4a3c-200">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a4a3c-200">Additional resources</span></span>

- [<span data-ttu-id="a4a3c-201">Разработка новых конфигураций электронной отчетности для создания отчетов в формате Word</span><span class="sxs-lookup"><span data-stu-id="a4a3c-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="a4a3c-202">Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="a4a3c-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]