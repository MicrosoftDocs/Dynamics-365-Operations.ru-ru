---
title: Что нового и что изменилось в Dynamics 365 Talent (3 декабря 2019 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1ed998302762203bad736161a27a48152de65f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897726"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (3 декабря 2019 г.)

В этой статье описываются новые и измененные компоненты в Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2646. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Рабочая область управления функциями

Рабочая область **Управление функциями** содержит список функций, предоставляемых в каждом выпуске. По умолчанию новые функции отключены. Можно использовать рабочую область для их включения и просмотра документации по ним. Дополнительные сведения об управлении функциями см. в разделе [Обзор управления функциями](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Все новые возможности остаются в виде предварительного просмотра по крайней мере на 30 дней, а обычно 30-60 дней. Основные функции обычно доступны в октябре и апрель каждого года, следующего за периодом предварительного просмотра. После отображения новых возможностей в рабочей области **Управление функциями** их можно включить. Некоторые функции могут быть включены по умолчанию.
 
Время от времени неотъемлемая функция будет включена по умолчанию и не может быть отключена (например, в рабочей области **Управление функциями**).
 
Когда функция обычно доступна, она может быть включена или выключена в производственных средах. Рабочая область **Управление функциями** показывает, что функция предварительного просмотра станет обязательной. Эта дата обычно приходится на 1 октября или 1 апреля, чтобы соответствовать полугодовым плановым выпускам. Вы не можете отключить обязательные функции. До тех пор, пока она не станет обязательной, можно включать и выключать функцию во всех средах.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Добавление автоматического планирования очистки истории пакетных заданий (332528)

С помощью этого изменения **История пакетных заданий** работает каждую ночь и удаляет элементы пакетных заданий старше 30 дней.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent не реагирует в действия работника, когда длина идентификационного номера не соответствует типу идентификации (390971)

Этот релиз исправляет проблему, когда длина идентификационного номера не соответствует определению в типе идентификации. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Фиксированная компенсация не обновляет уровень с изменениями в деталях позиции (348085)

В выпуске на этой неделе **Дата начала компенсации** определяет задание, связанное с позицией на тот момент времени при создании новой записи фиксированной компенсации для сотрудника.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Списки работников, сотрудников и подрядчиков показывают тип работника как "оба", когда они должны быть только работниками или подрядчиками (384473)

Это изменение точно отражает введенный тип работника (подрядчика или работника).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Уведомления по электронной почте для новых действий по найму не содержат информацию об имени из-за политики безопасности (383402)

Это изменение исправляет информацию, отображаемую в полях имени или фамилии в заполнителях для рабочего процесса, когда включена расширенная безопасность.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Система разрешает запросы двух полных дней отпуска на один день (379284)

С этим изменением вы не можете выдавать два запроса на отпуск в один и тот же день. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Список изменений адреса должен быть отсортирован к дате вступления в силу (352798)

С этим изменением список изменений адреса теперь отсортирован по **Действует с**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Запросы на отпуск должны разрешить удаления из Common Data Service в Talent (376999)

При этом изменении запросы на отпуск "черновик" и "отменено" могут быть удалены из Common Data Service, а затем удалены из Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Удаление кодов дохода разрешено, когда сотруднику присваивается один и тот же код дохода (371792)

В этом выпуске необходимо сначала удалить код дохода у сотрудника, прежде чем удалить код дохода из системы.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Рабочий процесс отпуска и отсутствия с двумя этапами утверждения завершается ошибкой (391116)

При этом изменении рабочий процесс отпуска и отсутствия продолжается на всех этапах, когда для запроса настроено несколько этапов утверждения.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Дата выпуска не синхронизируется с Common Data Service при обновлении или вводе в Talent (397361)

Это изменение исправляет проблему, когда дата выпуска для записей **Идентификация лица** не синхронизируются с Common Data Service из Talent.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Ошибка круговой ссылки иерархии при назначении менеджера на должность (386659)

Это изменение исправляет уникальный сценарий, при котором появляется ошибка круговой ссылки при назначении нового менеджера на должность.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Объекты Common Data Service, которые сейчас поддерживают настраиваемые поля

Следующие объекты Common Data Service теперь поддерживают настраиваемые поля:

| Название | Объект |
| --- | --- |
| Выплаты по банковскому счету | cdm_bankaccountdisbursement |
| Частота расчета льгот | cdm_benefitcalculationfrequency |
| Частоты расчета для платежного периода для льгот | cdm_benefitcalculationfrequencypayperiod |
| Ставка расчета льгот | cdm_benefitcalculationrate |
| Сведения о ставке расчета льгот | cdm_benefitcalculationratedetail |
| Параметр льготы | cdm_benefitoption |
| План льготы | cdm_benefitplan (не включено для поддержки настраиваемых полей) |
| Тип льготы | cdm_benefittype |
| Календарь бизнес-процесса | cdm_businessprocesscalendar |
| Назначение группы бизнес-процессу | cdm_businessprocessgroupassignment |
| Группа задач библиотеки бизнес-процессов | cdm_businessprocesslibrarytaskgroup |
| Стадия бизнес-процесса | cdm_businessprocessstage |
| Заголовок шаблона контрольного списка | cdm_businessprocesstemplateheader |
| Задача шаблона контрольного списка | cdm_businessprocesstemplatetask |
| Организация | cdm_company |
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
| Отдел | cdm_department |
| Занятость | cdm_employment |
| Этническое происхождение | cdm_ethnicorigin |
| Мероприятие фиксированной компенсации | cdm_fixedcompensationevent |
| Должность | cdm_job |
| Функциональные обязанности | cdm_jobfunction |
| Позиция | cdm_jobposition |
| Тип должности | cdm_jobtype |
| Язык | cdm_language |
| Банковская проводка отпуска | cdm_leavebanktransaction |
| Регистрация отпуска | cdm_leaveenrollment |
| План отпусков | cdm_leaveplan |
| Запрос на отпуск | cdm_leaverequest |
| Сведения запроса отпуска | cdm_leaverequestdetail |
| Тип отпуска | cdm_leavetype |
| Код основания типа отпуска | cdm_leavetypereasoncode |
| Цикл оплаты | cdm_paycycle |
| Платежный период | cdm_payperiod |
| Код дохода в зарплате | cdm_payrollearningcode |
| Выпускающее агентство по идентификации лиц | cdm_personidentificationissuingagency |
| Тип позиции | cdm_positiontype |
| Назначение работника на позицию | cdm_positionworkerassignmentmap |
| Код основания | cdm_reasoncode |
| Тип навыка | cdm_skilltype |
| Налоговый регион | cdm_taxregion |
| Положение о передаче прав на льготы | cdm_vestingrule |
| Статус ветерана | cdm_veteranstatus |
| Рабочий календарь | cdm_workcalendar |
| Календарный день работы | cdm_workcalendarday |
| Праздничный день в рабочем календаре |cdm_workcalendarholiday |
| Строка праздничного дня в рабочем календаре | cdm_workcalendarholidayline |
| Интервал рабочего времени | cdm_workcalendartimeinterval (не включено для поддержки настраиваемых полей) |
| Рабочий | cdm_worker |
| Адрес работника | cdm_workeraddress |
| Банковский счет работника | cdm_workerbankaccount |
| Фиксированная компенсация для работника | cdm_workerfixedcompensation |
| Личные данные работника | cdm_workerpersonaldetail |
| Идентификационный код работника | cdm_workerpersonidentificationnumber |
| Идентификационный тип работника | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>В режиме предварительного просмотра

Функции предварительной версии доступны только в средах **Песочница**.

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.
