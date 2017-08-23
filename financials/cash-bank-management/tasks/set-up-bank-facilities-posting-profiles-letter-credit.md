--- 
title: "Настройка банковских услуг и профилей разноски для аккредитива"
description: "Эта процедура иллюстрирует создание банковской услуги и профиля разноски, необходимых для обработки аккредитивов."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 4cf5d982fa58df93529f3506beef46f660265530
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Настройка банковских услуг и профилей разноски для аккредитива

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура иллюстрирует создание банковской услуги и профиля разноски, необходимых для обработки аккредитивов. 

В этих задачах используется демонстрационная компания USMF.






## <a name="general-ledger-parameter"></a>Параметр главной книги
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".
2. Разверните раздел "Банковский документ".
3. Выберите параметр "Включить импортный аккредитив".
4. Выберите параметр "Включить экспортный аккредитив".
5. Нажмите кнопку "Сохранить".
6. Закройте страницу.

## <a name="create-bank-facility"></a>Создание банковской услуги
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Банковские ссуды".
2. Щелкните "Создать".
3. В поле "Группа ссуды" введите имя группы банковских услуг.
4. В поле "Описание" введите описание группы банковских услуг.
5. Нажмите кнопку "Сохранить".
6. Перейдите на вкладку "Типы ссуд".
7. Щелкните "Создать".
8. В поле "Тип ссуды" введите уникальный код.
9. В поле "Описание" введите значение.
10. В поле "Группа ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
11. Поиск и выбор требуемой записи в списке.
12. В списке перейдите по ссылке в выбранной строке.
13. В поле "Характер ссуды" выберите характер банковской услуги.
14. Нажмите кнопку "Сохранить".
15. Закройте страницу.

## <a name="bank-posting-profile"></a>Профиль разноски банка
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профиль разноски банковских документов".
2. Щелкните "Создать".
3. В поле "Номер счета/группы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. Поиск и выбор требуемой записи в списке.
5. В списке перейдите по ссылке в выбранной строке.
6. Выберите главный счет для сопоставления.
    * Этот счет используется при расчете прогноза движения денежных средств.  
7. В поле "Счет расходов" выберите счет для расходных проводок.
8. В поле "Счет маржи" выберите счет для проводок маржи.
    * Этот счет дебетуется при разноске открывающей маржи и кредитуется при разноске платежа.  
9. Нажмите кнопку "Сохранить".

