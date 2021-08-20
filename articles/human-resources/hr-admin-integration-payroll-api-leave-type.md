---
title: Тип отпуска
description: В этой теме представлены сведения и пример запроса для сущности типа отпуска в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5e64b533ad7be23060701e8826a25736a078b59d1ecf824bee0e2dd05c9c78f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713110"
---
# <a name="leave-type"></a>Тип отпуска

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность типа отпуска для Dynamics 365 Human Resources.

### <a name="description"></a>описание

Эта сущность предоставляет информацию для указанного типа отпуска.

Физическое имя: mshr_essleavetypeentity.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код типа отпуска**</br>mshr_leavetypeid</br>*Строка* | Только для чтения | Код типа отпуска. |
| **Описание**</br>mshr_description</br>*Строка* | Только для чтения | Описание типа отпуска. |
| **Категория**</br>mshr_category</br>*Набор параметров mshr_LeaveTypeCategory* | Только для чтения | Категория типа отпуска. |
| **Требуется код основания**</br>mshr_isreasoncoderequired</br>*Набор параметров mshr_NoYes* | Только для чтения | Определяет, является ли код основания обязательным для типа отпуска. |
| **Согласие отпуска**</br>mshr_leaveamountunit</br>*Набор параметров mshr_LeaveAmountUnit* | Только для чтения | Согласие данного типа отпуска. |
| **Включить половину дня**</br>mshr_enablehalfdaydefinition</br>*Набор параметров mshr_NoYes* | Определяет, активирована ли половина дня для типа отпуска. |
| **ИД области данных**</br>mshr_dataareaid_id</br>*Строка* | Только для чтения | Указывает юридическое лицо (компанию). |
| **Сущность типа отпуска**</br>mshr_essleavetypeentityid</br>*GUID* | Создано системой | Создаваемое системой значение идентификатора GUID, чтобы однозначно определить тип отпуска. |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Отклик**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
