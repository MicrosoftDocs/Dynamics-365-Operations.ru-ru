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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="bd74a-103">Разработка конфигурации для создания отчетов в формате OpenXML для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="bd74a-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd74a-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую шаблон для создания электронных документов в формате OPENXML.</span><span class="sxs-lookup"><span data-stu-id="bd74a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="bd74a-105">Эта конфигурация будет использоваться для обработки платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="bd74a-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="bd74a-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="bd74a-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="bd74a-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="bd74a-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="bd74a-108">Также необходимо иметь файл Excel, который будет импортирован при создании шаблона.</span><span class="sxs-lookup"><span data-stu-id="bd74a-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="bd74a-109">Доступ к этой файлу можно получить на странице https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="bd74a-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="bd74a-110">Отправка конфигурации модели данных платежей</span><span class="sxs-lookup"><span data-stu-id="bd74a-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="bd74a-111">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="bd74a-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="bd74a-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bd74a-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bd74a-113">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="bd74a-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="bd74a-114">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="bd74a-114">Click Set active.</span></span>
4. <span data-ttu-id="bd74a-115">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="bd74a-115">Click Repositories.</span></span>
    * <span data-ttu-id="bd74a-116">Выберите репозиторий для типа "Операционные ресурсы", если он имеется.</span><span class="sxs-lookup"><span data-stu-id="bd74a-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="bd74a-117">Если он доступен, пропустите следующие шаги по созданию нового репозитория.</span><span class="sxs-lookup"><span data-stu-id="bd74a-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="bd74a-118">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bd74a-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="bd74a-119">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="bd74a-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="bd74a-120">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="bd74a-120">Click Create repository.</span></span>
8. <span data-ttu-id="bd74a-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd74a-121">Click OK.</span></span>
9. <span data-ttu-id="bd74a-122">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="bd74a-122">Click Open.</span></span>
10. <span data-ttu-id="bd74a-123">В дереве выберите "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="bd74a-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="bd74a-124">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="bd74a-124">Click Import.</span></span>
    * <span data-ttu-id="bd74a-125">Импортируйте эту модель данных.</span><span class="sxs-lookup"><span data-stu-id="bd74a-125">Import this data model.</span></span> <span data-ttu-id="bd74a-126">Она будет использоваться в качестве источника данных в новой конфигурации формата.</span><span class="sxs-lookup"><span data-stu-id="bd74a-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="bd74a-127">Пропустите этот шаг, если эта конфигурация уже была импортирована.</span><span class="sxs-lookup"><span data-stu-id="bd74a-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="bd74a-128">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="bd74a-128">Click Yes.</span></span>
13. <span data-ttu-id="bd74a-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-129">Close the page.</span></span>
14. <span data-ttu-id="bd74a-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="bd74a-131">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="bd74a-131">Create a new format configuration</span></span>
1. <span data-ttu-id="bd74a-132">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="bd74a-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="bd74a-133">В дереве выберите "Модель платежа".</span><span class="sxs-lookup"><span data-stu-id="bd74a-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="bd74a-134">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bd74a-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="bd74a-135">В поле "Создать" введите "Формат, основанный на модели данных PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="bd74a-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="bd74a-136">Создайте формат, основанный на модели данных PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="bd74a-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="bd74a-137">В поле "Имя" введите "Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="bd74a-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="bd74a-138">Пример отчета о листе</span><span class="sxs-lookup"><span data-stu-id="bd74a-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="bd74a-139">В поле "Описание" введите "Пример отчета о листе для платежей поставщиков".</span><span class="sxs-lookup"><span data-stu-id="bd74a-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="bd74a-140">Пример отчета о листе для платежей поставщиков.</span><span class="sxs-lookup"><span data-stu-id="bd74a-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="bd74a-141">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd74a-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="bd74a-142">Выберите определение "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="bd74a-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="bd74a-143">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bd74a-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="bd74a-144">Разработка нового документа в формате листа OPENXML</span><span class="sxs-lookup"><span data-stu-id="bd74a-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="bd74a-145">В дереве выберите "Модель платежа\Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="bd74a-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="bd74a-146">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="bd74a-146">Click Designer.</span></span>
3. <span data-ttu-id="bd74a-147">В области действий щелкните "Импорт".</span><span class="sxs-lookup"><span data-stu-id="bd74a-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="bd74a-148">Щелкните "Импорт из Excel".</span><span class="sxs-lookup"><span data-stu-id="bd74a-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="bd74a-149">Нажмите кнопку Вложения.</span><span class="sxs-lookup"><span data-stu-id="bd74a-149">Click Attachments.</span></span>
    * <span data-ttu-id="bd74a-150">Вложите существующий документ Excel как шаблон.</span><span class="sxs-lookup"><span data-stu-id="bd74a-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="bd74a-151">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-151">Click New.</span></span>
