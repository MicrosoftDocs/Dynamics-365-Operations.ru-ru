--- 
title: "Изменение формата для повторного применения шаблона Microsoft Excel для электронной отчетности (ER)"
description: "Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру \"Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a><span data-ttu-id="e004b-103">Изменение формата для повторного применения шаблона Microsoft Excel для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="e004b-103">Modify a format by reapplying a Microsoft Excel template for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e004b-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML".</span><span class="sxs-lookup"><span data-stu-id="e004b-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="e004b-105">Эта процедура показывает, как изменить конфигурацию формата электронной отчетности путем применения шаблона Microsoft Excel с внесенными изменениями.</span><span class="sxs-lookup"><span data-stu-id="e004b-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="e004b-106">В этой процедуре вам предстоит импортировать измененный шаблон Excel в конфигурации формата шаблона электронной отчетности, созданные для демонстрационной компании Litware, Inc., а затем сформировать электронные документы.</span><span class="sxs-lookup"><span data-stu-id="e004b-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="e004b-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="e004b-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="e004b-108">Действия можно выполнять с использованием набора данных GBSI.</span><span class="sxs-lookup"><span data-stu-id="e004b-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="e004b-109">Прежде чем начать, загрузите и сохраните файл SampleVendPaymWsReport2.xlsx, который указан в разделе справки "Изменение формата электронной отчетности путем повторного применения шаблона Microsoft Excel" (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="e004b-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="e004b-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="e004b-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e004b-111">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="e004b-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="e004b-112">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="e004b-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="e004b-113">Выбор формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e004b-113">Select the ER format</span></span>
1. <span data-ttu-id="e004b-114">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="e004b-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="e004b-115">В дереве разверните узел "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="e004b-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="e004b-116">В дереве выберите "Модель платежа\Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="e004b-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="e004b-117">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="e004b-117">Click Attachments.</span></span>
    * <span data-ttu-id="e004b-118">Обратите внимание, что файл SampleVendPaymWsReport.xlsx Excel в настоящее время используется в качестве шаблона для обработки журнала платежей.</span><span class="sxs-lookup"><span data-stu-id="e004b-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="e004b-119">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="e004b-119">Click Open.</span></span>
    * <span data-ttu-id="e004b-120">Щелкните "Открыть", чтобы просмотреть макет шаблона Excel.</span><span class="sxs-lookup"><span data-stu-id="e004b-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="e004b-121">Просмотрите шаблон.</span><span class="sxs-lookup"><span data-stu-id="e004b-121">Review the template.</span></span> <span data-ttu-id="e004b-122">Обратите внимание, что в настоящее время он включает следующие сведения для каждой строки платежа: номер счета поставщика, имя поставщика, банк, внутренний номер, номер счета, дебет, кредит и валюту.</span><span class="sxs-lookup"><span data-stu-id="e004b-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="e004b-123">В данном примере мы хотим расширить их список путем добавления сведений о дате платежа.</span><span class="sxs-lookup"><span data-stu-id="e004b-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="e004b-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e004b-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="e004b-125">Повторное применение нового шаблона Excel к формату электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e004b-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="e004b-126">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="e004b-126">Click Designer.</span></span>
    * <span data-ttu-id="e004b-127">Откройте черновую версию выбранного формата электронной отчетности для редактирования.</span><span class="sxs-lookup"><span data-stu-id="e004b-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="e004b-128">В области действий щелкните "Импорт".</span><span class="sxs-lookup"><span data-stu-id="e004b-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="e004b-129">Щелкните "Обновление из Excel".</span><span class="sxs-lookup"><span data-stu-id="e004b-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="e004b-130">Щелкните "Обновить шаблон" и выберите файл SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="e004b-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="e004b-131">Щелкните "Обновить шаблон" и выберите ранее загруженный файл SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="e004b-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="e004b-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e004b-132">Click OK.</span></span>
    * <span data-ttu-id="e004b-133">Применяется шаблон SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="e004b-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="e004b-134">Структура формата электронной отчетности синхронизируется с содержимым шаблона, элементы которого добавляются в формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e004b-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="e004b-135">Все существующие элементы в формате электронной отчетности, которые не входят в отчет, удаляются из определения формата.</span><span class="sxs-lookup"><span data-stu-id="e004b-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="e004b-136">В дереве выберите "Excel".</span><span class="sxs-lookup"><span data-stu-id="e004b-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="e004b-137">Обратите внимание, что поле "Шаблон" теперь содержит ссылку на новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="e004b-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="e004b-138">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="e004b-138">Click Attachments.</span></span>
7. <span data-ttu-id="e004b-139">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="e004b-139">Click Open.</span></span>
    * <span data-ttu-id="e004b-140">Щелкните "Открыть", чтобы просмотреть измененный шаблон Excel.</span><span class="sxs-lookup"><span data-stu-id="e004b-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="e004b-141">Просмотрите шаблон.</span><span class="sxs-lookup"><span data-stu-id="e004b-141">Review the template.</span></span> <span data-ttu-id="e004b-142">Обратите внимание, что в нем теперь содержится строка для даты платежа.</span><span class="sxs-lookup"><span data-stu-id="e004b-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="e004b-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e004b-143">Close the page.</span></span>
9. <span data-ttu-id="e004b-144">В дереве разверните "Excel".</span><span class="sxs-lookup"><span data-stu-id="e004b-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="e004b-145">В дереве разверните "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="e004b-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="e004b-146">В дереве выберите "Excel\PaymLines\PaymDate".</span><span class="sxs-lookup"><span data-stu-id="e004b-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="e004b-147">Обратите внимание, что формат электронной отчетности теперь содержит более одного элемента.</span><span class="sxs-lookup"><span data-stu-id="e004b-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="e004b-148">В шаблон Excel была добавлена ячейка PaymDate.</span><span class="sxs-lookup"><span data-stu-id="e004b-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="e004b-149">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="e004b-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="e004b-150">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="e004b-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="e004b-151">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="e004b-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="e004b-152">В дереве выберите "модель\Платежи\Дата проводки(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="e004b-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="e004b-153">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="e004b-153">Click Bind.</span></span>
    * <span data-ttu-id="e004b-154">Укажите, какие данные добавляются в новую ячейку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e004b-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="e004b-155">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e004b-155">Click Save.</span></span>
18. <span data-ttu-id="e004b-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e004b-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="e004b-157">Включение измененной черновой версии формата электронной отчетности для использования при обработке журнала платежей</span><span class="sxs-lookup"><span data-stu-id="e004b-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="e004b-158">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="e004b-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="e004b-159">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="e004b-159">Click User parameters.</span></span>
3. <span data-ttu-id="e004b-160">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="e004b-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="e004b-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e004b-161">Click OK.</span></span>
5. <span data-ttu-id="e004b-162">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="e004b-162">Click Edit.</span></span>
6. <span data-ttu-id="e004b-163">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="e004b-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="e004b-164">Использование измененной черновой версии формата электронной отчетности для использования при обработке журнала платежей</span><span class="sxs-lookup"><span data-stu-id="e004b-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="e004b-165">Просмотрите созданный лист, включая новый элемент сведений строк платежа — дату платежа.</span><span class="sxs-lookup"><span data-stu-id="e004b-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


