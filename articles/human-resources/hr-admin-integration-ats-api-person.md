---
title: Физическое лицо
description: В этом разделе описывается сущность физического лица для Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a13222317ba59868686be5ce24c970d6a068f8bc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464186"
---
# <a name="person"></a>Физическое лицо

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность физического лица для Dynamics 365 Human Resources.

Физическое имя: mshr_dirpersonentity

### <a name="description"></a>описание

Эта сущность предоставляет личные сведения для лица, которое является кандидатом.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности физического лица**<br>mshr_dirpersonentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой | Созданный системой уникальный идентификатор записи сущности. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Только для чтения<br>Требуется<br>Создано системой | Созданный системой уникальный идентификатор для физического лица, удобный для восприятия пользователем.  |
| **ФИО**<br>mshr_name<br>*Строка* | Только для чтения<br>Требуется | Значение поля является объединением имени, отчества, префикса фамилии и фамилии в заказе, указанном в поле **Отображать последовательность имен как**. |
| **Псевдоним имени**<br>mshr_namealias<br>*Строка* | Чтение/запись<br>Необязательный | Псевдоним имени, который может быть указан для физического лица. |
| **Известен как**<br>mshr_knownas<br>*Строка* | Чтение/запись<br>Необязательный | Имя, которое может использоваться для физического лица, если оно обычно известно под другим именем. |
| **Код языка**<br>mshr_languageid<br>*Строка* | Чтение/запись<br>Необязательный | Код языка основного языка физического лица, как определено в формате ISO 639-1. |
| **Адресные книги**<br>mshr_addressbooks<br>*Строка* | Чтение/запись<br>Необязательный | Адресная книга, которой может быть назначено физическое лицо. Адресные книги, настроенные для организации, перечисляются в сущности mshr_diraddressbooksentity. |
| **День юбилея**<br>mshr_anniversaryday<br>*Int* | Чтение/запись<br>Необязательный | День юбилея физического лица. |
| **Месяц юбилея**<br>mshr_anniversarymonth<br>*набор параметров mshr_monthsofyear* | Чтение/запись<br>Необязательный | Месяц юбилея физического лица. |
| **Год юбилея**<br>mshr_anniversaryyear<br>*Int* | Чтение/запись<br>Необязательный | Год юбилея физического лица. |
| **День рождения**<br>mshr_birthday<br>*Int* | Чтение/запись<br>Необязательный | День рождения физического лица. |
| **Месяц рождения**<br>mshr_birthmonth<br>*набор параметров mshr_monthsofyear* | Чтение/запись<br>Необязательный | Месяц рождения физического лица. |
| **Год рождения**<br>mshr_birthyear<br>*Int* | Чтение/запись<br>Необязательный | Год рождения физического лица. |
| **Имена детей**<br>mshr_childrennames<br>*Строка* | Чтение/запись<br>Необязательный | Строка для имен детей данного физического лица. Нет обязательного разграничения. |
| **Род**<br>mshr_gender<br>*набор параметров mshr_hcmpersongender* | Чтение/запись<br>Необязательный | Пол физического лица. |
| **Хобби**<br>mshr_hobbies<br>*Строка* | Чтение/запись<br>Необязательный | Хобби физического лица. |
| **Инициалы**<br>mshr_initials<br>*Строка* | Чтение/запись<br>Необязательный | Инициалы имени физического лица. |
| **Семейное положение**<br>mshr_maritalstatus<br>*набор параметров mshr_hcmpersonmaritalstatus* | Чтение/запись<br>Необязательный | Семейное положение физического лица. |
| **Фонетическое имя**<br>mshr_phoneticfirstname<br>*Строка* | Чтение/запись<br>Необязательный | Фонетическая транскрипция имени физического лица. |
| **Фонетическая фамилия**<br>mshr_phoneticlastname<br>*Строка* | Чтение/запись<br>Необязательный | Фонетическая транскрипция фамилии физического лица. |
| **Фонетическое отчество**<br>mshr_phoneticmiddlename<br>*Строка* | Чтение/запись<br>Необязательный | Фонетическая транскрипция фамилии физического лица. |
| **Личный суффикс**<br>mshr_personalsuffix<br>*Строка* | Чтение/запись<br>Необязательный | Личный суффикс физического лица. Допустимые значения в сущности mshr_dirnameaffixentity, где mshr_type имеет значение Suffix (200000001). |
| **Обращение**<br>mshr_personaltitle<br>*Строка* | Чтение/запись<br>Необязательный | Личное обращение для данного физического лица. Допустимые значения в сущности mshr_dirnameaffixentity, где mshr_type имеет значение Title (200000000).
| **Профессиональный суффикс**<br>mshr_professionalsuffix<br>*Строка* | Чтение/запись<br>Необязательный | Профессиональный суффикс. |
| **Должность**<br>mshr_professionaltitle<br>*Строка* | Чтение/запись<br>Необязательный | Должность. |
| **Полный основной адрес**<br>mshr_fullprimaryaddress<br>*Строка* | Чтение/запись<br>Необязательный | Полный основной адрес физического лица, объединение полей основного адреса. |
| **Адрес: город**<br>mshr_addresscity<br>*Строка* | Чтение/запись<br>Необязательный | Город основного адреса физического лица. Настройте в сущности mshr_logisticsaddresscityentity. |
| **Страна и регион адреса**<br>mshr_addresscountryregionid<br>*Строка* | Чтение/запись<br>Необязательный | Страна/регион основного адреса физического лица. Допустимые значения в сущности mshr_logisticsaddresscountryregionentity. |
| **Код ISO страны и региона адреса**<br>mshr_addresscountryregionisocode<br>*Строка* | Чтение/запись<br>Необязательный | Код ISO страны/региона основного адреса физического лица. |
| **Страна адреса**<br>mshr_addresscounty<br>*Строка* | Чтение/запись<br>Необязательный | Страна основного адреса физического лица. Настройте в сущности mshr_logisticsaddresscountyentity. |
| **Название района адреса**<br>mshr_addressdistrictname<br>*Строка* | Чтение/запись<br>Необязательный | Район основного адреса физического лица. Настройте в сущности mshr_logisticsaddressdistrictentity. |
| **Широта адреса**<br>mshr_addresslatitude<br>*Строка* | Чтение/запись<br>Необязательный | Широта основного адреса физического лица. |
| **Код местонахождения адреса**<br>mshr_addresslocationid<br>*Строка* | Чтение/запись<br>Необязательный | Уникальный идентификатор местоположения основного адреса физического лица. Допустимые значения в сущности mshr_logisticspostaladdresslocationcdsentity. |
| **Роли местонахождения адреса**<br>mshr_addresslocationroles<br>*Строка* | Чтение/запись<br>Необязательный | Роль местоположения основного адреса физического лица. Настройте в сущности mshr_logisticslocationrolecdsentity. |
| **Долгота адреса**<br>mshr_addresslongitude<br>*Строка* |  Чтение/запись<br>Необязательный | Долгота основного адреса физического лица. |
| **Состояние адреса**<br>mshr_addressstate<br>*Строка* | Чтение/запись<br>Необязательный | Состояние основного адреса физического лица. Настройте в сущности mshr_logisticsaddressstateentity. |
| **Улица в адресе**<br>mshr_addressstreet<br>*Строка* | Чтение/запись<br>Необязательный | Улица основного адреса физического лица. |
| **Адрес действителен с**<br>mshr_addressvalidfrom<br>*Дата* | Чтение/запись<br>Необязательный | Дата, с которой основной адрес физического лица является действительным. |
| **Адрес действителен по**<br>mshr_addressvalidto<br>*Дата* | Чтение/запись<br>Необязательный | Дата, по которую основной адрес физического лица является действительным. |
| **Почтовый индекс адреса**<br>mshr_addresszipcode<br>*Строка* | Чтение/запись<br>Необязательный | Почтовый код основного адреса физического лица. Настройте в сущности mshr_logisticsaddresspostalcodeentity. |
| **Адрес является частным**<br>mshr_addressisprivate<br>*набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Определяет, является ли основной адрес физического лица общим для других сотрудников организации. |
| **Описание адреса**<br>mshr_addressdescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание основного адреса физического лица. |
| **Основной контактный адрес электронной почты**<br>mshr_primarycontactemail<br>*Строка* | Чтение/запись<br>Необязательный | Основной адрес электронной почты физического лица. |
| **Описание основного контактного адреса электронной почты**<br>mshr_primarycontactemaildescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставляемое для основного адреса электронной почты. |
| **Основной контактный адрес электронной почты является IM**<br>mshr_primarycontactemailisim<br>*набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Определяет, доступен ли основной адрес электронной почты для мгновенных сообщений. |
| **Назначение основного контактного адреса электронной почты**<br>mshr_primarycontactemailpurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основного адреса электронной почты. Настройте в сущности mshr_logisticslocationroleentity. |
| **Основной контактный факс**<br>mshr_primarycontactfax<br>*Строка* | Чтение/запись<br>Необязательный | Номер основного факса. |
| **Описание основного контактного факса**<br>mshr_primarycontactfaxdescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставляемое для основного номера факса. |
| **Добавочный номер основного контактного факса**<br>mshr_primarycontactfaxextension<br>*Строка* | Чтение/запись<br>Необязательный | Добавочный номер для основного номера факса. |
| **Назначение основного контактного факса**<br>mshr_primarycontactfaxpurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основного номера факса. Настройте в сущности mshr_logisticslocationroleentity.
| **Основной контактный телефон**<br>mshr_primarycontactphone<br>*Строка* | Чтение/запись<br>Необязательный | Номер основного телефона. |
| **Описание основного контактного телефона**<br>mshr_primarycontactphonedescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставляемое для основного номера телефона. |
| **Добавочный номер основного контактного телефона**<br>mshr_primarycontactphoneextension<br>*Строка* | Чтение/запись<br>Необязательный | Добавочный номер для основного номера телефона. |
| **Основной контактный телефон является мобильным**<br>mshr_primarycontactphoneismobile<br>*набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Определяет, является ли основной номер телефона мобильным телефоном. |
| **Назначение основного контактного телефона**<br>mshr_primarycontactphonepurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основного номера телефона. Настройте в сущности mshr_logisticslocationroleentity. |
| **Основной контактный телекс**<br>mshr_primarycontacttelex<br>*Строка* | Чтение/запись<br>Необязательный | Номер основного телекса. |
| **Описание основного контактного телекса**<br>mshr_primarycontacttelexdescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставляемое для основного номера телекса физического лица. |
| **Назначение основного контактного телекса**<br>mshr_primarycontacttelexpurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основного номера телекса физического лица. Настройте в сущности mshr_logisticslocationroleentity. |
| **Основной контактный URL-адрес**<br>mshr_primarycontacturl<br>*Строка* | Чтение/запись<br>Необязательный | Основной URL-адрес. |
| **Описание основного контактного URL-адреса**<br>mshr_primarycontacturldescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставленное для основного URL-адреса физического лица. |
| **Назначение основного контактного URL-адреса**<br>mshr_primarycontacturldescription<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основного URL-адреса физического лица. Настройте в сущности mshr_logisticslocationroleentity. |
| **Основной контактный Facebook**<br>mshr_primarycontactfacebook<br>*Строка* | Чтение/запись<br>Необязательный | Основная учетная запись Facebook. Идентифицируется кодом пользователя. |
| **Описание основного контактного адреса Facebook**<br>mshr_primarycontactfacebookdescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставленное для основной учетной записи Facebook физического лица. |
| **Основная контактная учетная запись Facebook является частной**<br>mshr_primarycontactfacebookisprivate<br>*набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Определяет, будет ли основная учетная запись Facebook видимой для других пользователей. |
| **Назначение основной контактной учетной записи Facebook**<br>mshr_primarycontactfacebookpurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основной учетной записи Facebook физического лица. Настройте в сущности mshr_logisticslocationroleentity. |
| **Основная контактная LinkedIn**<br>mshr_primarycontactlinkedin<br>*Строка* | Чтение/запись<br>Необязательный | Основная учетная запись LinkedIn. Идентифицируется по имени пользователя. |
| **Описание основной контактной учетной записи LinkedIn**<br>mshr_primarycontactlinkedindescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставленное для основной учетной записи LinkedIn физического лица. |
| **Основная контактная учетная запись LinkedIn является частной**<br>mshr_primarycontactlinkedinisprivate<br>*набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Определяет, предоставлен ли общий доступ к информации об основной учетной записи LinkedIn для других пользователей. |
| **Назначение основной контактной учетной записи LinkedIn**<br>mshr_primarycontactlinkedinpurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основной учетной записи LinkedIn физического лица. Настройте в сущности mshr_logisticslocationroleentity. |
| **Основная контактная учетная запись Twitter**<br>mshr_primarycontacttwitter<br>*Строка* | Чтение/запись<br>Необязательный | Основная учетная запись Twitter данного физического лица. Идентифицируется по @username. |
| **Описание основной контактной учетной записи Twitter**<br>mshr_primarycontacttwitterdescription<br>*Строка* | Чтение/запись<br>Необязательный | Описание, предоставленное для основной учетной записи Twitter физического лица. |
| **Основная контактная учетная запись Twitter является частной**<br>mshr_primarycontacttwitterisprivate<br>*набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Определяет, предоставлен ли общий доступ к информации об основной учетной записи Twitter для других пользователей. |
| **Назначение основной контактной учетной записи Twitter**<br>mshr_primarycontacttwitterpurpose<br>*Строка* | Чтение/запись<br>Необязательный | Назначение для основной учетной записи Twitter физического лица. Настройте в сущности mshr_logisticslocationroleentity. |
| **Тип субъекта**<br>mshr_partytype<br>*Строка* | Чтение/запись<br>Необязательный | Тип субъекта для данного физического лица. Всегда будет иметь значение **Физическое лицо** для кандидатов. |
| **Отображать последовательность имен как**<br>mshr_namesequencedisplayas<br>*Строка* | Чтение/запись<br>Необязательный | Последовательность, в которой свойства имени физического лица объединяются в значение свойства "Имя" (mshr_name). |
| **Имя**<br>mshr_firstname<br>*Строка* | Чтение/запись<br>Требуется | Имя физического лица. |
| **Отчество**<br>mshr_middlename<br>*Строка* | Чтение/запись<br>Необязательный | Отчество физического лица. |
| **Префикс фамилии**<br>mshr_lastnameprefix<br>*Строка* | Чтение/запись<br>Необязательный | Префикс фамилии физического лица. |
| **Фамилия**<br>mshr_lastname<br>*Строка* | Чтение/запись<br>Необязательный | Фамилия физического лица. |
| **Код электронного местоположения**<br>mshr_electroniclocationid<br>*Строка* | Чтение/запись<br>Необязательный | Код электронного местоположения физического лица. |
| **Часовой пояс адреса**<br>mshr_addresstimezone<br>*Int* | Чтение/запись<br>Необязательный | Часовой пояс основного адреса физического лица. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]