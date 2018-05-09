--- 
title: "Разработка конфигурации для создания отчетов в формате OpenXML для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать новую конфигурацию электронной отчетности, содержащую шаблон для создания электронных документов в формате OPENXML."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d410e49e2248e503c5935a0d7e95b63a8381a6a8
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="57402-103">Разработка конфигурации для создания отчетов в формате OpenXML для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="57402-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57402-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую шаблон для создания электронных документов в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="57402-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="57402-105">Эта конфигурация будет использоваться для обработки платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="57402-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="57402-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="57402-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="57402-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="57402-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="57402-108">Необходимо загрузить и сохранить файл Microsoft Excel, [Шаблон отчета о платежах](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="57402-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="57402-109">Отправка конфигурации модели данных платежей</span><span class="sxs-lookup"><span data-stu-id="57402-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="57402-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="57402-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="57402-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="57402-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="57402-112">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="57402-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="57402-113">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="57402-113">Click Set active.</span></span>
4. <span data-ttu-id="57402-114">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="57402-114">Click Repositories.</span></span>
    * <span data-ttu-id="57402-115">Выберите репозиторий для типа "Операционные ресурсы", если он имеется.</span><span class="sxs-lookup"><span data-stu-id="57402-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="57402-116">Если он доступен, пропустите следующие шаги по созданию нового репозитория.</span><span class="sxs-lookup"><span data-stu-id="57402-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="57402-117">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="57402-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="57402-118">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="57402-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="57402-119">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="57402-119">Click Create repository.</span></span>
8. <span data-ttu-id="57402-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57402-120">Click OK.</span></span>
9. <span data-ttu-id="57402-121">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="57402-121">Click Open.</span></span>
10. <span data-ttu-id="57402-122">В дереве выберите "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="57402-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="57402-123">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="57402-123">Click Import.</span></span>
    * <span data-ttu-id="57402-124">Импортируйте эту модель данных.</span><span class="sxs-lookup"><span data-stu-id="57402-124">Import this data model.</span></span> <span data-ttu-id="57402-125">Она будет использоваться в качестве источника данных в новой конфигурации формата.</span><span class="sxs-lookup"><span data-stu-id="57402-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="57402-126">Пропустите этот шаг, если эта конфигурация уже была импортирована.</span><span class="sxs-lookup"><span data-stu-id="57402-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="57402-127">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="57402-127">Click Yes.</span></span>
13. <span data-ttu-id="57402-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-128">Close the page.</span></span>
14. <span data-ttu-id="57402-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="57402-130">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="57402-130">Create a new format configuration</span></span>
1. <span data-ttu-id="57402-131">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="57402-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="57402-132">В дереве выберите "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="57402-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="57402-133">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="57402-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="57402-134">В поле "Создать" введите "Формат, основанный на модели данных PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="57402-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="57402-135">Создайте формат, основанный на модели данных PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="57402-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="57402-136">В поле "Имя" введите "Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="57402-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="57402-137">Пример отчета о листе</span><span class="sxs-lookup"><span data-stu-id="57402-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="57402-138">В поле "Описание" введите "Пример отчета о листе для платежей поставщиков".</span><span class="sxs-lookup"><span data-stu-id="57402-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="57402-139">Пример отчета о листе для платежей поставщиков.</span><span class="sxs-lookup"><span data-stu-id="57402-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="57402-140">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57402-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="57402-141">Выберите определение "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="57402-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="57402-142">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="57402-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="57402-143">Разработка нового документа в формате листа OPENXML</span><span class="sxs-lookup"><span data-stu-id="57402-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="57402-144">В дереве выберите "Модель платежа\Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="57402-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="57402-145">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="57402-145">Click Designer.</span></span>
3. <span data-ttu-id="57402-146">В области действий щелкните "Импорт".</span><span class="sxs-lookup"><span data-stu-id="57402-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="57402-147">Щелкните "Импорт из Excel".</span><span class="sxs-lookup"><span data-stu-id="57402-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="57402-148">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="57402-148">Click Attachments.</span></span>
    * <span data-ttu-id="57402-149">Вложите существующий документ Excel как шаблон.</span><span class="sxs-lookup"><span data-stu-id="57402-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="57402-150">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57402-150">Click New.</span></span>
