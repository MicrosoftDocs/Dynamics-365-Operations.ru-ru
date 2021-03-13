---
title: Пример запроса кандидата для приема на работу
description: В этой теме представлен пример запроса для сущности кандидата на прием на работу в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 963e12e9114664a995b92ffe22063c14f904da35
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125769"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="61c39-103">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="61c39-103">Example query for Candidate to hire</span></span>

<span data-ttu-id="61c39-104">В этой теме представлен пример запроса для сущности кандидата на прием на работу в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="61c39-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="61c39-105">В этой теме представлен пример, демонстрирующий способы использования *глубокой вставки* для создания всех сведений о новой записи кандидата в одной операции API.</span><span class="sxs-lookup"><span data-stu-id="61c39-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="61c39-106">Дополнительные сведения о глубокой вставке см. в разделе [Создание записей связанной сущности в одной операции](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="61c39-106">For more information about deep inserts, see [Create related entity records in one operation](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="61c39-107">Сущность **mshr_hcmcandidatetohireentity** является уникальной, поскольку связана с сущностью **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="61c39-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="61c39-108">Многие свойства сущности **mshr_hcmcandidatetohireentity** (например, **mshr_firstname**, **mshr_lastname** и **mshr_birthdate**) наследуются из записи **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="61c39-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="61c39-109">При разноске новой записи кандидата в **mshr_hcmcandidatetohireentity** без использования операций глубокой вставки можно определить значения для этих свойств непосредственно в записи **mshr_hcmcandidatetohireentity**.</span><span class="sxs-lookup"><span data-stu-id="61c39-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="61c39-110">Соответствующая запись **mshr_dirpersonentity** создается неявно с определенными значениями для свойств.</span><span class="sxs-lookup"><span data-stu-id="61c39-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="61c39-111">Затем можно создать любые другие записи сущности (такие как навыки или образование) как отдельные вызовы API.</span><span class="sxs-lookup"><span data-stu-id="61c39-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="61c39-112">Однако, если необходимо использовать глубокие вставки для создания всех связанных сущностей в одной операции, свойства, относящиеся к сущности **mshr_dirpersonentity**, должны быть определены на этом вложенном уровне операции.</span><span class="sxs-lookup"><span data-stu-id="61c39-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="61c39-113">В этом примере показано, как создать запись кандидата, связанную запись физического лица и навыки и образование физического лица в трех вложенных уровнях с помощью глубоких вставок в одной операции API.</span><span class="sxs-lookup"><span data-stu-id="61c39-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="61c39-114">Пример не включает все свойства для каждой из сущностей API.</span><span class="sxs-lookup"><span data-stu-id="61c39-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="61c39-115">Это упрощено для демонстрационных целей.</span><span class="sxs-lookup"><span data-stu-id="61c39-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="61c39-116">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="61c39-116">**Request**</span></span>

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

<span data-ttu-id="61c39-117">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="61c39-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="61c39-118">См. также</span><span class="sxs-lookup"><span data-stu-id="61c39-118">See also</span></span>

[<span data-ttu-id="61c39-119">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="61c39-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>