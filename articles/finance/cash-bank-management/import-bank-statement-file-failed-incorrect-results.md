---
title: Устранение неполадок импорта файла банковской выписки
description: В этой статье объясняется, как исправить проблемы, которые возникают из-за небольших различий в файле банковской выписки.
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151771"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Устранение неполадок импорта файла банковской выписки

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Эта функция станет устаревшей в сентябре 2022 года, новые пользователи должны использовать электронную отчетность.

Важно, чтобы файл банковской выписки из банка соответствовал макету, поддерживаемому в Microsoft Dynamics 365 Finance. Из-за строгих стандартов для банковских выписок большинство интеграций будут работать надлежащим образом. Однако иногда файл выписки невозможно импортировать или он выдает неверные результаты. Обычно эти проблемы возникают из-за небольших различий в файле банковской выписки. В этой статье описывается, как исправить эти различия и устранить проблемы.

## <a name="what-is-the-error"></a>В чем заключается ошибка?

После попытки импорта файла банковской выписки перейдите в журнал заданий управления данными и просмотрите сведениям о выполнении, чтобы найти ошибку. Сведения об ошибке могут отобразиться, если навести указатель мыши на выписку, сальдо или строку выписки. Однако, скорее всего, сведений будет недостаточно для определения поля или элемента, который является причиной проблемы.

> [!NOTE]
> Импортированные банковские выписки могут перекрываться только для одного момента времени.  Например, если выписка заканчивается в 00:00 1-го января 2021 года, то начальная дата следующей выписки может быть 00:00 1-го января 2021 года, 00:00:00.

## <a name="what-are-the-differences"></a>В чем различия?
Сравните определение формата файла банка с определением импорта Finance и обратите внимание на все различия в полях и элементах. Сравните файл банковской выписки с соответствующим примером файла Finance. В файлах ISO20022 все различия должны быть хорошо видны.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Различия часового пояса в импортированных банковских выписках
Значения даты и времени в файле импорта могут отличаться от значений даты и времени, которые отображаются в приложениях для управления финансами и операциями. Чтобы не допустить такого несоответствия, введите предпочтительный часовой пояс на странице **Настройка источников данных**. Дополнительную информацию о вводе предпочтительного часового пояса см. в разделе [Настройка расширенного процесса импорта банковской выверки](set-up-advanced-bank-reconciliation-import-process.md).

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

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Скопируйте содержимое файла банковской выписки и вставьте его в XML-файл, чтобы оно заменило часть **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Отладка XSLT

Дополнительные сведения см. в разделе <https://msdn.microsoft.com/library/ms255605.aspx>.

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

Скорректируйте преобразование, чтобы получить соответствующее поле или элемент в файле банковской выписки. Затем сопоставьте это поле или элемент с соответствующим элементом Finance.

### <a name="debitcredit-indicator"></a>Индикатор дебета/кредита

Иногда дебеты могут быть импортированы как кредиты, а кредиты — как дебеты. Чтобы устранить эту проблему, необходимо изменить соответствующее преобразование XSLT. Если банковские выписки поступают из нескольких банков, убедитесь, что все они используют один подход дебета/кредита, или создайте отдельные преобразования.

-   Шаблон BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   Шаблон ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   Шаблон MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Примеры форматов банковской выписки и технических макетов
В следующей таблице приведены примеры определений технических макетов для расширенных файлов импорта банковской выписки и трех связанных примеров файлов банковской выписки. Можно загрузить файлы примеров и технические макеты здесь: [Примеры импорта файлов](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Определение технического макета                             | Пример файла банковской выписки          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

