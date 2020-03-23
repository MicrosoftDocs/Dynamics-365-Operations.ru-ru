---
title: Импортный аккредитив
description: Эта процедура содержит указания по импорту аккредитива.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72a50b2cdda5d66e8aa4660f914e6f5e51531b5f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188150"
---
# <a name="import-letter-of-credit"></a>Импортный аккредитив

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура содержит указания по импорту аккредитива. Перед выполнением этой процедуры необходимо настроить следующее: банковские кредиты, профили разноски, договора о банковских кредитах и сведения о банковском счете поставщика.

В данной процедуре используется демонстрационная компания USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Создание заказа на покупку с аккредитивом
1. Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".
2. Щелкните "Создать".
3. В поле "Счет поставщика" введите или выберите значение.
4. Поиск и выбор требуемой записи в списке.
5. В списке перейдите по ссылке в выбранной строке.
6. Разверните раздел "Общие".
7. В поле "Сайт" введите или выберите значение.
8. В списке перейдите по ссылке в выбранной строке.
9. В поле "Склад" введите или выберите значение.
10. В списке перейдите по ссылке в выбранной строке.
11. В поле "Дата учета" введите дату.
12. В поле "Дата поставки" введите дату.
    * Примечание. В поле "Тип банковского документа" необходимо выбрать значение "Аккредитив".  
13. Нажмите кнопку "OК".
14. В поле "Код номенклатуры" введите или выберите значение.
15. В списке найдите и выберите требуемую запись.
16. В списке перейдите по ссылке в выбранной строке.
17. Разверните раздел "Сведения о строке".
18. Перейдите на вкладку "Поставка".
19. В поле "Дата поставки" введите дату.
20. В поле "Подтвержденная дата доставки" введите дату.
21. В поле "Цена за единицу" введите число.
    * Определите сведения аккредитива.  
22. В области действий щелкните "Управлять".
23. Щелкните "Аккредитив / импортное инкассо".
24. В поле "Дата заявления" введите дату и время.
    * Убедитесь, что в поле "Банковский счет" имеется активный банковский счет по умолчанию, который основан на дате подачи заявления.  
25. В поле "Номер банковского документа" введите значение.
26. В поле "Дата прихода" введите дату и время.
27. Разверните раздел "Банковский документ".
28. В поле "Дата окончания срока действия" введите дату и время.
29. Разверните раздел "Сведения о банке".
30. В поле "Авизующий банк" введите или выберите значение.
31. В списке перейдите по ссылке в выбранной строке.
32. Нажмите кнопку "Сохранить".
33. Щелкните "Извлечь отгрузки по заказу на покупку".
34. Закройте страницу.
35. В области действий щелкните "Покупка".
36. Нажмите кнопку "Подтвердить".
37. В области действий щелкните "Управлять".
38. Щелкните "Аккредитив / импортное инкассо".
39. Щелкните "Обработать".
40. Нажмите кнопку "Подтвердить".
    * Убедитесь, что сальдо кредита уменьшает сумму покупки.  В этом примере сумма покупки = 500,00, кредитный лимит = 10000,00, поэтому сальдо кредита = 9500,00.  
41. Закройте страницу.
42. В поле "Цена за единицу" введите число.
43. Нажмите кнопку "Сохранить".
44. В области действий щелкните "Покупка".
45. Нажмите кнопку "Подтвердить".
    * Измените аккредитив в соответствии с изменением в цене за единицу.  
46. В области действий щелкните "Управлять".
47. Щелкните "Аккредитив / импортное инкассо".
    * Измените аккредитив в соответствии с изменением в цене единицы покупки.  
48. Щелкните "Обработать".
49. Щелкните "Изменить".
50. Щелкните "Удалить".
51. Щелкните Да.
52. Щелкните "Извлечь отгрузки по заказу на покупку".
53. Щелкните "Обработать".
54. Нажмите кнопку "Подтвердить".
    * Убедитесь, что сальдо кредита уменьшает сумму покупки.  В этом примере измененная сумма покупки = 600,00, кредитный лимит = 10000,00, поэтому сальдо кредита = 9400,00.  
