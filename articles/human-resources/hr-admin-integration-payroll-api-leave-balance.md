---
title: Сальдо отпуска
description: В этой теме представлены сведения и пример запроса для сущности сальдо отпуска в Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab136e9b40de280387dc3c5207a08a6bb357941feb3a8c736d9671f7850f2bf8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782691"
---
# <a name="leave-balance"></a>Сальдо отпуска

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность сальдо отпуска для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность обеспечивает сальдо отпусков для данного сотрудника по типу отпуска.

Физическое имя: mshr_essleavebalanceentities.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника. |
| **Текущее сальдо**</br>mshr_balanceavailable</br>*Десятичн.* | Только для чтения | Текущее сальдо сотрудника. |
| **Вид**</br>mshr_balanceavailable</br>*Строка* | Только для чтения | Код типа отпуска. |
| **Ставка начисления**</br>mshr_accrualratedescription</br> | Только для чтения | Ставка начисления. |
| **Последняя сумма переноса**</br>mshr_lastcarryforwardamount</br>*Десятичн.* | Только для чтения | Сумма последнего переноса. |
| **Полученные в этом году**</br>mshr_takenthisyear</br>*Десятичн.* | Только для чтения | Сумма отпуска, взятая за этот год. |
| **Итого за этот год**</br>mshr_totalthisyear</br>*Десятичн.* | Только для чтения | Общая сумма для этого года. |
| **ИД области данных**</br>mshr_dataareaid_id</br>*Строка* | Только для чтения | Указывает юридическое лицо (компанию). |
| **Основное поле**</br>mshr_primaryfield</br>*GUID* | Только для чтения</br>Создано системой | |
| **Код типа отпуска**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Только для чтения</br>Зарубежный ключ:mshr_essleavetypeentityid сущности mshr_essleavetypeentity  | Код типа отпуска |
| **Сущность сальдо отпуска**</br>mshr_essleavebalanceentityid</br>*GUID* | Создано системой | Создаваемое системой значение GUID для уникальной идентификации сальдо. |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Отклик**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
