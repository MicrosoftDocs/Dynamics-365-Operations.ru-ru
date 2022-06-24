---
title: Журнал имен сотрудников
description: В этой статье представлены сведения и пример запроса для сущности "Журнал имен сотрудников" в Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875781"
---
# <a name="person-name-history"></a>Журнал имен сотрудников


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Журнал имен сотрудников" в Dynamics 365 Human Resources.

Физическое имя: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Описание

Эта сущность предоставляет информацию о журнале имен для данного человека.

> [!IMPORTANT] 
> Поля **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** и **NameValidTo** больше недоступны для сущности "Сотрудник с заработной платой". Они были удалены, чтобы гарантировать, что только один вступивший в силу источник данных поддерживает эту сущность.

## <a name="properties"></a>Свойства

| Свойство</br>**Физическое имя**</br>**_Тип_** | Использование | Описание |
| --- | --- | --- |
| **Имя**</br>mshr_firstname</br>*Строка* | Только для чтения | Имя. |
| **Префикс фамилии**</br>mshr_lastnameprefix</br>*Строка*) | Только для чтения | Префикс фамилии. |
| **Фамилия**</br>mshr_lastname</br>*Строка*) | Только для чтения | Фамилия. |
| **Отчество**</br>mshr_middlename</br>*Строка*) | Только для чтения | Отчество. |
| **Действительно до**</br>mshr_validto</br>*Строка*) | Только для чтения | Дата, до которой имя является действительным. |
| **Номер субъекта**</br>mshr_partynumber</br>*Строка* | Только для чтения | Созданный системой уникальный идентификатор для физического лица, удобный для восприятия пользователем. |
| **Основное поле**</br>mshr_primaryfield</br>*Строка* | Только для чтения | Уникальный идентификатор записи. |
| **Код сущности для журнала имени лица**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Создано системой | Созданное системой значение глобального уникального идентификатора (GUID), уникально идентифицирующее запись. |

## <a name="relations"></a>Связи

| Значение свойства | Связанный объект | Свойство навигации | Тип сбора |
| --- | --- | --- | --- |
| Неприменимо | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Неприменимо | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Пример запроса для "Сотрудник с заработной платой"

**Запрос**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Отклик**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