7. <span data-ttu-id="bd74a-152">Щелкните "Файл".</span><span class="sxs-lookup"><span data-stu-id="bd74a-152">Click File.</span></span>
    * <span data-ttu-id="bd74a-153">Укажите на существующий файл Excel.</span><span class="sxs-lookup"><span data-stu-id="bd74a-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="bd74a-154">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-154">Close the page.</span></span>
9. <span data-ttu-id="bd74a-155">В поле "Шаблон" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd74a-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="bd74a-156">Выберите вложенный файл Excel для использования в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="bd74a-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="bd74a-157">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd74a-157">Click OK.</span></span>
    * <span data-ttu-id="bd74a-158">Обратите внимание, что компоненты формата электронной отчетности были созданы в формате создания, основанном на структуре ссылочного документа MS Excel (с именем "диапазоны").</span><span class="sxs-lookup"><span data-stu-id="bd74a-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="bd74a-159">Создание нового источника данных для расчета итогов по кодам валюты</span><span class="sxs-lookup"><span data-stu-id="bd74a-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="bd74a-160">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="bd74a-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="bd74a-161">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bd74a-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="bd74a-162">В дереве выберите "Функции\Группировка по".</span><span class="sxs-lookup"><span data-stu-id="bd74a-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="bd74a-163">В поле "Имя" введите "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="bd74a-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="bd74a-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="bd74a-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="bd74a-165">Щелкните "Изменить группу по".</span><span class="sxs-lookup"><span data-stu-id="bd74a-165">Click Edit group by.</span></span>
