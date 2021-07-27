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
ms.openlocfilehash: e13a6b3608802eb7bb2bc00686c2e914cc765587
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314173"
---
# <a name="payroll-position"></a>Позиция зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность должностей зарплаты в Dynamics 365 Human Resources.

Физическое имя: mshr_payrollpositionentity.

### <a name="description"></a>описание

Эта сущность предоставляет информацию, связанную с должностью, для указанного сотрудника.

Физическое имя: 

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Обычные часы за год**<br>annualregularhours<br>*Десятичн.* | Только для чтения<br>Требуется | Обычные часы за год, определенные для данной должности.  |
| **ИД сущности Сведения о заработной плате для должностей**<br>payrollpositiondetailsentityid<br>*Guid* | Требуется<br>Создано системой. | Создаваемое системой значение GUID для уникальной идентификации должности.  |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Требуется<br>Создано системой |  |
| **Значение идентификатора задания должности**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |ИД задания, связанный с должностью.|
| **Значение идентификатора План фиксированной компенсации**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | ИД плана фиксированной компенсации, связанный с должностью. |
| **ИД цикли оплаты**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Цикл оплаты, определенный для данной должности. |
| **Оплачивается юридическим лицом**<br>paidbylegalentity<br>*Строка* | Только для чтения<br>Требуется | Юридическое лицо, определенное в должности, ответственной за осуществление платежа. |
| **Код должности**<br>mshr_positionid<br>*Строка* | Только для чтения<br>Требуется | Код должности. |
| **Действительно до**<br>validto<br>*Смещение даты и времени* | Только для чтения<br>Требуется |Дата, начиная с которой будут действительны сведения о должности.  |
| **Действительно с**<br>validfrom<br>*Смещение даты и времени* | Только для чтения<br>Требуется |Дата, до которой будут действительны сведения о должности.  |

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
