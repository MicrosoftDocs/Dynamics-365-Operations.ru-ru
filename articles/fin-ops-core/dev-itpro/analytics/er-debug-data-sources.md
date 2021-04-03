---
title: Отладка источников данных для выполняемого формата электронной отчетности для анализа потока и преобразования данных
description: В этой теме объясняется, как можно отлаживать источники данных выполняемого формата электронной отчетности, чтобы лучше понимать настроенные поток и преобразование данных.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: bda81da80996d8cba38ac48e29c47ffef61d3bdb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562198"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="1f49e-103">Отладка источников данных для выполняемого формата электронной отчетности для анализа потока и преобразования данных</span><span class="sxs-lookup"><span data-stu-id="1f49e-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="1f49e-104">В процессе [настройки](tasks/er-format-configuration-2016-11.md) решения электронной отчетности (ER) для создания исходящих электронных документов определяются методы, используемые для извлечения данных из приложения и их ввода в формируемые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="1f49e-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="1f49e-105">Чтобы обеспечить более эффективную поддержку жизненного цикла решения ER, решение должно состоять из [модели данных](general-electronic-reporting.md#DataModelComponent) ER и [сопоставления](general-electronic-reporting.md#ModelMappingComponent) компонентов, а также [формата](general-electronic-reporting.md#FormatComponentOutbound) ER и компонентов сопоставления, чтобы сопоставление моделей было привязано к приложению, в то время как другие компоненты остаются независимыми от приложения.</span><span class="sxs-lookup"><span data-stu-id="1f49e-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="1f49e-106">Поэтому некоторые компоненты ER могут [влиять](general-electronic-reporting.md#FormatComponentOutbound) на процесс ввода данных в формируемые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="1f49e-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="1f49e-107">Иногда выходные данные выглядят иначе, чем те же данные в базе данных приложения.</span><span class="sxs-lookup"><span data-stu-id="1f49e-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="1f49e-108">В этих случаях нужно определить, какой компонент ER отвечает за преобразование данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="1f49e-109">Функция отладчика источника данных ER значительно сокращает время и затраты, связанные с таким исследованием.</span><span class="sxs-lookup"><span data-stu-id="1f49e-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="1f49e-110">Вы можете прервать выполнение формата ER и открыть интерфейс отладчика источника данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="1f49e-111">В нем можно посмотреть доступные источники данных и выбрать отдельный источник данных для выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f49e-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="1f49e-112">Такое выполнение вручную имитирует выполнение источника данных во время фактического выполнения формата ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="1f49e-113">Результат представляется на странице, где можно проанализировать полученные данные.</span><span class="sxs-lookup"><span data-stu-id="1f49e-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="1f49e-114">Чтобы включить функцию отладки источников данных, установите для параметра **Включить отладку данных при выполнении формата** значение **Да** в пользовательских параметрах ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="1f49e-115">Затем можно запустить отладку источника данных во время выполнения формата ER для создания исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="1f49e-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="1f49e-116">Вы также можете использовать параметр **Начать отладку**, чтобы начать отладку источника данных для формата ER, который настроен в [конструкторе операций ER](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="1f49e-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="1f49e-117">В этом разделе приводятся рекомендации по запуску отладки источников данных для выполняемых форматов ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="1f49e-118">В нем объясняется, как эти сведения могут помочь в понимании потока данных и преобразования данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="1f49e-119">В примерах этого раздела используется бизнес-процесс обработки платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="1f49e-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="1f49e-120">Ограничения</span><span class="sxs-lookup"><span data-stu-id="1f49e-120">Limitations</span></span>

<span data-ttu-id="1f49e-121">Отладчик источников данных может использоваться для доступа к источникам данных, которые используются в форматах ER, которые запускаются для формирования исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="1f49e-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="1f49e-122">Его нельзя использовать для отладки источников данных форматов ER, предназначенных для анализа входящих документов.</span><span class="sxs-lookup"><span data-stu-id="1f49e-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="1f49e-123">Следующие параметры форматов ER в настоящее время недоступны при отладки источников данных:</span><span class="sxs-lookup"><span data-stu-id="1f49e-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="1f49e-124">Преобразования форматов</span><span class="sxs-lookup"><span data-stu-id="1f49e-124">Format transformations</span></span>
- <span data-ttu-id="1f49e-125">Правила проверки форматов и сопоставления</span><span class="sxs-lookup"><span data-stu-id="1f49e-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="1f49e-126">Вспомогательные выражения</span><span class="sxs-lookup"><span data-stu-id="1f49e-126">Enabling expressions</span></span>
- <span data-ttu-id="1f49e-127">Сведения о сборе данных в памяти</span><span class="sxs-lookup"><span data-stu-id="1f49e-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1f49e-128">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="1f49e-128">Prerequisites</span></span>

- <span data-ttu-id="1f49e-129">Чтобы выполнить примеры в этом разделе, необходимо иметь доступ к одной из следующих [ролей](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="1f49e-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="1f49e-130">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="1f49e-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="1f49e-131">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="1f49e-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="1f49e-132">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="1f49e-132">System administrator</span></span>

- <span data-ttu-id="1f49e-133">Компания должна иметь значение **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="1f49e-134">Выполните действия в [Приложении 1](#appendix1) этого раздела, чтобы загрузить компоненты решения Microsoft ER, необходимые для обработки платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="1f49e-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="1f49e-135">Выполните действия в [Приложении 2](#appendix2) этого раздела, чтобы подготовить расчеты с поставщиками для обработки платежей поставщика с помощью решения ER, которое необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="1f49e-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="1f49e-136">Обработка платежа поставщику для получения файла платежа</span><span class="sxs-lookup"><span data-stu-id="1f49e-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="1f49e-137">Выполните действия в [Приложении 3](#appendix3) этого раздела, чтобы обработать платежи поставщикам.</span><span class="sxs-lookup"><span data-stu-id="1f49e-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Выполняется обработка платежа поставщику](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="1f49e-139">Загрузите и сохраните файл ZIP на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1f49e-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="1f49e-140">Извлеките файл платежа **ISO20022 Credit transfer.xml** из ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="1f49e-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="1f49e-141">Откройте извлеченный файл платежа с помощью средства просмотра файлов XML.</span><span class="sxs-lookup"><span data-stu-id="1f49e-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="1f49e-142">В файле платежа код IBAN (International Bank Account Number) банковского счета поставщика указан без пробелов.</span><span class="sxs-lookup"><span data-stu-id="1f49e-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="1f49e-143">Поэтому он отличается от значения, [введенного](#enteredIBANcode) на странице **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![Код IBAN без пробелов](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="1f49e-145">С помощью отладчика источников данных ER можно узнать, какой компонент решения ER используется для удаления пробелов из кода IBAN.</span><span class="sxs-lookup"><span data-stu-id="1f49e-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="1f49e-146">Включение отладки источников данных</span><span class="sxs-lookup"><span data-stu-id="1f49e-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="1f49e-147">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1f49e-148">На странице **Конфигурации** в области действий на вкладке **Конфигурации** в группе **Дополнительные параметры** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="1f49e-149">Для параметра **Включить отладку данных при выполнении формата** установите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f49e-150">Этот параметр используется отдельно для пользователя и для компании.</span><span class="sxs-lookup"><span data-stu-id="1f49e-150">This parameter is user-specific and company-specific.</span></span>

    ![Диалоговое окно параметров пользователя](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="1f49e-152">Обработка платежа поставщику для отладки</span><span class="sxs-lookup"><span data-stu-id="1f49e-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="1f49e-153">Выполните действия в [Приложении 3](#appendix3) этого раздела, чтобы обработать платежи поставщикам.</span><span class="sxs-lookup"><span data-stu-id="1f49e-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="1f49e-154">В окне сообщения выберите **Да** для подтверждения того, что требуется прервать обработку платежей поставщика, а вместо этого запустить отладку источника данных на странице **Отладка источников данных**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Окно сообщения о подтверждении](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="1f49e-156">Отладка источников данных, используемых в обработке платежей</span><span class="sxs-lookup"><span data-stu-id="1f49e-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="1f49e-157">Отладка сопоставления моделей</span><span class="sxs-lookup"><span data-stu-id="1f49e-157">Debug the model mapping</span></span>

1. <span data-ttu-id="1f49e-158">На странице **Отладка источников данных** в области действий выберите **Сопоставление моделей**, чтобы начать отладку из этого компонента ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="1f49e-159">На панели источников данных слева выберите **\$notSentTransactions**, а затем выберите **Читать все записи**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="1f49e-160">Можно выбрать **Читать 1 запись**, **Читать 10 записей**, **Читать 100 записей** или **Читать все записи**, чтобы получить нужное количество записей из выбранного источника данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="1f49e-161">Таким образом можно смоделировать доступ к источнику данных из выполняемого формата ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="1f49e-162">В области данных справа выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="1f49e-163">Можно увидеть, что выбранный источник данных типа **Список записей** содержит одну запись.</span><span class="sxs-lookup"><span data-stu-id="1f49e-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="1f49e-164">Разверните источник данных **\$notSentTransactions** и выберите вложенный метод **vendBankAccountInTransactionCompany()**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="1f49e-165">Разверните метод **vendBankAccountInTransactionCompany()** и выберите вложенное поле **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="1f49e-166">Выберите **Получить значение**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-166">Select **Get value**.</span></span>

    <span data-ttu-id="1f49e-167">Можно выбрать **Получить значение**, чтобы считать значение выбранного поля из выбранного источника данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="1f49e-168">Таким образом можно смоделировать доступ к этому полю из выполняемого формата ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="1f49e-169">Выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-169">Select **Expand all**.</span></span>

    ![Значение поля IBAN в сопоставлении моделей](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="1f49e-171">Как можно видеть, сопоставление моделей не имеет отношения к удалению пробелов, так как код IBAN, возвращаемый для банковского счета поставщика, содержит пробелы.</span><span class="sxs-lookup"><span data-stu-id="1f49e-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="1f49e-172">Поэтому необходимо продолжить отладку источника данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="1f49e-173">Отладка сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="1f49e-173">Debug the format mapping</span></span>

1. <span data-ttu-id="1f49e-174">На странице **Отладка источников данных** в области действий выберите **Сопоставление формата**, чтобы продолжить отладку из этого компонента ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="1f49e-175">Выберите источник **\$PaymentByDebtor**, а затем выберите **Читать все записи**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="1f49e-176">Разверните **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="1f49e-177">Разверните **\$PaymentByDebtor.Lines**, а затем выберите **Читать все записи**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="1f49e-178">Разверните **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="1f49e-179">Разверните **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, а затем выберите **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="1f49e-180">Выберите **Получить значение**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-180">Select **Get value**.</span></span>
8. <span data-ttu-id="1f49e-181">Выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-181">Select **Expand all**.</span></span>

    ![Значение поля IBAN в сопоставлении формата](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="1f49e-183">Как можно видеть, источники данных сопоставления формата не имеют отношения к удалению пробелов, так как код IBAN, возвращаемый ими для банковского счета поставщика, содержит пробелы.</span><span class="sxs-lookup"><span data-stu-id="1f49e-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="1f49e-184">Поэтому необходимо продолжить отладку источника данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="1f49e-185">Отладка формата</span><span class="sxs-lookup"><span data-stu-id="1f49e-185">Debug the format</span></span>

1. <span data-ttu-id="1f49e-186">На странице **Отладка источников данных** в области действий выберите **Формат**, чтобы продолжить отладку из этого компонента ER.</span><span class="sxs-lookup"><span data-stu-id="1f49e-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="1f49e-187">Разверните элементы формата и выберите **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, а затем выберите **Читать все записи**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="1f49e-188">Разверните элементы формата и выберите **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, а затем выберите **Читать все записи**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="1f49e-189">Разверните элементы формата и выберите **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, а затем выберите **Получить значение**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="1f49e-190">Выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-190">Select **Expand all**.</span></span>

    ![Значение поля IBAN в формате](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="1f49e-192">Как можно видеть, привязка формата не имеет отношения к удалению пробелов, так как код IBAN, возвращаемый для банковского счета поставщика, содержит пробелы.</span><span class="sxs-lookup"><span data-stu-id="1f49e-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="1f49e-193">Таким образом, элемент **BankIBAN** настроен на использование преобразования формата, которое удаляет пробелы.</span><span class="sxs-lookup"><span data-stu-id="1f49e-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="1f49e-194">Закройте отладчик источника данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="1f49e-195">Просмотр преобразований формата</span><span class="sxs-lookup"><span data-stu-id="1f49e-195">Review the format transformations</span></span>

1. <span data-ttu-id="1f49e-196">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1f49e-197">На странице **Конфигурации** выберите **Модель платежа** \> **Перенос кредита ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="1f49e-198">Выберите **Конструктор**, а затем разверните элементы и выберите **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![Элемент BankIBAN на странице конструктора формата](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="1f49e-200">Как можно видеть, элемент **BankIBAN** сконфигурирован для использования преобразования **удалить не буквенно-цифровые символы**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="1f49e-201">Выберите вкладку **Преобразования**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-201">Select the **Transformations** tab.</span></span>

    ![Вкладка "преобразования" для элемента BankIBAN](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="1f49e-203">Как можно видеть, преобразование **удалить не буквенно-цифровые символы** настроено для использования выражения, которое удаляет пробелы из введенной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="1f49e-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="1f49e-204">Начало отладки в конструкторе операций</span><span class="sxs-lookup"><span data-stu-id="1f49e-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="1f49e-205">При настройке черновой версии формата ER, которая может быть запущена непосредственно из конструктора операций, можно получить доступ к отладчику источников данных, выбрав команду **Начать отладку** в области действий.</span><span class="sxs-lookup"><span data-stu-id="1f49e-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Кнопка "Начать отладку" на странице "Конструктор форматов"](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="1f49e-207">Редактируемые в формате ER компоненты форматирования и преобразования доступны для отладки.</span><span class="sxs-lookup"><span data-stu-id="1f49e-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="1f49e-208">Начало отладки в конструкторе сопоставления моделей</span><span class="sxs-lookup"><span data-stu-id="1f49e-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="1f49e-209">При настройке сопоставления моделей ER, которое может быть запущено непосредственно со страницы **Сопоставление моделей**, можно получить доступ к отладчику источников данных, выбрав команду **Начать отладку** в области действий.</span><span class="sxs-lookup"><span data-stu-id="1f49e-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Кнопка "Начать отладку" на странице "Конструктор сопоставлений моделей"](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="1f49e-211">Изменяемый компонент сопоставления моделей в сопоставлении ER доступен для отладки.</span><span class="sxs-lookup"><span data-stu-id="1f49e-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="1f49e-212">Приложение 1. Получение решения ER</span><span class="sxs-lookup"><span data-stu-id="1f49e-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="1f49e-213">Загрузка решения ER</span><span class="sxs-lookup"><span data-stu-id="1f49e-213">Download an ER solution</span></span>

<span data-ttu-id="1f49e-214">Если необходимо использовать решение ER для создания файла электронного платежа для обрабатываемого платежа поставщику, можно [загрузить](download-electronic-reporting-configuration-lcs.md) формат платежей ER **Перенос кредита ISO20022**, доступный в библиотеки общих ресурсов в Microsoft Dynamics Lifecycle Services (LCS) или в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="1f49e-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Импорт формата платежей ER на странице "Репозиторий конфигураций"](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="1f49e-216">В дополнение к выбранному формату ER следующие [конфигурации](general-electronic-reporting.md#Configuration) должны быть автоматически импортированы в экземпляр Microsoft Dynamics 365 Finance в рамках решения **Перенос кредита ISO20022**:</span><span class="sxs-lookup"><span data-stu-id="1f49e-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="1f49e-217">**Модель платежа** [Конфигурация модели данных ER](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="1f49e-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="1f49e-218">**Перенос кредита ISO20022** [Конфигурация формата ER](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="1f49e-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="1f49e-219">**Сопоставление модели платежей 1611** [Конфигурация сопоставления моделей ER](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="1f49e-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="1f49e-220">**Сопоставление модели платежей назначению ISO20022** Конфигурация сопоставления моделей ER</span><span class="sxs-lookup"><span data-stu-id="1f49e-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="1f49e-221">Эти конфигурации можно найти на странице **Конфигурации** среды ER (**Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**).</span><span class="sxs-lookup"><span data-stu-id="1f49e-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Конфигурации, импортированные на странице конфигурации](./media/er-data-debugger-configurations.png)

<span data-ttu-id="1f49e-223">Если ранее указанные конфигурации отсутствуют в дереве конфигураций, необходимо вручную загрузить их из библиотеки общих ресурсов LCS так же, как вы загрузили формат платежей ER **Перенос кредита ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="1f49e-224">Анализ загруженного решения ER</span><span class="sxs-lookup"><span data-stu-id="1f49e-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="1f49e-225">Просмотр сопоставления моделей</span><span class="sxs-lookup"><span data-stu-id="1f49e-225">Review the model mapping</span></span>

1. <span data-ttu-id="1f49e-226">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1f49e-227">Выберите **Модель платежа** \> **Сопоставление модели платежей 1611**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="1f49e-228">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-228">Select **Designer**.</span></span>
4. <span data-ttu-id="1f49e-229">Выберите запись сопоставления **Сопоставление модели платежей ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="1f49e-230">Выберите **Конструктор**, а затем проверьте открытое сопоставление модели.</span><span class="sxs-lookup"><span data-stu-id="1f49e-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="1f49e-231">Обратите внимание, что поле **Платежи** модели данных привязано к источнику данных **\$notSentTransactions**, который возвращает список обрабатываемых строк платежа поставщику.</span><span class="sxs-lookup"><span data-stu-id="1f49e-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Поле платежей на странице конструктора сопоставления моделей](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="1f49e-233">Просмотр сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="1f49e-233">Review the format mapping</span></span>

1. <span data-ttu-id="1f49e-234">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1f49e-235">Выберите **Модель платежей** \> **Перенос кредита ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="1f49e-236">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-236">Select **Designer**.</span></span>
4. <span data-ttu-id="1f49e-237">На вкладке **Сопоставление** проверьте открытое сопоставление формата.</span><span class="sxs-lookup"><span data-stu-id="1f49e-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="1f49e-238">Обратите внимание, что элемент **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** файла **ISO20022CTReports** \> **XMLHeader** связан с источником данных **\$PaymentByDebtor**, который настроен на группировку записей в поле **Платежи** модели данных.</span><span class="sxs-lookup"><span data-stu-id="1f49e-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![Элемент PmtInf на странице конструктора формата](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="1f49e-240">Просмотр формата</span><span class="sxs-lookup"><span data-stu-id="1f49e-240">Review the format</span></span>

1. <span data-ttu-id="1f49e-241">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1f49e-242">Выберите **Модель платежей** \> **Перенос кредита ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="1f49e-243">Выберите **Конструктор**, а затем проверьте открытый формат.</span><span class="sxs-lookup"><span data-stu-id="1f49e-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="1f49e-244">Обратите внимание, что элемент **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** настроен на ввод кода IBAN счета поставщика в файле платежа.</span><span class="sxs-lookup"><span data-stu-id="1f49e-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![Элемент BankIBAN на странице конструктора формата](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="1f49e-246">Приложение 2. Настройка модуля "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="1f49e-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="1f49e-247">Изменение свойства поставщика</span><span class="sxs-lookup"><span data-stu-id="1f49e-247">Modify a vendor property</span></span>

1. <span data-ttu-id="1f49e-248">Перейдите в раздел **Расчеты с поставщиками** \> **Поставщики** \> **Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="1f49e-249">Выберите поставщика **DE-01002**, а затем в области действий на вкладке **Поставщик** в группе **Настройка** выберите **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="1f49e-250">На экспресс-вкладке **Идентификация** в поле **IBAN** <a name="enteredIBANcode"></a>введите **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="1f49e-251">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-251">Select **Save**.</span></span>

![Поле IBAN на странице банковских счетов поставщика](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="1f49e-253">Настройка способа оплаты</span><span class="sxs-lookup"><span data-stu-id="1f49e-253">Set up a method of payment</span></span>

1. <span data-ttu-id="1f49e-254">Перейдите в раздел **Расчеты с поставщиками** \> **Настройка платежей** \> **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="1f49e-255">Выберите способ оплаты **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="1f49e-256">На экспресс-вкладке **Форматы файлов** в разделе **Форматы файлов** установите для параметра **Универсальный электронный формат экспорта** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="1f49e-257">В поле **Экспорт конфигурации формата** выберите формат ER **Перенос кредита ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="1f49e-258">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-258">Select **Save**.</span></span>

![Настройки формата файлов на странице способов оплаты](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="1f49e-260">Добавление платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="1f49e-260">Add a vendor payment</span></span>

1. <span data-ttu-id="1f49e-261">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="1f49e-262">Добавьте новый журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="1f49e-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="1f49e-263">Выберите **Строки** и добавьте новую строку платежа.</span><span class="sxs-lookup"><span data-stu-id="1f49e-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="1f49e-264">В поле **Счет** выберите поставщика **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="1f49e-265">В поле **Дебет** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1f49e-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="1f49e-266">В поле **Способ оплаты** выберите **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="1f49e-267">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-267">Select **Save**.</span></span>

![Платеж поставщику добавлен на странице оплаты поставщику](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="1f49e-269">Приложение 3. Обработка платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="1f49e-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="1f49e-270">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="1f49e-271">На странице **Журнал платежей поставщику** выберите созданный ранее журнал платежей, а затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="1f49e-272">Выберите строку платежа, затем выберите **Статус платежа** \> **Нет**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="1f49e-273">Выберите **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="1f49e-274">В поле **Способ оплаты** выберите **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="1f49e-275">В поле **Банковский счет** выберите **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="1f49e-276">В диалоговом окне **Создать платежи** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="1f49e-277">В диалоговом окне **Параметры электронной отчетности** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1f49e-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]