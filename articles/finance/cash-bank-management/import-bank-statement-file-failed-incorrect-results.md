---
title: Устранение неполадок импорта файла банковской выписки
description: Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 Finance. Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом. Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты. Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки. В этой статье описывается, как исправить эти различия и устранить проблемы.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815892"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="48a8b-107">Устранение неполадок импорта файла банковской выписки</span><span class="sxs-lookup"><span data-stu-id="48a8b-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48a8b-108">Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="48a8b-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="48a8b-109">Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="48a8b-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="48a8b-110">Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты.</span><span class="sxs-lookup"><span data-stu-id="48a8b-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="48a8b-111">Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="48a8b-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="48a8b-112">В этой статье описывается, как исправить эти различия и устранить проблемы.</span><span class="sxs-lookup"><span data-stu-id="48a8b-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="48a8b-113">В чем заключается ошибка?</span><span class="sxs-lookup"><span data-stu-id="48a8b-113">What is the error?</span></span>
------------------

<span data-ttu-id="48a8b-114">После попытки импорта файла банковской выписки перейдите в журнал заданий управления данными и просмотрите сведениям о выполнении, чтобы найти ошибку.</span><span class="sxs-lookup"><span data-stu-id="48a8b-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="48a8b-115">Сведения об ошибке могут отобразиться, если навести указатель мыши на выписку, сальдо или строку выписки.</span><span class="sxs-lookup"><span data-stu-id="48a8b-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="48a8b-116">Однако, скорее всего, сведений будет недостаточно для определения поля или элемента, который является причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="48a8b-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="48a8b-117">Импортированные банковские выписки могут перекрываться только для одного момента времени.</span><span class="sxs-lookup"><span data-stu-id="48a8b-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="48a8b-118">Например, если выписка заканчивается в 00:00 1-го января 2021 года, то начальная дата следующей выписки может быть 00:00 1-го января 2021 года, 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="48a8b-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="48a8b-119">В чем различия?</span><span class="sxs-lookup"><span data-stu-id="48a8b-119">What are the differences?</span></span>
<span data-ttu-id="48a8b-120">Сравните определение формата файла банка с определением импорта Finance и обратите внимание на все различия в полях и элементах.</span><span class="sxs-lookup"><span data-stu-id="48a8b-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="48a8b-121">Сравните файл банковской выписки с соответствующим примером файла Finance.</span><span class="sxs-lookup"><span data-stu-id="48a8b-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="48a8b-122">В файлах ISO20022 все различия должны быть хорошо видны.</span><span class="sxs-lookup"><span data-stu-id="48a8b-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="48a8b-123">Различия часового пояса в импортированных банковских выписках</span><span class="sxs-lookup"><span data-stu-id="48a8b-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="48a8b-124">Значения даты и времени в файле импорта могут отличаться от значений даты и времени, которые отображаются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48a8b-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="48a8b-125">Чтобы не допустить такого несоответствия, введите предпочтительный часовой пояс на странице **Настройка источников данных**.</span><span class="sxs-lookup"><span data-stu-id="48a8b-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="48a8b-126">Дополнительную информацию о вводе предпочтительного часового пояса см. в разделе [Настройка расширенного процесса импорта банковской выверки](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="48a8b-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="48a8b-127">Преобразования</span><span class="sxs-lookup"><span data-stu-id="48a8b-127">Transformations</span></span>
<span data-ttu-id="48a8b-128">Обычно изменение необходимо внести в одно из трех преобразований.</span><span class="sxs-lookup"><span data-stu-id="48a8b-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="48a8b-129">Каждое преобразование предназначено для определенного стандарта.</span><span class="sxs-lookup"><span data-stu-id="48a8b-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="48a8b-130">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="48a8b-130">Resource name</span></span>                                         | <span data-ttu-id="48a8b-131">Имя файла</span><span class="sxs-lookup"><span data-stu-id="48a8b-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="48a8b-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="48a8b-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="48a8b-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="48a8b-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="48a8b-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="48a8b-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="48a8b-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="48a8b-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="48a8b-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="48a8b-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="48a8b-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="48a8b-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="48a8b-138">Отладка преобразований</span><span class="sxs-lookup"><span data-stu-id="48a8b-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="48a8b-139">Корректировка файлов BAI2 и MT940</span><span class="sxs-lookup"><span data-stu-id="48a8b-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="48a8b-140">Файлы BAI2 и MT940 — это основанные на тексте файлы, которые требуют корректировки для включения отладки XSLT-преобразований документов (XSLT).</span><span class="sxs-lookup"><span data-stu-id="48a8b-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="48a8b-141">Программа выполняет эту корректировку при импорте файла.</span><span class="sxs-lookup"><span data-stu-id="48a8b-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="48a8b-142">Создайте XML-файла и скопируйте в него следующий текст.</span><span class="sxs-lookup"><span data-stu-id="48a8b-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="48a8b-143">Скопируйте содержимое файла банковской выписки и вставьте его в XML-файл, чтобы оно заменило часть **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="48a8b-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="48a8b-144">Отладка XSLT</span><span class="sxs-lookup"><span data-stu-id="48a8b-144">Debug the XSLT</span></span>

