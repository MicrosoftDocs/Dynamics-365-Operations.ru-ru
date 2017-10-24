---
title: "Синхронизация контактов из Sales с клиентами в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации счетов из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Синхронизация контактов из Sales с клиентами в Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration). 

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации счетов из Microsoft Dynamics 365 for Sales (Sales) с Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise, (Finance and Operations).

## <a name="template-and-task"></a>Шаблон и задача

Следующие шаблоны и базовые задачи используются для синхронизации счетов из Sales с Finance and Operations:

- **Имя шаблона:** счета (Sales в Fin and Ops)
- **Имя задачи в проекте:** Счета — Счет — Клиенты

Синхронизацию задач требуется выполнить до синхронизации счета/клиента: нет

## <a name="entity-set"></a>Набор объектов

| Прод.    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Счета | Учетная запись | Клиенты              |

## <a name="entity-flow"></a>Поток объектов

Счета управляются в Sales и синхронизируются с Finance and Operations как клиенты. Свойство **Управляется извне** этих клиентов имеет значение **Да** для отслеживания клиентов, которые создаются в Sales. Во время выставления накладных эта информация используется для фильтрации накладных, которые синхронизируются с Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Решение "Перспективный клиент в наличные деньги" для Sales

Поле **Номер счета** доступно на странице **Счет**. Оно является естественным и уникальным ключом для поддержки интеграции. Функция естественного ключа решения управления взаимоотношениями с клиентами (CRM) могут повлиять на клиентов, уже использующих поле **Номер счета**, но не использующих значение **Номер счета** для счета. В настоящее время решение интеграции не поддерживает это.

При создании нового счета, если значение **Номер счета** еще не существует, оно создается автоматически с использованием номерной серии. Значение состоит из **ACC**, после чего следует увеличивающая номерная серия и суффикс из шести символов. Пример: **ACC-01000-BVRCPS**

При применении решения интеграции для Sales сценарий обновления задает значение в поле **Номер счета** для существующих счетов в Sales. Если значения **Номер счета** не существуют, используется номерная серия, описанная выше.

## <a name="preconditions-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

- Сопоставление **CustomerGroupId** из **CDS &gt; Место назначения** необходимо исправить на значение, допустимое в Finance and Operations. Можно указать значение по умолчанию или задать значение, используя сопоставление значений. Значение шаблона по умолчанию — **10**.
- Поле **Код страны/региона адреса** является обязательным в Finance and Operations. Чтобы избежать ошибок синхронизации, можно указать в сопоставлении из **CDS &gt; Место назначения** значение по умолчанию. Это значение по умолчанию будет использоваться, если это поле оставить пустым в Sales.

    - Значение шаблона по умолчанию для **AddressCountryRegionISOCode** — **США**.
    - Значение шаблона по умолчанию для **DeliveryAddressCountryRegionISOCode** — **США**.

- Добавляя следующие сопоставления из **CDS &gt; Место назначения**, можно уменьшить число обновлений вручную, необходимых в Finance and Operations. Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.

    - **SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Finance and Operations. Сайт по умолчанию может использоваться из продукта или из клиента в заголовке заказа. Значение шаблона по умолчанию для **SiteId** — **1**.
    - **WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Finance and Operations. Склад по умолчанию может использоваться из продукта или из клиента в заголовке заказа в Finance and Operations. Значение шаблона по умолчанию для **WarehouseId** — **13**.
    - **LanguageId** — язык необходим для создания предложений и заказов на продажу в Finance and Operations. По умолчанию используется язык из заголовка заказа от клиента. Значение шаблона по умолчанию для **LanguageId** — **en-us**.

- Обновите код организации CDS (**Organization_OrganizationId**) в сопоставлении **Источник &gt; CDS**. Значение шаблона по умолчанию — **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Сопоставление шаблона в интеграторе данных

> [!NOTE]
> Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию. Чтобы сопоставить эти поля, необходимо настроить преобразование значений. Преобразование значений относится к данным в организациях, между которыми синхронизируется объект.

На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.

![Сопоставление шаблона в интеграторе данных](./media/accounts-template-mapping-data-integrator-1.png)

![Сопоставление шаблона для счетов в интеграторе данных](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Связанные разделы

[Синхронизация продуктов из Finance and Operations с продуктами в Sales](products-template-mapping.md)

[Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations](contacts-template-mapping.md)

[Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations](sales-quotation-template-mapping.md)

[Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales](sales-order-template-mapping.md)

[Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales](sales-invoice-template-mapping.md)




