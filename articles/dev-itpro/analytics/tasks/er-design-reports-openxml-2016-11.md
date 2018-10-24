--- 
title: "Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML (ноябрь 2016 г.)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать новую конфигурацию электронной отчетности, содержащую шаблон для создания электронных документов в формате OPENXML."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="8883f-103">Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="8883f-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8883f-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую шаблон для создания электронных документов в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="8883f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="8883f-105">Эта конфигурация будет использоваться для обработки платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="8883f-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="8883f-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="8883f-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="8883f-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="8883f-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="8883f-108">Также необходимо иметь файл Excel, который будет импортирован при создании шаблона.</span><span class="sxs-lookup"><span data-stu-id="8883f-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="8883f-109">Этот файл можно взять из [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="8883f-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="8883f-110">Отправка конфигурации модели данных платежей</span><span class="sxs-lookup"><span data-stu-id="8883f-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="8883f-111">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="8883f-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8883f-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8883f-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8883f-113">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="8883f-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="8883f-114">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="8883f-114">Click Set active.</span></span>
4. <span data-ttu-id="8883f-115">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="8883f-115">Click Repositories.</span></span>
    * <span data-ttu-id="8883f-116">Выберите репозиторий для типа "Операционные ресурсы", если он имеется.</span><span class="sxs-lookup"><span data-stu-id="8883f-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="8883f-117">Если он доступен, пропустите следующие шаги по созданию нового репозитория.</span><span class="sxs-lookup"><span data-stu-id="8883f-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="8883f-118">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8883f-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="8883f-119">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="8883f-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="8883f-120">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="8883f-120">Click Create repository.</span></span>
8. <span data-ttu-id="8883f-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8883f-121">Click OK.</span></span>
9. <span data-ttu-id="8883f-122">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="8883f-122">Click Open.</span></span>
10. <span data-ttu-id="8883f-123">В дереве выберите "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="8883f-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="8883f-124">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="8883f-124">Click Import.</span></span>
    * <span data-ttu-id="8883f-125">Импортируйте эту модель данных.</span><span class="sxs-lookup"><span data-stu-id="8883f-125">Import this data model.</span></span> <span data-ttu-id="8883f-126">Она будет использоваться в качестве источника данных в новой конфигурации формата.</span><span class="sxs-lookup"><span data-stu-id="8883f-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="8883f-127">Пропустите этот шаг, если эта конфигурация уже была импортирована.</span><span class="sxs-lookup"><span data-stu-id="8883f-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="8883f-128">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="8883f-128">Click Yes.</span></span>
13. <span data-ttu-id="8883f-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-129">Close the page.</span></span>
14. <span data-ttu-id="8883f-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="8883f-131">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="8883f-131">Create a new format configuration</span></span>
1. <span data-ttu-id="8883f-132">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="8883f-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="8883f-133">В дереве выберите "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="8883f-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="8883f-134">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8883f-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8883f-135">В поле "Создать" введите "Формат, основанный на модели данных PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="8883f-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="8883f-136">Создайте формат, основанный на модели данных PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="8883f-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="8883f-137">В поле "Имя" введите "Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="8883f-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="8883f-138">Пример отчета о листе</span><span class="sxs-lookup"><span data-stu-id="8883f-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="8883f-139">В поле "Описание" введите "Пример отчета о листе для платежей поставщиков".</span><span class="sxs-lookup"><span data-stu-id="8883f-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="8883f-140">Пример отчета о листе для платежей поставщиков.</span><span class="sxs-lookup"><span data-stu-id="8883f-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="8883f-141">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8883f-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8883f-142">Выберите определение "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="8883f-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="8883f-143">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="8883f-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="8883f-144">Разработка нового документа в формате листа OPENXML</span><span class="sxs-lookup"><span data-stu-id="8883f-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="8883f-145">В дереве выберите "Модель платежа\Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="8883f-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="8883f-146">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="8883f-146">Click Designer.</span></span>
3. <span data-ttu-id="8883f-147">В области действий щелкните "Импорт".</span><span class="sxs-lookup"><span data-stu-id="8883f-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="8883f-148">Щелкните "Импорт из Excel".</span><span class="sxs-lookup"><span data-stu-id="8883f-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="8883f-149">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="8883f-149">Click Attachments.</span></span>
    * <span data-ttu-id="8883f-150">Вложите существующий документ Excel как шаблон.</span><span class="sxs-lookup"><span data-stu-id="8883f-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="8883f-151">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8883f-151">Click New.</span></span>
7. <span data-ttu-id="8883f-152">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="8883f-152">Click File.</span></span>
    * <span data-ttu-id="8883f-153">Укажите на существующий файл Excel.</span><span class="sxs-lookup"><span data-stu-id="8883f-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="8883f-154">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-154">Close the page.</span></span>
9. <span data-ttu-id="8883f-155">В поле "Шаблон" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8883f-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="8883f-156">Выберите вложенный файл Excel для использования в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="8883f-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="8883f-157">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8883f-157">Click OK.</span></span>
    * <span data-ttu-id="8883f-158">Обратите внимание, что компоненты формата электронной отчетности были созданы в формате создания, основанном на структуре ссылочного документа MS Excel (с именем "диапазоны").</span><span class="sxs-lookup"><span data-stu-id="8883f-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="8883f-159">Создание нового источника данных для расчета итогов по кодам валюты</span><span class="sxs-lookup"><span data-stu-id="8883f-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="8883f-160">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="8883f-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8883f-161">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8883f-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="8883f-162">В дереве выберите "Функции\Группировка по".</span><span class="sxs-lookup"><span data-stu-id="8883f-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="8883f-163">В поле "Имя" введите "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="8883f-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="8883f-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="8883f-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="8883f-165">Щелкните "Изменить группу по".</span><span class="sxs-lookup"><span data-stu-id="8883f-165">Click Edit group by.</span></span>
6. <span data-ttu-id="8883f-166">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="8883f-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="8883f-167">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="8883f-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="8883f-168">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="8883f-168">Click Add field to.</span></span>
9. <span data-ttu-id="8883f-169">Щелкните "Элементы для группировки".</span><span class="sxs-lookup"><span data-stu-id="8883f-169">Click What to group.</span></span>
10. <span data-ttu-id="8883f-170">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="8883f-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="8883f-171">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="8883f-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="8883f-172">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="8883f-172">Click Add field to.</span></span>
13. <span data-ttu-id="8883f-173">Щелкните "Сгруппированные поля".</span><span class="sxs-lookup"><span data-stu-id="8883f-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="8883f-174">В дереве выберите "модель\Платежи\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="8883f-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="8883f-175">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="8883f-175">Click Add field to.</span></span>
16. <span data-ttu-id="8883f-176">Щелкните "Поля агрегирования".</span><span class="sxs-lookup"><span data-stu-id="8883f-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="8883f-177">В поле "Метод" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="8883f-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="8883f-178">Выберите функцию агрегирования SUM.</span><span class="sxs-lookup"><span data-stu-id="8883f-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="8883f-179">В поле "Имя" введите "TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="8883f-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="8883f-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="8883f-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="8883f-181">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8883f-181">Click Save.</span></span>
20. <span data-ttu-id="8883f-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-182">Close the page.</span></span>
21. <span data-ttu-id="8883f-183">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8883f-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="8883f-184">Сопоставление компонентов формата с источниками данных</span><span class="sxs-lookup"><span data-stu-id="8883f-184">Map format components to data sources</span></span>
1. <span data-ttu-id="8883f-185">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="8883f-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="8883f-186">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="8883f-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="8883f-187">В дереве разверните узел "модель\Платежи\Инициирующий субъект(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="8883f-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="8883f-188">В дереве выберите "модель\Платежи\Инициирующий субъект(InitiatingParty)\Имя".</span><span class="sxs-lookup"><span data-stu-id="8883f-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="8883f-189">В дереве разверните "Excel\ReportHeader".</span><span class="sxs-lookup"><span data-stu-id="8883f-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="8883f-190">В дереве выберите "Excel\ReportHeader\CompanyName".</span><span class="sxs-lookup"><span data-stu-id="8883f-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="8883f-191">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-191">Click Bind.</span></span>
8. <span data-ttu-id="8883f-192">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="8883f-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="8883f-193">В дереве разверните узел "модель\Платежи\Кредитор\Идентификация".</span><span class="sxs-lookup"><span data-stu-id="8883f-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="8883f-194">В дереве выберите "модель\Платежи\Кредитор\Идентификация\Код источника(SourceID)".</span><span class="sxs-lookup"><span data-stu-id="8883f-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="8883f-195">В дереве разверните "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="8883f-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="8883f-196">В дереве выберите "Excel\PaymLines\VendAccountName".</span><span class="sxs-lookup"><span data-stu-id="8883f-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="8883f-197">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-197">Click Bind.</span></span>
14. <span data-ttu-id="8883f-198">В дереве выберите "модель\Платежи\Кредитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="8883f-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="8883f-199">В дереве выберите "Excel\PaymLines\VendName".</span><span class="sxs-lookup"><span data-stu-id="8883f-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="8883f-200">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-200">Click Bind.</span></span>
17. <span data-ttu-id="8883f-201">В дереве разверните узел "модель\Платежи\Счет кредитора(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="8883f-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="8883f-202">В дереве выберите "модель\Платежи\Счет кредитора(CreditorAccount)\Имя".</span><span class="sxs-lookup"><span data-stu-id="8883f-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="8883f-203">В дереве выберите "Excel\PaymLines\Банк".</span><span class="sxs-lookup"><span data-stu-id="8883f-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="8883f-204">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-204">Click Bind.</span></span>
21. <span data-ttu-id="8883f-205">В дереве выберите "модель\Платежи\Агент кредитора(CreditorAgent)\Внутренний номер(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="8883f-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="8883f-206">В дереве выберите "Excel\PaymLines\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="8883f-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="8883f-207">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-207">Click Bind.</span></span>
24. <span data-ttu-id="8883f-208">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="8883f-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="8883f-209">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)\Identification".</span><span class="sxs-lookup"><span data-stu-id="8883f-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="8883f-210">В дереве выберите "модель\Платежи\Счет кредитора(CreditorAccount)\Идентификация\Номер".</span><span class="sxs-lookup"><span data-stu-id="8883f-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="8883f-211">В дереве выберите "Excel\PaymLines\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="8883f-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="8883f-212">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-212">Click Bind.</span></span>
29. <span data-ttu-id="8883f-213">В дереве выберите "модель\Платежи\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="8883f-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="8883f-214">В дереве выберите "Excel\PaymLines\Дебет".</span><span class="sxs-lookup"><span data-stu-id="8883f-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="8883f-215">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-215">Click Bind.</span></span>
32. <span data-ttu-id="8883f-216">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="8883f-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="8883f-217">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="8883f-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="8883f-218">В дереве разверните узел "модель\Платежи\Счет кредитора(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="8883f-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="8883f-219">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="8883f-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="8883f-220">В дереве выберите "Excel\PaymLines\Валюта".</span><span class="sxs-lookup"><span data-stu-id="8883f-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="8883f-221">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-221">Click Bind.</span></span>
38. <span data-ttu-id="8883f-222">В дереве разверните узел "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="8883f-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="8883f-223">В дереве разверните узел "PaymentByCurrency\сгруппировано".</span><span class="sxs-lookup"><span data-stu-id="8883f-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="8883f-224">В дереве выберите "PaymentByCurrency\сгруппировано\Валюта".</span><span class="sxs-lookup"><span data-stu-id="8883f-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="8883f-225">В дереве разверните "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="8883f-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="8883f-226">В дереве выберите "Excel\SummaryLines\SummaryCurrency".</span><span class="sxs-lookup"><span data-stu-id="8883f-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="8883f-227">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-227">Click Bind.</span></span>
44. <span data-ttu-id="8883f-228">В дереве разверните узел "PaymentByCurrency\агрегировано".</span><span class="sxs-lookup"><span data-stu-id="8883f-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="8883f-229">В дереве выберите "PaymentByCurrency\агрегировано\TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="8883f-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="8883f-230">В дереве выберите "Excel\SummaryLines\SummaryAmount".</span><span class="sxs-lookup"><span data-stu-id="8883f-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="8883f-231">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-231">Click Bind.</span></span>
48. <span data-ttu-id="8883f-232">В дереве выберите "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="8883f-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="8883f-233">В дереве выберите "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="8883f-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="8883f-234">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-234">Click Bind.</span></span>
51. <span data-ttu-id="8883f-235">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="8883f-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="8883f-236">В дереве выберите "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="8883f-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="8883f-237">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="8883f-237">Click Bind.</span></span>
54. <span data-ttu-id="8883f-238">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8883f-238">Click Save.</span></span>
55. <span data-ttu-id="8883f-239">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="8883f-240">Использование созданной конфигурации для обработки платежей</span><span class="sxs-lookup"><span data-stu-id="8883f-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="8883f-241">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="8883f-241">Click Change status.</span></span>
2. <span data-ttu-id="8883f-242">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="8883f-242">Click Complete.</span></span>
3. <span data-ttu-id="8883f-243">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8883f-243">Click OK.</span></span>
4. <span data-ttu-id="8883f-244">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-244">Close the page.</span></span>
5. <span data-ttu-id="8883f-245">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-245">Close the page.</span></span>
6. <span data-ttu-id="8883f-246">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="8883f-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="8883f-247">Используйте экспресс-фильтр для фильтрации поля "Способ оплаты" со значением ''Электронно".</span><span class="sxs-lookup"><span data-stu-id="8883f-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="8883f-248">Электронно</span><span class="sxs-lookup"><span data-stu-id="8883f-248">Electronic</span></span>  
8. <span data-ttu-id="8883f-249">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="8883f-249">Click Edit.</span></span>
9. <span data-ttu-id="8883f-250">Разверните раздел "Форматы файлов".</span><span class="sxs-lookup"><span data-stu-id="8883f-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="8883f-251">В поле "Общая электронная отчетность" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="8883f-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="8883f-252">В поле "Экспорт конфигурации формата" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8883f-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="8883f-253">Выберите конфигурацию "Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="8883f-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="8883f-254">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8883f-254">Click Save.</span></span>
13. <span data-ttu-id="8883f-255">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8883f-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="8883f-256">Использование созданной конфигурации для тестирования обработки журналов платежей</span><span class="sxs-lookup"><span data-stu-id="8883f-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="8883f-257">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="8883f-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8883f-258">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8883f-258">Click New.</span></span>
    * <span data-ttu-id="8883f-259">Создайте новый журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="8883f-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="8883f-260">В поле "Имя" введите "VendPay".</span><span class="sxs-lookup"><span data-stu-id="8883f-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="8883f-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="8883f-261">VendPay</span></span>  
4. <span data-ttu-id="8883f-262">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="8883f-262">Click Lines.</span></span>
5. <span data-ttu-id="8883f-263">В поле "Счет" укажите значения "GB_SI_000001".</span><span class="sxs-lookup"><span data-stu-id="8883f-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="8883f-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="8883f-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="8883f-265">Установите для параметра "Дебет" значение "1000".</span><span class="sxs-lookup"><span data-stu-id="8883f-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="8883f-266">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8883f-266">Click New.</span></span>
8. <span data-ttu-id="8883f-267">В поле "Счет" укажите значения "GB_SI_000005".</span><span class="sxs-lookup"><span data-stu-id="8883f-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="8883f-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="8883f-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="8883f-269">Установите для параметра "Дебет" значение "2000".</span><span class="sxs-lookup"><span data-stu-id="8883f-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="8883f-270">В поле "Валюта" введите значение "Евро".</span><span class="sxs-lookup"><span data-stu-id="8883f-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="8883f-271">Евро</span><span class="sxs-lookup"><span data-stu-id="8883f-271">EUR</span></span>  
11. <span data-ttu-id="8883f-272">В поле "Корр.счет" укажите требуемые значения "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="8883f-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8883f-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8883f-273">GBSI OPER</span></span>  
12. <span data-ttu-id="8883f-274">В поле "Способ оплаты" введите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="8883f-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8883f-275">Электронно</span><span class="sxs-lookup"><span data-stu-id="8883f-275">Electronic</span></span>  
13. <span data-ttu-id="8883f-276">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8883f-276">Click Save.</span></span>
14. <span data-ttu-id="8883f-277">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="8883f-277">Click Generate payments.</span></span>
15. <span data-ttu-id="8883f-278">В поле "Способ оплаты" введите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="8883f-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8883f-279">Электронно</span><span class="sxs-lookup"><span data-stu-id="8883f-279">Electronic</span></span>  
16. <span data-ttu-id="8883f-280">В поле "Имя файла" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="8883f-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="8883f-281">Например, введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="8883f-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="8883f-282">В поле "Банковский счет" введите "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="8883f-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8883f-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8883f-283">GBSI OPER</span></span>  
18. <span data-ttu-id="8883f-284">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8883f-284">Click OK.</span></span>
19. <span data-ttu-id="8883f-285">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8883f-285">Click OK.</span></span>
    * <span data-ttu-id="8883f-286">Просмотрите созданный лист, включая сведения строк платежа, а так же итоги для каждого кода валюты, используемого в этом сообщении платежа.</span><span class="sxs-lookup"><span data-stu-id="8883f-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


