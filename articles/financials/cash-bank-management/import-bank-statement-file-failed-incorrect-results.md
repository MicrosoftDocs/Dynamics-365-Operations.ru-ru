---
title: "Устранение неполадок импорта файла банковской выписки"
description: "Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 for Finance and Operations. Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом. Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты. Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки. В этой статье описывается, как исправить эти различия и устранить проблемы."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a5f53a76ebd0bd428f791ce8493e9f388eb8e2fa
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="1f072-107">Устранение неполадок импорта файла банковской выписки</span><span class="sxs-lookup"><span data-stu-id="1f072-107">Bank statement file import troubleshooting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1f072-108">Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f072-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="1f072-109">Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="1f072-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="1f072-110">Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты.</span><span class="sxs-lookup"><span data-stu-id="1f072-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="1f072-111">Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="1f072-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="1f072-112">В этой статье описывается, как исправить эти различия и устранить проблемы.</span><span class="sxs-lookup"><span data-stu-id="1f072-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="1f072-113">В чем заключается ошибка?</span><span class="sxs-lookup"><span data-stu-id="1f072-113">What is the error?</span></span>
------------------

<span data-ttu-id="1f072-114">После попытки импорта файла банковской выписки перейдите в журнал заданий управления данными и просмотрите сведениям о выполнении, чтобы найти ошибку.</span><span class="sxs-lookup"><span data-stu-id="1f072-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="1f072-115">Сведения об ошибке могут отобразиться, если навести указатель мыши на выписку, сальдо или строку выписки.</span><span class="sxs-lookup"><span data-stu-id="1f072-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="1f072-116">Однако, скорее всего, сведений будет недостаточно для определения поля или элемента, который является причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="1f072-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="1f072-117">В чем различия?</span><span class="sxs-lookup"><span data-stu-id="1f072-117">What are the differences?</span></span>
<span data-ttu-id="1f072-118">Сравните определение формата файла банка с определением импорта Finance and Operations и обратите внимание на все различия в полях и элементах.</span><span class="sxs-lookup"><span data-stu-id="1f072-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="1f072-119">Сравните файл банковской выписки с соответствующим примером файла Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f072-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="1f072-120">В файлах ISO20022 все различия должны быть хорошо видны.</span><span class="sxs-lookup"><span data-stu-id="1f072-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="1f072-121">Преобразования</span><span class="sxs-lookup"><span data-stu-id="1f072-121">Transformations</span></span>
<span data-ttu-id="1f072-122">Обычно изменение необходимо внести в одно из трех преобразований.</span><span class="sxs-lookup"><span data-stu-id="1f072-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="1f072-123">Каждое преобразование предназначено для определенного стандарта.</span><span class="sxs-lookup"><span data-stu-id="1f072-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="1f072-124">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="1f072-124">Resource name</span></span>                                         | <span data-ttu-id="1f072-125">Имя файла</span><span class="sxs-lookup"><span data-stu-id="1f072-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="1f072-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="1f072-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="1f072-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="1f072-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="1f072-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="1f072-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="1f072-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="1f072-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="1f072-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="1f072-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="1f072-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="1f072-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="1f072-132">Отладка преобразований</span><span class="sxs-lookup"><span data-stu-id="1f072-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="1f072-133">Корректировка файлов BAI2 и MT940</span><span class="sxs-lookup"><span data-stu-id="1f072-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="1f072-134">Файлы BAI2 и MT940 — это основанные на тексте файлы, которые требуют корректировки для включения отладки XSLT-преобразований документов (XSLT).</span><span class="sxs-lookup"><span data-stu-id="1f072-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="1f072-135">Программа выполняет эту корректировку при импорте файла.</span><span class="sxs-lookup"><span data-stu-id="1f072-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="1f072-136">Создайте XML-файла и скопируйте в него следующий текст.</span><span class="sxs-lookup"><span data-stu-id="1f072-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="1f072-137">Скопируйте содержимое файла банковской выписки и вставьте его в XML-файл, чтобы оно заменило часть **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="1f072-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="1f072-138">Отладка XSLT</span><span class="sxs-lookup"><span data-stu-id="1f072-138">Debug the XSLT</span></span>

