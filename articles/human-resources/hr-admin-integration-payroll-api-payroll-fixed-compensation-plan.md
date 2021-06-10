---
title: План фиксированной компенсации зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059096"
---
# <a name="payroll-fixed-compensation-plan"></a>План фиксированной компенсации зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сотрудника**<br>mshr_fk_employee_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ:mshr_Employee_id of mshr_payrollemployeeentity entity  | Код сотрудника |
| **Ставка зарплаты**<br>mshr_payrate<br>*Десятичн.* | Только для чтения<br>Требуется | Ставка оплаты, определенная в плане фиксированной компенсации. |
| **Код плана**<br>mshr_planid<br>*Строка* | Только для чтения<br>Требуется |Определение плана компенсации.  |
| **Действительно с**<br>mshr_validfrom<br>*Смещение даты и времени* |  Только для чтения<br>Требуется |Дата, с которой действительна фиксированная компенсация сотрудника.  |
| **Сущность плана фиксированной компенсации заработной платы**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Требуется<br>Создано системой | Создаваемое системой значение GUID для однозначной идентификации плана компенсации. |
| **Частота платежей**<br>mshr_payfrequency<br>*Строка* | Только для чтения<br>Требуется |Частота выплаты сотруднику.  |
| **Действительно до**<br>mshr_validto<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, до которой действительна фиксированная компенсация сотрудника. |
| **Код должности**<br>mshr_positionid<br>*Строка* | Только для чтения <br>Требуется | ИД разноски, связанный с сотрудником и соглашением о регистрации плана фиксированной компенсации. |
| **Валютное**<br>mshr_currency<br>*Строка* | Только для чтения <br>Требуется |Валюта, определенная для плана фиксированной компенсации   |
| **Табельный номер**<br>mshr_personnelnumber<br>*Строка* | Только для чтения<br>Требуется |Уникальный табельный номер для сотрудника.  |

**Запрос**

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
