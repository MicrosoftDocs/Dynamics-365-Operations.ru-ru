---
title: Устранение неполадок импорта файла банковской выписки
description: Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 Finance. Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом. Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты. Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки. В этой статье описывается, как исправить эти различия и устранить проблемы.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 612ded1f68cc8e1b26b8046501bae1707175e23a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188334"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="b12f0-107">Устранение неполадок импорта файла банковской выписки</span><span class="sxs-lookup"><span data-stu-id="b12f0-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b12f0-108">Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b12f0-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="b12f0-109">Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="b12f0-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="b12f0-110">Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты.</span><span class="sxs-lookup"><span data-stu-id="b12f0-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="b12f0-111">Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="b12f0-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="b12f0-112">В этой статье описывается, как исправить эти различия и устранить проблемы.</span><span class="sxs-lookup"><span data-stu-id="b12f0-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="b12f0-113">В чем заключается ошибка?</span><span class="sxs-lookup"><span data-stu-id="b12f0-113">What is the error?</span></span>
------------------

<span data-ttu-id="b12f0-114">После попытки импорта файла банковской выписки перейдите в журнал заданий управления данными и просмотрите сведениям о выполнении, чтобы найти ошибку.</span><span class="sxs-lookup"><span data-stu-id="b12f0-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="b12f0-115">Сведения об ошибке могут отобразиться, если навести указатель мыши на выписку, сальдо или строку выписки.</span><span class="sxs-lookup"><span data-stu-id="b12f0-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="b12f0-116">Однако, скорее всего, сведений будет недостаточно для определения поля или элемента, который является причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="b12f0-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="b12f0-117">В чем различия?</span><span class="sxs-lookup"><span data-stu-id="b12f0-117">What are the differences?</span></span>
<span data-ttu-id="b12f0-118">Сравните определение формата файла банка с определением импорта Finance и обратите внимание на все различия в полях и элементах.</span><span class="sxs-lookup"><span data-stu-id="b12f0-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="b12f0-119">Сравните файл банковской выписки с соответствующим примером файла Finance.</span><span class="sxs-lookup"><span data-stu-id="b12f0-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="b12f0-120">В файлах ISO20022 все различия должны быть хорошо видны.</span><span class="sxs-lookup"><span data-stu-id="b12f0-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="b12f0-121">Различия часового пояса в импортированных банковских выписках</span><span class="sxs-lookup"><span data-stu-id="b12f0-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="b12f0-122">Значения даты и времени в файле импорта могут отличаться от значений даты и времени, которые отображаются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b12f0-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="b12f0-123">Чтобы не допустить такого несоответствия, введите предпочтительный часовой пояс на странице **Настройка источников данных**.</span><span class="sxs-lookup"><span data-stu-id="b12f0-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="b12f0-124">Дополнительную информацию о вводе предпочтительного часового пояса см. в разделе [Настройка расширенного процесса импорта банковской выверки](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="b12f0-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="b12f0-125">Преобразования</span><span class="sxs-lookup"><span data-stu-id="b12f0-125">Transformations</span></span>
<span data-ttu-id="b12f0-126">Обычно изменение необходимо внести в одно из трех преобразований.</span><span class="sxs-lookup"><span data-stu-id="b12f0-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="b12f0-127">Каждое преобразование предназначено для определенного стандарта.</span><span class="sxs-lookup"><span data-stu-id="b12f0-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="b12f0-128">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="b12f0-128">Resource name</span></span>                                         | <span data-ttu-id="b12f0-129">Имя файла</span><span class="sxs-lookup"><span data-stu-id="b12f0-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="b12f0-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="b12f0-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="b12f0-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="b12f0-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="b12f0-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="b12f0-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="b12f0-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="b12f0-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="b12f0-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="b12f0-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="b12f0-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="b12f0-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="b12f0-136">Отладка преобразований</span><span class="sxs-lookup"><span data-stu-id="b12f0-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="b12f0-137">Корректировка файлов BAI2 и MT940</span><span class="sxs-lookup"><span data-stu-id="b12f0-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="b12f0-138">Файлы BAI2 и MT940 — это основанные на тексте файлы, которые требуют корректировки для включения отладки XSLT-преобразований документов (XSLT).</span><span class="sxs-lookup"><span data-stu-id="b12f0-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="b12f0-139">Программа выполняет эту корректировку при импорте файла.</span><span class="sxs-lookup"><span data-stu-id="b12f0-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="b12f0-140">Создайте XML-файла и скопируйте в него следующий текст.</span><span class="sxs-lookup"><span data-stu-id="b12f0-140">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="b12f0-141">Скопируйте содержимое файла банковской выписки и вставьте его в XML-файл, чтобы оно заменило часть **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="b12f0-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="b12f0-142">Отладка XSLT</span><span class="sxs-lookup"><span data-stu-id="b12f0-142">Debug the XSLT</span></span>

