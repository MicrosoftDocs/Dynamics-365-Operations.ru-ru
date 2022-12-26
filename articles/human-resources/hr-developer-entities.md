---
title: Таблицы Dataverse
description: Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838591"
---
# <a name="dataverse-tables"></a>Таблицы Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.

> [!NOTE]
> Сущности Human Resources соответствуют таблицам Dataverse. Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Доступны следующие таблицы Dataverse на основе сущностей Human Resources.

Дополнительные сведения об известных проблемах см. в разделе [Поиск проблем в Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>Таблицы льгот

| Имя | Таблица | Известные проблемы  | Статус |
| --- | --- |    --------|----------  |
| Частота расчета льгот | cdm_benefitcalculationfrequency |     |     |
| Частоты расчета для платежного периода для льгот | cdm_benefitcalculationfrequencypayperiod |     |     |
| Ставка расчета льгот | cdm_benefitcalculationrate |    |     |
| Сведения о ставке расчета льгот | cdm_benefitcalculationratedetail |753225 | Разрешено  |
| Параметр льготы | cdm_benefitoption |    |     |
| План льготы | cdm_benefitplan (не включено для поддержки настраиваемых полей) |    |     |
| Тип льготы | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Таблицы задач бизнес-процесса

| Имя | Таблица |Известные проблемы  | Статус |
| --- | --- |   --------|----------   |
| Календарь бизнес-процесса | cdm_businessprocesscalendar | 751867 | Разрешено |
| Назначение группы бизнес-процессу | cdm_businessprocessgroupassignment | 751869  751863 | Активные сотрудники|
| Группа задач библиотеки бизнес-процессов | cdm_businessprocesslibrarytaskgroup |751866 | Закрыто |
| Стадия бизнес-процесса | cdm_businessprocessstage |      |     |
| Заголовок шаблона контрольного списка | cdm_businessprocesstemplateheader |     |     |
| Задача шаблона контрольного списка | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Таблицы компенсаций

| Имя | Таблица |Известные проблемы  | Статус |
| --- | --- | ----------      | -------    |
| Фиксированный план компенсации | cdm_compensationfixedplan |754453 | Закрыто |
| Сетка компенсации | cdm_compensationgrid |             |     |
| Уровень компенсации | cdm_compensationlevel |           |     |
| Частота компенсационных выплат | cdm_compensationpayfrequency |                  |     |
| Настройка опорной точки компенсации | cdm_compensationreferencepointsetup |               |     |
| Линия настройки опорных точки компенсации | cdm_compensationreferencepointsetupline |             |     |
| Регион компенсации | cdm_compensationregion |                   |     |
| Структура компенсации | cdm_compensationstructure |    754456        | Закрыто    |
| План переменной компенсации | cdm_compensationvariableplan |               |     |
| Уровень плана переменной компенсации | cdm_compensationvariableplanlevel |                |     |
| Тип плана переменной компенсации | cdm_compensationvariableplantype |               |     |
| Мероприятие фиксированной компенсации | cdm_fixedcompensationevent |               |     |
| Положение о передаче прав на льготы | cdm_vestingrule |              |     |
| Фиксированная компенсация работника | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Таблицы организаций

| Имя | Таблица |Известные проблемы  | Статус |
| --- | --- | ----------      | -------    |
| Отдел | cdm_department |  752194    | Закрыто    |
| Занятость | cdm_employment | 762414  |  Закрыто  |
| Компания | cdm_company |  |     |
| Должность | cdm_job |  |     |
| Функциональные обязанности | cdm_jobfunction |        |     |
| Должность | cdm_jobposition | 752214      | Закрыто    |
| Тип позиции | cdm_positiontype |            |     |
| Назначение работника на должность | cdm_positionworkerassignmentmap | 752224    |  Закрыто   |
| Аналитика должности | cdm_jobpositiondimension|       |     |
| Тип вакансии | cdm_jobtype |      |     |
| Язык | cdm_language |        |     |
| Должность | cdm_title |       |     |

> [!NOTE]
> Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Dataverse. Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Dataverse в Human Resources. 

## <a name="leave-and-absence-tables"></a>Таблицы отпусков и отсутствия

| Имя | Таблица | Известные проблемы  | Статус |
| --- | --- |   ----------      | -------    |
| Банковская проводка отпуска | cdm_leavebanktransaction |  752252    |    Разрешено |
| Регистрация отпуска | cdm_leaveenrollment |  752934    |Закрыто     |
| План отпусков | cdm_leaveplan |   752232   |   Закрыто  |
| Запрос на отпуск | cdm_leaverequest | 753207     | Закрыто    |
| Сведения запроса отпуска | cdm_leaverequestdetail | 753207     |   Закрыто  |
| Тип отпуска | cdm_leavetype |      |     |
| Код основания типа отпуска | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>Интеграция с двойной записью с использованием таблиц Dataverse для отпусков и отсутствия доступна только в том случае, если функция **Настройка нескольких типов отпусков в одном плане отпусков** включена в Microsoft Dynamics 365 Finance с помощью пункта **Управление функциями**. 

## <a name="payroll-tables"></a>Таблицы зарплаты

| Имя | Таблица |Известные проблемы  | Статус |
| --- | --- |  ----------      | -------    |
| Цикл оплаты | cdm_paycycle |    |     |
| Платежный период | cdm_payperiod |          |     |
| Код дохода по зарплате | cdm_payrollearningcode |   754458        |   Закрыто  |
| Выплаты по банковскому счету | cdm_bankaccountdisbursement |    751904     |   Закрыто  |
| Налоговый регион | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Таблицы работников

| Имя | Таблица |Известные проблемы  | Статус |
| --- | --- |----------      | -------    |
| Работник | cdm_worker |    751906    |    Закрыто |
| Адрес работника | cdm_workeraddress |   754465     |Закрыто     |
| Личные данные работника | cdm_workerpersonaldetail |   751906     |   Закрыто  |
| Идентификационный код работника | cdm_workerpersonidentificationnumber |  766704      |   Закрыто  |
| Идентификационный тип работника | cdm_workerpersonidentificationtype |        |     |
| Рабочий календарь | cdm_workcalendar |        |     |
| Календарный день работы | cdm_workcalendarday |        |     |
| Праздничный день в рабочем календаре |cdm_workcalendarholiday |        |     |
| Строка праздничного дня в рабочем календаре | cdm_workcalendarholidayline |        |     |
| Интервал рабочего времени | cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей) |        |     |
| Банковский счет работника | cdm_workerbankaccount |        |     |

## <a name="worker-setup-tables"></a>Таблицы настройки работников

| ФИО | Таблица |
| --- | --- |
| Статус ветерана | cdm_veteranstatus |
| Этническое происхождение | cdm_ethnicorigin |
| Код основания | cdm_reasoncode |
| Агентство, выпускающее средства идентификации пользователей | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Таблицы компетенции

| ФИО | Таблица |
| --- | --- |
| Тип навыка | cdm_skilltype |

## <a name="table-relationship-models"></a>Модели связи таблиц

### <a name="worker"></a>Рабочий

![Работник.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Работа и должность

![Работа и должность.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Выгоды

![Выгоды.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Компенсация

![Компенсация.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Отпуск

![Отпуск.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Рабочий календарь

![Рабочий календарь.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>См. также

[Выбор технологии интеграции данных](hr-admin-integration-choose-technology.md)<br>
[Настройка интеграции Dataverse](hr-admin-integration-common-data-service.md)<br>
[Настройка виртуальных таблиц Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Вопросы и ответы по виртуальным таблицам Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Обновления терминологии](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
