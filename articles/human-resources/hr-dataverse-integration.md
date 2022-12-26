---
title: Настройка интеграции с таблицами Dataverse
description: Эта статья описывает интеграцию между Microsoft Dynamics 365 Human Resources и Dataverse.
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838631"
---
# <a name="configure-integration-with-dataverse-tables"></a>Настройка интеграции с таблицами Dataverse

>[!Important]
>Функции, перечисленные в этой статье, в настоящее время доступны для клиентов в модуле Dynamics 365 Human Resources в инфраструктуре для управления финансами и операциями. 


Чтобы интегрировать Microsoft Dynamics 365 Human Resources с Dataverse, можно использовать [интегратор данных](/powerapps/administrator/data-integrator). Шаблон передачи из Human Resources в Dataverse позволяет передавать данные для заданий, должностей, работников и другого из Human Resources в Dataverse, а также из Dataverse в Human Resources, создавая записи и обеих системах.

## <a name="system-requirements-for-human-resources"></a>Требования к системе для Human Resources

Для интеграционного решения требуются следующие версии Human Resources и Dynamics 365 Finance: 

- Dynamics 365 Finance версии 7.2 или более новая версия
- Среда Dynamics CRM, в которой была создана база данных и разрешены приложения Dynamics 365

## <a name="template-and-tasks"></a>Шаблон и задачи

Выполните следующие шаги для доступа к шаблону передачи данных из Human Resources в Finance.

