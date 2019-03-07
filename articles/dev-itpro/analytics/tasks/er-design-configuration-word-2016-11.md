---
title: Разработка конфигураций электронной отчетности для создания отчетов в формате Word
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить форматы электронной отчетности для создания отчетов в виде файлов Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "362357"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="e3eb6-103">Разработка конфигураций электронной отчетности для создания отчетов в формате Word</span><span class="sxs-lookup"><span data-stu-id="e3eb6-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3eb6-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности (ER), может настроить форматы электронной отчетности для создания отчетов в виде файлов Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="e3eb6-105">Эти шаги можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="e3eb6-106">Для выполнения этих шагов необходимо сначала выполнить шаги в руководстве по задаче "Создание конфигурации электронной отчетности для создания отчетов в формате OPENXML".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="e3eb6-107">Необходимо заранее загрузить и сохранить локально для следующие шаблоны для примера отчета:</span><span class="sxs-lookup"><span data-stu-id="e3eb6-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="e3eb6-108">Шаблон отчета о платежах</span><span class="sxs-lookup"><span data-stu-id="e3eb6-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="e3eb6-109">Связанный шаблон отчета о платежах</span><span class="sxs-lookup"><span data-stu-id="e3eb6-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="e3eb6-110">Эта процедура для функции, которая была добавлена в версии 1611 Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="e3eb6-111">Выбор существующей конфигурации отчета электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e3eb6-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="e3eb6-112">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e3eb6-113">Убедитесь, что поставщик конфигураций Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="e3eb6-114">выбран как активный.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-114">is selected as active.</span></span>  
2. <span data-ttu-id="e3eb6-115">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="e3eb6-116">Мы повторно используем существующую конфигурацию ER, которая изначально была создана для создания выходных данных отчета в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="e3eb6-117">В дереве разверните узел "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="e3eb6-118">В дереве выберите "Модель платежа\Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="e3eb6-119">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="e3eb6-120">Замена шаблона Excel на шаблон Word</span><span class="sxs-lookup"><span data-stu-id="e3eb6-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="e3eb6-121">В настоящее время документ Excel используется как шаблон для создания выходных данных в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="e3eb6-122">Мы импортируем шаблон отчета в формате Word.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="e3eb6-123">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-123">Click Attachments.</span></span>
    * <span data-ttu-id="e3eb6-124">Замените существующий шаблон Excel на ранее загруженный шаблон Word — SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="e3eb6-125">Обратите внимание, что этот шаблон содержит только макет документа, который требуется создать как выходные данные ER.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="e3eb6-126">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-126">Click Delete.</span></span>
3. <span data-ttu-id="e3eb6-127">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-127">Click Yes.</span></span>
4. <span data-ttu-id="e3eb6-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-128">Click New.</span></span>
5. <span data-ttu-id="e3eb6-129">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-129">Click File.</span></span>
6. <span data-ttu-id="e3eb6-130">Щелкните Обзор.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-130">Click Browse.</span></span> <span data-ttu-id="e3eb6-131">Найдите и выберите ранее загруженный шаблон SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="e3eb6-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-132">Click OK.</span></span>
    * <span data-ttu-id="e3eb6-133">Выберите шаблон, загруженный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="e3eb6-134">В поле "Шаблон" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="e3eb6-135">Расширение шаблона Word путем добавления пользовательской XML-части</span><span class="sxs-lookup"><span data-stu-id="e3eb6-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="e3eb6-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-136">Click Save.</span></span>
    * <span data-ttu-id="e3eb6-137">В дополнение к сохранению изменений конфигурации действие "Сохранить" также обновит присоединенный шаблон Word.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="e3eb6-138">Структура созданного формата передается в документ Word в качестве новой пользовательской XML-части с именем "Отчет".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="e3eb6-139">Обратите внимание, что присоединенный шаблон Word содержит не только макет документа, который требуется создать как выходные данные ER, но он также содержит структуру данных, которую ER заполнит в этот шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="e3eb6-140">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-140">Click Attachments.</span></span>
    * <span data-ttu-id="e3eb6-141">Теперь необходимо привязать элементы пользовательской XML-части "Отчет" к частям документа Word.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="e3eb6-142">Если вы знакомы с документами Word, которые можно создать как формы, содержащие элементы управления содержимым, связанные с элементами пользовательских XML-частей, воспроизведите все шаги следующей подзадачи для создания такого документа.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="e3eb6-143">Дополнительные сведения см. по следующей ссылке: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="e3eb6-144">В противном случае пропустите все действия, указанные в следующей подзадаче.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="e3eb6-145">Получение Word с пользовательской XML-частью для привязки данных</span><span class="sxs-lookup"><span data-stu-id="e3eb6-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="e3eb6-146">Откройте этот документ в Word и выполните следующие действия: - Откройте вкладку "Разработчик Word" (настройте ленту, если она еще не включена).</span><span class="sxs-lookup"><span data-stu-id="e3eb6-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="e3eb6-147">- Выберите область сопоставления XML.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="e3eb6-148">- Выберите пользовательскую XML-часть "Отчет" в поиске.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="e3eb6-149">- Выполните сопоставление элементов выбранной пользовательской XML-части и элементов управления содержимым документа Word.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="e3eb6-150">- Сохраните обновленный документ Word на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="e3eb6-151">Отправка шаблона Word с пользовательской XML-частью, связанной с элементами управления содержимым</span><span class="sxs-lookup"><span data-stu-id="e3eb6-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="e3eb6-152">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-152">Click Delete.</span></span>
