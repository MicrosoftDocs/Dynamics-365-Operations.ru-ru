---
title: Настройка и создание файлов положительных платежей
description: В этой теме описывается, как настроить положительный платеж и создавать файлы положительных платежей.
author: abruer
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 600e3279536857dbb804ef420572fad42fe72311
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189530"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="088a0-103">Настройка и создание файлов положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="088a0-104">В этой теме описывается, как настроить положительный платеж и создавать файлы положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="088a0-105">Настройте положительные платежи для формирования электронного списка чеков, предоставляемых банку.</span><span class="sxs-lookup"><span data-stu-id="088a0-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="088a0-106">Затем, когда чек передается в банк, банк сравнивает чек со списком чеков.</span><span class="sxs-lookup"><span data-stu-id="088a0-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="088a0-107">Если чек соответствует чеку в списке, банк производит клиринг чека.</span><span class="sxs-lookup"><span data-stu-id="088a0-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="088a0-108">Если чек не соответствует чеку в списке, банк отправляет чек на рассмотрение.</span><span class="sxs-lookup"><span data-stu-id="088a0-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="088a0-109">Безопасность для файлов положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-109">Security for positive pay files</span></span>
<span data-ttu-id="088a0-110">Файлы положительных платежей могут содержать конфиденциальные сведения о получателях и суммах чеков.</span><span class="sxs-lookup"><span data-stu-id="088a0-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="088a0-111">Поэтому убедитесь, что вы используете соответствующие меры безопасности со времени создания файлов и до получения файлов банком.</span><span class="sxs-lookup"><span data-stu-id="088a0-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="088a0-112">Файлы положительных платежей загружаются в местоположение, указанное вашим веб-браузером.</span><span class="sxs-lookup"><span data-stu-id="088a0-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="088a0-113">Так как файлы положительных платежей могут содержать конфиденциальные сведения, важно, чтобы только уполномоченные пользователи имели доступ для создания и просмотра этих сведений в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="088a0-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="088a0-114">Используйте приведенную ниже таблицу, которая поможет определить требуемые привилегии.</span><span class="sxs-lookup"><span data-stu-id="088a0-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="088a0-115">Задача</span><span class="sxs-lookup"><span data-stu-id="088a0-115">Task</span></span></th>
<th><span data-ttu-id="088a0-116">Привилегия</span><span class="sxs-lookup"><span data-stu-id="088a0-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="088a0-117">Создание файлов положительных платежей со страницы списка <strong>Банковские счета</strong> или со страницы <strong>Банковские счета</strong>.</span><span class="sxs-lookup"><span data-stu-id="088a0-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="088a0-118"><strong>Ведение сведений о положительных платежах банка</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="088a0-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="088a0-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="088a0-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="088a0-120">Создание файлов положительных платежей для нескольких юридических лиц и банковских счетов со страницы <strong>Создать файл положительных платежей</strong>.</span><span class="sxs-lookup"><span data-stu-id="088a0-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="088a0-121"><strong>Ведение сведений о положительных платежах банка</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="088a0-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="088a0-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="088a0-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="088a0-123">Просмотр файлов положительных платежей на странице <strong>Сводка по файлу положительных платежей</strong>.</span><span class="sxs-lookup"><span data-stu-id="088a0-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="088a0-124"><strong>Просмотр сведений о положительных платежах для многих юридических лиц</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="088a0-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="088a0-125">Проверка банковского файла положительных платежей на странице <strong>Сводка по файлу положительных платежей</strong>.</span><span class="sxs-lookup"><span data-stu-id="088a0-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="088a0-126"><strong>Подтвердить файл положительных платежей</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="088a0-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="088a0-127">Отзыв банковского файла положительных платежей на странице <strong>Сводка по файлу положительных платежей</strong>.</span><span class="sxs-lookup"><span data-stu-id="088a0-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="088a0-128"><strong>Отозвать файл положительных платежей</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="088a0-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="088a0-129">Настройка формата положительного платежа</span><span class="sxs-lookup"><span data-stu-id="088a0-129">Set up a positive pay format</span></span>
<span data-ttu-id="088a0-130">Файлы положительных платежей создаются с помощью записей данных.</span><span class="sxs-lookup"><span data-stu-id="088a0-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="088a0-131">Чтобы можно было создать файл положительных платежей, необходимо настроить входной формат преобразования, который будет использоваться для преобразования данных чека в формат, который можно передавать банку.</span><span class="sxs-lookup"><span data-stu-id="088a0-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="088a0-132">На странице **Формат положительного платежа** можно создать код и описание формата файла.</span><span class="sxs-lookup"><span data-stu-id="088a0-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="088a0-133">Входной формат преобразования должен иметь тип XML.</span><span class="sxs-lookup"><span data-stu-id="088a0-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="088a0-134">Конкретный формат зависит от используемого файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="088a0-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="088a0-135">Например, в представленном образце XSLT-файла используется формат **XML-элемент**.</span><span class="sxs-lookup"><span data-stu-id="088a0-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="088a0-136">Используйте действие **Отправка файла для преобразования**, чтобы указать местоположение файла преобразования для формата, который требуется для вашего банка.</span><span class="sxs-lookup"><span data-stu-id="088a0-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="088a0-137">Пример: XSLT-файл для файла положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="088a0-138">Назначение формата положительных платежей банковскому счету</span><span class="sxs-lookup"><span data-stu-id="088a0-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="088a0-139">Для каждого банковского счета, для которого требуется создать информацию положительных платежей, необходимо назначить формат положительных платежей, заданный в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="088a0-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="088a0-140">На странице **Банковские счета** выберите формат положительных платежей, соответствующий банковскому счету.</span><span class="sxs-lookup"><span data-stu-id="088a0-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="088a0-141">В поле **Дата начала положительных платежей** введите первую дату создания файлов положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="088a0-142">Важно ввести дату в этой поле.</span><span class="sxs-lookup"><span data-stu-id="088a0-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="088a0-143">В противном случае первый созданный файл положительных платежей будет включать все чеки, когда-либо созданные для данного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="088a0-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="088a0-144">Назначение номерной серии для файлов положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="088a0-145">Каждый файл положительных платежей должен иметь уникальный номер.</span><span class="sxs-lookup"><span data-stu-id="088a0-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="088a0-146">Используйте вкладку **Номерные серии** на странице **Параметры управления банком и кассовыми операциями** для создания номерной серии для файлов положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="088a0-147">Создание файла положительных платежей для одного банковского счета</span><span class="sxs-lookup"><span data-stu-id="088a0-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="088a0-148">Можно создать файл положительных платежей для одного юридического лица и одного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="088a0-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="088a0-149">Сведения о порядке создания файлов положительных платежей для нескольких юридических лиц и банковских счетов одновременно см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="088a0-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="088a0-150">Чтобы создать файла положительных платежей для одного юридического лица и одного банковского счета, откройте диалоговое окно **Создать файл положительных платежей** со страницы **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="088a0-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="088a0-151">В поле **Дата прекращения** введите последнюю дату чека для включения в файл положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="088a0-152">Все чеки, которые не были включены в файл положительных платежей на конец этой даты чека, включаются в файл.</span><span class="sxs-lookup"><span data-stu-id="088a0-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="088a0-153">Создание файла положительных платежей для нескольких банковских счетов</span><span class="sxs-lookup"><span data-stu-id="088a0-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="088a0-154">Чтобы создать файл положительных платежей для нескольких банковских счетов, используйте периодическую задачу **Создать файл положительных платежей**.</span><span class="sxs-lookup"><span data-stu-id="088a0-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="088a0-155">Выберите формат положительных платежей для файла и укажите, нужно ли создавать файл для всех юридических лиц или для выбранного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="088a0-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="088a0-156">Можно также создать файл положительных платежей для всех банковских счетов, которые используют указанных формат положительных платежей, или для выбранного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="088a0-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="088a0-157">В поле **Дата прекращения** введите последнюю дату чека для включения в файл положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="088a0-158">Все чеки, которые не были включены в файл положительных платежей на конец этой даты чека, включаются в файл.</span><span class="sxs-lookup"><span data-stu-id="088a0-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="088a0-159">Просмотр результатов создания файла положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="088a0-160">После того как файл положительных платежей создан, можно просматривать результаты на странице **Сводка по файлу положительных платежей**.</span><span class="sxs-lookup"><span data-stu-id="088a0-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="088a0-161">Для просмотра сведений об отдельных чеках используйте страницу сведений **Файл положительных платежей**.</span><span class="sxs-lookup"><span data-stu-id="088a0-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="088a0-162">Подтверждение файла положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-162">Confirm a positive pay file</span></span>
<span data-ttu-id="088a0-163">После оплаты чеков, перечисленных в файле положительных платежей, вы получаете номер подтверждения из банка.</span><span class="sxs-lookup"><span data-stu-id="088a0-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="088a0-164">Затем можно подтвердить файл положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="088a0-165">На странице **Сводка по файлу положительных платежей** выберите файл положительных платежей со статусом **Создан**, затем выберите действие **Ввести подтверждение**.</span><span class="sxs-lookup"><span data-stu-id="088a0-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="088a0-166">При подтверждении файла положительных платежей записывается номер подтверждения, полученный от банка.</span><span class="sxs-lookup"><span data-stu-id="088a0-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="088a0-167">Отзыв файла положительных платежей</span><span class="sxs-lookup"><span data-stu-id="088a0-167">Recall a positive pay file</span></span>
<span data-ttu-id="088a0-168">Если необходимо изменить файл положительных платежей, можно отозвать его.</span><span class="sxs-lookup"><span data-stu-id="088a0-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="088a0-169">На странице **Сводка по файлу положительных платежей** выберите файл положительных платежей со статусом **Создан**, затем выберите действие **Отозвать**.</span><span class="sxs-lookup"><span data-stu-id="088a0-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="088a0-170">Для каждого чека в файле положительных платежей сбрасывается поле, которое указывает, что чек включен в файл положительных платежей.</span><span class="sxs-lookup"><span data-stu-id="088a0-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="088a0-171">Затем можно создать новый файл положительных платежей, который включает чек, который был отозван.</span><span class="sxs-lookup"><span data-stu-id="088a0-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



