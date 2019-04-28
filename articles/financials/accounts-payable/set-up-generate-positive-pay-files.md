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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a5579eae5117a7a3ca517bbcc235c2ed2d925d7f
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2019
ms.locfileid: "896726"
---
# <a name="set-up-and-generate-positive-pay-files"></a>Настройка и создание файлов положительных платежей

[!include [banner](../includes/banner.md)]

В этой теме описывается, как настроить положительный платеж и создавать файлы положительных платежей. 

Настройте положительные платежи для формирования электронного списка чеков, предоставляемых банку. Затем, когда чек передается в банк, банк сравнивает чек со списком чеков. Если чек соответствует чеку в списке, банк производит клиринг чека. Если чек не соответствует чеку в списке, банк отправляет чек на рассмотрение.

## <a name="security-for-positive-pay-files"></a>Безопасность для файлов положительных платежей
Файлы положительных платежей могут содержать конфиденциальные сведения о получателях и суммах чеков. Поэтому убедитесь, что вы используете соответствующие меры безопасности со времени создания файлов и до получения файлов банком. Файлы положительных платежей загружаются в местоположение, указанное вашим веб-браузером. Так как файлы положительных платежей могут содержать конфиденциальные сведения, важно, чтобы только уполномоченные пользователи имели доступ для создания и просмотра этих сведений в Microsoft Dynamics 365 for Finance and Operations. Используйте приведенную ниже таблицу, которая поможет определить требуемые привилегии.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Задача</th>
<th>Привилегия</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Создание файлов положительных платежей со страницы списка <strong>Банковские счета</strong> или со страницы <strong>Банковские счета</strong>.</td>
<td><ul>
<li><strong>Ведение сведений о положительных платежах банка</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Создание файлов положительных платежей для нескольких юридических лиц и банковских счетов со страницы <strong>Создать файл положительных платежей</strong>.</td>
<td><ul>
<li><strong>Ведение сведений о положительных платежах банка</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Просмотр файлов положительных платежей на странице <strong>Сводка по файлу положительных платежей</strong>.</td>
<td><strong>Просмотр сведений о положительных платежах для многих юридических лиц</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Проверка банковского файла положительных платежей на странице <strong>Сводка по файлу положительных платежей</strong>.</td>
<td><strong>Подтвердить файл положительных платежей</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Отзыв банковского файла положительных платежей на странице <strong>Сводка по файлу положительных платежей</strong>.</td>
<td><strong>Отозвать файл положительных платежей</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Настройка формата положительного платежа
Файлы положительных платежей создаются с помощью записей данных. Чтобы можно было создать файл положительных платежей, необходимо настроить входной формат преобразования, который будет использоваться для преобразования данных чека в формат, который можно передавать банку. На странице **Формат положительного платежа** можно создать код и описание формата файла. Входной формат преобразования должен иметь тип XML. Конкретный формат зависит от используемого файла преобразования. Например, в представленном образце XSLT-файла используется формат **XML-элемент**. Используйте действие **Отправка файла для преобразования**, чтобы указать местоположение файла преобразования для формата, который требуется для вашего банка.

## <a name="example-xslt-file-for-positive-pay-file"></a>Пример: XSLT-файл для файла положительных платежей
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Назначение формата положительных платежей банковскому счету
Для каждого банковского счета, для которого требуется создать информацию положительных платежей, необходимо назначить формат положительных платежей, заданный в предыдущем разделе. На странице **Банковские счета** выберите формат положительных платежей, соответствующий банковскому счету. В поле **Дата начала положительных платежей** введите первую дату создания файлов положительных платежей. Важно ввести дату в этой поле. В противном случае первый созданный файл положительных платежей будет включать все чеки, когда-либо созданные для данного банковского счета.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Назначение номерной серии для файлов положительных платежей
Каждый файл положительных платежей должен иметь уникальный номер. Используйте вкладку **Номерные серии** на странице **Параметры управления банком и кассовыми операциями** для создания номерной серии для файлов положительных платежей.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Создание файла положительных платежей для одного банковского счета
Можно создать файл положительных платежей для одного юридического лица и одного банковского счета. Сведения о порядке создания файлов положительных платежей для нескольких юридических лиц и банковских счетов одновременно см. в следующем разделе. Чтобы создать файла положительных платежей для одного юридического лица и одного банковского счета, откройте диалоговое окно **Создать файл положительных платежей** со страницы **Банковские счета**. В поле **Дата прекращения** введите последнюю дату чека для включения в файл положительных платежей. Все чеки, которые не были включены в файл положительных платежей на конец этой даты чека, включаются в файл.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Создание файла положительных платежей для нескольких банковских счетов
Чтобы создать файл положительных платежей для нескольких банковских счетов, используйте периодическую задачу **Создать файл положительных платежей**. Выберите формат положительных платежей для файла и укажите, нужно ли создавать файл для всех юридических лиц или для выбранного юридического лица. Можно также создать файл положительных платежей для всех банковских счетов, которые используют указанных формат положительных платежей, или для выбранного банковского счета. В поле **Дата прекращения** введите последнюю дату чека для включения в файл положительных платежей. Все чеки, которые не были включены в файл положительных платежей на конец этой даты чека, включаются в файл.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Просмотр результатов создания файла положительных платежей
После того как файл положительных платежей создан, можно просматривать результаты на странице **Сводка по файлу положительных платежей**. Для просмотра сведений об отдельных чеках используйте страницу сведений **Файл положительных платежей**.

## <a name="confirm-a-positive-pay-file"></a>Подтверждение файла положительных платежей
После оплаты чеков, перечисленных в файле положительных платежей, вы получаете номер подтверждения из банка. Затем можно подтвердить файл положительных платежей. На странице **Сводка по файлу положительных платежей** выберите файл положительных платежей со статусом **Создан**, затем выберите действие **Ввести подтверждение**. При подтверждении файла положительных платежей записывается номер подтверждения, полученный от банка.

## <a name="recall-a-positive-pay-file"></a>Отзыв файла положительных платежей
Если необходимо изменить файл положительных платежей, можно отозвать его. На странице **Сводка по файлу положительных платежей** выберите файл положительных платежей со статусом **Создан**, затем выберите действие **Отозвать**. Для каждого чека в файле положительных платежей сбрасывается поле, которое указывает, что чек включен в файл положительных платежей. Затем можно создать новый файл положительных платежей, который включает чек, который был отозван.



