---
title: Распределение и планирование анкет
description: В этой статье объясняется, как распределить составленные анкеты, чтобы они были доступны отдельному пользователю или группе пользователей, которые должны ее заполнить.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5372841c841e82d116381d7ce8fe48af8ddfb036
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010321"
---
# <a name="distribute-and-schedule-questionnaires"></a>Распределение и планирование анкет

В этой статье объясняется, как распределить составленные анкеты, чтобы они были доступны отдельному пользователю или группе пользователей, которые должны ее заполнить. 

Существует несколько способов распределить анкету:

-   Пометить анкету как активную. Анкета будет доступна всем сотрудникам до тех пор, пока группа анкет не будет настроена для ограничения доступа к анкете.
-   Присвоить права на группу анкет. После этого анкета станет доступна всем членам выбранной группы.
-   Создать запланированные опросы. Анкета будет доступна только определенному сотруднику.
-   Создать график. Анкета станет доступна нескольким людям.

## <a name="marking-a-questionnaire-as-active"></a>Пометка анкеты как активной

Задав в поле **Активно** значение **Да** на странице **Анкеты**, вы предоставляете доступ для заполнения анкеты всем сотрудникам. Респонденты могут заполнить анкету несколько раз. Эта возможность полезна, если вы хотите получать отзывы на протяжении всего года. Например, вы можете создать анкету, в которой сотрудники смогут оставлять отзывы о качестве обедов в кафетерии.

## <a name="questionnaire-groups"></a>Группы анкет

Можно настроить группы анкет, а затем включить респондентов, для которых предназначена анкета. 

Группы анкет можно создавать на следующих страницах.

-   **Группы анкет** — только отдельные люди в группе анкет могут заполнять выбранную анкету. Например, если вашей аудиторией являются подрядчики, можно создать группу анкет, относящуюся к этим респондентам.
-   **Члены группы анкет** — можно добавлять людей в группы анкет.

Чтобы назначить группу анкет анкете, на странице **Анкеты** щелкните **Права доступа**. После сохранения анкеты как активной члены группы анкет смогут заполнить анкету. Эта возможность полезна, если вы хотите протестировать анкету на определенной группе людей, прежде чем предлагать ее более широкой группе, или если вы хотите нацелить анкету на очень специфическую аудиторию.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Запланированные опросы в анкете

Запланированные опросы — это составленные анкеты, для которых выбраны респонденты. 

> [!NOTE]
> Чтобы настроить запланированный опрос, сперва следует составить анкету. 

На странице **Запланированный опрос** можно создать запланированный опрос для отдельного сотрудника. В списке на странице отображаются все запланированные анкеты. 

Запланированные опросы применяются также на странице **Графики анкетирования**, где можно планировать анкеты для многих людей.

-   Сотрудники
-   Слушатели курса
-   Подразделения

Каждый человек может заполнить анкету только один раз.

## <a name="scheduling-a-questionnaire"></a>Планирование анкетирования

Дополнительно можно запланировать анкетирование нескольких респондентов.

### <a name="planning-types"></a>Типы планирования

Типы планирования необходимы для формирования расписания запланированных опросов для нескольких респондентов. Типы планирования используются для классификации расписаний анкетирования. Например, можно планировать анкеты для следующих целей:

-   Оценка
-   Исследование
-   Тестирование

Типы планирования для расписания анкетирования можно задать на странице **Графики анкетирования**.

### <a name="reference-types-for-questionnaire"></a>Типы ссылок для анкеты

Вы можете использовать типы ссылок, чтобы вводить критерии для респондентов, которых вы можете выбрать для планирования анкеты. 

Используйте страницу **Типы ссылок**, чтобы настроить типы ссылок для анкеты. Каждый тип ссылки соответствует таблице в Microsoft Dynamics 365 Finance. При создании планов анкет можно указывать отдельные записи в таблице или диапазоне таблиц, с которыми будет связана анкета. 

Например, если вы выберете таблицу "Курсы", вы можете указать, для какого конкретно курса будет предназначена анкета. Когда вы настроите ссылки для таблицы "Курсы", некоторые поля и кнопки на странице **Курсы** станут доступными.

### <a name="questionnaire-schedules"></a>Графики анкетирования

Графики анкетирования можно использовать для создания нескольких запланированных опросов для группы пользователей на основании типа ссылки. Создайте график на странице **Графики анкетирования**. Выберите тип планирования для классификации графика и выберите тип ссылки, который следует использовать для запроса системы относительно определенных пользователей. Например, если задать тип ссылки как таблицу "Курсы", можно выбрать определенный курс в поле **Ссылка**. 

Щелкните **Сведения о настройке**, чтобы выбрать анкету и другие критерии. Например, укажите имя инструктора как критерий, если анкета является оценкой инструктора. По завершении ввода сведений настройки система создаст запланированные сеансы опроса для пользователей, включенных в запрос. 

Щелкните **Запланированные опросы**, чтобы осмотреть сеансы ответов для графика. Можно вручную создать дополнительные запланированные опросы или удалить запланированные опросы, на которые получены ответы. 

Щелкните **Функции** &gt; **Начать**, чтобы сделать анкету доступной для пользователей в связанных запланированных опросах. Щелкните **Ответы**, чтобы просмотреть заполненные ответы на анкету. Также можно скопировать параметры графика анкеты, запланированные опросы и ответы в новый график анкеты.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Уведомление респондентов о доступных для них анкетах
При распространении анкет необходимо уведомить респондентов о том, что им доступны анкеты. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Уведомление респондентов о запланированном опросе

Если вы используете запланированный опрос, необходимо уведомить респондента напрямую, например по телефону или электронной почте.

### <a name="notifying-respondents-about-a-scheduling"></a>Уведомление респондентов о планировании

Страница **Графики анкетирования** позволяет подготовить и отправить электронные письма всем респондентам, назначенным для опроса. Введите текст сообщения электронной почты на вкладке **Электронная почта для портала самообслуживания сотрудников**. После запуска графика щелкните **Функции** &gt; **Отправить сообщение электронной почты**, чтобы создать и отправить сообщение электронной почты респондентам. После этого респонденты смогут войти на веб-сайт и заполнить анкету. 

> [!NOTE]
> Прежде чем вы можете использовать функциональность электронной почты, администратор ИТ должен ввести параметры электронной почты на странице **Параметры электронной почты**.

## <a name="ending-a-scheduled-questionnaire"></a>Завершение запланированного анкетирования

Можно завершить запланированную анкету, после того как все респонденты завершили заданные сеансы опроса. После завершения запланированного анкетирования, его настройки не могут копироваться в новый график. 

> [!NOTE]
>   Если один или несколько респондентов не заполнили анкету, а требуется закончить планирование, удалите сначала соответствующих респондентов из списка, который находится на странице **Запланированный опрос**. Затем можно завершить планирование.

## <a name="completing-questionnaires"></a>Заполнение анкет

После составления и распространения анкеты выбранные респонденты могут ее заполнить. Заполните анкеты, доступные в двух местах:

-   В области перехода щелкните **Анкеты** &gt; **Распределить** &gt; **Заполнение анкеты**.
-   На портале самообслуживания сотрудников щелкните **Анкеты для заполнения**.

Анкеты могут быть сделаны доступными для всех пользователей сети, либо для всех пользователей в сети.

