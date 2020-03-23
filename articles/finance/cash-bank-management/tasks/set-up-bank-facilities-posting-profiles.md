---
title: Настройка банковских услуг и профилей разноски для гарантийного письма
description: Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 427159048ffbb17749e813d67a900622900a7f21
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179609"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Настройка банковских услуг и профилей разноски для гарантийного письма

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма.



В этой задаче используется демонстрационная компания USMF. 




## <a name="general-ledger-parameter"></a>Параметр главной книги
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".
2. Разверните раздел "Банковский документ".
3. Выберите параметр "Разрешить гарантийные письма".
4. В поле "Журнал проводок" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. Поиск и выбор требуемой записи в списке.
6. В списке перейдите по ссылке в выбранной строке.
7. Откройте вкладку Номерные серии.
    * Определение кода номерной серии для номеров гарантийного письма и ссылок на проводки гарантийного письма  
8. Нажмите кнопку "Сохранить".
9. Закройте страницу.

## <a name="create-bank-facility"></a>Создание банковской услуги
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Банковские ссуды".
2. Щелкните "Создать".
3. В поле "Группа ссуды" введите имя группы банковских услуг для проводки гарантийного письма.
4. В поле "Описание" введите значение.
5. Нажмите кнопку "Сохранить".
6. Перейдите на вкладку "Типы ссуд".
7. Щелкните "Создать".
8. В поле "Тип ссуды" введите имя типа банковской услуги, которая связана с договором о банковских услугах.
9. В поле "Описание" введите значение.
10. В поле "Группа ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
11. Поиск и выбор требуемой записи в списке.
12. В списке перейдите по ссылке в выбранной строке.
13. В поле "Характер ссуды" выберите один из вариантов.
14. Нажмите кнопку "Сохранить".
15. Закройте страницу.

## <a name="bank-posting-profile"></a>Профиль разноски банка
1. Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профиль разноски банковских документов".
2. Щелкните "Создать".
3. В поле "Номер счета/группы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. Поиск и выбор требуемой записи в списке.
5. В списке перейдите по ссылке в выбранной строке.
6. В поле "Закрытие счета" выберите счет ГК для сопоставления.
7. В поле "Счет расходов" выберите счет для расходных проводок.
8. В поле "Счет маржи" выберите счет для проводки маржи.
9. В поле "Счет ликвидации" выберите счет ликвидации для проводки гарантийного письма. 
10. Нажмите кнопку Сохранить.
11. Закройте страницу.
