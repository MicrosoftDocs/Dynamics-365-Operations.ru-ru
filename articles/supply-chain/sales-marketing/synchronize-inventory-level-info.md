---
title: Синхронизация сведений уровня запасов из Finance and Operations в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "356791"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Синхронизация сведений об уровне запасов Finance and Operations с Field Service 

[!include[banner](../includes/banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующие шаблон и базовые задачи используются для синхронизации корректировок и перемещений наличных запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

**Шаблон в интеграции данных**
- Запасы продуктов (из Finance and Operations в Field Service)
  
**Задача в проекте интеграции данных**
- Запасы продуктов

Чтобы была возможна синхронизация уровней запасов, требуются следующие задачи синхронизации:
- Склады (из Finance and Operations в Field Service) 
- Продукты Field Service с единицей измерения складских запасов (из Finance and Operations в Sales) 

## <a name="entity-set"></a>Набор объектов

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Запасы CDS в наличии по складам     |

## <a name="entity-flow"></a>Поток объектов
Сведения об уровне запасов из Finance and Operations отправляются в Field Service для выбранных продуктов. Сведения об уровне запасов включают: 
- Количество в наличии (текущее зарегистрированное физическое количество, находящееся на складе)
- Количество по заказу (общее зарегистрированное количество по заказу, например заказы на продажу)
- Заказанное количество (общее зарегистрированное заказанное количество, например заказы на покупку)

Эти сведения фиксируются по выпущенным продуктам для каждого склада и синхронизируются на основе отслеживания изменений при изменении уровня запасов.

В Field Service решение интеграции создает журналы запасов для разницы, чтобы уровни в Field Service соответствовали уровням в Finance and Operations.

Приложение Finance and Operations играет роль ведущего для уровней запасов. Поэтому важно настроить интеграцию для заказов на выполнение работ, перемещений и корректировок из Field Service в Finance and Operations, если эта функция используется в Field Service, вместе с синхронизацией уровней запасов из Finance and Operations.

Продукты и склады, где уровни запасов поддерживаются из Finance and Operations, могут контролироваться с помощью расширенных запросов и фильтрация (Power Query).

> [!NOTE]
> Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне = Нет**) и затем сопоставить их с одним складом в Finance and Operations с функцией расширенного запроса и фильтрации. Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и отправляло только обновления в приложение Finance and Operations. В этом случае Field Service не будет получать обновления уровней запасов из Finance and Operations. Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Сущность **Внешние запасы продукта** используется только для обработки интеграции на сервере. Эта сущность получает значения уровня складских запасов из Finance and Operations в интеграции, затем преобразует эти значения для журналов ручных запасов, которые затем изменяют складские продукты на складе.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

### <a name="data-integration-project"></a>Проект интеграции данных
Можно применить фильтры с расширенными запросами и фильтрацией, чтобы только определенные продукты и склады отправляли информацию об уровне запасов из Finance and Operations в Field Service.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Запасы продуктов (из Finance and Operations в Field Service): Запасы продуктов

[![Сопоставление шаблона в интеграции данных](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
