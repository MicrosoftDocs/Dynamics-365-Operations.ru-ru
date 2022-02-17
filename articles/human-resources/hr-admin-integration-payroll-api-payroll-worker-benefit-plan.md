---
title: План льгот сотрудника для зарплаты
description: В этой теме представлены сведения и пример запроса для сущности плана льгот работнику по зарплате в Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1805f7efaf2efc48d5996776f3aa27d75606886f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068442"
---
# <a name="payroll-worker-benefit-plan"></a>План льгот сотрудника для зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность плана льгот работнику по зарплате для Dynamics 365 Human Resources.

Физическое имя: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>описание

Эта сущность предоставляет информацию о плане льгот для данного сотрудника.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения</br>Требуется | Уникальный табельный номер для сотрудника. |
| **Код информации о компании**</br>mshr_legalentityID</br>*Строка* | Только для чтения | Указывает юридическое лицо (компанию). |
| **Код периода**</br>mshr_periodid</br>*Строка* | Только для чтения | Идентификатор периода. |
| **Код плана**</br>mshr_planid</br>*Строка* | Только для чтения | Идентификатор плана. |
| **Параметр покрытия**</br>mshr_coverageoptionid</br>*Строка* | Только для чтения | Идентификация параметра покрытия. |
| **Дата начала вычета**</br>mshr_deductionstartdatetime</br>*Смещение даты и времени* | Только для чтения | Дата начала вычета. |
| **Дата окончания вычета**</br>mshr_deductionenddatetime</br>*Смещение даты и времени* | Только для чтения | Дата окончания вычета. |
| **Состояние**</br>mshr_status</br>*[Набор параметров статуса плана сотрудника для льготы](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Только для чтения | Статус плана льгот. |
| **Действительно с**</br>mshr_validfrom</br>*Смещение даты и времени* | Только для чтения | Время, начиная с которого эта запись действительна. |
| **Действительно до**</br>mshr_validto</br>*Смещение даты и времени* |  Только для чтения | Время, вплоть до которого эта запись действительна. |
| **Код типа плана**</br>mshr_plantypeid</br>*Строка* | Только для чтения | Идентификатор типа плана. |
| **Код типа плана**</br>mshr_plantypecode</br>*[набор параметров покрытия типа плана льгот](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Только для чтения | Детализация типа плана. |
| **Число платежных периодов**</br>mshr_payperiod</br>*Целое число* | Только для чтения | Число платежных периодов, которое представляет частоту выплаты поставщиком льготы или сотрудником. Эта сумма будет использоваться для суммы ежегодной зарплаты по льготе сотрудника. |
| **Сумма сотрудника**</br>mshr_amountemployee</br>*Десятичное* | Только для чтения | Сумма или процент сотрудника. |
| **Сумма работодателя**</br>mshr_amountemployer</br>*Десятичное* | Только для чтения | Сумма или процент работодателя. |
| **Основное поле**</br>mshr_primaryfield</br>*Строка* | Создано системой | Основное поле. |
| **Значение идентификатора работника** </br>_mshr_fk_worker_id_value</br>*GUID* | Внешний ключ: mshr_hcmworkerbaseentityid сущности mshr_hcmworkerbaseentity. | Созданный системой уникальный идентификатор для работника. |
| **Значение кода периода**</br> _mshr_fk_period_id_value</br>*GUID* | Внешний ключ: mshr_benefitperiodentityid сущности mshr_benefitperiodentity. | Созданный системой уникальный идентификатор для периода. |
| **Значение кода плана**</br> _mshr_fk_plan_id_value</br>*GUID* | Внешний ключ: mshr_benefitplanentityid сущности mshr_benefitplanentity. | Созданный системой уникальный идентификатор для плана. |
| **Значение кода типа плана**</br> _mshr_fk_plantype_id_value</br>*GUID* | Внешний ключ: mshr_benefitplantypeentityid сущности mshr_benefitplantypeentity. | Созданный системой уникальный идентификатор для плана. |
| **Значение идентификатора параметра покрытия**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Внешний ключ: mshr_benefitcoverageoptionentityid сущности mshr_benefitcoverageoptionentity. | Созданный системой уникальный идентификатор для плана. |
| **Значение кода сущности плана льгот работника по зарплате**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Только для чтения </br> Создано системой | Созданный системой уникальный идентификатор записи. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Пример запроса для плана льгот для работника по зарплате

**Запрос**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Отклик**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
