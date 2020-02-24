---
title: Настройка интеграции с Finance
description: В этой статье описываются функции, доступные для интеграции Dynamics 365 Human Resources и Dynamics 365 Finance.
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
ms.openlocfilehash: 2e7070f627654c9eb889f3e0ee27e37681db0502
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010307"
---
# <a name="configure-integration-with-finance"></a>Настройка интеграции с Finance

В этой статье описываются функции, доступные для интеграции Dynamics 365 Human Resources и Dynamics 365 Finance. Шаблон Human Resources в Finance, доступный с помощью [интегратора данных](https://docs.microsoft.com/powerapps/administrator/data-integrator), разрешает поток данных для заданий, должностей и работников. Данные переносятся из Human Resources в Finance. Шаблон не позволяет передавать данные из обратно из Finance в Human Resources. 

![Поток интеграции из Human Resources в Finance](./media/TalentFinOpsFlow.png)

Решение Human Resources в Finance предоставляет следующие типы синхронизации данных. 

- Управление заданиями в Human Resources и их синхронизация из Human Resources в Finance.
- Управление должностями и назначениями на должности в Human Resources и их синхронизация из Human Resources в Finance.
- Управление занятностями в Human Resources и их синхронизация из Human Resources в Finance.
- Управление работниками и адресами работников в Human Resources и их синхронизация из Human Resources в Finance.

## <a name="system-requirements-for-human-resources"></a>Требования к системе для Human Resources
Для интеграционного решения требуются следующие версии Human Resources и Finance: 
- Dynamics 365 Human Resources в Common Data Service.
- Dynamics 365 Finance версии 7.2 или более новая версия.

## <a name="template-and-tasks"></a>Шаблон и задачи

Чтобы открыть шаблон, выполните следующее.
1. Откройте [Центр администрирования Power Apps](https://admin.powerapps.com/). 
1. Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны. Для каждого юридического лица, для которого необходимо выполнить интеграцию в Finance, должен быть создан новый проект.

Следующий шаблон используется для синхронизации записей из Human Resources в Finance.

- **Имя шаблона в интеграции данных:** Human Resources (Human Resources Common Data Service в Finance)

  > [!NOTE]
  > Имя задачи содержит объекты, используемые в каждом приложении. Источник (Human Resources) в левой части, а место назначения (Finance and Operations) справа.

Следующие базовые задачи используются для синхронизации записей из Human Resources в Finance.
- Функциональные обязанности в функциональные обязанности компенсации
- Подразделения в операционные единицу
- Типы должности в тип должности компенсации
- Должности в должности
- Должности в сведения о должности
- Типы позиции в тип позиций
- Позиции должностей в базовую позицию
- Позиций должности в сведения о позиции
- Позиции должности в длительности позиции
- Позиции должности в иерархии позиции
- Работники с работником
- Занятость с занятостью
- Занятость со сведениями о занятости
- Назначение работника позиции с назначениями работника позиции
- Адреса работника с почтовым адресом V2

## <a name="template-mappings"></a>Сопоставления шаблона

### <a name="job-functions-to-compensation-job-function"></a>Функциональные обязанности в функциональные обязанности компенсации

| Объект Common Data Service (источник)                 | Объект Finance and Operations (назначение) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Имя функции)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Подразделения в операционные единицу

| Объект Common Data Service (источник)                           | Объект Finance and Operations (назначение) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Типы должности в тип должности компенсации

| Объект Common Data Service (источник)                   | Объект Finance and Operations (назначение) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Должности в должности

| Объект Common Data Service (источник)                                           | Объект Finance and Operations (назначение)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Должности в сведения о должности

| Объект Common Data Service (источник)                                             | Объект Finance and Operations (назначение) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (тип задания (название типа задания))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (функциональные обязанности (название функциональных обязанностей)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (действительно с)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (действительно до)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent (эквивалент полного времени по умолчанию)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Типы позиции в тип позиций

| Объект Common Data Service (источник)                       | Объект Finance and Operations (назначение) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Позиции должностей в базовую позицию

| Объект Common Data Service (источник)                           | Объект Finance and Operations (назначение) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (номер позиции задания) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Позиций должности в сведения о позиции

| Объект Common Data Service (источник)                                                      | Объект Finance and Operations (назначение)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (номер позиции задания)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (задание (имя))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (подразделение (номер подразделения)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (тип позиции (название))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (доступно для назначения)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (действительно с)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (действительно до)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (эквивалент полного времени)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Позиции должности в длительности позиции

| Объект Common Data Service (источник)                             | Объект Finance and Operations (назначение) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (номер позиции задания)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (рассчитанная активация) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (расчетный выход на пенсию) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hiearchies"></a>Позиции должности в иерархии позиции

| Объект Common Data Service (источник)                                                                           | Объект Finance and Operations (назначение) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (номер позиции задания)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (действительно с)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (действительно до)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Работники с работником
| Объект Common Data Service (источник)                           | Объект Finance and Operations (назначение)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Занятость с занятостью

| Объект Common Data Service (источник)                                             | Объект Finance and Operations (назначение) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Занятость со сведениями о занятости

| Объект Common Data Service (источник)                                             | Объект Finance and Operations (назначение)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (действительно с)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (действительно до)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Назначение работника позиции с назначениями работника позиции

| Объект Common Data Service (источник)                                             | Объект Finance and Operations (назначение)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (номер позиции задания)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (действительно с)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (действительно до)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Адреса работника с почтовым адресом V2

| Объект Common Data Service (источник)                                             | Объект Finance and Operations (назначение)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Соображения по интеграции
При интеграции данных из Human Resources в Finance интеграция попытается выполнить сопоставление записей на основе идентификатора. Если совпадение найдено, данные в Finance будут перезаписаны значениями в Human Resources. Однако если логически они являются разными записями, а один и тот же идентификатор был создан в Human Resources и Finance на основе соответствующей номерной серии, то возникает проблема.

Области, в которых это может произойти: это "работник", использующий номер персонала для выполнения сопоставления, и "должность". Задания не используют номерные серии. В результате, если один и тот же код задания присутствует в Human Resources и Finance, информация Human Resources перезапишет информацию Dynamics 365 Finance. 

Чтобы не допустить возникновения ошибок с повторяющимися идентификаторами, можно либо добавить префикс в [номерную серию](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json), либо установить начальный номер в номерной серии, который находится за пределами диапазона другой системы. 

Идентификатор местоположения, используемый для адреса работника, не является частью номерной серии. При интеграции адреса работника из Human Resources в Finance, если адрес работника уже существует в Finance, может быть создана дублирующаяся запись адреса. 

На следующем рисунке показан пример сопоставления шаблона в интеграторе данных. 

![Сопоставление шаблона](./media/IntegrationMapping.png)


