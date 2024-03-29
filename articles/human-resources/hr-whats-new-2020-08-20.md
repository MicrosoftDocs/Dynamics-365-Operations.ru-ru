---
title: Что нового и что изменилось в Dynamics 365 Human Resources (20 августа 2020 г.)
description: В этой статье описываются новые или измененные функции в Microsoft Dynamics 365 Human Resources от 20 августа 2020 года.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c71a742022afba36c417092d5a9b75c78600357
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902179"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (20 августа 2020 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.3478. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Отображение сведений о предстоящих и ожидающих отпусках на карточках в рабочей области пользователей

В карточках отпусков и отсутствий в рабочем пространстве **Сотрудники** теперь доступны параметры запроса ожидающих и предстоящих отпусков.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Поле "Частный" не имеет значение "Да" по умолчанию для роли сотрудника в модуле самообслуживания сотрудника (477106)

Поле **Частный** теперь по умолчанию равно **Да**, когда сотрудники добавляют новые записи адресов через страницу **Личные данные** в службе самообслуживания сотрудников. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Кандидаты для найма на экспресс-вкладке в модуле "Управление персоналом" показывают неверное количество кандидатов (470110)

Страница **Управление персоналом** теперь будет точно отображать число кандидатов для найма. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Невозможно ввести отсутствие по болезни для уволенного сотрудника, когда для начисления установлено значение ноль (446195)

Проводки отпусков теперь разрешены для сотрудников, которые были уволены в будущем, и для начисления установлено значение ноль. Проводки отпусков можно ввести до даты увольнения сотрудника. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Добавление настраиваемых полей в новую форму сотрудника отключает поля в панели операций для управления отпуском (473314)

Параметры области действий в новой форме **Сотрудник** в модуле **Управление отпусками** больше не будут отключаться, если в новую форму **Сотрудник** добавлены настраиваемые поля.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Если сделать поле комментария к отпуску обязательным, то запрос отпуска можно отправить при отсутствии введенного комментария (473543)

Поля комментариев теперь могут быть обязательными, а запросы отпусков учитывают эту настройку. Обязательные поля являются предварительной версией функции.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>Объект DMF доступен для приостановки начисления

Объект DMF теперь доступен для приостановки начисления.

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="mandatory-fields"></a>Обязательные поля

Можно сделать поля обязательными, используя возможности персонализации в Human Resources. Для этой функции требуются **сохраненные представления**. Дополнительные сведения о сохраненных представлениях см. в:

- [Сохраненные представления — общая доступность](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) в плане выпуска Dynamics 365 волны 2 за 2020 год
- [Создание форм, использующих сохраненные представления](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Приложение Human Resources в Teams

Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams. Они могут взаимодействовать с ботом для создания запросов на отпуск. Дополнительные сведения см.

- [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 1 за 2020 год
- [Приложение Human Resources в Teams](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Скоро

### <a name="human-resources-app-in-teams-preview-features"></a>Предварительные версии функций приложения Human Resources в Teams
 
-  **Уведомления**: отправители и утверждающие запросы отпусков получают уведомления в приложении Human Resources в Teams. Утверждающие смогут утверждать или отклонять запросы отпусков, и отправители будут получать уведомление, если запрос был утвержден или отклонен.
 
- **Календарь отпусков руководителя**: руководители смогут просматривать утвержденные и ожидающие отпуска для их непосредственных подчиненных в представлении календаря. Это представление упрощает понимание того, когда члены рабочей группы не находятся на рабочем месте.

### <a name="checklist-entities-included-in-dataverse"></a>Сущности контрольного списка, включенные в Dataverse

Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.

## <a name="known-issues"></a>Известные проблемы

В рабочей области **управления функциями** могут отображаться функции, которые отключены в качестве предварительных функций предварительного просмотра, когда они обычно доступны. Далее приведен список общедоступных функций, которые показывают неправильный статус. 

- Управление льготами
- Управление обращениями
- Ведение журнала базы данных (аудит)
- Начисление отпуска для одной компании или одного плана
- Приостановка начисления отпусков и отсутствия
- Код основания корректировки сальдо и комментарий
- Покупка и продажа отпуска
- Календарь отпусков и отсутствия
- Правила переноса отпуска
- Аудит начисления отпуска
- Удаление начисления отпуска
- Округление начислений отпусков
- Настройка нескольких типов отпусков в одном плане отпусков
- Улучшения обновления отгулов
- Использовать FTE сотрудника для начислений
- Представление межфирменной компенсации
- Печать оценок производительности
- Корректировки праздников при начислении отпуска

### <a name="benefit-plan-employee-entity"></a>Сущность плана льгот сотрудников 

Недавно мы обнаружили две ошибки, связанные с сущностью **BenefitsPlanEmployee**. При импорте регистраций работников **Код покрытия** и **Код типа плана** устанавливаются неправильно. Эта проблема приводит к неправильному отображению планов льгот сотрудников в форме **План льгот работников** и в форме **Открытие регистрации** в службе самообслуживания сотрудников. Эта проблема также может повлиять на способность сотрудника выбирать планы в службе самообслуживания сотрудников. В настоящее время нет обходного пути. Мы рассматриваем это как исправление высокого приоритета, и исправление будет развернуто в следующем выпуске.

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]