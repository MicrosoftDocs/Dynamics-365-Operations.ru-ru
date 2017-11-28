---
title: "Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации счетов из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 16bbca2d9eb8c3d9c33752404ebecbe4415517a2
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для прямой синхронизации организаций из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

## <a name="data-flow-in-prospect-to-cash"></a>Поток данных в решение "Перспективный клиент в наличные деньги"

Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Finance and Operations и Sales.  Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales. На следующем рисунке показано, как данные синхронизируются между Finance and Operations и Sales.

[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи

Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования PowerApps](https://preview.admin.powerapps.com/dataintegration). Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.

Следующий шаблон и базовая задача используется для синхронизации счетов из Sales с Finance and Operations:

- **Имя шаблона в интеграции данных:** "Организации (из Sales в Fin and Ops) — напрямую"
- **Имя задачи в проекте:** Организации — Клиенты

Никакие задачи синхронизации не требуются до того, как можно будет выполнить синхронизацию организаций/клиентов.

## <a name="entity-set"></a>Набор объектов

| Прод.    | Finance and Operations |
|----------|------------------------|
| Счета | Клиенты V2           |

## <a name="entity-flow"></a>Поток объектов

Счета управляются в Sales и синхронизируются с Finance and Operations как клиенты. Свойство **Управляется извне** этих клиентов имеет значение **Да** для отслеживания клиентов, которые происходят из Sales. Во время выставления накладных эта информация используется для фильтрации накладных, которые синхронизируются с Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>Решение "Перспективный клиент в наличные деньги" для Sales

Поле **Номер счета** доступно на странице **Счет**. Оно является естественным и уникальным ключом для поддержки интеграции. Функция естественного ключа решения управления взаимоотношениями с клиентами (CRM) могут повлиять на клиентов, уже использующих поле **Номер счета**, но не использующих значение **Номер счета** для счета. В настоящее время решение интеграции не поддерживает это.

При создании нового счета, если значение **Номер счета** еще не существует, оно создается автоматически с использованием номерной серии. Значение состоит из **ACC**, после чего следует увеличивающая номерная серия и суффикс из шести символов. Пример: **ACC-01000-BVRCPS**

При применении решения интеграции для Sales сценарий обновления задает значение в поле **Номер счета** для существующих счетов в Sales. Если значения **Номер счета** не существуют, используется номерная серия, упомянутая выше.

## <a name="preconditions-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

- Сопоставление **CustomerGroupId** необходимо обновить до допустимого значения в Finance and Operations. Можно указать значение по умолчанию или задать значение, используя сопоставление значений.

    Значение шаблона по умолчанию — **10**.

- Добавляя следующие сопоставления, можно уменьшить число обновлений вручную, необходимых в Finance and Operations. Можно использовать значение по умолчанию или сопоставление значений, например, из поля **Страна/регион** или **Город**.

    - **SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Finance and Operations. Сайт по умолчанию может использоваться из продукта или из клиента в заголовке заказа.

        Значение шаблона по умолчанию — **1**.

    - **WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Finance and Operations. Склад по умолчанию может использоваться из продукта или из клиента в заголовке заказа в Finance and Operations.

        Значение шаблона по умолчанию — **13**.

    - **LanguageId** — язык необходим для создания предложений и заказов на продажу в Finance and Operations. По умолчанию используется язык из заголовка заказа от клиента.

        Значение шаблона по умолчанию — **en-us**.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

> [!NOTE]
> Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию. Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.

На следующем рисунке показан пример сопоставления шаблона в интеграции данных. 

> [!NOTE]
> Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Finance and Operations.

![Сопоставление шаблона в интеграции данных](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Связанные разделы


[Решение "Перспективный клиент в наличные деньги"](prospect-to-cash.md)

[Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations](accounts-template-mapping-direct.md)

[Синхронизация контактов непосредственно из Sales с контактами и клиентами в Finance and Operations](contacts-template-mapping-direct.md)

[Синхронизация заголовков и строк заказов на продажу непосредственно из Finance and Operations в Sales](sales-order-template-mapping-direct.md)

[Синхронизация заголовков и строк счетов продажи непосредственно из Finance and Operations в Sales](sales-invoice-template-mapping-direct.md)

