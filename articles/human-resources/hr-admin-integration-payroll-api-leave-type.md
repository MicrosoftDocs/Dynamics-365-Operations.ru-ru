---
title: Тип отпуска
description: В этой статье представлены сведения и пример запроса для сущности "Тип отпуска" в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893796"
---
# <a name="leave-type"></a>Тип отпуска


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Тип отпуска" для Dynamics 365 Human Resources.

### <a name="description"></a>Описание

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
