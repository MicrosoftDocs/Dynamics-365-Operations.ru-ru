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
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722639"
---
# <a name="payroll-position-job"></a>Задание позиции зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность задания должности зарплаты для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность предоставляет отношение между должностью и заданием для указанного плана фиксированной компенсации.

Физическое имя: mshr_payrollpositionjobentity.

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код задания**<br>mshr_jobid<br>*Строка* | Только для чтения<br>Требуется |ИД задания. |
| **Действительно с**<br>mshr_validto<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, начиная с которой действует связь должности и задания. |
| **Действительно до**<br>mshr_validto<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, до которой действует связь задания и должности.  |
| **Код должности**<br>mshr_positionid<br>*Строка* | Только для чтения<br>Требуется | Код должности. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Требуется<br>Создано системой |  |
| **Значение идентификатора задания должности**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |ИД задания, связанный с должностью.|
| **Значение идентификатора План фиксированной компенсации**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | ИД плана фиксированной компенсации, связанный с должностью. |
| **ИД сущности задания позиции заработной платы**<br>mshr_payrollpositionjobentityid<br>*Guid* | Требуется<br>Создано системой. | Создаваемое системой значение GUID для уникальной идентификации задания.  |

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
