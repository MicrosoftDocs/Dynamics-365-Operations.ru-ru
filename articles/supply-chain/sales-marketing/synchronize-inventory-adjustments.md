---
title: "Синхронизация перемещений и корректировок запасов из Field Service в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Синхронизация корректировок запасов из Field Service в Finance and Operations

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации корректировок и перемещений запасов из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.

**Имя шаблонов в интеграции данных:**
- Корректировка запасов (из Field Service в Finance and Operations)
- Перемещение запасов (из Field Service в Finance and Operations)

**Имена задач в проектах интеграции данных:**
- Корректировки запасов
- Перемещение запасов

## <a name="entity-set"></a>Набор объектов
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Заголовки и строки журналов корректировки запасов CDS |
| msdyn_inventoryadjustmentproducts | Заголовки и строки журналов перемещения запасов CDS   |

## <a name="entity-flow"></a>Поток объектов
Корректировки и перемещения запасов, выполненные в приложении Field Service, синхронизируются с Finance and Operations, когда значение в поле **Состояние разноски** изменяется с "Создано" на "Разнесено". Когда это происходит, заказ на корректировку или перемещение будет заблокирован и станет доступен только для чтения, так как корректировки и перемещения могут быть разнесены в Finance and Operations и, следовательно, не могут быть изменены.
В Finance and Operations можно настроить пакетное задание для автоматической разноски журналов корректировок и перемещений запасов, созданных с интеграцией. Подробные сведения о том, как включить это пакетное задание, см. в предварительных условиях ниже.

## <a name="field-service-crm-solution"></a>Решение Field Service CRM 
Поле "Ед. изм. складского учета" было добавлено в сущность "Продукт". Это поле требуется, так как единицы измерения продаж и складского учета не всегда совпадают в Operations, и для складских запасов в Operations требуется единица измерения складского учета.
При установке продукта для продукта корректировки запасов для корректировки запасов и перемещения запасов единицы измерения извлекается из значения продукта запасов продуктов. Если значение найдено, поле единицы измерения будет заблокировано в продукте корректировки запасов

Поле "Состояние разноски" было добавлено как в сущность корректировки запасов, так и в сущность перемещения запасов. Это поле используется как фильтр при отправке корректировки или перемещения в приложение Operations. Поле по умолчанию принимает значение "Создано (1)", затем оно не отправляется в Operations. После изменения значения на "Разнесено (2)" оно отправляется в Operations, но вы больше не сможете изменить ничего в корректировках или перемещениях или добавить новые строки в нее.
Поле номерной серии было добавлено в сущность продукта корректировки запасов. Это поле помогает интеграции иметь уникальный номер, чтобы интеграция знала, когда выполняется создание, а когда — обновление. При создании первого продукта корректировки запасов создается новая запись в сущности P2C AutoNumber для поддержания номерных серий и префикса, который используется.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

### <a name="in-finance-and-operations"></a>В Finance and Operations
Журналы запасов интеграции, созданные при интеграции, могут быть автоматически разнесены с помощью пакетного задания. Эта функция включается из пункта: Управление запасами > Периодические задачи > Интеграция CDS > Разноска журналов запасов интеграции

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Корректировка запасов (Field Service с Finance and Operations): Корректировка запасов

[![Сопоставление шаблона в интеграции данных](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Перемещение запасов (Field Service с Finance and Operations): Перемещение запасов

[![Сопоставление шаблона в интеграции данных](./media/FSTrans1.png)](./media/FSTrans1.png)