2. <span data-ttu-id="e3eb6-153">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-153">Click Yes.</span></span>
    * <span data-ttu-id="e3eb6-154">Добавление нового шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-154">Add a new template.</span></span> <span data-ttu-id="e3eb6-155">Если вы выполнили действия, описанные в предыдущей подзадаче, выберите документ Word, который был подготовлен и сохранен локально.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="e3eb6-156">В противном случае выберите ранее загруженный шаблон SampleVendPaymDocReportBounded.docx MS Word.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="e3eb6-157">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-157">Click New.</span></span>
4. <span data-ttu-id="e3eb6-158">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-158">Click File.</span></span>
5. <span data-ttu-id="e3eb6-159">Щелкните Обзор.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-159">Click Browse.</span></span> <span data-ttu-id="e3eb6-160">Найдите и выберите ранее загруженный шаблон SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="e3eb6-161">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-161">Click OK.</span></span>
6. <span data-ttu-id="e3eb6-162">В поле "Шаблон" выберите документ, загруженный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="e3eb6-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-163">Click Save.</span></span>
8. <span data-ttu-id="e3eb6-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="e3eb6-165">Выполнение формата для создания выходных данных Word</span><span class="sxs-lookup"><span data-stu-id="e3eb6-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="e3eb6-166">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="e3eb6-167">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-167">Click User parameters.</span></span>
3. <span data-ttu-id="e3eb6-168">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="e3eb6-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-169">Click OK.</span></span>
5. <span data-ttu-id="e3eb6-170">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-170">Click Edit.</span></span>
6. <span data-ttu-id="e3eb6-171">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="e3eb6-172">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-172">Click Save.</span></span>
8. <span data-ttu-id="e3eb6-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-173">Close the page.</span></span>
9. <span data-ttu-id="e3eb6-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-174">Close the page.</span></span>
10. <span data-ttu-id="e3eb6-175">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="e3eb6-176">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-176">Click Lines.</span></span>
12. <span data-ttu-id="e3eb6-177">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="e3eb6-178">Щелкните "Статус платежа".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-178">Click Payment status.</span></span>
14. <span data-ttu-id="e3eb6-179">Щелкните "Нет".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-179">Click None.</span></span>
15. <span data-ttu-id="e3eb6-180">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-180">Click Generate payments.</span></span>
16. <span data-ttu-id="e3eb6-181">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-181">Click OK.</span></span>
17. <span data-ttu-id="e3eb6-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e3eb6-182">Click OK.</span></span>
    * <span data-ttu-id="e3eb6-183">Проанализируйте созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-183">Analyze the generated output.</span></span> <span data-ttu-id="e3eb6-184">Обратите внимание, что созданные выходные данные представлены в формате Word и содержат сведения об обработанных платежах.</span><span class="sxs-lookup"><span data-stu-id="e3eb6-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

