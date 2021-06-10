---
title: Пример запроса кандидата для приема на работу
description: В этой теме представлен пример запроса для сущности кандидата на прием на работу в Dynamics 365 Human Resources.
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
ms.openlocfilehash: efec8c0a8eb75f818acd4ed02632f1db96719d81
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054724"
---
# <a name="example-query-for-candidate-to-hire"></a>Пример запроса кандидата для приема на работу

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме представлен пример запроса для сущности кандидата на прием на работу в Dynamics 365 Human Resources.

В этой теме представлен пример, демонстрирующий способы использования *глубокой вставки* для создания всех сведений о новой записи кандидата в одной операции API. Дополнительные сведения о глубокой вставке см. в разделе [Создание записей связанной сущности в одной операции](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Сущность **mshr_hcmcandidatetohireentity** является уникальной, поскольку связана с сущностью **mshr_dirpersonentity**. Многие свойства сущности **mshr_hcmcandidatetohireentity** (например, **mshr_firstname**, **mshr_lastname** и **mshr_birthdate**) наследуются из записи **mshr_dirpersonentity**. При разноске новой записи кандидата в **mshr_hcmcandidatetohireentity** без использования операций глубокой вставки можно определить значения для этих свойств непосредственно в записи **mshr_hcmcandidatetohireentity**. Соответствующая запись **mshr_dirpersonentity** создается неявно с определенными значениями для свойств. Затем можно создать любые другие записи сущности (такие как навыки или образование) как отдельные вызовы API.

Однако, если необходимо использовать глубокие вставки для создания всех связанных сущностей в одной операции, свойства, относящиеся к сущности **mshr_dirpersonentity**, должны быть определены на этом вложенном уровне операции.

В этом примере показано, как создать запись кандидата, связанную запись физического лица и навыки и образование физического лица в трех вложенных уровнях с помощью глубоких вставок в одной операции API.

> [!NOTE]
> Пример не включает все свойства для каждой из сущностей API. Это упрощено для демонстрационных целей.

**Запрос**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Отклик**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]