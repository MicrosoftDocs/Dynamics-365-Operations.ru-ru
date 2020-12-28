---
title: Объекты Common Data Service
description: Microsoft Dynamics 365 Human Resources использует Common Data Service для включения сценариев расширяемости и интеграции.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530014"
---
# <a name="common-data-service-entities"></a>Объекты Common Data Service

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources использует Common Data Service для включения сценариев расширяемости и интеграции.

Дополнительные сведения о Common Data Service см. в разделе [Что такое Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Доступны следующие объекты Управление персоналом в Common Data Service.

## <a name="benefit-entities"></a>Объекты льгот

| Название | Объект |
| --- | --- |
| Частота расчета льгот | cdm_benefitcalculationfrequency |
| Частоты расчета для платежного периода для льгот | cdm_benefitcalculationfrequencypayperiod |
| Ставка расчета льгот | cdm_benefitcalculationrate |
| Сведения о ставке расчета льгот | cdm_benefitcalculationratedetail |
| Параметр льготы | cdm_benefitoption |
| План льготы | cdm_benefitplan (не включено для поддержки настраиваемых полей) |
| Тип льготы | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Объекты задач бизнес-процесса

| Название | Объект |
| --- | --- |
| Календарь бизнес-процесса | cdm_businessprocesscalendar |
| Назначение группы бизнес-процессу | cdm_businessprocessgroupassignment |
| Группа задач библиотеки бизнес-процессов | cdm_businessprocesslibrarytaskgroup |
| Стадия бизнес-процесса | cdm_businessprocessstage |
| Заголовок шаблона контрольного списка | cdm_businessprocesstemplateheader |
| Задача шаблона контрольного списка | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Объекты компенсации

| Название | Объект |
| --- | --- |
| План фиксированной компенсации | cdm_compensationfixedplan |
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
| Фиксированная компенсация для работника | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Объекты организации

| Название | Объект |
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
> Финансовые аналитики для **Тип должности**, **Назначение работника на должность** и **Занятость** обеспечивают однонаправленную интеграцию с Common Data Service. Обновления финансовых аналитик в данный момент не могут выполнять синхронизацию из Common Data Service в Human Resources. 

## <a name="leave-and-absence-entities"></a>Объекты отпусков и отсутствия

| Наименование | Объект |
| --- | --- |
| Банковская проводка отпуска | cdm_leavebanktransaction |
| Регистрация отпуска | cdm_leaveenrollment |
| План отпусков | cdm_leaveplan |
| Запрос на отпуск | cdm_leaverequest |
| Сведения запроса отпуска | cdm_leaverequestdetail |
| Тип отпуска | cdm_leavetype |
| Код основания типа отпуска | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Объекты заработной платы

| Название | Объект |
| --- | --- |
| Цикл оплаты | cdm_paycycle |
| Платежный период | cdm_payperiod |
| Код дохода в зарплате | cdm_payrollearningcode |
| Выплаты по банковскому счету | cdm_bankaccountdisbursement |
| Налоговый регион | cdm_taxregion |

## <a name="worker-entities"></a>Объекты работника

| Название | Объект |
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

## <a name="worker-setup-entities"></a>Объекты настройки работника

| Название | Объект |
| --- | --- |
| Статус ветерана | cdm_veteranstatus |
| Этническое происхождение | cdm_ethnicorigin |
| Код основания | cdm_reasoncode |
| Выпускающее агентство по идентификации лиц | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Объекты компетенции

| Название | Объект |
| --- | --- |
| Тип навыка | cdm_skilltype |

## <a name="entity-relationship-models"></a>Модели связи объектов

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

[Выбор технологии интеграции данных](hr-admin-integration-choose-technology.md)</br>
[Настройка интеграции Common Data Service](hr-admin-integration-common-data-service.md)