7. <span data-ttu-id="57402-151">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="57402-151">Click File.</span></span>
    * <span data-ttu-id="57402-152">Укажите на существующий файл Excel.</span><span class="sxs-lookup"><span data-stu-id="57402-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="57402-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-153">Close the page.</span></span>
9. <span data-ttu-id="57402-154">В поле "Шаблон" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57402-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="57402-155">Выберите вложенный файл Excel для использования в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="57402-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="57402-156">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57402-156">Click OK.</span></span>
    * <span data-ttu-id="57402-157">Обратите внимание, что компоненты формата электронной отчетности были созданы в формате создания, основанном на структуре ссылочного документа MS Excel (с именем "диапазоны").</span><span class="sxs-lookup"><span data-stu-id="57402-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="57402-158">Создание нового источника данных для расчета итогов по кодам валюты</span><span class="sxs-lookup"><span data-stu-id="57402-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="57402-159">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="57402-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="57402-160">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="57402-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="57402-161">В дереве выберите "Функции\Группировка по".</span><span class="sxs-lookup"><span data-stu-id="57402-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="57402-162">В поле "Имя" введите "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="57402-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="57402-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="57402-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="57402-164">Щелкните "Изменить группу по".</span><span class="sxs-lookup"><span data-stu-id="57402-164">Click Edit group by.</span></span>
