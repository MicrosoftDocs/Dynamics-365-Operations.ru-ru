---
title: "Устранение неполадок импорта файла банковской выписки"
description: "Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 for Operations. Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом. Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты. Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки. В этой статье описывается, как исправить эти различия и устранить проблемы."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: 9717cf2f36033efe8465906324966242977c6eb2
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Устранение неполадок импорта файла банковской выписки

[!include[banner](../includes/banner.md)]


Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 for Operations. Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом. Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты. Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки. В этой статье описывается, как исправить эти различия и устранить проблемы.

<a name="what-is-the-error"></a>В чем заключается ошибка?
------------------

После попытки импорта файла банковской выписки перейдите в журнал заданий управления данными и просмотрите сведениям о выполнении, чтобы найти ошибку. Сведения об ошибке могут отобразиться, если навести указатель мыши на выписку, сальдо или строку выписки. Однако, скорее всего, сведений будет недостаточно для определения поля или элемента, который является причиной проблемы.

## <a name="what-are-the-differences"></a>В чем различия?
Сравните определение формата файла банка с определением импорта Microsoft Dynamics 365 for Operations и обратите внимание на все различия в полях и элементах. Сравните файл банковской выписки с соответствующим примером файла Dynamics 365 for Operations. В файлах ISO20022 все различия должны быть хорошо видны.

## <a name="transformations"></a>Преобразования
Обычно изменение необходимо внести в одно из трех преобразований. Каждое преобразование предназначено для определенного стандарта.

| Имя ресурса                                         | Имя файла                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Отладка преобразований
### <a name="adjust-the-bai2-and-mt940-files"></a>Корректировка файлов BAI2 и MT940

Файлы BAI2 и MT940 — это основанные на тексте файлы, которые требуют корректировки для включения отладки XSLT-преобразований документов (XSLT). Программа выполняет эту корректировку при импорте файла.

1.  Создайте XML-файла и скопируйте в него следующий текст.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Скопируйте содержимое файла банковской выписки и вставьте его в XML-файл, чтобы оно заменило часть **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Отладка XSLT

Дополнительные сведения см. в разделе <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Запустите Microsoft Visual Studio.
2.  Создайте приложение консоли.
3.  Откройте соответствующее преобразование XSLT.
4.  Щелкните XLST и его страницу свойств.
5.  Настройте ввод на расположение файла банковской выписки.
6.  Укажите расположение и имя файла для выходного файла.
7.  Настройте требуемые точки останова.
8.  В меню щелкните **XML** &gt; **Запустить отладку XSLT**.

### <a name="format-the-xslt-output"></a>Форматирование выходного файла XSLT

При выполнении преобразования создается выходной файл, который можно просмотреть в Visual Studio. Нажмите сочетание клавиш CTRL+A, CTRL+K и CTRL+D, чтобы быстро отформатировать выходной файл.

### <a name="adjust-the-transformation"></a>Корректировка преобразования

Скорректируйте преобразование, чтобы получить соответствующее поле или элемент в файле банковской выписки. Затем сопоставьте это поле или элемент с соответствующим элементом Dynamics 365 for Operations.

### <a name="debitcredit-indicator"></a>Индикатор дебета/кредита

Иногда дебеты могут быть импортированы как кредиты, а кредиты — как дебеты. Чтобы устранить эту проблему, необходимо изменить соответствующее преобразование XSLT. Если банковские выписки поступают из нескольких банков, убедитесь, что все они используют один подход дебета/кредита, или создайте отдельные преобразования.

-   Шаблон BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   Шаблон ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   Шаблон MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Примеры форматов банковской выписки и технических макетов
В следующей таблице приведены примеры определений технических макетов для расширенных файлов импорта банковской выписки и трех связанных примеров файлов банковской выписки. Файлы примеров и технические макеты можно загрузить здесь: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Определение технического макета                             | Пример файла банковской выписки          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





