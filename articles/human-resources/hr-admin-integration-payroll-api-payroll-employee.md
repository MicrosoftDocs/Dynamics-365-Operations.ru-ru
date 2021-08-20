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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768199"
---
# <a name="payroll-employee"></a>Сотрудник зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность сотрудника зарплаты для Dynamics 365 Human Resources.

Физическое имя: mshr_payrollemployeeentity.

### <a name="description"></a>описание

Эта сущность предоставляет информацию о сотруднике. Перед использованием этой сущности необходимо задать [параметры интеграции зарплаты](hr-admin-integration-payroll-api-parameters.md).

>[!IMPORTANT] 
>Поля **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** и **NameValidTo** больше недоступны для этой сущности. Это гарантирует, что имеется только одна дата вступления в силу для резервного копирования источника данных для этой сущности.
>Эти поля будут доступны в **DirPersonNameHistoricalEntity**, которая была выпущена в обновлении платформы 43. Имеется отношение OData из **PayrollEmployeeEntity** в **DirPersonNameHistoricalEntity** в поле **Физическое лицо**. 

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Табельный номер**<br>mshr_personnelnumber<br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Создано системой |  |
| **Код информации о компании**<br>mshr_legalentityID<br>*Строка* | Только для чтения | Указывает юридическое лицо (компанию). |
| **Род**<br>mshr_gender<br>[набор параметров mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Только для чтения | Пол сотрудника. |
| **Код сущности заработной платы сотрудника**<br>mshr_payrollemployeeentityid<br>*GUID* | Требуется<br>Создано системой | Создаваемое системой значение GUID для уникальной идентификации сотрудника. |
| **Дата начала трудоустройства**<br>mshr_employmentstartdate<br>*Смещение даты и времени* | Только для чтения | Дата начала занятости сотрудника. |
| **ИД типа идентификации**<br>mshr_identificationtypeid<br>*Строка* |Только для чтения | Тип идентификации, определенный для сотрудника. |
| **Дата окончания трудоустройства**<br>mshr_employmentenddate<br>*Смещение даты и времени* | Только для чтения |Дата окончания занятости сотрудника.  |
| **ИД области данных**<br>mshr_dataareaid_id<br>*GUID* | Только для чтения <br>Создано системой | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию). |
| **Действительно до**<br>mshr_namevalidto<br>*Смещение даты и времени* |  Только для чтения | Дата, до которой действительны сведения о сотруднике. |
| **Дата рождения**<br>mshr_birthdate<br>*Смещение даты и времени* | Только для чтения | Дата рождения сотрудника |
| **Идентификационный номер для**<br>mshr_identificationnumber<br>*Строка* | Только для чтения |Идентификационный номер, определенный для сотрудника.  |

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
## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