<span data-ttu-id="1f072-139">Дополнительные сведения см. в разделе <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="1f072-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="1f072-140">Запустите Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1f072-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="1f072-141">Создайте приложение консоли.</span><span class="sxs-lookup"><span data-stu-id="1f072-141">Create a console application.</span></span>
3.  <span data-ttu-id="1f072-142">Откройте соответствующее преобразование XSLT.</span><span class="sxs-lookup"><span data-stu-id="1f072-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="1f072-143">Щелкните XLST и его страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="1f072-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="1f072-144">Настройте ввод на расположение файла банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="1f072-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="1f072-145">Укажите расположение и имя файла для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="1f072-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="1f072-146">Настройте требуемые точки останова.</span><span class="sxs-lookup"><span data-stu-id="1f072-146">Set the required break points.</span></span>
8.  <span data-ttu-id="1f072-147">В меню щелкните **XML** &gt; **Запустить отладку XSLT**.</span><span class="sxs-lookup"><span data-stu-id="1f072-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="1f072-148">Форматирование выходного файла XSLT</span><span class="sxs-lookup"><span data-stu-id="1f072-148">Format the XSLT output</span></span>

<span data-ttu-id="1f072-149">При выполнении преобразования создается выходной файл, который можно просмотреть в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1f072-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="1f072-150">Нажмите сочетание клавиш CTRL+A, CTRL+K и CTRL+D, чтобы быстро отформатировать выходной файл.</span><span class="sxs-lookup"><span data-stu-id="1f072-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="1f072-151">Корректировка преобразования</span><span class="sxs-lookup"><span data-stu-id="1f072-151">Adjust the transformation</span></span>

<span data-ttu-id="1f072-152">Скорректируйте преобразование, чтобы получить соответствующее поле или элемент в файле банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="1f072-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="1f072-153">Затем сопоставьте это поле или элемент с соответствующим элементом Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1f072-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="1f072-154">Индикатор дебета/кредита</span><span class="sxs-lookup"><span data-stu-id="1f072-154">Debit/credit indicator</span></span>

<span data-ttu-id="1f072-155">Иногда дебеты могут быть импортированы как кредиты, а кредиты — как дебеты.</span><span class="sxs-lookup"><span data-stu-id="1f072-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="1f072-156">Чтобы устранить эту проблему, необходимо изменить соответствующее преобразование XSLT.</span><span class="sxs-lookup"><span data-stu-id="1f072-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="1f072-157">Если банковские выписки поступают из нескольких банков, убедитесь, что все они используют один подход дебета/кредита, или создайте отдельные преобразования.</span><span class="sxs-lookup"><span data-stu-id="1f072-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="1f072-158">Шаблон BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="1f072-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="1f072-159">Шаблон ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="1f072-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="1f072-160">Шаблон MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="1f072-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="1f072-161">Примеры форматов банковской выписки и технических макетов</span><span class="sxs-lookup"><span data-stu-id="1f072-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="1f072-162">В следующей таблице приведены примеры определений технических макетов для расширенных файлов импорта банковской выписки и трех связанных примеров файлов банковской выписки.</span><span class="sxs-lookup"><span data-stu-id="1f072-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="1f072-163">Можно загрузить файлы примеров и технические макеты здесь: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="1f072-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="1f072-164">Определение технического макета</span><span class="sxs-lookup"><span data-stu-id="1f072-164">Technical layout definition</span></span>                             | <span data-ttu-id="1f072-165">Пример файла банковской выписки</span><span class="sxs-lookup"><span data-stu-id="1f072-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="1f072-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="1f072-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="1f072-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="1f072-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="1f072-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="1f072-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="1f072-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="1f072-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="1f072-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="1f072-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="1f072-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="1f072-171">BAI2StatementExample</span></span>                 |






