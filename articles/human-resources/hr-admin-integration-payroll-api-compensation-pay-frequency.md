---
title: Частота компенсационных выплат
description: В этом разделе представлены сведения и пример запроса для сущности частоты компенсационных выплат в Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066151"
---
# <a name="compensation-pay-frequency"></a>Частота компенсационных выплат


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность частоты компенсационных выплат в Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Описание

Эта сущность предоставляет информацию о преобразовании ставок оплаты для данной частоты компенсационных выплат.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Тип_** | Использование | Описание |
| --- | --- | --- |
| **Преобразование годовой ставки оплаты**</br>mshr_annualconversionfactor</br>*Десятичное* | Только для чтения | Ежегодный коэффициент преобразования для частоты платежей. |
| **Описание**</br>mshr_description</br>*Строка* | Только для чтения | Описание коэффициента преобразования. |
| **Преобразование почасовой ставки оплаты**</br>mshr_hourlyconversionfactor</br>*Десятичное* | Только для чтения | Почасовой коэффициент преобразования для частоты платежей. |
| **Преобразование месячной ставки оплаты**</br>mshr_monthlyconversionfactor</br>*Десятичное* | Только для чтения | Ежемесячный коэффициент преобразования для частоты платежей. |
| **Преобразование ставки оплаты**</br>mshr_payrateconversion</br>*Строка* | Только для чтения | Уникальная строка для указания коэффициента преобразования. |
| **Период**</br>mshr_period</br>*набор параметров периода* | Только для чтения | Основной период для данного преобразования ставки заработной платы. |
| **Преобразование еженедельной ставки оплаты**</br>mshr_weeklyconversionfactor</br>*Десятичное* | Только для чтения | Еженедельный коэффициент преобразования для частоты платежей. |
| **ИД области данных**</br>mshr_dataareaid</br>*Строка* | Только для чтения | Юридическое лицо (компания). |
| **ИД сущности частоты компенсационных выплат**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Создано системой | Созданное системой значение глобального уникального идентификатора (GUID), уникально идентифицирующее запись. |

## <a name="example-query-for-payroll-employee"></a>Пример запроса для заработной платы сотрудника

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Отклик**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
