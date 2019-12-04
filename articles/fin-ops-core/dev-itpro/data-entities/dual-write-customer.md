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
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769691"
---
# <a name="integrated-customer-master"></a>Интегрированный мастер клиентов

[!include [banner](../includes/banner.md)]

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

Приложения Finance and Operations | Другие приложения Dynamics 365         | Описание
----------------------------|---------------------------------|------------
Контакты CDS V2             | контакты                        | Этот шаблон синхронизирует все первичные, вторичные и третичные контактные данные клиентов и поставщиков.
Группы клиентов             | msdyn_customergroups            | Этот шаблон синхронизирует сведения о группах клиентов.
Способ оплаты клиента     | msdyn_customerpaymentmethods    | Этот шаблон синхронизирует сведения о способах оплаты клиентов.
Клиенты V3                | счета                        | Этот шаблон синхронизирует основную информацию о клиентах для коммерческих и организационных клиентов.
Клиенты V3                | контакты                        | Этот шаблон синхронизирует справочник клиентов для клиентов и конечных пользователей.
Карта постоянного клиента                | msdyn_loyaltycards              | Этот шаблон синхронизирует сведения о картах лояльности клиентов.
Аффиксы имен                | msdyn_nameaffixes               | Этот шаблон синхронизирует ссылочные данные аффиксов имен как для клиентов, так и для поставщиков.
Строки платежных дней CDS V2    | msdyn_paymentdaylines           | Этот шаблон синхронизирует ссылочные данные строк дней оплаты как для клиентов, так и для поставщиков.
Платежные дни CDS            | msdyn_paymentdays               | Этот шаблон синхронизирует ссылочные данные дней оплаты как для клиентов, так и для поставщиков.
Строки графика платежей      | msdyn_paymentschedulelines      | Синхронизирует ссылочные данные строк графиков оплаты как для клиентов, так и для поставщиков.
График оплаты            | msdyn_paymentschedules          | Этот шаблон синхронизирует ссылочные данные графиков оплаты как для клиентов, так и для поставщиков.
Условия оплаты            | msdyn_paymentterms              | Этот шаблон синхронизирует ссылочные данные условий оплаты (условия оплаты) как для клиентов, так и для поставщиков.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
