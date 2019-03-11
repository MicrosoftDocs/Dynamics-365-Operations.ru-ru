---
title: Синхронизация перемещений и корректировок запасов из Field Service в Finance and Operations
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: aa54945cea5821da163e1f6ea1747ac29b31a3ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "308376"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Синхронизация корректировок запасов из Field Service в Finance and Operations

[!include[banner](../includes/banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующие шаблон и базовые задачи используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.

**Шаблоны в интеграции данных**
- Корректировка запасов (из Field Service в Finance and Operations)
- Перемещение запасов (из Field Service в Finance and Operations)

**Задачи в проектах интеграции данных**
- Корректировки запасов
- Перемещение запасов

## <a name="entity-set"></a>Набор объектов
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Заголовки и строки журналов корректировки запасов CDS |
| msdyn_inventoryadjustmentproducts | Заголовки и строки журналов перемещения запасов CDS   |

## <a name="entity-flow"></a>Поток объектов
Корректировки и перемещения запасов, выполненные в приложении Field Service, синхронизируются с Finance and Operations после изменения значения в поле **Состояние разноски** изменяется с **Создано** на **Разнесено**. В этом случае заказ на корректировку или перемещение будет заблокирован и становится доступным только для чтения. Это означает, что корректировки и переносы можно разносить в Finance and Operations, но не могут быть изменены. В Finance and Operations можно настроить пакетное задание для автоматической разноски журналов корректировок и перемещений запасов, которые были созданы во время интеграции. Подробные сведения о том, как включить это пакетное задание, см. в следующих предварительных условиях.

## <a name="field-service-crm-solution"></a>Решение Field Service CRM 
Поле **Ед. изм. складского учета** было добавлено в сущность **Продукт**. Это поле требуется, так как единицы измерения продаж и складского учета не всегда совпадают в Finance and Operations, и единица измерения складского учета требуется для складских запасов в Finance and Operations.
При установке продукта для продукта корректировки запасов для корректировки запасов и перемещения запасов единицы измерения извлекается из значения продукта запасов продуктов. Если значение найдено, поле **Единица измерения** будет заблокировано в продукте корректировки запасов.

Поле **Состояние разноски** было добавлено как в сущность **Корректировка запасов**, так и в сущность **Перемещение запасов**. Это поле используется как фильтр при отправке корректировки или перемещения в приложение Finance and Operations. По умолчанию для этого поля задано значение "Создано (1)", однако оно не передается в Finance and Operations. После обновления значения на "Разнесено (2)", оно отправляется в Finance and Operations, но после этого вы больше не сможете изменить корректировку или перемещение или добавить новые строки.

Поле **Номерная серия** было добавлено в сущность **Продукт корректировки запасов**. Это поле гарантирует, что интеграция имеет уникальный номер, поэтому интеграция может создавать и обновлять корректировку. При создании первого продукта корректировки запасов создается новая запись в сущности **P2C AutoNumber** для поддержания номерных серий и префикса, который используется.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

### <a name="finance-and-operations"></a>Finance and Operations
Журналы запасов интеграции, созданные при интеграции, могут быть автоматически разнесены с использованием пакетного задания. Эта функция включается из пункта **Управление запасами > Периодические задачи > Интеграция CDS > Разноска журналов запасов интеграции**.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Корректировка запасов (Field Service с Finance and Operations): Корректировка запасов

[![Сопоставление шаблона в интеграции данных](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Перемещение запасов (Field Service с Finance and Operations): Перемещение запасов

[![Сопоставление шаблона в интеграции данных](./media/FSTrans1.png)](./media/FSTrans1.png)
