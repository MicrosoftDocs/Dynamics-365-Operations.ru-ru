---
title: Образование физического лица
description: В этой статье описывается сущность "Образование физического лица" для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
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
ms.openlocfilehash: 0fbbb467852d2aeb070c7732c9aa3108fd504de0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893913"
---
# <a name="person-education"></a>Образование физического лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Образование физического лица" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersoneducationentity

## <a name="description"></a>описание

Эта сущность содержит историю образования физического лица, которое является кандидатом. Образование связано с записью сотрудника, позволяющей связывать образование с любыми другими ролями, созданными для физического лица, в дополнение к записи кандидата (работник, подрядчик и так далее).

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности образования физического лица**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор записи сущности образования физического лица. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется | Уникальный идентификатор записи субъекта (физического лица) для кандидата. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Уникальный код, создаваемый системой для записи физического лица кандидата. |
| **Основа кредитов**<br>mshr_creditbasis<br>*Набор параметров mshr_hcmeducationcreditbasis* | Чтение/запись<br>Необязательный | Основа кредитов образовательной ученой степени. |
| **Кредитов завершено**<br>mshr_creditscompleted<br>*Десятичн.* | Чтение/запись<br>Необязательный | Число кредитов, выполненных для образования. |
| **Заработанные кредиты**<br>mshr_creditsearned<br>*Десятичн.* | Чтение/запись<br>Необязательный | Количество кредитов, заработанных для записи по образованию для степени в ходе выполнения. |
| **Требуются кредиты**<br>mshr_creditsneeded<br>*Десятичн.* | Чтение/запись<br>Необязательный | Количество кредитов, необходимое для степени в ходе выполнения. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Необязательный | Описание степени кандидата. |
| **ИД уровня образования**<br>mshr_educationlevelid<br>*Строка* | Чтение/запись<br>Необязательный | Идентификатор уровня образования. | 
| **Значение ИД уровня образования**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmeducationdegreeentityid сущности mshr_hcmeducationdegreeentity | Созданный системой идентификатор для записи образовательной степени. Этот идентификатор предоставляет степени и уровни образования, определенные для организации. |
| **ИД образовательной дисциплины**<br>mshr_educationdisciplineid<br>*Строка* | Чтение/запись<br>Требуется<br>Внешний ключ: EducationDiscipline | Идентификатор образовательной дисциплины. |
| **Значение ИД образовательной дисциплины**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmeducationdisciplineentityid сущности mshr_hcmeducationdisciplineentity | Уникальный код, создаваемый системой для образовательной дисциплины записи образования. |
| **Дополнительная специализация**<br>mshr_secondaryemphasis<br>*Строка* | Чтение/запись<br>Необязательный | Дополнительная специализация полученной ученой степени. |
| **ИД образовательного учреждения**<br>mshr_educationinstitutionid<br>*Строка* | Чтение/запись<br>Необязательный | Идентификатор образовательного учреждения, в котором проходило обучение. |
| **Значение ИД образовательного учреждения**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmeducationinstitutionentityid сущности mshr_hcmeducationinstitutionentity | Создаваемый системой идентификатор образовательного учреждения. |
| **Дата начала**<br>mshr_startdate<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата начала образования для полученной степени. |
| **Дата окончания**<br>mshr_enddate<br>*Дата и время* | Чтение/запись<br>Требуется | Дата выпуска учетных данных. |
| **Длительность**<br>mshr_duration<br>*Десятичн.* | Чтение/запись<br>Необязательный | Длительность времени для записи образования. |
| **Ед. изм. продолжительности**<br>mshr_durationunit<br>*Набор параметров mshr_periodunit* | Чтение/запись<br>Необязательный | Единица времени, связанная с длительностью записи образования. |
| **Средний балл**<br>mshr_gradepointaverage<br>*Десятичн.* | Чтение/запись<br>Необязательный | Средний балл, полученный за степень. |
| **Шкала оценки**<br>mshr_gradescale<br>*Строка* | Чтение/запись<br>Необязательный | Шкала, используется для среднего балла. |
| **Основание**<br>mshr_notes<br>*Строка* | Чтение/запись<br>Необязательный | Примечания для использования сотрудником или менеджером по найму персонала. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле, используемое в качестве другого первичного идентификатора записи сущности. Комбинация номера сущности, кода дисциплины образования, кода учебного заведения и кода уровня образования. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
