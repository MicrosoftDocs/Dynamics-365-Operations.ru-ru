---
title: Интегрированный мастер клиентов
description: Эта тема описывает интеграцию данных клиента между Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5af584eb0bdb65942921847219b46b8f93dae79d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350919"
---
# <a name="integrated-customer-master"></a>Интегрированный справочник клиентов

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Данные клиентов могут обрабатываться в нескольких приложениях Dynamics 365. Например, строка клиента может быть получена через действия продажи в Dynamics 365 Sales (приложение на основе модели в Dynamics 365) или строка может происходить из розничной деятельности в Dynamics 365 Commerce (приложение Finance and Operations). Вне зависимости от того, где созданы данные клиента, они интегрируются в фоновом режиме. Интегрированная главная база данных клиентов предоставляет гибкие возможности контролировать данные клиентов в любом приложении Dynamics 365 и обеспечивает полное представление клиента во всем наборе приложений Dynamics 365.

## <a name="customer-data-flow"></a>Поток данных клиентов

*Клиент* — это хорошо определенная концепция в приложениях. Таким образом, интеграция данных клиентов просто включает в себя согласование концепции клиента между двумя приложениями. На следующем рисунке показан поток данных клиентов.

![Поток данных клиентов.](media/dual-write-customer-data-flow.png)

Клиенты могут быть широко классифицированы на два типа: коммерческие/организационные клиенты и потребители/конечные пользователи. Эти два типа клиентов хранятся и обрабатываются по-разному в Finance and Operations и Dataverse.

В Finance and Operations как коммерческие/организационные клиенты, так и потребители/конечные пользователи обрабатываются в одной таблице, которая называется **CustTable** (CustCustomerV3Entity), и классифицируются на основе атрибута **Тип**. (Если для параметра **Тип** задано значение **Организация**, клиент является коммерческим/организационным клиентом, а если для параметра **Тип** задано значение **Физическое лицо**, то клиент является потребителем/конечным пользователем.) Информация об основном контактном лице обрабатывается через таблицу SMMContactPersonEntity.

В Dataverse коммерческие/организационные клиенты обрабатываются в таблице "Организация" и идентифицируются в качестве клиентов, когда атрибут **RelationshipType** имеет значение **Клиент**. Как потребители/конечные пользователи, так и контактное лицо представлены таблицей "Контакт". Чтобы обеспечить четкое разделение между потребителем/конечным пользователем и контактным лицом, таблица **Контакт** имеет флаг типа Boolean, который называется **Для продажи**. Когда параметр **Для продажи** имеет значение **True**, контакт является потребителем/конечным пользователем, и для этого контакта могут быть созданы предложения с расценками и заказы. Когда параметр **Для продажи** имеет значение **False**, контакт является просто основным контактным лицом клиента.

Когда контакт, для которого невозможны продажи, участвует в процессе предложений с расценками или заказа, для параметра **Для продажи** устанавливается значение **True**, чтобы пометить контакт как контакт для продажи. Контакт, который стал контактом для продажи, остается контактом для продажи.

## <a name="templates"></a>Шаблоны

Данные о клиентах включают всю информацию о клиенте, например, группу клиентов, адреса, контактную информацию, профиль платежа, профиль счета-фактуры и статус лояльности. Коллекция сопоставлений таблиц работает совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

Приложения Finance and Operations | Другие приложения Dynamics 365         | Описание
----------------------------|---------------------------------|------------
Контакты CDS V2             | контакты                        | Этот шаблон синхронизирует все первичные, вторичные и третичные контактные данные клиентов и поставщиков.
Группы клиентов             | msdyn_customergroups            | Этот шаблон синхронизирует сведения о группах клиентов.
Способ оплаты клиента     | msdyn_customerpaymentmethods    | Этот шаблон синхронизирует сведения о способах оплаты клиентов.
Клиенты V3                | счета                        | Этот шаблон синхронизирует основную информацию о клиентах для коммерческих и организационных клиентов.
Клиенты V3                | контакты                        | Этот шаблон синхронизирует справочник клиентов для клиентов и конечных пользователей.
Аффиксы имен                | msdyn_nameaffixes               | Этот шаблон синхронизирует ссылочные данные аффиксов имен как для клиентов, так и для поставщиков.
Строки платежных дней CDS V2    | msdyn_paymentdaylines           | Этот шаблон синхронизирует ссылочные данные строк дней оплаты как для клиентов, так и для поставщиков.
Платежные дни CDS            | msdyn_paymentdays               | Этот шаблон синхронизирует ссылочные данные дней оплаты как для клиентов, так и для поставщиков.
Строки графика платежей      | msdyn_paymentschedulelines      | Синхронизирует ссылочные данные строк графиков оплаты как для клиентов, так и для поставщиков.
График оплаты            | msdyn_paymentschedules          | Этот шаблон синхронизирует ссылочные данные графиков оплаты как для клиентов, так и для поставщиков.
Условия оплаты            | msdyn_paymentterms              | Этот шаблон синхронизирует ссылочные данные условий оплаты (условия оплаты) как для клиентов, так и для поставщиков.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]