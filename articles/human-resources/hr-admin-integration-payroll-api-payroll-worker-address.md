---
title: Адрес работника зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882062"
---
# <a name="payroll-worker-address"></a>Адрес работника зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Город**<br>mshr_city<br>*Строка* | Только для чтения<br>Требуется | Город, определенный для адреса.   |
| **Табельный номер**<br>mshr_personnelnumber<br>*Строка* | Только для чтения<br>Требуется | Уникальный табельный номер для сотрудника.  |
| **Страна/регион**<br>mshr_countryregionid<br>*Строка* | Только для чтения<br>Требуется | Страна/регион, определенные для адреса  |
| **Действительно с**<br>mshr_postaladdressvalidfrom<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, начиная с которой адрес является действительным. |
| **Работал по адресу**<br>mshr_isworkedinaddressbr>*Int32* | Только для чтения<br>Требуется | Обозначает, находится ли адрес по месту работы сотрудника. |
| **Райoн**<br>mshr_county<br>*Строка* | Только для чтения<br>Требуется | Страна, определенная для адреса.  |
| **ИД адреса работника зарплаты**<br>mshr_payrollworkeraddressentityid<br>*GUID* | Требуется<br>Создано системой | Создаваемое системой значение GUID для уникальной идентификации адреса.  |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется |  |
| **Улица**<br>mshr_street<br>*Строка* | Только для чтения<br>Требуется | Улица, определенная для адреса. |
| **Действительно до**<br>mshr_postaladdressvalidto<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, до которой адрес является действительным.  |
| **Код местонахождения**<br>mshr_locationidbr>*Строка* | Только для чтения <br>Требуется | ИД для адреса.  |
| **Почтовый индекс**<br>mshr_zipcode<br>*Строка* | Только для чтения <br>Требуется |Идентификационный номер, определенный для сотрудника.  |
| **Жил по адресу**<br>mshr_islivedinaddressbr>*Строка* | Только для чтения<br>Требуется | Обозначает, находится ли адрес там, где живет сотрудник. |
| **Область/штат/провинция**<br>mshr_state<br>*Строка* | Только для чтения<br>Требуется | Регион, определенный для адреса.  |

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