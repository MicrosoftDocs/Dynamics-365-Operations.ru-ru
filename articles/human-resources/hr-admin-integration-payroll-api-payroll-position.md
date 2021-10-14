---
title: Сведения о заработной плате для должностей
description: В этом разделе представлены сведения и пример запроса для сущности Сведения о заработной плате для должностей в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 76131b6cc7ee58d4a095da4ac56cd97124e42587
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559370"
---
# <a name="payroll-position"></a>Позиция зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность должностей зарплаты в Dynamics 365 Human Resources.

Физическое имя: mshr_payrollpositionentity.

### <a name="description"></a>описание

Эта сущность предоставляет информацию, связанную с должностью, для указанного сотрудника.

Физическое имя: mshr_payrollpositionentity.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Тип_** | Использование | Описание |
| --- | --- | --- |
| **Код должности**</br>mshr_positionid</br>*Строка* | Только для чтения | Код должности. |
| **ИД цикли оплаты**</br>mshr_paycycleid</br>*Строка* | Только для чтения | Цикл оплаты, который определен для данной должности. |
| **Обычные часы за год**</br>annualregularhours</br>*Десятичное* | Только для чтения | Обычные часы за год, которые определены для данной должности. |
| **Оплачивается юридическим лицом**</br>paidbylegalentity</br>*Строка* | Только для чтения | Юридическое лицо, которое определено в должности и ответственное за осуществление платежа. |
| **Действительно до**</br>validto</br>*Смещение даты и времени* | Только для чтения | Дата, до которой будут действительны сведения о должности. |
| **Действительно с**</br>validfrom</br>*Смещение даты и времени* | Только для чтения | Дата, с которой будут действительны сведения о должности. |
| **Основное поле**</br>mshr_primaryfield</br>*Строка* | Создано системой | Основное поле. |
| **ИД сущности Сведения о заработной плате для должностей**</br>payrollpositiondetailsentityid</br>*Guid* | Требуется</br>Создано системой. | Созданное системой значение глобального уникального идентификатора (GUID), уникально идентифицирующее должность. |

## <a name="relations"></a>Связи

| Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Неприменимо |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Неприменимо |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Отклик**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
