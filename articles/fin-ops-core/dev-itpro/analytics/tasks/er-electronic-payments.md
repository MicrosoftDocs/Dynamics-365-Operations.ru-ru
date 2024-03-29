---
title: Электронная отчетность — Создание электронных документов для платежей с помощью конфигурации формата
description: В этой статье описывается, как использовать новую конфигурацию формата электронной отчетности (ER), чтобы создавать электронные документы для обработки платежей.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
ms.openlocfilehash: b70b246e3618e8f083e5f6757ee8a97d8072a635
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290885"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>Электронная отчетность — Создание электронных документов для платежей с помощью конфигурации формата

[!include [banner](../../includes/banner.md)]

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
7. Выберите конфигурацию формата BACS (Соединенное Королевство, вымышленный).
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
