--- 
title: "Проводка, связанная с гарантийным письмом"
description: "Эта процедура содержит указания по обработке гарантийного письма."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5835469cff8295bc6486c097eaf26114fa547c00
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="letter-of-guarantee-transaction"></a>Проводка, связанная с гарантийным письмом

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура содержит указания по обработке гарантийного письма.



Прежде чем выполнять эту процедуру, необходимо выполнить следующие задачи.

- Настроить банковские услуги и профили разноски для гарантийного письма.

- Создать соглашение о банковских услугах для гарантийного письма.



В данной процедуре используется демонстрационная компания USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Создание заказа на продажу с гарантийным письмом
1. Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".
2. Щелкните "Создать".
3. В поле "Счет клиента" введите или выберите значение.
4. Разверните раздел "Общие".
5. В поле "Сайт" введите или выберите значение.
6. В списке перейдите по ссылке в выбранной строке.
7. В поле "Склад" введите или выберите значение.
8. В списке перейдите по ссылке в выбранной строке.
9. В поле "Тип банковского документа" выберите "Гарантийное письмо".
10. Нажмите кнопку OK.
11. В поле "Код номенклатуры" введите или выберите значение.
12. В поле "Цена за единицу" введите число.
13. Разверните раздел "Сведения о строке".
14. Перейдите на вкладку "Поставка".
    * Примечание. Выберите "Контроль даты поставки = Нет"  
15. В поле "Запрошенная дата отгрузки" введите дату.
16. В поле "Подтвержденная дата отгрузки" введите дату.

## <a name="process-letter-of-guaranteerequest"></a>Обработка запроса гарантийного письма
1. В области действий щелкните "Управлять".
2. Щелкните "Гарантийное письмо".
3. В области действий щелкните "Гарантийное письмо".
4. Щелкните "Запрос", чтобы открыть раскрывающуюся форму диалогового окна.
5. В поле "Тип" введите или выберите значение.
6. В списке перейдите по ссылке в выбранной строке.
7. В поле "Значение" введите число.
8. В поле "Дата окончания срока действия" введите дату и время.
9. Нажмите кнопку "OК".
10. Закройте страницу.

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>Обработка отправки гарантийного письмо в банк
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".
2. В списке найдите и выберите требуемую запись.
3. Щелкните "Отправить в банк", чтобы открыть раскрывающееся диалоговое окно.
4. В поле "Банковский счет" введите или выберите значение.
5. В списке перейдите по ссылке в выбранной строке.
6. Нажмите кнопку "OК".

## <a name="process-letter-of-guaranteereceive-from-bank"></a>Обработка получения гарантийного письма от банка
1. Щелкните "Получить от банка", чтобы открыть раскрывающееся диалоговое окно.
2. В поле "Код банка" введите значение.
    * Проверьте значения в рассчитываемых полях "Маржа" и "Расход".  
3. Нажмите кнопку "OК".
4. Разверните раздел "Действия".
    * Подтвердите запись "Получить от банка".  
5. Щелкните для перехода по ссылке в поле "Номер партии журнала".
6. Щелкните "Строки".
    * Проверьте разноску записей журнала.  
7. Закройте страницу.

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>Обработка передачи гарантийное письмо бенефициару
1. Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".
2. В списке перейдите по ссылке в выбранной строке.
3. В области действий щелкните "Управлять".
4. Щелкните "Гарантийное письмо".
5. В области действий щелкните "Гарантийное письмо".
6. Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.
7. Нажмите кнопку "OК".
8. Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".
9. В списке найдите и выберите требуемую запись.
10. Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.
11. Нажмите кнопку "OК".
12. Разверните раздел "Действия".
    * Проверка запись "Передать бенефициару".  

## <a name="process-letter-of-guaranteeincrease-value"></a>Обработка увеличения стоимости гарантийного письма
1. Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".
2. В списке перейдите по ссылке в выбранной строке.
3. В области действий щелкните "Управлять".
4. Щелкните "Гарантийное письмо".
5. В области действий щелкните "Гарантийное письмо".
6. Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.
7. В поле "Добавляемая стоимость" введите число.
8. Нажмите кнопку "OК".
9. Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".
10. В списке найдите и выберите требуемую запись.
11. Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.
12. Нажмите кнопку "OК".
13. Разверните раздел "Действия".
    * Проверьте запись "Увеличить значение".  
14. В списке найдите и выберите требуемую запись.
15. Щелкните для перехода по ссылке в поле "Номер партии журнала".
16. Щелкните "Строки".
    * Проверьте разнесенные записи журнала.  

## <a name="process-letter-of-guaranteeliquidate"></a>Обработка ликвидации гарантийного письма
1. Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".
2. В списке перейдите по ссылке в выбранной строке.
3. В области действий щелкните "Управлять".
4. Щелкните "Гарантийное письмо".
5. В области действий щелкните "Гарантийное письмо".
6. Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.
7. Нажмите кнопку "OК".
8. Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".
9. В списке найдите и выберите требуемую запись.
10. Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.
11. Нажмите кнопку "OК".
12. Разверните раздел "Действия".
    * Проверьте запись "Ликвидировать".  
13. В списке найдите и выберите требуемую запись.
14. Щелкните для перехода по ссылке в поле "Номер партии журнала".
15. Щелкните "Строки".
    * Проверьте разнесенные записи журнала.  
16. Закройте страницу.

