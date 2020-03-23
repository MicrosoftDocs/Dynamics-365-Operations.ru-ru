---
title: Электронная отчетность — Создание электронных документов для платежей с помощью конфигурации формата
description: В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может использовать новую конфигурацию формата электронной отчетности для создания электронных документов для обработки платежей.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184999"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>Электронная отчетность — Создание электронных документов для платежей с помощью конфигурации формата

[!include [task guide banner](../../includes/task-guide-banner.md)]

В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может использовать новую конфигурацию формата электронной отчетности для создания электронных документов для обработки платежей. Эти шаги можно выполнить в демонстрационной компании GBSI.

Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание конфигурации с форматом платежного документа".


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Изменение конфигурации метода электронного платежа
1. Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".
2. Переключите раздел "Формат файла", чтобы развернуть его, если это необходимо.
3. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Способ оплаты" по значению "Электронно".
4. Щелкните "Изменить".
5. Установите в поле "Общая электронная отчетность" значение "Да".
    * Выберите значение "Да", чтобы использовать шаблон общей электронной отчетности для создания файлов платежей.  
6. В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
7. Выберите конфигурацию формата BACS (Великобритания, вымышленный).
8. Нажмите кнопку "Сохранить".
9. Закройте страницу.

## <a name="test-the-format-of-generated-payment-files"></a>Проверка формата созданных файлов платежей
1. Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".
2. Щелкните "Создать".
3. В списке пометьте выбранную строку.
4. В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. В списке перейдите по ссылке в выбранной строке.
    * Выберите VendPay.  
6. Нажмите кнопку "Сохранить".
7. Щелкните "Строки".
8. В поле "Компания" введите DEMF.
    * DEMF  
9. В поле "Счет" укажите значения "DE-01001".
    * DE - 01001  
10. В поле "Описание" введите "Платеж".
    * Платеж  
11. В поле "Дебет" введите число.
    * В тысячах  
12. Перейдите на вкладку Платеж.
13. В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
14. В списке найдите и выберите требуемую запись.
    * Выберите значение "Электронно".  
15. В списке перейдите по ссылке в выбранной строке.
16. Нажмите кнопку "Сохранить".
17. Щелкните "Создать платежи".
18. В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
19. В списке найдите и выберите требуемую запись.
    * Выберите значение "Электронно".  
20. В списке перейдите по ссылке в выбранной строке.
    * Выберите значение "Электронно".  
21. В поле "Имя файла" введите значение.
    * Например, введите "платежи".  
22. В поле "Банковский счет" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
23. В списке перейдите по ссылке в выбранной строке.
    * Выберите значение GBSI OPER.  
24. Нажмите кнопку "OК".
25. Нажмите кнопку "OК".
    * Проанализируйте созданный файл платежа в формате XML. Сравните его с созданным макетом документа и определенными атрибутами проводки по оплате.  
