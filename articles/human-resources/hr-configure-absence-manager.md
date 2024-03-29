---
title: Настройка роли менеджера по отсутствию
description: В этой статье объясняется, как настроить роль менеджера отсутствия для управления отпусками сотрудников.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b752b722bf63958fc35b10a4612f7f02e2e8e717
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337038"
---
# <a name="configure-the-absence-manager-role"></a>Настройка роли менеджера по отсутствию


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В некоторых организациях менеджеры пользователей не могут управлять отпуском для своей рабочей группы. Вместо этого менеджер отсутствия может обрабатывать этот процесс для членов рабочей группы в нескольких отделах и рабочих группах. Менеджеры по отсутствию имеют следующие возможности для управления отпуском:

- Просмотр и утверждение выходных на основе альтернативной иерархии.
- Просмотр балансов участников рабочей группы.
- Просмотр календаря отсутствия.

## <a name="turn-on-the-feature"></a>Включение функции

1. В рабочей области **Администрирование системы** выберите **Управление функциями**.
2. На вкладке **Управление функциями** включите функцию **Менеджер отсутствия для управления отсутствием**.

## <a name="define-a-custom-hierarchy"></a>Определение пользовательской иерархии

Функция менеджера отсутствия использует настраиваемую иерархию, которая должна быть настроена.

1. В рабочей области **Администрирование организации** выберите **Типы иерархии должностей**.
2. Создайте тип иерархии должностей с именем **Отпуск**.
3. В рабочей области **Отпуск и отсутствие** в области **Ссылки** выберите **Параметры отпусков и отсутствия**.
4. На вкладке **Общие** в раскрывающемся списке **Иерархия отсутствия** выберите тип иерархии **Отпуск**, который был создан ранее. Эта связь иерархии отпуска должна быть выполнена для каждого юридического лица, в котором будет использоваться функция менеджера отсутствия.

После определения типа иерархии подчиненный иерархии должностей должен быть назначен этой должности.

1. В рабочей области **Администрирование организации** выберите **Все должности**.
2. Выберите должность, в которую добавляется иерархия отпусков.
3. На вкладке **Отношения** выберите **Добавить**.
4. В поле **Имя иерархии** выберите **Отпуск**.
5. В поле **Отчитывается перед должностью** выберите должность. Имя работника заполняется автоматически после выбора должности.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Назначение роли менеджера по отсутствию пользователю

Роль менеджера отсутствия должна быть назначена сотрудникам, чтобы позволить им утверждать или отклонять запросы на отпуск.

1. В рабочей области **Администрирование системы** выберите **Ссылки**.
2. В разделе **Пользователи** выберите ссылку **Пользователи**.
3. В списке пользователей выберите пользователя, которому требуется назначить роль менеджера отсутствия.
4. На вкладке **Роль пользователя** выберите **Назначить роли**.
5. В списке выберите роль **Менеджер отсутствия**. Затем выберите **OK**.

    > [!IMPORTANT]
    > Убедитесь, что роль сотрудника также была назначена пользователю, которому назначается роль менеджера отсутствия. В противном случае работник не сможет использовать эту функцию.

6. После создания иерархии отпусков ее можно просмотреть, выполнив следующие шаги:

    1. В рабочей области **Администрирование организации** выберите **Иерархия должностей**.
    2. В поле **Тип иерархии** выберите **Отпуск**.

## <a name="absence-manager-workspace"></a>Рабочая область менеджера по отсутствию

В рабочей области **Самообслуживание сотрудников** на вкладке **Управление отпусками** отображаются сведения об отсутствии сотрудников, назначенных менеджеру по отсутствию в иерархии отпусков. Имеется несколько вариантов, доступных для диспетчера отпусков: 
 - Проверка запросов на отгулы.</br>
 - Отправка запроса на отгул от имени сотрудника.</br>
 - Просмотр всех сотрудников, назначенных им в рамках иерархии отпусков.</br>
 - Просмотр календаря менеджера по отсутствию.</br>

