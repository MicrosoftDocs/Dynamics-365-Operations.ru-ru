---
title: Адрес физического лица
description: В этой статье описывается сущность "Адрес физического лица" для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be5cf649771eaddcb4f2198821530e61b76b2cd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871026"
---
# <a name="person-address"></a>Адрес физического лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Адрес физического лица" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersonaddressentities

## <a name="description"></a>описание

Эта сущность содержит список почтовых адресов для записей кандидатов.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности адреса физического лица**<br>mshr_hcmpersonaddressentityid<br>*Строка* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор записи сущности. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется | ИД связанной записи субъекта (физического лица). |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **Код местонахождения**<br>mshr_locationid<br>*Строка* | Чтение/запись<br>Требуется | ИД местоположения записи адреса. Настройте в сущности mshr_logisticspostaladdresslocationcdsentity. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описание адреса кандидата. |
| **Роли**<br>mshr_roles<br>*Строка* | Чтение/запись<br>Требуется | Роли, назначенные для этого адреса. Можно назначить несколько ролей. Каждая роль должна быть разделена точкой с запятой. Допустимые значения, содержащиеся в сущности mshr_logisticslocationroleentity. |
| **Улица**<br>mshr_street<br>*Строка* | Чтение/запись<br>Необязательный | Номер дома. |
| **Город**<br>mshr_city<br>*Строка* | Чтение/запись<br>Необязательный | Город в адресе. Настройте в сущности mshr_logisticsaddresscityentity. |
| **Область/штат/провинция**<br>mshr_state<br>*Строка* | Чтение/запись<br>Необязательный | Регион в адресе. Настройте в сущности mshr_logisticsaddressstateentity. |
| **Райoн**<br>mshr_county<br>*Строка* | Чтение/запись<br>Необязательный | Район в адресе. Настройте в сущности mshr_logisticsaddresscountyentity. |
| **Почтовый индекс**<br>mshr_zipcode<br>*Строка* | Чтение/запись<br>Необязательный | Почтовый индекс в адресе. Настройте в сущности mshr_logisticsaddresspostalcodeentity. |
| **Код страны/региона**<br>mshr_countryregionid<br>*Строка* | Чтение/запись<br>Необязательный | Страна или регион в адресе. |
| **Значение кода страны/региона**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_logisticaddresscountryregionentityid сущности mshr_logisticsaddresscountryregionentity | Созданный системой уникальный идентификатор страны/региона адреса. |
| **Является основным**<br>mshr_isprimary<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Указывает, является ли этот адрес основным адресом физического лица определенной роли. |
| **Является частным**<br>mshr_isprivate<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Указывает, является ли этот адрес личным адресом для данного физического лица. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле, используемое в качестве первичного идентификатора записи сущности. Комбинация номера субъекта и кода местоположения. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
