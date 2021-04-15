---
title: Навык физического лица
description: В этом разделе описывается сущность навыка физического лица для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be2d024de22c4e255cf9163010149818256a3427
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798017"
---
# <a name="person-skill"></a>Навык физического лица

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность навыка физического лица для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersonskillentity

## <a name="description"></a>описание

Эта сущность описывает навыки кандидата.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности навыка физического лица**<br>mshr_hcmpersonskillentityid<br>*GUID* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор записи сущности. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется |   ИД связанной записи субъекта (физического лица). |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **Удостоверяющий**<br>mshr_certifier<br>*Строка* | Чтение/запись<br>Необязательный | Табельный номер сотрудника, который сертифицирован для данного навыка. |
| **Значение ИД удостоверяющего**<br>_mshr_fk_certifier_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmworkerentityid сущности mshr_hcmworkerentity | Созданный системой уникальный идентификатор записи работника для работника, который сертифицировал навык. |
| **ИД навыка**<br>mshr_skillid<br>*Строка* | Чтение/запись<br>Требуется | Идентификатор навыка, определенный в модуле Human Resources. |
| **Значение ИД навыка**<br>_mshr_fk_skill_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmskillentityid сущности mshr_hcmskillentity | Создаваемый системой идентификатор выбранного навыка. |
| **Опыт в годах**<br>mshr_yearsofexperience<br>*Десятичн.* | Чтение/запись<br>Необязательный | Опыт в годах для данного навыка кандидата. |
| **ИД оценки**<br>mshr_ratingid<br>*Строка* | Чтение/запись<br>Требуется | Тип шкалы оценки. Для этой сущности значением является **Навыки**. |
| **Тип уровня**<br>mshr_leveltype<br>*Набор параметров mshr_hrmskillleveltype* | Чтение/запись<br>Требуется | Классификация типов для уровня, назначенного данному навыку. |
| **ИД уровня**<br>mshr_levelid<br>*Строка* | Чтение/запись<br>Требуется | ИД уровня рейтинга, который имеет кандидат для этого навыка. |
| **Значение ИД уровня рейтинга**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmratinglevelentityid сущности mshr_hcmratinglevelentity | Создаваемый системой идентификатор уровня рейтинга. |
| **Дата уровня**<br>mshr_leveldate<br>*Дата и время* | Чтение/запись<br>Требуется | Дата, когда был оценен уровень навыка кандидата. |
| **Экзаминатор уровня рейтинга**<br>mshr_ratinglevelexaminer<br>*Строка* | Чтение/запись<br>Необязательный | Табельный номер сотрудника, который оценил кандидата. |
| **Значение ИД экзаминатора уровня рейтинга**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmworkerentityid сущности mshr_hcmworkerentity | Созданный системой идентификатор работника, который проверил уровень навыка кандидата. |
| **Проверено**<br>mshr_verified<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Указывает, был ли проверен оцененный уровень навыка. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле для, использования в качестве идентификатора записи сущности. Комбинация номера субъекта, типа уровня, ИД навыка и даты уровня. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]