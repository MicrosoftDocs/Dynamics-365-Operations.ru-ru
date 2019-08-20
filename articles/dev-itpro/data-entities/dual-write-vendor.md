---
title: Интегрированный мастер поставщиков
description: Эта тема описывает интеграцию данных поставщиков между Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789235"
---
## <a name="integrated-vendor-master"></a>Интегрированный мастер поставщиков

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Термин *поставщик* относится к организации-поставщику или индивидуальному предпринимателю, который является частью процесса цепочки поставок и поставляет товары для бизнеса. Хотя *поставщик* является устоявшейся концепцией в Microsoft Dynamics 365 for Finance and Operations, концепция поставщика не существует в Dynamics 365 for Customer Engagement. Вместо этого некоторые предприятия перегружают сущность организации для хранения как информации о клиентах, так и в информации о поставщиках. Другие компании используют пользовательскую концепцию поставщика. Интеграция Common Data Service поддерживает оба подхода. Таким образом, вы можете включить любой из дизайнов, в зависимости от вашего бизнес-сценария.

Интеграция данных поставщиков между Finance and Operations и Customer Engagement позволяет обрабатывать данные в нескольких местах. Независимо от того, откуда поступают данные поставщика, они интегрируются за кулисами вне зависимости от границ приложений и различий в инфраструктуре. 

### <a name="vendor-data-flow"></a>Поток данных поставщика

Если вы хотите использовать Customer Engagement для обработки поставщиков и хотите изолировать информацию о поставщиках от информации о клиентах, вы можете использовать новый дизайн поставщика.

![Поток данных поставщика](media/dual-write-vendor-data-flow.png)

Если вы хотите использовать Customer Engagement для обработки поставщиков и хотите продолжать использовать сущность "Организация" для хранения информации о поставщиках, вы можете использовать новый расширенный дизайн поставщика. В этом дизайне расширенная информация о поставщиках, например группа поставщиков и профиль разноски поставщиков, хранятся в подробных сведениях о поставщике.

![Поток расширенных данных поставщика](media/dual-write-vendor-detail.jpg)

Контактная информация поставщика напоминает контактную информацию клиента. За кулисами информация контактного лица хранится и извлекается из одних и тех же сущностей.

## <a name="templates"></a>Шаблоны

Данные о поставщиках включают всю информацию о поставщике, например, группу поставщиков, адреса, контактную информацию, профиль платежа и профиль счета-фактуры. Коллекция сопоставлений сущностей работает совместно во время взаимодействия данных о поставщиках, как показано в следующей таблице.

Finance and Operations  | Приложение Customer Engagement
------------------------|---------------------------------
Поставщик V2               | Счет
Поставщик V2               | Msdyn\_vendors
Контакты CDS V2         | Контакт
Группы поставщиков           | Msdyn\_vendorgroups
Метод платежа поставщика   | Msdyn\_vendorpaymentmethods
График платежей        | Msdyn\_paymentschedules
График платежей        | Msdyn\_paymentschedulelines
Платежный день CDS         | Msdyn\_paymentdays
Строки платежных дней CDS   | Msdyn\_paymentdaylines
Условия оплаты        | Msdyn\_paymentterms
Аффиксы имен            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Поставщик V2 и организация 

Предприятия, которые используют сущность организации для хранения информации о поставщиках, могут продолжать использовать ее таким же образом. Они также могут воспользоваться явной функциональностью поставщика, которая появляется из-за интеграции с Finance and Operations.

## <a name="vendor-v2-and-msdyn_vendors"></a>Поставщик V2 и Msdyn\_vendors

Компании, которые используют пользовательское решение для поставщиков, могут воспользоваться готовой концепцией поставщиков, которая вводится в Common Data Service из-за интеграции с Finance and Operations. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Контакты

Этот шаблон синхронизирует все сведения об основных, вторых и третьих контактах как для клиентов, так и для поставщиков, между Finance and Operations и Customer Engagement. Для получения подробной информации о сопоставлении объектов см. в разделе [Интегрированный мастер клиентов](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Группы поставщиков

Этот шаблон синхронизирует информацию о группах поставщиков между Finance and Operations и Customer Engagement.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
ОПИСАНИЕ | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Метод платежа поставщикам

Этот шаблон синхронизирует информацию о способах оплаты поставщикам между Finance and Operations и Customer Engagement.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
НАИМЕНОВАНИЕ | = | msdyn\_name
ОПИСАНИЕ | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

