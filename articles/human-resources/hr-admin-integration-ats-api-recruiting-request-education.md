---
title: Образование в запросе по набору сотрудников
description: В этом разделе описывается сущность образования в запросе на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126082"
---
# <a name="recruiting-request-education"></a>Образование в запросе по набору сотрудников

В этом разделе описывается сущность образования в запросе на набор сотрудников для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>описание

Описывает требования к образованию для RecruitingRequest.

### <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности образования запроса на набор персонала**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Только для чтения<br>Требуется | Создаваемый системой уникальный идентификатор для записи образования в запросе на набор сотрудников. |
| **ИД запроса на набор сотрудников**<br>mshr_recruitingrequestid<br>*Строка* | Однократная запись<br>Требуется | Уникальный идентификатор связанного запроса по набору сотрудников, доступный для чтения пользователем. |
| **Значение ИД запроса на набор сотрудников**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmrecruitingrequestentityid сущности mshr_hcmrecruitingrequestentity | Создаваемый системой уникальный идентификатор связанного запроса на набор сотрудников. |
| **ИД уровня образования**<br>mshr_educationlevelid<br>*Строка* | Однократная запись<br>Требуется | Требуемый уровень образования. |
| **Значение ИД уровня образования**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmeducationlevelentityid сущности mshr_hcmeducationlevelentity | Созданный системой уникальный идентификатор требуемого уровня образования. |
| **Описание уровня образования**<br>mshr_educationleveldescription<br>*Строка* | Только для чтения<br>Требуется | Описание уровня, необходимого для данного навыка. |
| **ИД образовательной дисциплины**<br>mshr_educationdisciplinedescription<br>*Строка* | Однократная запись<br>Требуется | Область образовательной дисциплины. |
| **Значение ИД образовательной дисциплины**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmeducationdisciplineentityid сущности mshr_hcmeducationdisciplineentity | Созданный системой уникальный идентификатор области образовательной дисциплины. |
| **Описание образовательной дисциплины**<br>mshr_educationdisciplinedescription<br>Строка | Только для чтения<br>Требуется | Описание области образовательной дисциплины. |
| **ИД области данных**<br>mshr_dataareaid<br>*Строка* | Чтение/запись<br>Необязательный | Указывает юридическое лицо (компанию).|
| **Значение ИД области данных**<br>_mshr_dataareaid_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: cdm_companyid сущности cdm_company | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию). |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Объединение значения запроса на набор сотрудников, ИД уровня образования и ИД образовательной дисциплины в качестве другого метода для уникальной идентификации записи. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]