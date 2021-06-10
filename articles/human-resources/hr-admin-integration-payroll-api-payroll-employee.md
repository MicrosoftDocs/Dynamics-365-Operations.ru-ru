---
title: Сотрудник зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности заработной платы сотрудника в Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87efbf7063de373e1e0b844ff1b942cdaab4a021
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055060"
---
# <a name="payroll-employee"></a>Сотрудник зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе представлены сведения и пример запроса для сущности заработной платы сотрудника в Dynamics 365 Human Resources.

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Табельный номер**<br>mshr_personnelnumber<br>*Строка* | Только для чтения<br>Требуется | Уникальный табельный номер для сотрудника. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Требуется<br>Создано системой |  |
| **Фамилия**<br>mshr_lastname<br>*Строка* | Только чтение<br>Требуется | Фамилия сотрудника. |
| **Код информации о компании**<br>mshr_legalentityID<br>*Строка* | Только для чтения<br>Требуется | Указывает юридическое лицо (компанию). |
| **Действительно с**<br>mshr_namevalidfrom<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, с которой действительны сведения о сотруднике.  |
| **Род**<br>mshr_gender<br>*Int32* | Только для чтения<br>Требуется | Пол сотрудника. |
| **Код сущности заработной платы сотрудника**<br>mshr_payrollemployeeentityid<br>*GUID* | Требуется<br>Создано системой | Создаваемое системой значение GUID для уникальной идентификации сотрудника. |
| **Дата начала трудоустройства**<br>mshr_employmentstartdate<br>*Смещение даты и времени* | Только для чтения<br>Требуется | Дата начала занятости сотрудника. |
| **ИД типа идентификации**<br>mshr_identificationtypeid<br>*Строка* |Только для чтения<br>Требуется | Тип идентификации, определенный для сотрудника. |
| **Дата окончания трудоустройства**<br>mshr_employmentenddate<br>*Смещение даты и времени* | Только для чтения<br>Требуется |Дата окончания занятости сотрудника.  |
| **ИД области данных**<br>mshr_dataareaid_id<br>*GUID* | Требуется <br>Создано системой | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию). |
| **Действительно до**<br>mshr_namevalidto<br>*Смещение даты и времени* |  Только для чтения<br>Требуется | Дата, до которой действительны сведения о сотруднике. |
| **Дата рождения**<br>mshr_birthdate<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата рождения сотрудника |
| **Идентификационный номер для**<br>mshr_identificationnumber<br>*Строка* | Только для чтения <br>Требуется |Идентификационный номер, определенный для сотрудника.  |
| **Имя**<br>mshr_firstname<br>*Строка* | Только для чтения<br>Требуется | Имя сотрудника. |
| **Отчество**<br>mshr_middlename<br>*Строка* | Только для чтения<br>Требуется |Отчество сотрудника.  |

## <a name="example-query-for-payroll-employee"></a>Пример запроса для заработной платы сотрудника

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Отклик**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
