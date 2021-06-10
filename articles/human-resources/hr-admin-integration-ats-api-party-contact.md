---
title: Контакт субъекта
description: В этом разделе описывается сущность контакта субъекта для Dynamics 365 Human Resources.
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
ms.openlocfilehash: b37910f10c0d89e2659aa0bfbdc601c3592f896c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053811"
---
# <a name="party-contact"></a>Контакт субъекта

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность контакта субъекта для Dynamics 365 Human Resources.

Физическое имя: mshr_dirpartycontactentities

## <a name="description"></a>описание

Эта сущность описывает контактную информацию кандидата, включая телефон, адрес электронной почты и учетные записи социальных сетей.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД сущности контакта субъекта**<br>mshr_dirpartycontactentityid<br>*Строка* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор записи сущности. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется | ИД связанной записи субъекта (физического лица). |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **Код местонахождения**<br>mshr_locationid<br>*Строка* | Чтение/запись<br>Требуется | ИД местоположения записи адреса. Настройте в сущности mshr_logisticspostaladdresslocationcdsentity. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описание контактных данных. |
| **Вид**<br>mshr_type<br>*Набор параметров mshr_logisticselectronicaddressmethodtype* | Чтение/запись<br>Требуется | Тип сведений о контакте. |
| **Код страны или региона**<br>mshr_countryregioncode<br>*Строка* | Чтение/запись<br>Необязательный | Страна или регион в адресе. |
| **Указатель**<br>mshr_locator<br>*Строка* | Чтение/запись<br>Необязательный | Сведения о контакте. Например, если типом является **Адрес электронной почты**, то в этом поле будет указан адрес электронной почты кандидата. |
| **Расширение указателя**<br>mshr_locatorextension<br>*Строка* | Чтение/запись<br>Необязательный | Расширение указателя. Например, если типом является **Телефон**, то это свойство будет содержать добавочный номер телефона. |
| **Является мобильным**<br>mshr_ismobile<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Указывает, является ли номер телефона мобильным номером. |
| **Является мгновенным сообщением**<br>mshr_isinstantmessage<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Указывает, разрешен ли телефон для обмена мгновенными сообщениями. |
| **Является основным**<br>mshr_isprimary<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Определяет основной контакт типа контакта. Для каждого типа контакта должна существовать только одна основная запись. |
| **Является частным**<br>mshr_isprivate<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Требуется | Указывает, является ли этот адрес личным адресом для данного физического лица. |
| **Целевые назначения**<br>mshr_purpose<br>*Строка* | Чтение/запись<br>Необязательный | Название/роль контактных данных. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле, используемое в качестве первичного идентификатора записи сущности. Комбинация номера субъекта, типа, описания и указателя. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]