6. <span data-ttu-id="57402-165">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="57402-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="57402-166">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="57402-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="57402-167">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="57402-167">Click Add field to.</span></span>
9. <span data-ttu-id="57402-168">Щелкните "Элементы для группировки".</span><span class="sxs-lookup"><span data-stu-id="57402-168">Click What to group.</span></span>
10. <span data-ttu-id="57402-169">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="57402-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="57402-170">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="57402-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="57402-171">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="57402-171">Click Add field to.</span></span>
13. <span data-ttu-id="57402-172">Щелкните "Сгруппированные поля".</span><span class="sxs-lookup"><span data-stu-id="57402-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="57402-173">В дереве выберите "модель\Платежи\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="57402-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="57402-174">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="57402-174">Click Add field to.</span></span>
16. <span data-ttu-id="57402-175">Щелкните "Поля агрегирования".</span><span class="sxs-lookup"><span data-stu-id="57402-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="57402-176">В поле "Метод" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="57402-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="57402-177">Выберите функцию агрегирования SUM.</span><span class="sxs-lookup"><span data-stu-id="57402-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="57402-178">В поле "Имя" введите "TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="57402-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="57402-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="57402-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="57402-180">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57402-180">Click Save.</span></span>
20. <span data-ttu-id="57402-181">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-181">Close the page.</span></span>
21. <span data-ttu-id="57402-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57402-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="57402-183">Сопоставление компонентов формата с источниками данных</span><span class="sxs-lookup"><span data-stu-id="57402-183">Map format components to data sources</span></span>
1. <span data-ttu-id="57402-184">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="57402-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="57402-185">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="57402-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="57402-186">В дереве разверните узел "модель\Платежи\Инициирующий субъект(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="57402-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="57402-187">В дереве выберите "модель\Платежи\Инициирующий субъект(InitiatingParty)\Имя".</span><span class="sxs-lookup"><span data-stu-id="57402-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="57402-188">В дереве разверните "Excel\ReportHeader".</span><span class="sxs-lookup"><span data-stu-id="57402-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="57402-189">В дереве выберите "Excel\ReportHeader\CompanyName".</span><span class="sxs-lookup"><span data-stu-id="57402-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="57402-190">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-190">Click Bind.</span></span>
8. <span data-ttu-id="57402-191">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="57402-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="57402-192">В дереве разверните узел "модель\Платежи\Кредитор\Идентификация".</span><span class="sxs-lookup"><span data-stu-id="57402-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="57402-193">В дереве выберите "модель\Платежи\Кредитор\Идентификация\Код источника(SourceID)".</span><span class="sxs-lookup"><span data-stu-id="57402-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="57402-194">В дереве разверните "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="57402-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="57402-195">В дереве выберите "Excel\PaymLines\VendAccountName".</span><span class="sxs-lookup"><span data-stu-id="57402-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="57402-196">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-196">Click Bind.</span></span>
14. <span data-ttu-id="57402-197">В дереве выберите "модель\Платежи\Кредитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="57402-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="57402-198">В дереве выберите "Excel\PaymLines\VendName".</span><span class="sxs-lookup"><span data-stu-id="57402-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="57402-199">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-199">Click Bind.</span></span>
17. <span data-ttu-id="57402-200">В дереве разверните узел "модель\Платежи\Счет кредитора(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="57402-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="57402-201">В дереве выберите "модель\Платежи\Счет кредитора(CreditorAccount)\Имя".</span><span class="sxs-lookup"><span data-stu-id="57402-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="57402-202">В дереве выберите "Excel\PaymLines\Банк".</span><span class="sxs-lookup"><span data-stu-id="57402-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="57402-203">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-203">Click Bind.</span></span>
21. <span data-ttu-id="57402-204">В дереве выберите "модель\Платежи\Агент кредитора(CreditorAgent)\Внутренний номер(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="57402-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="57402-205">В дереве выберите "Excel\PaymLines\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="57402-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="57402-206">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-206">Click Bind.</span></span>
24. <span data-ttu-id="57402-207">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="57402-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="57402-208">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)\Identification".</span><span class="sxs-lookup"><span data-stu-id="57402-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="57402-209">В дереве выберите "модель\Платежи\Счет кредитора(CreditorAccount)\Идентификация\Номер".</span><span class="sxs-lookup"><span data-stu-id="57402-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="57402-210">В дереве выберите "Excel\PaymLines\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="57402-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="57402-211">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-211">Click Bind.</span></span>
29. <span data-ttu-id="57402-212">В дереве выберите "модель\Платежи\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="57402-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="57402-213">В дереве выберите "Excel\PaymLines\Дебет".</span><span class="sxs-lookup"><span data-stu-id="57402-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="57402-214">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-214">Click Bind.</span></span>
32. <span data-ttu-id="57402-215">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="57402-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="57402-216">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="57402-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="57402-217">В дереве разверните узел "модель\Платежи\Счет кредитора(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="57402-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="57402-218">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="57402-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="57402-219">В дереве выберите "Excel\PaymLines\Валюта".</span><span class="sxs-lookup"><span data-stu-id="57402-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="57402-220">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-220">Click Bind.</span></span>
38. <span data-ttu-id="57402-221">В дереве разверните узел "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="57402-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="57402-222">В дереве разверните узел "PaymentByCurrency\сгруппировано".</span><span class="sxs-lookup"><span data-stu-id="57402-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="57402-223">В дереве выберите "PaymentByCurrency\сгруппировано\Валюта".</span><span class="sxs-lookup"><span data-stu-id="57402-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="57402-224">В дереве разверните "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="57402-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="57402-225">В дереве выберите "Excel\SummaryLines\SummaryCurrency".</span><span class="sxs-lookup"><span data-stu-id="57402-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="57402-226">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-226">Click Bind.</span></span>
44. <span data-ttu-id="57402-227">В дереве разверните узел "PaymentByCurrency\агрегировано".</span><span class="sxs-lookup"><span data-stu-id="57402-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="57402-228">В дереве выберите "PaymentByCurrency\агрегировано\TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="57402-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="57402-229">В дереве выберите "Excel\SummaryLines\SummaryAmount".</span><span class="sxs-lookup"><span data-stu-id="57402-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="57402-230">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-230">Click Bind.</span></span>
48. <span data-ttu-id="57402-231">В дереве выберите "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="57402-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="57402-232">В дереве выберите "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="57402-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="57402-233">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-233">Click Bind.</span></span>
51. <span data-ttu-id="57402-234">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="57402-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="57402-235">В дереве выберите "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="57402-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="57402-236">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="57402-236">Click Bind.</span></span>
54. <span data-ttu-id="57402-237">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57402-237">Click Save.</span></span>
55. <span data-ttu-id="57402-238">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="57402-239">Использование созданной конфигурации для обработки платежей</span><span class="sxs-lookup"><span data-stu-id="57402-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="57402-240">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="57402-240">Click Change status.</span></span>
2. <span data-ttu-id="57402-241">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="57402-241">Click Complete.</span></span>
3. <span data-ttu-id="57402-242">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57402-242">Click OK.</span></span>
4. <span data-ttu-id="57402-243">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-243">Close the page.</span></span>
5. <span data-ttu-id="57402-244">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-244">Close the page.</span></span>
6. <span data-ttu-id="57402-245">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="57402-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="57402-246">Используйте экспресс-фильтр для фильтрации поля "Способ оплаты" со значением ''Электронно".</span><span class="sxs-lookup"><span data-stu-id="57402-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="57402-247">Электронно</span><span class="sxs-lookup"><span data-stu-id="57402-247">Electronic</span></span>  
8. <span data-ttu-id="57402-248">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="57402-248">Click Edit.</span></span>
9. <span data-ttu-id="57402-249">Разверните раздел "Форматы файлов".</span><span class="sxs-lookup"><span data-stu-id="57402-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="57402-250">В поле "Общая электронная отчетность" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="57402-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="57402-251">В поле "Экспорт конфигурации формата" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="57402-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="57402-252">Выберите конфигурацию "Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="57402-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="57402-253">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57402-253">Click Save.</span></span>
13. <span data-ttu-id="57402-254">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="57402-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="57402-255">Использование созданной конфигурации для тестирования обработки журналов платежей</span><span class="sxs-lookup"><span data-stu-id="57402-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="57402-256">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="57402-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="57402-257">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57402-257">Click New.</span></span>
    * <span data-ttu-id="57402-258">Создайте новый журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="57402-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="57402-259">В поле "Имя" введите "VendPay".</span><span class="sxs-lookup"><span data-stu-id="57402-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="57402-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="57402-260">VendPay</span></span>  