<span data-ttu-id="48a8b-145">Дополнительные сведения см. в разделе <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="48a8b-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="48a8b-146">Запустите Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="48a8b-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="48a8b-147">Создайте приложение консоли.</span><span class="sxs-lookup"><span data-stu-id="48a8b-147">Create a console application.</span></span>
3.  <span data-ttu-id="48a8b-148">Откройте соответствующее преобразование XSLT.</span><span class="sxs-lookup"><span data-stu-id="48a8b-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="48a8b-149">Щелкните XLST и его страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="48a8b-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="48a8b-150">Настройте ввод на расположение файла банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="48a8b-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="48a8b-151">Укажите расположение и имя файла для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="48a8b-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="48a8b-152">Настройте требуемые точки останова.</span><span class="sxs-lookup"><span data-stu-id="48a8b-152">Set the required break points.</span></span>
8.  <span data-ttu-id="48a8b-153">В меню щелкните **XML** &gt; **Запустить отладку XSLT**.</span><span class="sxs-lookup"><span data-stu-id="48a8b-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="48a8b-154">Форматирование выходного файла XSLT</span><span class="sxs-lookup"><span data-stu-id="48a8b-154">Format the XSLT output</span></span>

<span data-ttu-id="48a8b-155">При выполнении преобразования создается выходной файл, который можно просмотреть в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="48a8b-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="48a8b-156">Нажмите сочетание клавиш CTRL+A, CTRL+K и CTRL+D, чтобы быстро отформатировать выходной файл.</span><span class="sxs-lookup"><span data-stu-id="48a8b-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="48a8b-157">Корректировка преобразования</span><span class="sxs-lookup"><span data-stu-id="48a8b-157">Adjust the transformation</span></span>

<span data-ttu-id="48a8b-158">Скорректируйте преобразование, чтобы получить соответствующее поле или элемент в файле банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="48a8b-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="48a8b-159">Затем сопоставьте это поле или элемент с соответствующим элементом Finance.</span><span class="sxs-lookup"><span data-stu-id="48a8b-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="48a8b-160">Индикатор дебета/кредита</span><span class="sxs-lookup"><span data-stu-id="48a8b-160">Debit/credit indicator</span></span>

<span data-ttu-id="48a8b-161">Иногда дебеты могут быть импортированы как кредиты, а кредиты — как дебеты.</span><span class="sxs-lookup"><span data-stu-id="48a8b-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="48a8b-162">Чтобы устранить эту проблему, необходимо изменить соответствующее преобразование XSLT.</span><span class="sxs-lookup"><span data-stu-id="48a8b-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="48a8b-163">Если банковские выписки поступают из нескольких банков, убедитесь, что все они используют один подход дебета/кредита, или создайте отдельные преобразования.</span><span class="sxs-lookup"><span data-stu-id="48a8b-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="48a8b-164">Шаблон BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="48a8b-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="48a8b-165">Шаблон ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="48a8b-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="48a8b-166">Шаблон MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="48a8b-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="48a8b-167">Примеры форматов банковской выписки и технических макетов</span><span class="sxs-lookup"><span data-stu-id="48a8b-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="48a8b-168">В следующей таблице приведены примеры определений технических макетов для расширенных файлов импорта банковской выписки и трех связанных примеров файлов банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="48a8b-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="48a8b-169">Можно загрузить файлы примеров и технические макеты здесь: [Примеры импорта файлов](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="48a8b-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="48a8b-170">Определение технического макета</span><span class="sxs-lookup"><span data-stu-id="48a8b-170">Technical layout definition</span></span>                             | <span data-ttu-id="48a8b-171">Пример файла банковской выписки</span><span class="sxs-lookup"><span data-stu-id="48a8b-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="48a8b-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="48a8b-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="48a8b-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="48a8b-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="48a8b-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="48a8b-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="48a8b-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="48a8b-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="48a8b-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="48a8b-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="48a8b-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="48a8b-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
