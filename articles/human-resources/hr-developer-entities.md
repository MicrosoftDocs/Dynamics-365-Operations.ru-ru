---
title: Таблицы Dataverse
description: Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893408"
---
# <a name="dataverse-tables"></a>Таблицы Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources использует Dataverse для включения сценариев расширяемости и интеграции.

> [!NOTE]
> Сущности Human Resources соответствуют таблицам Dataverse. Дополнительные сведения об Dataverse (ранее Common Data Service) и обновлениях терминологии см. в разделе [Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Доступны следующие таблицы Dataverse на основе сущностей Human Resources.

## <a name="benefit-tables"></a>Таблицы льгот

| ФИО | Таблица |
| --- | --- |
| Частота расчета льгот | cdm_benefitcalculationfrequency |
| Частоты расчета для платежного периода для льгот | cdm_benefitcalculationfrequencypayperiod |
| Ставка расчета льгот | cdm_benefitcalculationrate |
| Сведения о ставке расчета льгот | cdm_benefitcalculationratedetail |
| Параметр льготы | cdm_benefitoption |
| План льготы | cdm_benefitplan (не включено для поддержки настраиваемых полей) |
| Тип льготы | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Таблицы задач бизнес-процесса

| ФИО | Таблица |
| --- | --- |
| Календарь бизнес-процесса | cdm_businessprocesscalendar |
| Назначение группы бизнес-процессу | cdm_businessprocessgroupassignment |
| Группа задач библиотеки бизнес-процессов | cdm_businessprocesslibrarytaskgroup |
| Стадия бизнес-процесса | cdm_businessprocessstage |
| Заголовок шаблона контрольного списка | cdm_businessprocesstemplateheader |
| Задача шаблона контрольного списка | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Таблицы компенсаций

| ФИО | Таблица |
| --- | --- |
| Фиксированный план компенсации | cdm_compensationfixedplan |
| Сетка компенсации | cdm_compensationgrid |
| Уровень компенсации | cdm_compensationlevel |
| Частота компенсационных выплат | cdm_compensationpayfrequency |
| Настройка опорной точки компенсации | cdm_compensationreferencepointsetup |
| Линия настройки опорных точки компенсации | cdm_compensationreferencepointsetupline |
| Регион компенсации | cdm_compensationregion |
| Структура компенсации | cdm_compensationstructure |
| План переменной компенсации | cdm_compensationvariableplan |
| Уровень плана переменной компенсации | cdm_compensationvariableplanlevel |
| Тип плана переменной компенсации | cdm_compensationvariableplantype |
| Мероприятие фиксированной компенсации | cdm_fixedcompensationevent |
| Положение о передаче прав на льготы | cdm_vestingrule |
| Фиксированная компенсация работника | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Таблицы организаций

| ФИО | Таблица |
| --- | --- |
| Отдел | cdm_department |
| Занятость | cdm_employment |
| Организация | cdm_company |
| Должность | cdm_job |
| Функциональные обязанности | cdm_jobfunction |
| Должность | cdm_jobposition |
| Тип позиции | cdm_positiontype |
| Назначение работника на должность | cdm_positionworkerassignmentmap |
| Аналитика должности | cdm_jobpositiondimension|
| Тип вакансии | cdm_jobtype |
| Язык | cdm_language |
| Должность | cdm_title |

> [!NOTE]
> Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Dataverse. Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Dataverse в Human Resources. 

## <a name="leave-and-absence-tables"></a>Таблицы отпусков и отсутствия

| ФИО | Таблица |
| --- | --- |
| Банковская проводка отпуска | cdm_leavebanktransaction |
| Регистрация отпуска | cdm_leaveenrollment |
| План отпусков | cdm_leaveplan |
| Запрос на отпуск | cdm_leaverequest |
| Сведения запроса отпуска | cdm_leaverequestdetail |
| Тип отпуска | cdm_leavetype |
| Код основания типа отпуска | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Таблицы зарплаты

| ФИО | Таблица |
| --- | --- |
| Цикл оплаты | cdm_paycycle |
| Платежный период | cdm_payperiod |
| Код дохода по зарплате | cdm_payrollearningcode |
| Выплаты по банковскому счету | cdm_bankaccountdisbursement |
| Налоговый регион | cdm_taxregion |

## <a name="worker-tables"></a>Таблицы работников

| ФИО | Таблица |
| --- | --- |
| Рабочий | cdm_worker |
| Адрес работника | cdm_workeraddress |
| Личные данные работника | cdm_workerpersonaldetail |
| Идентификационный код работника | cdm_workerpersonidentificationnumber |
| Идентификационный тип работника | cdm_workerpersonidentificationtype |
| Рабочий календарь | cdm_workcalendar |
| Календарный день работы | cdm_workcalendarday |
| Праздничный день в рабочем календаре |cdm_workcalendarholiday |
| Строка праздничного дня в рабочем календаре | cdm_workcalendarholidayline |
| Интервал рабочего времени | cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей) |
| Банковский счет работника | cdm_workerbankaccount |

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

![Рабочий](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Работа и должность

![Работа и должность](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Льготы

![Льготы](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Компенсация

![Компенсация](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Отпуск

![Отпуск](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Рабочий календарь

![Рабочий календарь](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>См. также

[Выбор технологии интеграции данных](hr-admin-integration-choose-technology.md)<br>
[Настройка интеграции Dataverse](hr-admin-integration-common-data-service.md)<br>
[Настройка виртуальных таблиц Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Вопросы и ответы по виртуальным таблицам Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Что такое Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Обновления терминологии](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]