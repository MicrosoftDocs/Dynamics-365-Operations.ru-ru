---
title: Адрес работника зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.
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
ms.openlocfilehash: bf3fc5f333333b9a832ecb9c185473e476ac231d
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559517"
---
# <a name="payroll-worker-address"></a>Адрес работника зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность задания адреса работника зарплаты для Dynamics 365 Human Resources.

Физическое имя: mshr_payrollworkeraddressentity.

### <a name="description"></a>описание

Эта сущность предоставляет место жительства для заработной платы и место работы зарплаты для данного сотрудника.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Тип_** | Использование | Описание |
| --- | --- | --- |
| **Табельный номер**</br>mshr_personnelnumber</br>*Строка* | Только для чтения | Уникальный табельный номер для сотрудника. |
| **Код местонахождения**</br>mshr_locationidbr>*Строка* | Только для чтения | ИД для адреса. |
| **Жил по адресу**</br>mshr_islivedinaddressbr </br> *[Набор параметров mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Только для чтения | Значение, указывающее, является ли адрес местом, в котором живет сотрудник. |
| **Работал по адресу** </br> mshr_isworkedinaddressbr </br>*[Набор параметров mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Только для чтения | Значение, указывающее, является ли адрес местом, в котором работает сотрудник. |
| **Страна/регион**</br>mshr_countryregionid</br>*Строка* | Только для чтения</br>Требуется | Страна или регион, определенные для адреса. |
| **Почтовый индекс**</br>mshr_zipcode<br>*Строка* | Только для чтения | Идентификационный номер, который определен для сотрудника. |
| **Улица**</br>mshr_street</br>*Строка* | Только для чтения | Улица, которая определена для адреса. |
| **Город**</br>mshr_city</br>*Строка* | Только для чтения | Город, который определен для адреса. |
| **Область/штат/провинция**</br>mshr_state</br>*Строка* | Только для чтения | Область или край, определенные для адреса. |
| **Округ**</br>mshr_county</br>*Строка* | Только для чтения | Район, который определен для адреса. |
| **Действительно с**</br>mshr_postaladdressvalidfrom</br>*Смещение даты и времени* | Только для чтения | Дата, начиная с которой адрес является действительным. |
| **Действительно до**</br>mshr_postaladdressvalidto</br>*Смещение даты и времени* | Только для чтения | Дата, по которую адрес является действительным. |
| **Основное поле**</br>mshr_primaryfield</br>*Строка* | Только для чтения | Основное поле. |
| **ИД адреса работника зарплаты**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Создано системой | Созданное системой значение глобального уникального идентификатора (GUID), уникально идентифицирующее адрес. |

## <a name="relations"></a>Связи

| Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Пример запроса

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Отклик**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