6. <span data-ttu-id="bd74a-166">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="bd74a-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="bd74a-167">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="bd74a-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="bd74a-168">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="bd74a-168">Click Add field to.</span></span>
9. <span data-ttu-id="bd74a-169">Щелкните "Элементы для группировки".</span><span class="sxs-lookup"><span data-stu-id="bd74a-169">Click What to group.</span></span>
10. <span data-ttu-id="bd74a-170">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="bd74a-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="bd74a-171">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="bd74a-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="bd74a-172">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="bd74a-172">Click Add field to.</span></span>
13. <span data-ttu-id="bd74a-173">Щелкните "Сгруппированные поля".</span><span class="sxs-lookup"><span data-stu-id="bd74a-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="bd74a-174">В дереве выберите "модель\Платежи\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="bd74a-175">Щелкните "Добавить поле в".</span><span class="sxs-lookup"><span data-stu-id="bd74a-175">Click Add field to.</span></span>
16. <span data-ttu-id="bd74a-176">Щелкните "Поля агрегирования".</span><span class="sxs-lookup"><span data-stu-id="bd74a-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="bd74a-177">В поле "Метод" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="bd74a-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="bd74a-178">Выберите функцию агрегирования SUM.</span><span class="sxs-lookup"><span data-stu-id="bd74a-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="bd74a-179">В поле "Имя" введите "TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="bd74a-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="bd74a-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="bd74a-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="bd74a-181">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bd74a-181">Click Save.</span></span>
20. <span data-ttu-id="bd74a-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-182">Close the page.</span></span>
21. <span data-ttu-id="bd74a-183">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd74a-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="bd74a-184">Сопоставление компонентов формата с источниками данных</span><span class="sxs-lookup"><span data-stu-id="bd74a-184">Map format components to data sources</span></span>
1. <span data-ttu-id="bd74a-185">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="bd74a-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="bd74a-186">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="bd74a-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="bd74a-187">В дереве разверните узел "модель\Платежи\Инициирующий субъект(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="bd74a-188">В дереве выберите "модель\Платежи\Инициирующий субъект(InitiatingParty)\Имя".</span><span class="sxs-lookup"><span data-stu-id="bd74a-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="bd74a-189">В дереве разверните "Excel\ReportHeader".</span><span class="sxs-lookup"><span data-stu-id="bd74a-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="bd74a-190">В дереве выберите "Excel\ReportHeader\CompanyName".</span><span class="sxs-lookup"><span data-stu-id="bd74a-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="bd74a-191">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-191">Click Bind.</span></span>
8. <span data-ttu-id="bd74a-192">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="bd74a-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="bd74a-193">В дереве разверните узел "модель\Платежи\Кредитор\Идентификация".</span><span class="sxs-lookup"><span data-stu-id="bd74a-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="bd74a-194">В дереве выберите "модель\Платежи\Кредитор\Идентификация\Код источника(SourceID)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="bd74a-195">В дереве разверните "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="bd74a-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="bd74a-196">В дереве выберите "Excel\PaymLines\VendAccountName".</span><span class="sxs-lookup"><span data-stu-id="bd74a-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="bd74a-197">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-197">Click Bind.</span></span>
14. <span data-ttu-id="bd74a-198">В дереве выберите "модель\Платежи\Кредитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="bd74a-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="bd74a-199">В дереве выберите "Excel\PaymLines\VendName".</span><span class="sxs-lookup"><span data-stu-id="bd74a-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="bd74a-200">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-200">Click Bind.</span></span>
17. <span data-ttu-id="bd74a-201">В дереве разверните узел "модель\Платежи\Счет кредитора(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="bd74a-202">В дереве выберите "модель\Платежи\Счет кредитора(CreditorAccount)\Имя".</span><span class="sxs-lookup"><span data-stu-id="bd74a-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="bd74a-203">В дереве выберите "Excel\PaymLines\Банк".</span><span class="sxs-lookup"><span data-stu-id="bd74a-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="bd74a-204">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-204">Click Bind.</span></span>
21. <span data-ttu-id="bd74a-205">В дереве выберите "модель\Платежи\Агент кредитора(CreditorAgent)\Внутренний номер(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="bd74a-206">В дереве выберите "Excel\PaymLines\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="bd74a-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="bd74a-207">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-207">Click Bind.</span></span>
24. <span data-ttu-id="bd74a-208">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="bd74a-209">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)\Identification".</span><span class="sxs-lookup"><span data-stu-id="bd74a-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="bd74a-210">В дереве выберите "модель\Платежи\Счет кредитора(CreditorAccount)\Идентификация\Номер".</span><span class="sxs-lookup"><span data-stu-id="bd74a-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="bd74a-211">В дереве выберите "Excel\PaymLines\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="bd74a-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="bd74a-212">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-212">Click Bind.</span></span>
29. <span data-ttu-id="bd74a-213">В дереве выберите "модель\Платежи\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="bd74a-214">В дереве выберите "Excel\PaymLines\Дебет".</span><span class="sxs-lookup"><span data-stu-id="bd74a-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="bd74a-215">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-215">Click Bind.</span></span>
32. <span data-ttu-id="bd74a-216">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="bd74a-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="bd74a-217">В дереве разверните узел "model\Payments\Creditor Account(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="bd74a-218">В дереве разверните узел "модель\Платежи\Счет кредитора(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="bd74a-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="bd74a-219">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="bd74a-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="bd74a-220">В дереве выберите "Excel\PaymLines\Валюта".</span><span class="sxs-lookup"><span data-stu-id="bd74a-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="bd74a-221">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-221">Click Bind.</span></span>
38. <span data-ttu-id="bd74a-222">В дереве разверните узел "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="bd74a-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="bd74a-223">В дереве разверните узел "PaymentByCurrency\сгруппировано".</span><span class="sxs-lookup"><span data-stu-id="bd74a-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="bd74a-224">В дереве выберите "PaymentByCurrency\сгруппировано\Валюта".</span><span class="sxs-lookup"><span data-stu-id="bd74a-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="bd74a-225">В дереве разверните "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="bd74a-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="bd74a-226">В дереве выберите "Excel\SummaryLines\SummaryCurrency".</span><span class="sxs-lookup"><span data-stu-id="bd74a-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="bd74a-227">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-227">Click Bind.</span></span>
44. <span data-ttu-id="bd74a-228">В дереве разверните узел "PaymentByCurrency\агрегировано".</span><span class="sxs-lookup"><span data-stu-id="bd74a-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="bd74a-229">В дереве выберите "PaymentByCurrency\агрегировано\TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="bd74a-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="bd74a-230">В дереве выберите "Excel\SummaryLines\SummaryAmount".</span><span class="sxs-lookup"><span data-stu-id="bd74a-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="bd74a-231">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-231">Click Bind.</span></span>
48. <span data-ttu-id="bd74a-232">В дереве выберите "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="bd74a-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="bd74a-233">В дереве выберите "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="bd74a-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="bd74a-234">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-234">Click Bind.</span></span>
51. <span data-ttu-id="bd74a-235">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="bd74a-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="bd74a-236">В дереве выберите "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="bd74a-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="bd74a-237">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-237">Click Bind.</span></span>
54. <span data-ttu-id="bd74a-238">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bd74a-238">Click Save.</span></span>
55. <span data-ttu-id="bd74a-239">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="bd74a-240">Использование созданной конфигурации для обработки платежей</span><span class="sxs-lookup"><span data-stu-id="bd74a-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="bd74a-241">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="bd74a-241">Click Change status.</span></span>
2. <span data-ttu-id="bd74a-242">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="bd74a-242">Click Complete.</span></span>
3. <span data-ttu-id="bd74a-243">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd74a-243">Click OK.</span></span>
4. <span data-ttu-id="bd74a-244">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-244">Close the page.</span></span>
5. <span data-ttu-id="bd74a-245">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-245">Close the page.</span></span>
6. <span data-ttu-id="bd74a-246">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="bd74a-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="bd74a-247">Используйте экспресс-фильтр для фильтрации поля "Способ оплаты" со значением ''Электронно".</span><span class="sxs-lookup"><span data-stu-id="bd74a-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="bd74a-248">Электронно</span><span class="sxs-lookup"><span data-stu-id="bd74a-248">Electronic</span></span>  
8. <span data-ttu-id="bd74a-249">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bd74a-249">Click Edit.</span></span>
9. <span data-ttu-id="bd74a-250">Разверните раздел "Форматы файлов".</span><span class="sxs-lookup"><span data-stu-id="bd74a-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="bd74a-251">В поле "Общая электронная отчетность" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="bd74a-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="bd74a-252">В поле "Экспорт конфигурации формата" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd74a-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="bd74a-253">Выберите конфигурацию "Пример отчета о листе".</span><span class="sxs-lookup"><span data-stu-id="bd74a-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="bd74a-254">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bd74a-254">Click Save.</span></span>
13. <span data-ttu-id="bd74a-255">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd74a-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="bd74a-256">Использование созданной конфигурации для тестирования обработки журналов платежей</span><span class="sxs-lookup"><span data-stu-id="bd74a-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="bd74a-257">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="bd74a-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="bd74a-258">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-258">Click New.</span></span>
    * <span data-ttu-id="bd74a-259">Создайте новый журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="bd74a-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="bd74a-260">В поле "Имя" введите "VendPay".</span><span class="sxs-lookup"><span data-stu-id="bd74a-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="bd74a-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="bd74a-261">VendPay</span></span>  
4. <span data-ttu-id="bd74a-262">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="bd74a-262">Click Lines.</span></span>
5. <span data-ttu-id="bd74a-263">В поле "Счет" укажите значения "GB_SI_000001".</span><span class="sxs-lookup"><span data-stu-id="bd74a-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="bd74a-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="bd74a-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="bd74a-265">Установите для параметра "Дебет" значение "1000".</span><span class="sxs-lookup"><span data-stu-id="bd74a-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="bd74a-266">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd74a-266">Click New.</span></span>
8. <span data-ttu-id="bd74a-267">В поле "Счет" укажите значения "GB_SI_000005".</span><span class="sxs-lookup"><span data-stu-id="bd74a-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="bd74a-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="bd74a-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="bd74a-269">Установите для параметра "Дебет" значение "2000".</span><span class="sxs-lookup"><span data-stu-id="bd74a-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="bd74a-270">В поле "Валюта" введите значение "Евро".</span><span class="sxs-lookup"><span data-stu-id="bd74a-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="bd74a-271">Евро</span><span class="sxs-lookup"><span data-stu-id="bd74a-271">EUR</span></span>  
11. <span data-ttu-id="bd74a-272">В поле "Корр.счет" укажите требуемые значения "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="bd74a-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="bd74a-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="bd74a-273">GBSI OPER</span></span>  
12. <span data-ttu-id="bd74a-274">В поле "Способ оплаты" введите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="bd74a-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="bd74a-275">Электронно</span><span class="sxs-lookup"><span data-stu-id="bd74a-275">Electronic</span></span>  
13. <span data-ttu-id="bd74a-276">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bd74a-276">Click Save.</span></span>
14. <span data-ttu-id="bd74a-277">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="bd74a-277">Click Generate payments.</span></span>
15. <span data-ttu-id="bd74a-278">В поле "Способ оплаты" введите "Электронно".</span><span class="sxs-lookup"><span data-stu-id="bd74a-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="bd74a-279">Электронно</span><span class="sxs-lookup"><span data-stu-id="bd74a-279">Electronic</span></span>  
16. <span data-ttu-id="bd74a-280">В поле "Имя файла" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="bd74a-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="bd74a-281">Например, введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="bd74a-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="bd74a-282">В поле "Банковский счет" введите "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="bd74a-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="bd74a-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="bd74a-283">GBSI OPER</span></span>  
18. <span data-ttu-id="bd74a-284">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd74a-284">Click OK.</span></span>
19. <span data-ttu-id="bd74a-285">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd74a-285">Click OK.</span></span>
    * <span data-ttu-id="bd74a-286">Просмотрите созданный лист, включая сведения строк платежа, а так же итоги для каждого кода валюты, используемого в этом сообщении платежа.</span><span class="sxs-lookup"><span data-stu-id="bd74a-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


