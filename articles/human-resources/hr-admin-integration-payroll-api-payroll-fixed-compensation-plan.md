---
title: План фиксированной компенсации зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 14829f18fb5e3adde83e265cd6e70b60e1ff03ac
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069104"
---
# <a name="payroll-fixed-compensation-plan"></a>План фиксированной компенсации зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность плана фиксированной компенсации зарплаты для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность предоставляет план фиксированной компенсации, назначенный для данной должности сотрудника.

Физическое имя: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код плана**</br>mshr_planid</br>*Строка* | Только для чтения | Определение плана компенсации.  |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника. |
| **Ставка зарплаты**</br>mshr_payrate</br>*Десятичное* | Только для чтения | Ставка оплаты, определенная в плане фиксированной компенсации. |
| **Код должности**</br>mshr_positionid</br>*Строка* | Только для чтения | Код должности, связанный с сотрудником и соглашением о регистрации плана фиксированной компенсации. |
| **Действительно с**</br>mshr_validfrom</br>*Смещение даты и времени* |  Только для чтения | Дата, с которой действительна фиксированная компенсация сотрудника.  |
| **Действительно до**</br>mshr_validto</br>*Смещение даты и времени* | Только для чтения | Дата, до которой действительна фиксированная компенсация сотрудника. |
| **Частота платежей**</br>mshr_payfrequency</br>*Строка* | Только для чтения | Код [частоты выплат компенсаций](hr-admin-integration-payroll-api-compensation-pay-frequency.md) для данной ставки зарплаты. |
| **Валюта**</br>mshr_currency</br>*Строка* | Только для чтения | Валюта, определенная для плана фиксированной компенсации. |
| **Сущность плана фиксированной компенсации заработной платы**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Создано системой | Создаваемое системой значение GUID для однозначной идентификации плана компенсации. |

## <a name="relations"></a>Связи

|Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Отклик**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
