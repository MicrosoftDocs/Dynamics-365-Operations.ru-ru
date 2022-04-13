---
title: Журнал имен сотрудников
description: В этой теме представлены сведения и пример запроса для сущности журнала имен сотрудников в Dynamics 365 Human Resources.
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
ms.openlocfilehash: db22a602c782cef15b6e5769b9c0726dff158160
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533608"
---
# <a name="person-name-history"></a>Журнал имен сотрудников


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой теме описывается сущность журнала имен сотрудников в Dynamics 365 Human Resources.

Физическое имя: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Описание

Эта сущность предоставляет информацию о журнале имен для данного человека.

> [!IMPORTANT] 
> Поля **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** и **NameValidTo** больше недоступны для сущности сотрудника заработной платы. Они были удалены, чтобы гарантировать, что только один вступивший в силу источник данных поддерживает эту сущность.

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

## <a name="example-query-for-payroll-employee"></a>Пример запроса для заработной платы сотрудника

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
