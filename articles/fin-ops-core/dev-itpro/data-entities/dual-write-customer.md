---
title: Интегрированный мастер клиентов
description: В этом разделе описывается интеграция данных клиентов между Finance and Operations и Common Data Service.
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
ms.openlocfilehash: a66beb6338ea593247c79a11feb7f301d56f32a9
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572526"
---
# <a name="integrated-customer-master"></a>Интегрированный мастер клиентов

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Это типично для записей клиентов, что они обрабатываются в нескольких приложениях. Например, деятельность по продажам может использовать записи коммерческих клиентов через приложение Sales, а электронная коммерция или розничные продажи могут использовать записи клиентов через приложение Finance and Operations. Независимо от того, откуда берет начало запись клиента, она интегрируется за кулисами вне зависимости от границ приложений и различий в инфраструктуре. Интегрированная обработка клиентов помогает обрабатывать сценарии мультимастеринга и обеспечивает полное представление клиентов для набора приложений Dynamics 365.

## <a name="customer-data-flow"></a>Поток данных клиентов

*Клиент* — это хорошо определенная концепция в приложениях. Таким образом, интеграция данных клиентов просто включает в себя согласование концепции клиента между двумя приложениями. На следующем рисунке показан поток данных клиентов.

![Поток данных клиентов](media/dual-write-customer-data-flow.png)

Клиенты могут быть широко классифицированы на два типа: коммерческие/организационные клиенты и потребители/конечные пользователи. Эти два типа клиентов хранятся и обрабатываются по-разному в Finance and Operations и Common Data Service.

В Finance and Operations как коммерческие/организационные клиенты, так и потребители/конечные пользователи обрабатываются в одной таблице, которая называется **CustTable** (CustomerCustomerV3Entity), и классифицируются на основе атрибута **Тип**. (Если для параметра **Тип** задано значение **Организация**, клиент является коммерческим/организационным клиентом, а если для параметра **Тип** задано значение **Физическое лицо**, то клиент является потребителем/конечным пользователем.) Информация об основном контактном лице обрабатывается через сущность SMMContactPersonEntity.

В Common Data Service коммерческие/организационные клиенты обрабатываются в сущности "Организация" и идентифицируются в качестве клиентов, когда атрибут **RelationshipType** имеет значение **Клиент**. Как потребители/конечные пользователи, так и контактное лицо представлены сущностью "Контакт". Чтобы обеспечить четкое разделение между потребителем/конечным пользователем и контактным лицом, сущность **Контакт** имеет флаг типа Boolean, который называется **Для продажи**. Когда параметр **Для продажи** имеет значение **True**, контакт является потребителем/конечным пользователем, и для этого контакта могут быть созданы предложения с расценками и заказы. Когда параметр **Для продажи** имеет значение **False**, контакт является просто основным контактным лицом клиента.

Когда контакт, для которого невозможны продажи, участвует в процессе предложений с расценками или заказа, для параметра **Для продажи** устанавливается значение **True**, чтобы пометить контакт как контакт для продажи. Контакт, который стал контактом для продажи, остается контактом для продажи.

## <a name="templates"></a>Шаблоны

Данные о клиентах включают всю информацию о клиенте, например, группу клиентов, адреса, контактную информацию, профиль платежа, профиль счета-фактуры и статус лояльности. Коллекция сопоставлений сущностей работает совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

Приложения Finance and Operations    | Другие приложения Dynamics 365
--------------------------|---------------------------------
Клиент V3               | Счет
Клиент V3               | Контакт
Контакты CDS V2           | Контакт
Группы клиентов           | Msdyn\_customergroups
Способ оплаты клиента   | Msdyn\_customerpaymentmethods
Карта лояльности              | Msdyn\_loyaltycards
График платежей          | Msdyn\_paymentschedules
График платежей          | Msdyn\_paymentschedulelines
Платежный день CDS           | Msdyn\_paymentdays
Строки платежных дней CDS     | Msdyn\_paymentdaylines
Условия оплаты          | Msdyn\_paymentterms
Аффиксы имен              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Клиент V3 в организацию

Этот шаблон синхронизирует основную информацию о клиентах для коммерческих и организационных клиентов между приложениями Finance and Operations и Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | наименование
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | Факс
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
САЛЕСЕМО | = | описание
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | нет
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
нет | \>\> | address1\_addresstypecode
нет | \>\> | customertypecode
PARTYTYPE | \<\< | нет
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Контакт V3 в контакт

Этот шаблон синхронизирует основные данные о потребителях и конечных пользователей между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
нет | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | нет
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | нет
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | нет
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
нет | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
нет | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
нет | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | Факс
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
САЛЕСЕМО | = | описание

## <a name="contacts"></a>Контакты

Этот шаблон синхронизирует все сведения об основных, вторых и третьих контактах как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-contacts.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | нет
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | Факс
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | отдел
NOTES | = | описание
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
нет | \>\> | msdyn\_contactforvendor
нет | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Группы клиентов

Этот шаблон синхронизирует информацию о группах клиентов между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-customer-groups.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
ОПИСАНИЕ | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Способы оплаты клиентов

Этот шаблон синхронизирует информацию о способе платежа клиентов между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
НАИМЕНОВАНИЕ | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ОПИСАНИЕ | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Карты лояльности

Этот шаблон синхронизирует информацию о карте лояльности клиента между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Графики оплаты

Этот шаблон синхронизирует ссылочные данные графиков оплаты как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-payment-schedules.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
НАИМЕНОВАНИЕ | = | msdyn\_name
ОПИСАНИЕ | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Строки графика платежей

Синхронизация ссылочные данные строк графиков оплаты как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Платежные дни

Этот шаблон синхронизирует ссылочные данные платежных дней как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-payment-days.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
НАИМЕНОВАНИЕ | = | msdyn\_name
ОПИСАНИЕ | = | msdyn\_description

## <a name="payment-day-lines"></a>Строки платежных дней

Этот шаблон синхронизирует ссылочные данные строк платежных дней как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
НАИМЕНОВАНИЕ | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Сроки оплаты

Этот шаблон синхронизирует ссылочные данные условий оплаты (условия оплаты) как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-payment-terms.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
ОПИСАНИЕ | = | msdyn\_description
НАИМЕНОВАНИЕ | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Аффиксы имен

Этот шаблон синхронизирует ссылочные данные аффиксов имен как для клиентов, так и для поставщиков, между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![](media/dual-write-name-affixes.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
AFFIX | = | msdyn\_affix
ТИП | \>\< | msdyn\_affixtype
ОПИСАНИЕ | = | msdyn\_description
