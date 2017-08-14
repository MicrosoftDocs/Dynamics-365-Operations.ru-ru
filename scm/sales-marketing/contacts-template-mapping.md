---
title: "Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации контакта (контакты) и контакта (клиенты) из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации объектов "Контакт" (контакты) и "Контакт" (клиенты) из Microsoft Dynamics 365 for Sales (Sales) с Microsoft Dynamics 365 for Finance and Operations , выпуск Enterprise, (Finance and Operations).

## <a name="templates-and-tasks"></a>Шаблоны и задачи

Следующие шаблоны и базовые задачи используются для синхронизации объекта "Контакт" (контакты) в Sales с объектом "Контакт" (клиенты) в Finance and Operations:

- **Имена шаблонов:**

    - Контакты в контакт (Sales в Fin and Ops)
    - Контакты в клиента (Sales в Fin and Ops)

- **Имена задач в проекте:**

    - Контактные лица
    - ContactToCustomer

Следующая задача синхронизации необходима до синхронизации контактов: счета (Sales в Fin and Ops)

## <a name="entity-sets"></a>Наборы объектов

| Прод.    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Контактные лица | Контакт | Контакты CDS           |
| Контактные лица | Учетная запись | Клиенты V2           |

## <a name="entity-flow"></a>Поток объектов

Контакты управляются в Sales и синхронизируются с Common Data Service (CDS) и Finance and Operations.

Контакт в Sales может стать контактом в CDS и Finance and Operations. Либо он может стать счетом в CDS и клиентом в Finance and Operations. Для определения того, должен ли контакт извлекаться из Sales для синхронизации с CDS и Finance and Operations (например, контакты из Sales &gt; контакт в CDS &gt; контакты в Finance and Operations), система рассматривает следующие свойства контакта в Sales:

- **Синхронизация со счетом в CDS и клиентом в Finance and Operations:** контакты, параметр **Является активным клиентом** которых имеет значение **Да**.
- **Синхронизация с контактом в CDS и контактом в Finance and Operations:** контакты, для параметра **Является активным клиентом** которых задано значение **Нет**, и параметр **Компания** (родительский счет/контакт) указывает на счет (не контакт).

## <a name="prospect-to-cash-solution-for-sales"></a>Решение "Перспективный клиент в наличные деньги" для Sales 

Новое поле **Является активным клиентов** добавлено к контакту. Это поле используется для разделения контактов, имеющих мероприятия по продаже, и контактов, не имеющих мероприятия по продаже. В поле **Является активным клиентов** установлено значение **Да** только для контактов, с которыми связаны предложения, заказы или счета. Только эти контакты синхронизируются с Finance and Operations как клиенты.

Новое поле **IsCompanyAnAccount** добавлено к контакту. Это поле используется для указания того, связан ли контакт с компанией (родительским счетом/контактом) типа **Счет**. Эта информация используется для определения контактов, которые должны синхронизироваться с Finance and Operations как контакты.

Новое поле **Номер контакта** добавлено к контакту для предоставления естественного и уникального ключа для интеграции. Когда создается новый контакт, значение **Номер контакта** обновляется автоматически с использованием номерной серии. Значение состоит из **CON**, после чего следует увеличивающая номерная серия и суффикс из шести символов. Пример: **CON-01000-BVRCPS**

При добавлении решения интеграции для Sales в Sales сценарий обновления задает значение в поле **Номер контакта** для существующих контактов с использованием номерной серии, как описано выше. Сценарий обновления также задает для поля **Является активным клиентом** значение **Да** для всех контактов, имеющие мероприятия по продажам.

## <a name="in-finance-and-operations"></a>В Finance and Operations 

Контакты, помеченные с помощью свойства **IsContactPersonExternallyMaintained**. Это свойство указывает, что данный контакт ведется извне. В этом случае контакты, ведение которых выполняется извне, ведутся в Sales.

## <a name="preconditions-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

### <a name="contact-to-contact"></a>Контакт в контакт

- Обновите **Код организации CDS** в сопоставлении **Источник &gt; CDS**.

    - Значение шаблона по умолчанию для **Organization_OrganizationId [Organization ID]** — **ORG001**.
    - Значение шаблона по умолчанию для **PrimaryAccount_Organization_OrganizationId [Organization ID]** — **ORG001**.

- Поле **Код страны/региона адреса** является обязательным в Finance and Operations. Чтобы избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении **CDS &gt; Операции**. Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales. Значение шаблона по умолчанию для **PrimaryAddressCountryRegionISOCode** — **США**.
- Убедитесь, что значение в следующем поле существует в Finance and Operations. Если информация не требуется в Finance and Operations, можно удалить сопоставление из сопоставления **CDS &gt; Место назначения**.

    - **Имя поля в Finance and Operations:** "Решение"
    - **Сопоставление:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Контакт в клиента

- Обновите **Код организации CDS** в сопоставлении **Источник &gt; CDS**. Значение шаблона по умолчанию для **Organization_OrganizationId [Organization ID]** — **ORG001**.
- Поле **Код страны/региона адреса** является обязательным в Finance and Operations. Чтобы избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении **CDS &gt; Место назначения**. Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales. Значение шаблона по умолчанию для **PrimaryAddressCountryRegionISOCode** — **США**.
- Поле **CustomerGroup** является обязательным в Finance and Operations. Чтобы избежать ошибок синхронизации, можно указать значение по умолчанию в сопоставлении **CDS &gt; Место назначения**. Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales. Значение шаблона по умолчанию для **CustomerGroupId** — **10**.
- Добавляя следующие сопоставления из **CDS &gt; Место назначения**, можно уменьшить число обновлений вручную в Finance and Operations. Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.

    - **SiteId** — сайт по умолчанию также может быть определен в продуктах в Finance and Operations. Сайт необходим для создания предложений и заказов на продажу в Finance and Operations. Значение шаблона для **SiteId** не определено.
    - **WarehouseId** — склад по умолчанию также может быть определен в продуктах в Finance and Operations. Склад необходим для создания предложений и заказов на продажу в Finance and Operations. Значение шаблона для **WarehouseId** не определено.
    - **LanguageId** — язык необходим для создания предложений и заказов на продажу в Finance and Operations. Значение шаблона по умолчанию для **LanguageId** — **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Сопоставление шаблона в интеграторе данных

На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.

### <a name="contact-to-contact"></a>Контакт в контакт

![Сопоставление шаблона в интеграторе данных](./media/contacts-template-mapping-data-integrator-1.png)

![Сопоставление шаблона для контактов в интеграторе данных](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Контакт в клиента

![Сопоставление шаблона в интеграторе данных](./media/contacts-template-mapping-data-integrator-3.png)

![Сопоставление шаблона для контактов в интеграторе данных](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Связанные разделы

[Синхронизация продуктов из Finance and Operations с продуктами в Sales](products-template-mapping.md)

[Синхронизация контактов из Sales с клиентами в Finance and Operations](accounts-template-mapping.md)

[Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations](sales-quotation-template-mapping.md)

