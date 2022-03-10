---
title: Сотрудник зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности заработной платы сотрудника в Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: e853a8a5730d397f253c8ce3a330794594dfd907
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068492"
---
# <a name="payroll-employee"></a>Сотрудник зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность сотрудника зарплаты для Dynamics 365 Human Resources.

Физическое имя: mshr_payrollemployeeentity.

### <a name="description"></a>описание

Эта сущность предоставляет информацию о сотруднике. Перед использованием этой сущности необходимо задать [параметры интеграции зарплаты](hr-admin-integration-payroll-api-parameters.md).

>[!IMPORTANT] 
>Поля **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** и **NameValidTo** больше недоступны для этой сущности. Это гарантирует, что имеется только одна дата вступления в силу для резервного копирования источника данных для этой сущности.
>Эти поля будут доступны в **DirPersonNameHistoricalEntity**, которая была выпущена в обновлении платформы 43. Имеется связь OData из **PayrollEmployeeEntity** в **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код информации о компании**</br>mshr_legalentityid</br>*Строка* | Только для чтения | Указывает юридическое лицо (компанию). |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника. |
| **Дата начала трудоустройства**</br>mshr_employmentstartdate</br>*Смещение даты и времени* | Только для чтения | Дата начала занятости сотрудника. |
| **Дата окончания трудоустройства**</br>mshr_employmentenddate</br>*Смещение даты и времени* | Только для чтения |Дата окончания занятости сотрудника.  |
| **Дата рождения**</br>mshr_birthdate</br>*Смещение даты и времени* | Только для чтения | Дата рождения сотрудника. |
| **Род**</br>mshr_gender</br>[набор параметров mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Только для чтения | Пол сотрудника. |
| **Тип трудоустройства**</br>mshr_employmenttype</br>[Набор параметров mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Только для чтения | Тип трудоустройства. |
| **ИД типа идентификации**</br>mshr_identificationtypeid</br>*Строка* |Только для чтения | Тип идентификации, определенный для сотрудника. |
| **Идентификационный номер для**</br>mshr_identificationnumber</br>*Строка* | Только для чтения |Идентификационный номер, определенный для сотрудника. |
| **Готовы платить**</br>mshr_readytopay</br>[набор параметров mshr_noyes](hr-admin-integration-payroll-api-no-yes.md) | Только для чтения | Указывает, отмечен ли сотрудник как готовый к оплате. |
| **Код сущности заработной платы сотрудника**</br>mshr_payrollemployeeentityid</br>*GUID* | Создано системой | Созданное системой значение глобального уникального идентификатора (GUID), уникально идентифицирующее сотрудника. |

## <a name="relations"></a>Связи

|Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Пример запроса для заработной платы сотрудника

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
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
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