55. Закройте страницу.

## <a name="post-packing-slip"></a>Разноска отборочной накладной
1. В области действий щелкните "Получение".
2. Щелкните "Поступление продуктов".
3. В поле PurchParmTable_Num введите значение.
    * Выберите номер отгрузки, созданной со ссылкой на аккредитив.  
4. В списке перейдите по ссылке в выбранной строке.
5. В поле "Дата поступления продуктов" введите дату.
6. Нажмите кнопку "OК".
7. Закройте страницу.
8. Закройте страницу.

## <a name="verify-import-letter-of-credit-status"></a>Проверка статуса импортного аккредитива
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Импортный аккредитив и импортное инкассо".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
    * Проверьте статус импортного аккредитива.     
4. Закройте страницу.
5. Закройте страницу.

## <a name="post-purchase-invoice"></a>Разноска накладной по покупке
1. Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".
    * Выберите заказ на покупку, который был создан с аккредитивом.  
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
4. В области действий щелкните "Накладная".
5. Щелкните "Накладная".
6. В поле "Число" введите значение.
7. В поле "Номер отгрузки" введите или выберите значение.
8. В списке перейдите по ссылке в выбранной строке.
9. В поле "Дата накладной" введите дату.
10. Щелкните "Обновить статус сопоставления".
11. Щелкните "Разнести".
12. Закройте страницу.
13. Закройте страницу.

## <a name="verify-import-letter-of-credit-status"></a>Проверка статуса импортного аккредитива
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Импортный аккредитив и импортное инкассо".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
    * Проверьте импортный аккредитив 2.  
    * Проверка: Статус отгрузки = сведения об оприходованном банковском кредите  
4. Щелкните "Вид".
5. Щелкните "Печать заявления".
6. Нажмите кнопку "OК".
    * Проверьте, что аккредитив печатается.  
7. Закройте страницу.
8. Закройте страницу.
9. Закройте страницу.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Разноска журнала платежей поставщика для созданной накладной по покупке с аккредитивом
1. Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".
2. Щелкните "Создать".
3. В поле "Имя" введите или выберите значение.
4. В списке перейдите по ссылке в выбранной строке.
5. Выберите Строки.
6. В поле "Дата" введите дату.
7. В поле "Счет" укажите требуемые значения.
8. Щелкните "Сопоставление проводок".
9. Развернуть раздел "Итоговые значения".
10. В поле "Показать" выберите один из вариантов.
    * Убедитесь, что поля "Номер банковского документа" и "Номер отгрузки" были обновлены.  
11. Установите флажок "Пометка".
12. Нажмите кнопку "OК".
13. Перейдите на вкладку Платеж.
    * Убедитесь, что поля "Номер банковского документа" и "Номер отгрузки" были обновлены.  
14. Щелкните "Разнести".
15. Закройте страницу.
16. Закройте страницу.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Проверка статуса импортного аккредитива после оплаты накладной
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Импортный аккредитив и импортное инкассо".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
    * Проверьте статус импортного аккредитива.   
4. Закройте страницу.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Проверка лимита банковского кредита и отчета по использованию
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Запросы и отчеты" > "Аккредитивы или гарантийные письма" > "Отчет о банковских услугах и использовании".
2. Разверните раздел "Записи для добавления".
3. Щелкните "Фильтр".
    * Определите поле "Критерии", указав требуемый банковский счет.  
4. В поле "Критерии" введите или выберите значение.
5. В списке перейдите по ссылке в выбранной строке.
6. Нажмите кнопку "OК".
7. Нажмите кнопку "OК".
    * Проверьте отчет, в котором перечисляются проводки.  
    * Проверьте, что в отчете есть проводки с номером банковского документа, кредитным лимитом, использованной суммой и суммой сальдо кредита.  
8. Закройте страницу.