4. <span data-ttu-id="57402-261">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="57402-261">Click Lines.</span></span>
5. <span data-ttu-id="57402-262">В поле "Счет" укажите значения "GB_SI_000001".</span><span class="sxs-lookup"><span data-stu-id="57402-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="57402-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="57402-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="57402-264">Установите для параметра "Дебет" значение "1000".</span><span class="sxs-lookup"><span data-stu-id="57402-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="57402-265">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="57402-265">Click New.</span></span>
8. <span data-ttu-id="57402-266">В поле "Счет" укажите значения "GB_SI_000005".</span><span class="sxs-lookup"><span data-stu-id="57402-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="57402-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="57402-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="57402-268">Установите для параметра "Дебет" значение "2000".</span><span class="sxs-lookup"><span data-stu-id="57402-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="57402-269">В поле "Валюта" введите значение "Евро".</span><span class="sxs-lookup"><span data-stu-id="57402-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="57402-270">Евро</span><span class="sxs-lookup"><span data-stu-id="57402-270">EUR</span></span>  
11. <span data-ttu-id="57402-271">В поле "Корр.счет" укажите требуемые значения "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="57402-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="57402-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="57402-272">GBSI OPER</span></span>  
12. <span data-ttu-id="57402-273">В поле "Способ оплаты" введите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="57402-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="57402-274">Электронно</span><span class="sxs-lookup"><span data-stu-id="57402-274">Electronic</span></span>  
13. <span data-ttu-id="57402-275">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="57402-275">Click Save.</span></span>
14. <span data-ttu-id="57402-276">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="57402-276">Click Generate payments.</span></span>
15. <span data-ttu-id="57402-277">В поле "Способ оплаты" введите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="57402-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="57402-278">Электронно</span><span class="sxs-lookup"><span data-stu-id="57402-278">Electronic</span></span>  
16. <span data-ttu-id="57402-279">В поле "Имя файла" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="57402-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="57402-280">Например, введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="57402-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="57402-281">В поле "Банковский счет" введите "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="57402-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="57402-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="57402-282">GBSI OPER</span></span>  
18. <span data-ttu-id="57402-283">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57402-283">Click OK.</span></span>
19. <span data-ttu-id="57402-284">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="57402-284">Click OK.</span></span>
    * <span data-ttu-id="57402-285">Просмотрите созданный лист, включая сведения строк платежа, а так же итоги для каждого кода валюты, используемого в этом сообщении платежа.</span><span class="sxs-lookup"><span data-stu-id="57402-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


