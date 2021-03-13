---
title: Навык в запросе по набору сотрудников
description: В этом разделе описывается сущность навыка в запросе на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 83a9956b9aa820e8aca9bf6b2ab920a45c1061f6
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126010"
---
# <a name="recruiting-request-skill"></a>Навык в запросе по набору сотрудников

В этом разделе описывается сущность навыка в запросе на набор сотрудников для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>описание

Описывает требования к навыкам для RecruitingRequest.

### <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности навыка запроса на набор персонала**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Только для чтения<br>Требуется | Создаваемый системой уникальный идентификатор для записи **Навык запроса на набор сотрудников**. |
| **ИД запроса на набор сотрудников**<br>mshr_recruitingrequestid<br>*Строка* | Однократная запись<br>Требуется | Уникальный идентификатор связанного запроса по набору сотрудников, доступный для чтения пользователем. |
| **Значение ИД запроса на набор сотрудников**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Только для чтения<br>Требуется<br> Внешний ключ: mshr_hcmrecruitingrequestentityid сущности mshr_hcmrecruitingrequestentity | Создаваемый системой уникальный идентификатор связанного запроса на набор сотрудников. |
| **ИД навыка**<br>mshr_skillid<br>*Строка*<br> | Однократная запись<br>Требуется | Уникальный идентификатор требуемого навыка, доступный для чтения пользователем. |
| **Значение ИД навыка**<br>_mshr_fk_skill_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmskillentityid сущности mshr_hcmskillentity | Созданный системой уникальный идентификатор требуемого навыка. |
| **Код уровня оценки**<br>mshr_ratinglevelid<br>*Строка* | Однократная запись<br>Необязательный | Требуемое значение уровня навыков, выбранное для должности, на основе модели рейтинга, назначенной данному навыку. |
| **Значение ИД уровня рейтинга**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmratinglevelentityid сущности mshr_hcmratinglevelentity | Созданный системой уникальный идентификатор для уровня. |
| **Описание навыка**<br>mshr_skilldescription<br>*Строка* | Только для чтения<br>Требуется | Описание навыка. |
| **Описание уровня рейтинга**<br>mshr_ratingleveldescription<br>*Строка* | Только для чтения<br>Необязательный | Описание выбранного уровня навыка. |
| **ИД области данных**<br>mshr_dataareaid<br>*Строка* | Чтение/запись<br>Необязательный | Указывает юридическое лицо (компанию). |
| **Значение ИД области данных**<br>_mshr_dataareaid_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: cdm_companyid сущности cdm_company | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию). |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Объединение значения запроса на набор сотрудников и кода навыка в качестве другого метода для уникальной идентификации записи. |
| **ИД модели рейтинга**<br>mshr_ratingmodelid<br>*Строка* | Чтение-запись<br>Требуется | Модель рейтинга, используемая для оценки навыка. |
| **Значение ИД модели рейтинга**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmratingmodelentityid сущности mshr_hcmratingmodelentity | Созданный системой уникальный идентификатор модели рейтинга, используемой для оценки навыка. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)
