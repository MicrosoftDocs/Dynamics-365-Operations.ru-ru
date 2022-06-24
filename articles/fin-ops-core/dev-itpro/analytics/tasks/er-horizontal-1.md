---
title: Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)
description: В этой статье описывается, как настроить формат электронной отчетности (ER) для создания отчетов в виде файлов с листами OPENXML (Excel). (Часть 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 157a486252d9447c2509fe5e05b02cf1684683fd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886743"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)

[!include [banner](../../includes/banner.md)]

Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны. Эти шаги можно выполнить в любой компании.

Для выполнения этих действий необходимо сначала выполнить следующие три проводника по задачам:

"Электронная отчетность — Создание поставщика конфигурации и пометка его как активного"

"Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 1. Модель проектных данных)"

"Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 2. Сопоставление модели)"

Необходимо также загрузить и сохранить локальную копию шаблона с примером отчета, который находится здесь: [Sample Financial Dimensions Web Service Report](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.

## <a name="create-a-new-report-configuration"></a>Создание новой конфигурации отчета

1. Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".
2. В дереве выберите узел `Financial dimensions sample model`.
3. Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.
4. В поле Создать введите `Format based on data model Financial dimensions sample model`.
    * Используйте модель, заранее созданную как источник данных для нового отчета.  
5. В поле "Имя" введите `Sample report with horizontally expandable ranges`.
    * Пример отчета с горизонтально расширяемыми диапазонами  
6. В поле Описание введите `To make Excel output with dynamically adding columns`.
    * Создание выходных данных Excel с динамическим добавлением столбцов  
7. В поле "Определение модели данных" выберите "Запись".
8. Нажмите Создать конфигурацию.

## <a name="design-the-report-format"></a>Разработка формата отчета

1. Выберите Конструктор.
2. Включите кнопку-переключатель `Show details`.
3. В области действий щелкните "Импорт".
4. Щелкните "Импорт из Excel".
5. Нажмите кнопку Вложения.
    * Импортируйте шаблон отчета. Используйте файла Excel, загруженный для этого.  
6. Нажмите Создать.
7. Щелкните "Файл".
8. Закройте страницу.
9. В поле "Шаблон" введите или выберите значение.
    * Выберите загруженный шаблон.  
10. Нажмите кнопку "OК".
    * Добавьте новый диапазон для динамического создания выходных данных Excel с тем количеством столбцов, которое вы выбрали (в форме пользовательского диалогового окна) для финансовых аналитик. Каждая ячейка для каждого столбца представляет имя одной финансовой аналитики.  
11. Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.
12. В дереве выберите узел `Excel\Range`.
13. В поле "Диапазон Excel" введите `DimNames`.
    * DimNames  
14. В поле "Направление репликации" выберите `Horizontal`.
15. Нажмите кнопку "OК".
16. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. Щелкните "Переместить вверх".
18. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. Щелкните "Вырезать".
20. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. Щелкните "Вставить".
22. В дереве разверните узел `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. В дереве разверните узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. В дереве разверните узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * Добавьте новый диапазон для динамического создания выходных данных Excel с тем количеством столбцов, которое вы выбрали (в форме пользовательского диалогового окна) для финансовых аналитик. Каждая ячейка для каждого столбца представляет значение одной финансовой аналитики для каждой проводки в отчете.  
26. Щелкните "Добавить диапазон".
27. В поле "Диапазон Excel" введите `DimValues`.
    * DimValues  
28. В поле "Направление репликации" выберите `Horizontal`.
29. Нажмите кнопку "OК".
30. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. Щелкните "Вырезать".
32. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. Щелкните "Вставить".
34. В дереве разверните узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>Сопоставление элементов формата с источниками данных

1. Перейдите на вкладку "Сопоставление".
2. В дереве разверните узел `model: Data model Financial dimensions sample model`.
3. В дереве разверните узел `model: Data model Financial dimensions sample model\Journal: Record list`.
4. В дереве разверните узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. В дереве разверните узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. Щелкните "Связать".
9. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. Щелкните "Связать".
12. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. Щелкните "Связать".
15. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. Щелкните "Связать".
18. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. Щелкните "Связать".
21. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. Щелкните "Связать".
24. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. Щелкните "Связать".
27. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. Щелкните "Связать".
30. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. Щелкните "Связать".
33. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. Щелкните "Связать".
36. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. В дереве выберите узел `model: Data model Financial dimensions sample model\Journal: Record list`.
38. Щелкните "Связать".
39. В дереве разверните узел `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. В дереве выберите узел `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. Щелкните "Связать".
43. В дереве выберите узел `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. Щелкните "Связать".
46. В дереве выберите узел `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. В дереве выберите узел `model: Data model Financial dimensions sample model\Company: String`.
48. Щелкните "Связать".
49. Нажмите кнопку Сохранить.
50. Закройте страницу.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