1. Откройте [Центр администрирования Power Apps](https://admin.powerapps.com/). 
2. В среде выберите **Приложения Dynamics 365**, затем выберите **App Source** на панели инструментов.
3. Чтобы установить шаблон, выполните поиск "Human Resources с двойной записью" или перейдите непосредственно на следующий адрес: <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>.
3. После завершения установки откройте Dynamics 365 Finance.
4. Откройте рабочую область **Управление данными**. 
5. Выберите **Двойная запись**. 
6. Выполните процедуру для связи среды по крайней мере с одной компанией в организации. 
7. После завершения настройки ссылки на среду Dataverse выберите **Применить решение**. Решение применяется, и сопоставления устанавливаются в приложение интегратора.

## <a name="template-mappings"></a>Сопоставления шаблона

В следующих таблицах сопоставления шаблонов имя задачи указывает объекты, которые используются в каждом приложении. Finance расположено слева, Dataverse — справа.

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>Расходные операции банковского счета (двойная запись) в расход банковского счета

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| СУММА                         | cdm\_amount                                         |
| ПРИОРИТЕТ                       | cdm\_disbursementpriority                           |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| ОСТАТОК                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>Сведения о ставке расчета льгот (двойная запись) в сведения о ставке расчета льгот

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| ДЕЙСТВУЕТ                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| ИСТЕЧЕНИЕ СРОКА ДЕЙСТВИЯ                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| НАИМЕНОВАНИЕ                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>Заголовок расчета льгот в ставку расчета льгот

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>Вариант льготы в вариант льготы

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>Тип льготы в тип льготы

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>Бизнес-календарь в календарь бизнес-процессов

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| НАИМЕНОВАНИЕ                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>Бизнес-процесс в заголовок бизнес-процесса

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| СТАТУС                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>Группа задач библиотеки бизнес-процессов в группу задач библиотеки бизнес-процессов

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>Этап бизнес-процесса в этап бизнес-процесса

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>Задача бизнес-процесса в задачу бизнес-процесса

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| ИНСТРУКЦИИ                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| СТАТУС                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>Шаблон бизнес-процесса в заголовок шаблона контрольного списка

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>Задача шаблона бизнес-процесса в задачу шаблона контрольного списка

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| ОПИСАНИЕ                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| ИНСТРУКЦИИ                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>Частота расчета в частоту расчета льгот

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>Частота расчета для платежного периода в частота расчета льгот для платежного периода

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>Календарь в рабочий календарь

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>Таблица действий по фиксированной компенсации в событие фиксированной компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ДЕЙСТВИЕ                         | cdm\_name                                           |
| АКТИВНЫЙ                         | cdm\_isactive                                       |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ТИП                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>План фиксированной компенсации в план фиксированной компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ПЛАН                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ТИП                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| ВАЛЮТА                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>Сетки компенсаций в сетку компенсаций

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| ТИП                           | cdm\_type                                           |
| ВАЛЮТА                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>Функциональные обязанности компенсации в функциональные обязанности

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>Типы должности компенсации в тип должности

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>Частота компенсационных выплат в частоту компенсационных выплат

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| ПЕРИОД                         | cdm\_period                                         |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>Регионы компенсаций в регион компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| МЕСТОНАХОЖДЕНИЕ                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>План переменной компенсации версии 2 в план переменной компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>Тип переменной компенсации в тип плана переменной компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| ТИП                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>Правила по компенсации по положению о передаче прав на льготы в положение о передаче прав на льготы

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| ПРИМЕЧАНИЕ                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>Подразделение версии 2 в подразделение

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>Налоговый регион с двойной записью в налоговый регион

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ГОРОД                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| ОКРУГ                         | cdm\_county                                         |
| РЕГИОН                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>Идентификация сотрудника с двойной записью в личный идентификационный номер сотрудника

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>Структура компенсации в структуру компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| СУММА                         | cdm\_amount                                         |
| СЕТКА                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>Код дохода в код дохода для зарплаты

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>Фиксированная компенсация сотрудникам в фиксированную компенсацию работникам

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| ТИП                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| ПЛАН                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| ДЕЙСТВИЕ                         | cdm\_eventid.cdm\_name                               |
| ШАГ                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>Занятость по компании в занятость

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>Этническое происхождение в этническое происхождение

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>Назначение группы в назначение группы бизнес-процессу

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>Тип идентификации в тип личной идентификации работника

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>Выпускающее агентство в агентство, выпускающее средства идентификации пользователей

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ЭЛ. ПОЧТА                          | cdm\_email                                          |
| ДОБАВОЧНЫЙ                      | cdm\_extension                                      |
| ФАКС                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| НАИМЕНОВАНИЕ                           | cdm\_description                                    |
| ПЕЙДЖЕР                          | cdm\_pager                                          |
| SMS                            | cdm\_sms                                            |
| ТЕЛЕФОН                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>Позиции должностей с двойной записью в позицию должности

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| АКТИВАЦИЯ                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| ОПИСАНИЕ                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| RETIREMENT                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>Задания с двойной записью в задание

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>Коды языков в язык

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>Банковская проводка отпуска и отсутствия V2 в банковскую проводку отпуска

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| СУММА                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>Регистрация отпусков и отсутствий V2 в регистрацию отпусков

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>План отпусков и отсутствий V2 в план отпусков

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>Тип отпуска и отсутствия в тип отпуска

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| ТИП                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>Код основания типов отпусков и отсутствия в код основания типа отпуска

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>Сведения о запросе на отгул в сведения запроса отпуска

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| СУММА                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| ТИП                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>Заголовок запроса на отгул в запрос отпуска

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| СТАТУС                         | cdm\_status                                         |
| КОММЕНТАРИЙ                        | cdm\_comment                                        |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>Уровни в уровень компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ТИП                           | cdm\_type                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| УРОВЕНЬ                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>Заголовок процесса адаптации в заголовок процесса адаптации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>Цикл оплаты в цикл оплаты

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>Платежный период в платежный период

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| СТАТУС                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>Сведения о зарплате для должностей в сведения о должности для начисления зарплаты

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>Двойная запись аналитик должности по умолчанию в аналитику должности

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>Тип позиции в тип позиции

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| КЛАССИФИКАЦИЯ                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>Назначения работников на должности V2 в назначение работника на должность

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>Коды причин в код причины

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>Строка настройки опорных точек (двойная запись) в строку настройки опорных точек компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ОПИСАНИЕ                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>Настройки точек отсчета в настройку опорной точки компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ТИП                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>Типы навыков в тип навыков

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |

### <a name="titles-to-title"></a>Заголовки в заголовок

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>Уровень переменной компенсации V2 в уровень плана переменной компенсации

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>Статус ветерана в статус ветерана

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>Регистрации в рабочем календаре в регистрацию в рабочем календаре

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>Праздничный день в рабочем календаре в праздничный день в рабочем календаре

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| Идентификатор                             | cdm\_name                                           |
| ОПИСАНИЕ                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>Строка праздничного дня в рабочем календаре в строку праздничного дня в рабочем календаре

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| НАИМЕНОВАНИЕ                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>Работник в работника

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| GENDER                         | cdm\_gender                                         |
| ДАТА РОЖДЕНИЯ                      | cdm\_birthdate                                      |
| НАИМЕНОВАНИЕ                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>Банковские счета работников в банковский счет работника

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| ЭЛ. ПОЧТА                          | cdm\_email                                          |
| ДОБАВОЧНЫЙ                      | cdm\_extension                                      |
| ФАКС                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| ТЕЛЕФОН                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| НАИМЕНОВАНИЕ                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>Личные данные работника в личные данные работника

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| ДАТА РОЖДЕНИЯ                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| GENDER                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| ОБРАЗОВАНИЕ                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>Двойная запись почтовых адресов работников в адрес работника

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ТАБЕЛЬНЫЙ НОМЕР                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| ДЕЙСТВУЕТ                      | cdm\_effectivedate                                  |
| ИСТЕЧЕНИЕ СРОКА ДЕЙСТВИЯ                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>Рабочее время в интервал рабочего времени

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>Рабочее время в день рабочего календаря

| Сущность Finance                 | Таблица Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>Соображения по интеграции

- Все изменения, вносимые в данные в любой из этих систем, будут подвергнуты проверке другой системой. В случае сбоя данные не будут записаны ни в одной из систем. 
- Для всех операций записи используется задание данных по умолчанию (если в Finance используется пользовательская логика).
- Приложение интегратора с двойной записью использует ключи интеграции для сопоставления между двумя системами. Иногда сложно выбрать правильный ключ интеграции, особенно если несколько ключей интеграции удовлетворяют требованиям. Чтобы помочь с этим выбором, в следующей таблице перечислены рекомендуемые ключи интеграции для сопоставлений.

| Таблица Dataverse                          | Ключи интеграции |
|------------------------------------------|------------------|
| Выплаты по банковскому счету                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Частота расчета льгот            | cdm\_name |
| Частоты расчета для платежного периода для льгот | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_name |
| Ставка расчета льгот                 | cdm\_name |
| Сведения о ставке расчета льгот          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_name |
| Параметр льготы                           | cdm\_name |
| Тип льготы                             | cdm\_name |
| Календарь бизнес-процесса                | cdm\_name |
| Назначение группы бизнес-процессу        | cdm\_name |
| Заголовок бизнес-процесса                  | cdm\_processid |
| Группа задач библиотеки бизнес-процессов      | cdm\_processtype, cdm\_name |
| Стадия бизнес-процесса                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| Задача бизнес-процесса                    | cdm\_taskid |
| Бизнес-единица                            | |
| Заголовок шаблона контрольного списка                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| Задача шаблона контрольного списка                  | cdm\_taskid |
| Компания                                  | cdm\_companycode |
| Фиксированный план компенсации                  | cdm\_name, cdm\_company.cdm\_companycode |
| Сетка компенсации                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| Уровень компенсации                       | cdm\_name |
| Частота компенсационных выплат               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Настройка опорной точки компенсации       | cdm\_name, cdm\_companyid.cdm\_companycode |
| Линия настройки опорных точки компенсации  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| Регион компенсации                      | cdm\_name |
| Структура компенсации                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| План переменной компенсации               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Уровень плана переменной компенсации         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| Тип плана переменной компенсации          | cdm\_name, cdm\_companyid.cdm\_companycode |
| Валюта                                 | isocurrencycode |
| Отдел                               | cdm\_departmentnumber |
| Занятость                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Этническое происхождение                            | cdm\_name |
| Мероприятие фиксированной компенсации                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| Должность                                      | cdm\_name |
| Функциональные обязанности                             | cdm\_name |
| Должность                             | cdm\_jobpositionnumber |
| Аналитика должности                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| Тип вакансии                                 | cdm\_name |
| Язык                                 | cdm\_name |
| Банковская проводка отпуска                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Регистрация отпуска                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| План отпусков                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Запрос на отпуск                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| Сведения запроса отпуска                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| Тип отпуска                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| Код основания типа отпуска                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| Заголовок процесса адаптации                   | cdm\_processheaderid.cdm\_processid |
| Cтруктурное подразделение                             | |
| Цикл оплаты                                | cdm\_name |
| Платежный период                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| Код дохода по зарплате                     | cdm\_name |
| Сведения о должности для начисления зарплаты                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| Агентство, выпускающее средства идентификации пользователей     | cdm\_name |
| Тип позиции                            | cdm\_name |
| Назначение работника на должность               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| Код основания                              | cdm\_name |
| Тип навыка                               | cdm\_name |
| Налоговый регион                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| Команда                                     | azureactivedirectoryobjectid, membershiptype |
| Заголовок                                    | cdm\_name |
| Пользователь                                     | azureactivedirectoryobjectid |
| Положение о передаче прав на льготы                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| Статус ветерана                           | cdm\_name |
| Рабочий календарь                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| Календарный день работы                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Регистрация в рабочем календаре                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| Праздничный день в рабочем календаре                    | cdm\_name |
| Строка праздничного дня в рабочем календаре               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| Интервал рабочего времени              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Работник                                   | cdm\_workernumber |
| Адрес работника                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| Банковский счет работника                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| Фиксированная компенсация работника                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| Идентификационный код работника      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| Идентификационный тип работника        | cdm\_name |
| Личные данные работника                   | cdm\_workerid.cdm\_workernumber |
