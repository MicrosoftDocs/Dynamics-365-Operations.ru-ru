---
title: Что нового и что изменилось в Dynamics 365 Human Resources (16 сентября 2020 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources от 16 сентября 2020 года.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74a87ddb4ed14042dd4e716ad64bc844a800a0a0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114061"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Что нового и что изменилось в Dynamics 365 Human Resources (16 сентября 2020 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Human Resources. Изменения применяются для номера сборки 8.1.3557. Числа в скобках рядом с некоторыми функциями относятся к номерам поддержки в службе Lifecycle Services (LCS) для справки.

## <a name="included-in-this-release"></a>Включено в данный выпуск

-  [Сохраненные представления — общая доступность](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Дополнительные сведения см. в разделе [Сохраненные представления](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- Форма **Действия должности** имеет обновленную сетку измерений и новый диалог (469495).

- Если установить для параметра **Ограничить доступ к сведениям о работнике** значение "Да" в пункте **Расширенный доступ** раздела **Общие параметры Human Resources**, в формах льгот теперь отображаются только соответствующие работники (393384).

- Новые параметры создания календаря в сущности **WorkCalendar** (477055):<br>- Время окончания по умолчанию<br>- Время начала по умолчанию<br>- Является ли пятница рабочим днем<br>- Является ли понедельник рабочим днем<br>- Является ли суббота рабочим днем<br>- Является ли воскресенье рабочим днем<br>- Является ли четверг рабочим днем<br>- Является ли вторник рабочим днем<br>- Является ли среда рабочим днем<br>- Код праздничного дня в рабочем календаре

- Сущность **LeaveBankTransactionV1** теперь включает код причины (477823).

- Теперь можно сохранять записи задач (492923).

- Данные успешно публикуются из **HCMWorkerContactEntity** (427620).

- Экспресс-вкладка **Компенсация** теперь отображается для типа сотрудника подрядчика в форме **Действия сотрудников** (482494).

- Поля **Уровень** и **План** теперь являются обязательными, если задана **Фиксированная компенсация**. Если эти поля не заполнены, отображается сообщение об ошибке (482497).

- Поле **Тип плана** в разделе **Льготы** является раскрывающимся списком (488768).

- Системные администраторы теперь получают уведомление, если настраиваемое поле удаляется из модуля Human Resources (481408).

- В процессе увольнения сотрудника работа модуля Human Resources должна быть ожидаемой и не изменяет выбранную компанию после появления блокировки (479877). 

- Менеджеры больше не могут добавлять числовые столбцы с помощью персонализации (485317).

- Менеджеры больше не могут удалять фильтр диапазона данных из истечения срока действия идентификационных номеров (485321).

- Если поле **Кому подчиняется** пусто, сведения о должности продолжают отображаться при наведении указателя мыши на должность (433328).

- Сотрудники могут теперь просматривать сведения о плане льгот в модуле "Дистанционное обслуживание сотрудников" (481676).

- Сотрудники могут теперь видеть все зарегистрированные курсы (429048).

- Теперь можно ограничить параметры просмотра для страницы **Профессиональные сертификаты**. Можно ограничить параметры просмотра для текущего юридического лица, по статусу работника и по типу работника (451501). 


## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="human-resources-app-in-teams"></a>Приложение Human Resources в Teams

Сотрудники могут просматривать и запрашивать время отсутствия на работе в Microsoft Teams. Они могут взаимодействовать с ботом для создания запросов на отпуск. Дополнительные сведения см.

- [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 1 за 2020 год
- [Приложение Human Resources в Teams](https://go.microsoft.com/fwlink/?linkid=2127841) в документации Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Предварительные версии функций приложения Human Resources в Teams
 
-  **Уведомления**: отправители и утверждающие запросы отпусков получают уведомления в приложении Human Resources в Teams. Утверждающие могут утверждать или отклонять запросы на отсутствие. Отправители получат уведомление, если запрос был утвержден или отклонен. Дополнительные сведения см.
   - [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 2 за 2020 год
   - [Включение уведомлений для приложения Human Resources в Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) в документации Human Resources
   - [Включение или выключение уведомлений Teams для отдельных пользователей](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) в документации Human Resources
   - [Уведомления Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) в документации Human Resources
   - [Просмотр календаря отпусков вашей рабочей группы](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) в документации Human Resources
 
- **Календарь отпусков руководителя**: руководители могут просматривать утвержденные и ожидающие отпуска для их непосредственных подчиненных в представлении календаря. Это представление упрощает понимание того, когда члены рабочей группы не находятся на рабочем месте. Дополнительные сведения см.
   - [Отпуск сотрудника и опыт отсутствия в Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) в плане выпуска Dynamics 365 волны 2 за 2020 год
   - [Просмотр календаря отпусков вашей рабочей группы](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) в документации Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Параметр конфигурации для размещения списка рабочих элементов, назначенных мне (477004)

Новый параметр теперь становится доступным для позиционирования списка **Рабочие элементы, назначенные мне** в правом столбце панели мониторинга. При таком изменении все рабочие элементы и списки дел отображаются в одной области. Активируйте эту функцию, включив **Предварительная версия — улучшения рабочего процесса** в управлении функциями. Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

Эта функция также поддерживает параметры рабочего процесса, которые отображаются в формах действий персонала. Параметры рабочего процесса также появляются над экспресс-вкладкой действий для быстрого доступа. Дополнительные сведения см. 

- [Улучшения рабочего процесса управления предприятием и персоналом](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) в плане волны 2 выпуска 2020 года Dynamics 365

![Рабочие элементы, назначенные мне](./media/hr-workflow-work-items-assigned-to-me.png)

![Быстрый доступ к элементам рабочего процесса](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Календарь отпусков и отсутствия

В этой версии включены дополнительные параметры календаря для календарей отпусков и отсутствия. Дополнительные сведения см. в разделе [Просмотр календарей рабочей группы и компании](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Скоро

### <a name="checklist-entities-included-in-dataverse"></a>Сущности контрольного списка, включенные в Dataverse

Сущности контрольного списка для адаптации, увольнения, переходов и бизнес-процессов в скором времени будут доступны в Dataverse.

### <a name="benefits-management-reason-codes"></a>Коды причин управления льготами

Коды причин управления льготами скоро будут объединены с существующими кодами причин в Human Resources. Если созданные коды причин в модуле управления льготами имеют более 15 символов, необходимо изменить имя кода причины в форме **Коды причин** управления льготами, чтобы оно состояло не более чем из 15 символов. После обновления имени код причины появится под существующим кодом причины в управлении персоналом. Это изменение будет доступно в будущем и не повлияет на существующие функции.

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Human Resources](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2019, волна 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)
