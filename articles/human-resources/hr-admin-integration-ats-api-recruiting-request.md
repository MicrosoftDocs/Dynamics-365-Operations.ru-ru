---
title: Запрос на набор сотрудников
description: В этом разделе описывается сущность запроса на набор сотрудников для Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b89d257e3874ad7395c0a2c02f259c2f063aa8d0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500630"
---
# <a name="recruiting-request"></a>Запрос на набор сотрудников

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность запроса на набор сотрудников для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequestentity

### <a name="description"></a>описание

Описывается запрос на набор персонала для должности.

### <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД запроса на набор сотрудников**<br>mshr_recruitingrequestid<br>*Строка* | Только для чтения<br>Требуется<br>Создано системой | Понятный для пользователя уникальный идентификатор для запроса, который отображается в приложении HR. Номерная серия. |
| **ИД сущности запроса на набор сотрудников**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой | Создаваемое системой значение идентификатора GUID, чтобы однозначно определить запрос на набор сотрудников. |
| **ИД области данных**<br>mshr_dataareaid<br>*Строка* | Чтение/запись<br>Необязательный<br> | Указывает юридическое лицо (компанию) для запроса на набор сотрудников. |
| **Значение ИД области данных**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Только для чтения<br>Необязательный<br>Внешний ключ: cdm_companyid сущности cdm_company | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию) для запроса на набор сотрудников. |
| **Табельный номер специалиста по комплектации штата**<br>mshr_hiringmanagerpersonnelnumber<br>*Строка* | Чтение/запись<br>Необязательный | Табельный номер менеджера по найму на работу, связанного с этим запросом на набор сотрудников. |
| **Значение идентификатора менеджера по найму**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmworkerbaseentityid сущности mshr_hcmworkerbaseentity | Созданное системой значение GUID для идентификации менеджера, связанного с запросом на набор сотрудников. |
| **Номер субъекта специалиста по найму**<br>mshr_recruiterpartynumber<br>*Строка* | Чтение/запись<br>Необязательный | Номер лица (субъекта), выбранного для данного запроса. |
| **Значение ИД специалиста по найму**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданное системой значение GUID для идентификации специалиста по найму, связанного с запросом на набор сотрудников. |
| **Состояние**<br>mshr_status<br>Набор параметров *RecruitingRequestStatus* | Чтение/запись<br>Требуется<br> | Указывает статус запроса на набор сотрудников. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описывает запрос. |
| **ИД местонахождения запроса на набор сотрудников**<br>mshr_recruitingrequestlocationid<br>*Строка* | Чтение/запись<br>Необязательный | Понятный пользователю уникальный идентификатор местоположения должности, связанного с данным запросом. |
| **Значение ИД местонахождения набора сотрудников**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmrecruitingrequestlocationentityid сущности mshr_hcmrecruitingrequestlocationentity | Созданное системой значение GUID для идентификации местоположения запроса набора сотрудников, выбранного для запроса. |
| **Комментарии**<br>mshr_comments<br>*Строка* | Чтение/запись<br>Необязательный | Комментарии о запросе для использования менеджерами и специалистами по найму. |
| **Код задания**<br>mshr_jobid<br>*Строка* | Однократная запись<br>Требуется |   Понятный пользователю уникальный идентификатор должности, общих для всех позиций, связанных с данным запросом. |
| **Значение ИД должности**<br>_mshr_fk_job_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmjobentityid сущности mshr_hcmjobentity | Созданный системой уникальный идентификатор должности, общих для всех позиций, связанных с запросом на набор сотрудников. |
| **ИД заголовка**<br>mshr_titleid<br>*Строка* | Только для чтения<br>Требуется | Понятный пользователю уникальный идентификатор названия должности, связанной с данным запросом. |
| **Значение ИД заголовка**<br>_mshr_fk_title_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmtitleid сущности mshr_hcmtitleentity entity | Созданный системой уникальный идентификатор названия должности, выбранной для запроса на набор сотрудников. |
| **Код должностных обязанностей**<br>mshr_jobfunctionid<br>*Строка* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_jobfunctionid сущности mshr_hcmjobfunctionentity | Понятный пользователю уникальный идентификатор должностных обязанностей, связанных с данным запросом. |
| **Эквивалент полной занятости по умолчанию**<br>mshr_defaultfulltimeequivalency<br>*Двойной* | Только для чтения<br>Требуется | Эквивалент полной занятости для должности, где 1,0 представляет работника с полной занятостью. |
| **Категория нормативных должностей**<br>mshr_regulatoryjobcategory<br>Набор параметров *RegulatoryJobCategory* | Только для чтения<br>Необязательный | Категория должности EEO для должностных обязанностей, выбранных для должности. Допустимые значения, включенные в набор параметров HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **ИД типа вакансии**<br>mshr_jobtypeid<br>*Строка* | Только для чтения<br>Необязательный | Тип вакансии, связанный с должностью. Типы вакансий представляют собой определяемые пользователем значения, доступные в сущности mshr_hcmjobtypeentity. |
| **Значение ИД вакансии**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmjobtypeentityid сущности mshr_hcmjobtypenentity | Созданный системой уникальный идентификатор типа вакансии, связанного с вакансией для запроса на набор сотрудников. |
| **Статус "Освобожденный"**<br>mshr_exemptstatus<br>Набор параметров *JobExemptStatus* | Только для чтения<br>Необязательный | Статус исключения FLSA на основе типа вакансии. |
| **Ожидаемая дата начала**<br>mshr_estimatedstartdate<br>*Дата* | Чтение/запись<br>Требуется | Предполагаемая дата начала, с которой кандидат может приступить к работе. |
| **Внешнее описание**<br>mshr_externaldescription<br>*Строка* | Чтение/запись<br>Необязательный | Предназначенное для кандидата описание вакансии/должности. | 
| **Нижний порог компенсации**<br>mshr_compensationlowthreshold<br>*Двойной* | Чтение/запись<br>Необязательный | Нижняя граница для уровня компенсации. |
| **Контрольная точка компенсации**<br>mshr_compensationcontrolpoint<br>*Двойной* | Чтение/запись<br>Необязательный | Контрольная точка для уровня компенсации. |
| **Верхний порог компенсации**<br>mshr_compensationhighthreshold<br>*Двойной* | Чтение/запись<br>Необязательный | Верхняя граница для уровня компенсации. |
| **Уровень компенсации**<br>mshr_compensationlevelid<br>*Строка* | Чтение/запись<br>Необязательный | Уровень компенсации для должности. Должность может быть настроена с несколькими уровнями компенсации. Этот атрибут указывает выбранный уровень компенсации должности для данного запроса. |
| **Код компенсации для должности**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmjobcompensationentityid сущности mshr_hcmjobcompensationentity | Созданный системой уникальный идентификатор для уровня компенсации, связанного с вакансией для запроса на набор сотрудников. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
