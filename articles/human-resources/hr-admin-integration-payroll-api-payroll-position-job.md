---
title: Задание позиции зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности задания позиции заработной платы в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 349479d9e77861b54d879bcfd93f7af0e38cff95
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069840"
---
# <a name="payroll-position-job"></a>Задание позиции зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность задания должности зарплаты для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность предоставляет отношение между должностью и заданием для указанного плана фиксированной компенсации.

Физическое имя: mshr_payrollpositionjobentity.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Тип_** | Использование | Описание |
| --- | --- | --- |
| **Код должности**</br>mshr_positionid</br>*Строка* | Только для чтения | Код должности. |
| **Действительно с**</br>mshr_validto</br>*Смещение даты и времени* | Только для чтения | Это дата, начиная с которой действует связь должности и задания. |
| **Действительно до**</br>mshr_validto</br>*Смещение даты и времени* | Только для чтения | Дата, до которой действует связь задания и должности. |
| **Код задания**</br>mshr_jobid</br>*Строка* | Только для чтения | ИД задания. |
| **Основное поле**</br>mshr_primaryfield</br>*Строка* | Создано системой | Основное поле. |
| **ИД сущности задания позиции заработной платы**</br>mshr_payrollpositionjobentityid</br>*Guid* | Создано системой. | Созданное системой значение глобального уникального идентификатора (GUID), уникально идентифицирующее работу. |

## <a name="relations"></a>Связи

| Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Неприменимо |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Отклик**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
