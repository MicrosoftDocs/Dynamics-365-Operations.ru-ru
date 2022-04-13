---
title: План переменной компенсации зарплаты
description: В этой теме представлены сведения и пример запроса для сущности плана переменной компенсации заработной платы в Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5cc9e02ff2dd49e2eb0c8131fcff2eca4b9c3b1
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533657"
---
# <a name="payroll-variable-compensation-plan"></a>План переменной компенсации зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность плана переменной компенсации зарплаты для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность предоставляет план переменной компенсации, назначенный для данной должности сотрудника.

Физическое имя: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника.  |
| **Дата вознаграждения**</br>mshr_awarddate</br>*Смещение даты и времени* | Только для чтения | Дата вознаграждения. |
| **Тип премии**</br>mshr_awardtype</br>*[Набор параметров mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Только для чтения | Тип вознаграждения, определенный для плана переменных компенсаций. |
| **Валютное**</br>mshr_unitcurrencycode</br>*Строка* | Только для чтения |Валюта, определенная для плана переменной компенсации.   |
| **Код плана фиксированной компенсации**</br>mshr_fixedplanid</br>*Строка* | Только для чтения | План фиксированных компенсаций, который используется в качестве основы при расчете вознаграждения. |
| **Значение ед. изм.**</br>mshr_awardamount</br>*Десятичн.* | Только для чтения | Значение единицы |
| **Тип процесса**</br>mshr_processtype</br>*[Набор параметров mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Только для чтения | Тип процесса. |
| **Тип плана переменной компенсации**</br>Строка</br>*mshr_typeid* | Только для чтения | Тип плана переменной компенсации. |
| **Код плана переменной компенсации**</br>Строка</br>*mshr_planid* | Только для чтения | Код плана переменной компенсации. |
| **Число единиц**</br>Десятичное</br>*mshr_numberofunits* | Только для чтения | Количество единиц типа вознаграждения. |
| **Основное поле**</br>mshr_primaryfield</br>*GUID* | Только для чтения</br>Создано системой. | |
| **Сущность плана переменной компенсации зарплаты**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Создано системой | Создаваемое системой значение GUID для однозначной идентификации плана компенсации. |

## <a name="relations"></a>Связи 

|Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Отклик**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
