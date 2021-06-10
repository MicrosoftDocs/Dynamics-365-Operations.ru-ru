---
title: Позиция запроса на набор сотрудников
description: В этом разделе описывается сущность позиции запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: a709b8fb2f22c0e7a81399349cacbcfbfc91c8b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059264"
---
# <a name="recruiting-request-position"></a>Позиция запроса на набор сотрудников

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность позиции запроса на набор сотрудников для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>описание

Описывает должность или должности для заполнения для запроса на подбор персонала. Добавление должности в запрос набора персонала не является обязательным. Свойства должности доступны только для чтения, так как свойства должности для запроса на набор сотрудников не должны отличаться от свойств в главной записи должности. Если необходимо изменить свойства, это следует сделать в главной записи должности перед добавлением должности в запрос набора персонала.

### <a name="json-representation"></a>Представление JSON
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности должности запроса на набор персонала**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Только для чтения<br>Требуется |    Создаваемый системой идентификатор записи должности запроса на набор сотрудников. |
| **ИД запроса на набор сотрудников**<br>mshr_recruitingrequestid<br>*Строка* | Однократная запись<br>Требуется | Уникальный идентификатор запроса по набору сотрудников, доступный для чтения пользователем. |
| **Значение ИД запроса на набор сотрудников**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmrecruitingrequestentityid сущности mshr_hcmrecruitingrequestentity | Создаваемый системой идентификатор запроса на набор сотрудников, которому назначена должность. |
| **Код должности**<br>mshr_positionid<br>*Строка* | Однократная запись<br>Требуется | Уникальный идентификатор должности в понятном для пользователя виде. |
| **Значение кода должности**<br>_mshr_fk_position_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmpositionv2entityid сущности mshr_hcmpositionv2entity | Создаваемый системой идентификатор должности. |
| **Описание**<br>mshr_description<br>*Строка* | Только для чтения<br>Требуется | Описание должности. |
| **Код типа должности**<br>mshr_positiontypeid<br>*Строка* | Только для чтения<br>Необязательный | Понятный пользователю уникальный идентификатор типа должности для этой должности. |
| **Значение кода типа должности**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmpositiontypeentityid сущности mshr_hcmpositiontypeentity | Созданный системой уникальный идентификатор типа должности для данной должности. |
| **Состояние**<br>mshr_status<br>Набор параметров *RecruitingRequestPositionStatus* | Чтение/запись<br>Требуется | Статус должности для запроса на набор сотрудников. |
| **Номер подразделения**<br>mshr_departmentnumber<br>*Строка* | Только для чтения<br>Необязательный<br> | Номер подразделения для должности. |
| **Значение кода подразделения**<br>_mshr_fk_department_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_omdepartmententityid сущности mshr_omdepartmententity | Созданный системой уникальный идентификатор подразделения для должности. |
| **ИД вышестоящей должности**<br>mshr_reportstopositionid<br>*Строка* | Только для чтения<br>Требуется | Доступный для чтения пользователем идентификатор должности, которой подчинается должность, на которую производится набор, в организационной иерархии. |
| **Значение ИД вышестоящей должности**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmpositionv2entityid сущности mshr_hcmpositionv2entity | Создаваемый системой код должности, которой подчинается должность, на которую производится набор. |
| **Табельный номер руководителя**<br>mshr_reportstopersonnelnumber<br>*Строка* | Только для чтения<br>Требуется | Идентификатор работника, которому будет подчиняться нанятый кандидат. |
| **Значение ИД вышестоящего работника**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmworkerbaseentityid сущности mshr_hcmworkerbaseentity | Созданный системой идентификатор работника, которому будет подчиняться нанятый кандидат. |
| **Финансовая аналитика**<br>mshr_financialdimension<br>*Строка* | Только для чтения<br>Необязательный | Финансовая аналитика (например, центр затрат), назначенная данной должности. Финансовая аналитика назначается для каждой должности в каждом юридическом лице. Центры затрат, определенные в аналитиках, доступны через сущность mshr_dimattributeomcostcenterentity. |
| **ИД области данных**<br>mshr_dataareaid<br>*Строка* | Чтение/запись<br>Необязательный | Указывает юридическое лицо (компанию) для должности запроса на набор сотрудников. |
| **Значение ИД области данных**<br>_mshr_dataareaid_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: cdm_companyid сущности cdm_company | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию) для должности запроса на набор сотрудников. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Объединение значения запроса на набор сотрудников и кода должности в качестве другого метода для уникальной идентификации записи. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]