В рабочей области **Управление отпусками** представлены две вкладки:
 - **Запросы на отгулы**: на этой вкладке будут перечислены все ожидающие обработки запросы на отгулы, которые менеджер отсутствия может утвердить. Менеджер по отсутствиям может выбрать несколько записей и выполнить над ними действия одновременно. Если включен просмотр отпусков между компаниями, в этом списке отображаются ожидающие запросы отгулов для всех юридических лиц, к которым у них есть доступ. В противном случае будут показаны ожидающие запросы отгулов для выбранного юридического лица. </br>
 - **Все сотрудники**: на этой вкладке будут перечислены все сотрудники, назначенные менеджеру отсутствия в иерархии отпусков. Для каждого сотрудника имеется пара параметров:
    - **Запрос отгула** — отправка нового запроса отгула для выбранного сотрудника.</br>
    - **Отгулы** — просмотр балансов, утвержденных отгулов и запросов отгулов для выбранного сотрудника.</br>

## <a name="approve-time-off-requests"></a>Утверждение запросов на отгулы

Менеджеры отсутствия могут утверждать или отклонять запросы отгулов для сотрудников. 

> [!IMPORTANT]
> Прежде чем менеджеры отсутствия смогут утверждать или отклонять запросы отгулов, необходимо настроить рабочий процесс запроса отпусков, чтобы назначать им для просмотра рабочие элементы запросов отпусков.
>
> 1. На странице **Рабочие процессы управления персоналом** выберите или создайте рабочий процесс запроса отпуска.
> 2. Выберите параметр **Связать иерархию**, затем в поле **Имя иерархии** выберите **Отпуск**.
> 3. Обновление рабочего процесса в конструкторе рабочих процессов. В разделе **Тип назначения** выберите параметр **Иерархия**, затем на вкладке **Выбор иерархии** выберите **Настраиваемая иерархия**.
>
> Сведения о создании рабочего процесса запроса отпуска см. в разделе [Создание рабочего процесса запроса отпуска](hr-leave-and-absence-workflow.md).

1. В рабочей области **Самообслуживание сотрудников** выберите вкладку **Управление отпусками**.
2. На вкладке **Запросы отгулов**, выберите запросы отгулов, по которым необходимо выполнить действие. В этом представлении списка можно выбрать несколько записей.
3. Используйте кнопки действий в верхней части сетки для утверждения, отклонения или делегирования запроса на отгул. 

Кроме того, пользователь может также использовать плитку **Запросы отгулов** в левой части окна, чтобы перейти в список всех элементов работы запросов отгулов. 

## <a name="view-time-off-in-the-calendar"></a>Просмотр отгула в календаре

Пользователи, не имеющие роли менеджера отсутствия, могут просматривать запросы отгулов в своем календаре. Выполните следующие шаги для доступа к календарю отпусков.

> [!IMPORTANT]
> Системный администратор должен настроить параметры просмотра для календаря менеджера отсутствия. На странице **Параметры отпусков и отсутствия** на вкладке **Календарь** имеются параметры, позволяющие скрыть или отобразить дни рождения, отсутствия без сведений, отпуска отсутствия и ожидающие запросы на отпуск. Имеется также возможность отфильтровать параметр представления календаря по типу работника.

1. В рабочей области **Самообслуживание сотрудников** выберите **Управление отпусками**, затем **Календарь менеджера отсутствия**.
2. В поле **Дата** введите требуемые даты.
3. При необходимости обновите параметры просмотра.

В календаре менеджера отсутствия отображаются все записи для сотрудников, которые подчиняются менеджеру отсутствия в иерархии отпусков.

## <a name="see-also"></a>См. также

- [Обзор отпусков и отсутствия на работе](hr-leave-and-absence-overview.md)
- [Создание workflow-процесса запросов на отпуск](hr-leave-and-absence-workflow.md)
- [Просмотр календарей группы и компании](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