<span data-ttu-id="b12f0-143">Дополнительные сведения см. в разделе <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="b12f0-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="b12f0-144">Запустите Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b12f0-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="b12f0-145">Создайте приложение консоли.</span><span class="sxs-lookup"><span data-stu-id="b12f0-145">Create a console application.</span></span>
3.  <span data-ttu-id="b12f0-146">Откройте соответствующее преобразование XSLT.</span><span class="sxs-lookup"><span data-stu-id="b12f0-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="b12f0-147">Щелкните XLST и его страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="b12f0-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="b12f0-148">Настройте ввод на расположение файла банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="b12f0-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="b12f0-149">Укажите расположение и имя файла для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="b12f0-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="b12f0-150">Настройте требуемые точки останова.</span><span class="sxs-lookup"><span data-stu-id="b12f0-150">Set the required break points.</span></span>
8.  <span data-ttu-id="b12f0-151">В меню щелкните **XML** &gt; **Запустить отладку XSLT**.</span><span class="sxs-lookup"><span data-stu-id="b12f0-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="b12f0-152">Форматирование выходного файла XSLT</span><span class="sxs-lookup"><span data-stu-id="b12f0-152">Format the XSLT output</span></span>

<span data-ttu-id="b12f0-153">При выполнении преобразования создается выходной файл, который можно просмотреть в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b12f0-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="b12f0-154">Нажмите сочетание клавиш CTRL+A, CTRL+K и CTRL+D, чтобы быстро отформатировать выходной файл.</span><span class="sxs-lookup"><span data-stu-id="b12f0-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="b12f0-155">Корректировка преобразования</span><span class="sxs-lookup"><span data-stu-id="b12f0-155">Adjust the transformation</span></span>

<span data-ttu-id="b12f0-156">Скорректируйте преобразование, чтобы получить соответствующее поле или элемент в файле банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="b12f0-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="b12f0-157">Затем сопоставьте это поле или элемент с соответствующим элементом Finance.</span><span class="sxs-lookup"><span data-stu-id="b12f0-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="b12f0-158">Индикатор дебета/кредита</span><span class="sxs-lookup"><span data-stu-id="b12f0-158">Debit/credit indicator</span></span>

<span data-ttu-id="b12f0-159">Иногда дебеты могут быть импортированы как кредиты, а кредиты — как дебеты.</span><span class="sxs-lookup"><span data-stu-id="b12f0-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="b12f0-160">Чтобы устранить эту проблему, необходимо изменить соответствующее преобразование XSLT.</span><span class="sxs-lookup"><span data-stu-id="b12f0-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="b12f0-161">Если банковские выписки поступают из нескольких банков, убедитесь, что все они используют один подход дебета/кредита, или создайте отдельные преобразования.</span><span class="sxs-lookup"><span data-stu-id="b12f0-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="b12f0-162">Шаблон BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="b12f0-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="b12f0-163">Шаблон ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="b12f0-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="b12f0-164">Шаблон MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="b12f0-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="b12f0-165">Примеры форматов банковской выписки и технических макетов</span><span class="sxs-lookup"><span data-stu-id="b12f0-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="b12f0-166">В следующей таблице приведены примеры определений технических макетов для расширенных файлов импорта банковской выписки и трех связанных примеров файлов банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="b12f0-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="b12f0-167">Можно загрузить файлы примеров и технические макеты здесь: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="b12f0-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="b12f0-168">Определение технического макета</span><span class="sxs-lookup"><span data-stu-id="b12f0-168">Technical layout definition</span></span>                             | <span data-ttu-id="b12f0-169">Пример файла банковской выписки</span><span class="sxs-lookup"><span data-stu-id="b12f0-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="b12f0-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="b12f0-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="b12f0-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="b12f0-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="b12f0-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="b12f0-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="b12f0-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="b12f0-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="b12f0-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="b12f0-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="b12f0-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="b12f0-175">BAI2StatementExample</span></span>                 |





