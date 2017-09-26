--- 
title: "Распределение анкет с помощью планирования"
description: "Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам."
author: kherr75
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: d11d9b46dc7e13926472e2eca5c23a97d4248377
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="distribute-questionnaires-using-scheduling"></a>Распределение анкет с помощью планирования

[!include[task guide banner](../../includes/task-guide-banner.md)]

Планирование анкет позволяет планировать и распределять анкеты по нескольким респондентам. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-a-questionnaire-schedule"></a>Создание графика анкетирования
1. Перейдите в раздел "Анкета" > "Распределение" > "Графики анкетирования".
2. Щелкните "Создать".
3. В поле "Планирование" введите значение.
4. В поле "Описание" введите значение.
    * Настройте планирование как "анонимное", если ответы должны записываться без имен, связанных с ответом.  
    * Сначала необходимо настроить разрешение анонимных результатов в параметрах управления персоналом.  
5. В поле "Тип" выберите тип планирования.  В этом примере будет использоваться тип "Удовлетворенность".
6. В списке найдите и выберите требуемую запись.
7. В списке перейдите по ссылке в выбранной строке.
8. В поле "Дата" введите дату.
9. Разверните раздел "Электронная почта для портала самообслуживания сотрудников".
10. В поле "Тема" введите значение.
    * Пример. Анкета доступная  
11. В поле "Текст" введите текст сообщения электронной почты. Обратите внимание, что эту переменную можно использовать для подстановки значений в системе.
    * Пример.   Уважаемый %P%! Выполните вход на портал самообслуживания сотрудников для заполнения анкеты "Здоровье трудовых ресурсов".  Contoso  
12. Нажмите кнопку "Сохранить".

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Используйте "Сведения о настройке" для выбора анкеты (анкет) для ответов, а также запросы, используемые для выбора респондентов.
1. Щелкните "Сведения о настройке".
2. В списке выберите запрос для поиска в системе респондентов для анкеты.
    * Пример. Работники  
3. Нажмите "Просмотр или изменение запроса" для выбора конкретных людей или изменения запроса для поиска людей, соответствующих конкретным критериям.
    * Обратите внимание, что все респонденты должны быть пользователями в системе.  
4. В списке пометьте строку для "Респондент".
5. В поле "Критерии" введите или выберите значение.
    * Выберите Julia Funderburk  
6. В списке выберите Julia Funderburk
7. Нажмите кнопку "OК".
8. Перейдите на вкладку "Анкеты".
9. В дереве разверните узел для типа анкеты "Исследование уровня удовлетворенности".
10. В дереве установите флажок "Оценка здоровья трудовых ресурсов".
11. Нажмите кнопку "OК".
12. Щелкните "Запланированный опрос".
    * Обратите внимание, что запланированные опросы были созданы для каждого выбранного/опрошенного пользователя.  
13. Закройте страницу.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Запустите расписание анкеты, чтобы сделать анкету доступной для респондентов.
1. Щелкните Функции.
2. Щелкните "Начать".
3. Нажмите кнопку "OК".

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Отправьте электронное письмо, чтобы проинформировать респондентов о наличии анкеты.
1. Щелкните Функции.
2. Щелкните "Отправить сообщение электронной почты".
3. Щелкните "Отмена".

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Используйте запланированные опросы для отслеживания, кто должен заполнить анкету.
1. Щелкните "Запланированный опрос".
    * Удалите оставшийся запланированный опрос, когда вы готовы завершить запланированный опрос.  
2. Нажмите кнопку Удалить.
3. Щелкните Да.
4. Закройте страницу.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Завершите график, когда все респонденты заполнили анкету и (или) все оставшиеся запланированные опросы были удалены.
1. Щелкните Функции.
2. Щелкните "Готово".
3. Нажмите кнопку "OК".

