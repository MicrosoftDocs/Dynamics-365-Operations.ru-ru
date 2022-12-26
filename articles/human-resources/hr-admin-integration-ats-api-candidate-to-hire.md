---
title: Кандидат для приема на работу
description: В этой статье описывается сущность "Кандидат для приема на работу" для Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c243bdf81beabe9e1ee429227a6edf4d4864bfb
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832007"
---
# <a name="candidate-to-hire"></a>Кандидат для приема на работу


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Кандидат для приема на работу" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmcandidatetohireentity

## <a name="description"></a>описание

Эта сущность предоставляет сведения о кандидате, используемые для создания сотрудника в Dynamics 365 Human Resources. Она используется для чтения всех записей кандидатов и создания записей внутренних и внешних кандидатов, позволяя создавать личные сведения для нового кандидата.

При создании записи внешнего кандидата, который будет являться новой записью физического лица в системе, не следует определять номер субъекта (человека) при разноски новой записи кандидата. Новая запись сущности физического лица создается с новой записью кандидата.

При создании записи внутреннего кандидата (кандидата на должность, которая уже имеет запись сотрудника в компании), определите номер субъекта (лица) записи, которая уже существует для физического лица для свойства mshr_partynumber в записи кандидата, а не определяйте личные сведения (такие как имя, пол или дата рождения), которые будут использоваться для создания новой записи о физическом лице.

## <a name="json-representation"></a>Представление JSON

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
            "mshr_militaryserviceenddate": "Date",
            "mshr_militaryservicestartdate": "Date"
        }
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД сущности кандидата для приема на работу**<br>mshr_hcmcandidatetohireentityid<br>GUID | Только для чтения<br>Требуется<br>Создано системой | Созданный системой уникальный идентификатор записи сущности. |
| **ИД кандидата**<br>mshr_candidateid<br>Строка | Только для чтения<br>Требуется<br>Создано системой | Уникальный идентификатор для сущности. |
| **Номер субъекта**<br>mshr_partynumber<br>Строка | Только для чтения<br>Требуется | Номер субъекта (физического лица) в записи физического лица кандидата. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>GUID | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_direpersonentity | Уникальный код, создаваемый системой для записи субъекта (лица) кандидата. |
| **Тип субъекта**<br>mshr_partytype<br>Набор параметров mshr_dirpartytype | Только для чтения<br>Требуется | Тип субъекта записи, определенный в определенном наборе параметров mshr_dirpartytype. Для этой сущности типом всегда будет "Физическое лицо". |
| **ИД запроса на набор сотрудников**<br>mshr_recruitingrequestid<br>Строка | Однократная запись<br>Необязательный | Ссылка на запрос набора сотрудников, который удовлетворен данным кандидатом. |
| **Значение ИД запроса на набор сотрудников**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Чтение/запись<br>Необязательный<br>Внешний ключ: mshr_hcmrecruitingrequestentityid сущности mshr_hcmrecruitingrequestentity | Создаваемый системой уникальный код, запроса на набор сотрудников, который удовлетворяется этим кандидатом. |
| **Код должности**<br>mshr_positionid<br>Строка | Чтение/запись<br>Необязательный | Код должности, для которой рассматривается кандидат. |
| **Значение кода должности**<br>_mshr_fk_position_if_value<br>GUID | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmpositionv2entityid сущности mshr_hcmpositionv2entity | Создаваемый системой идентификатор должности, на которую рассматривается кандидат. |
| **Имя**<br>mshr_firstname<br>Строка | Чтение/запись<br>Требуется | Имя кандидата. |
| **Отчество**<br>mshr_middlename<br>Строка | Чтение/запись<br>Необязательный | Отчество кандидата. |
| **Префикс фамилии**<br>mshr_lastnameprefix<br>Строка | Чтение/запись<br>Необязательный | Префикс фамилии кандидата. |
| **Фамилия**<br>mshr_lastname<br>Строка | Чтение/запись<br>Необязательный | Фамилия кандидата. |
| **Род**<br>mshr_gender<br>Набор параметров mshr_hcmpersongender | Чтение/запись<br>Необязательный | Пол кандидата. |
| **Дата рождения**<br>mshr_birthdate<br>Дата и время | Чтение/запись<br>Необязательный | Дата рождения кандидата. |
| **Код страны гражданства**<br>mshr_citizenshipcountrycode<br>Строка | Чтение/запись<br>Необязательный | Указывает страну, гражданином которой является кандидат. Допустимыми кодами стран являются mshr_logisticaddresscountryregionentity. |
| **Код статуса ветерана**<br>mshr_veteranstatusid<br>Строка | Чтение/запись<br>Необязательный | Указывает статус ветерана для кандидата. |
| **Значение кода статуса ветерана**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmveteranstatusentityid сущности mshr_hcmveteranstatusentity | Созданный системой уникальный идентификатор записи сущности статуса ветерана. |
| **Дата начала воинской службы**<br>mshr_militaryservicestartdate<br>Дата и время | Чтение/запись<br>Необязательный | Дата начала военной службы кандидата. |
| **Дата окончания воинской службы**<br>mshr_militaryserviceenddate<br>Дата и время | Чтение/запись<br>Необязательный | Дата завершения военной службы кандидата. |
| **Инвалид войны**<br>mshr_isdisabledveteran<br>Набор параметров mshr_noyes | Чтение/запись<br>Необязательный | Указывает, имеет ли кандидат отключенный статус ветерана. |
| **Дата доступности**<br>mshr_availabilitydate<br>Дата и время | Чтение/запись<br>Необязательный | Самая ранняя дата, когда кандидат может выйти на работу. |
| **Готов к переезду**<br>mshr_iswillingtorelocate<br>Набор параметров mshr_noyes | Чтение/запись<br>Необязательный | Указывает, готов ли кандидат к переезду ради данной должности. |
| **Комментарии**<br>mshr_comments<br>Строка | Чтение/запись<br>Необязательный | Комментарии для использования специалистом или менеджером по найму персонала. |
| **Результат интеграции заявления**<br>mshr_applcantintegrationresult<br>Набор параметров mshr_applicantintegrationresult | Чтение/запись<br>Требуется | Статус кандидата в процессе найма на работу, связанный с интеграцией. |
| **ИД кода причины отказа в приеме на работу**<br>mshr_donothirereasoncodeid<br>Строка | Чтение/запись<br>Необязательный | Код причины при желании может быть указан, если статус (результат интеграции заявления) имеет значение "Не принят". |
| **Значение ИД кода причины**<br>_mshr_fk_reasoncode_id_value<br>GUID | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmreasoncodeentityid сущности mshr_hcmreasoncodeentity | Создаваемый системой уникальный идентификатор для кода причины **Не принимать на работу**. |
| **ИД области данных**<br>mshr_dataareaid<br>Строка | Чтение/запись<br>Необязательный |  Указывает юридическое лицо (компанию). |
| **Значение ИД области данных**<br>_mshr_dataareaid_id_value<br>GUID | Только для чтения<br>Необязательный<br>Внешний ключ: cdm_companyid сущности cdm_company | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию). |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
