---
title: Запрос на отпуск
description: В этой теме представлены сведения и пример запроса для сущности запроса отпуска в Dynamics 365 Human Resources.
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
ms.openlocfilehash: b7f5744265dd106f11e6ffe7334873e697a7ea13
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314471"
---
# <a name="leave-request"></a>Запрос на отпуск

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность запроса отпуска для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность предоставляет информацию для запроса отпуска.

Физическое имя: mshr_essleaverequestentity.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код запроса**</br>mshr_requestid</br>*Строка* | Только для чтения | Код запроса. |
| **Код типа отпуска**</br>mshr_leavetypeid</br>*Строка* | Только для чтения | Код типа отпуска. |
| **Дата**</br>mshr_leavedate</br>*Смещение даты и времени* | Только для чтения | Дата запроса отпуска. |
| **Сумма, руб.**</br>mshr_amount</br>*Десятичн.* | Только для чтения | Сумма запроса отпуска. |
| **Тип половины дня**</br>mshr_halfdaydefinition</br>*Набор параметров mshr_LeaveHalfDayDefinition* | Только для чтения | Тип отпуска половины дня. |
| **Комментарий**</br>mshr_comment</br>*Строка* | Только для чтения | Комментарий для запроса. |
| **Состояние**</br>mshr_status</br>*Набор параметров mshr_status* | Только для чтения | Статус запроса. |
| **Дата**</br>mshr_requestdate</br>*Смещение даты и времени* | Только для чтения | Дата запроса. |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника. |
| **Код основания**</br>mshr_reasoncodeid</br>*Строка* | Только для чтения | Код основания. |
| **ИД области данных**</br>mshr_dataareaid</br>*Строка* | Только для чтения | Указывает юридическое лицо (компанию). |
| **Основное поле**</br>mshr_primaryfield</br>*GUID* | Только для чтения</br>Создано системой | |
| **Сущности типа отпуска**</br>mshr_essleaverequestentityid</br>*GUID* | Создано системой | Создаваемое системой значение идентификатора GUID, чтобы однозначно определить запрос на отпуск. |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Отклик**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
