---
title: "Синхронизация сведений уровня запасов из Finance and Operations в Field Service"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Синхронизация сведений уровня запасов из Finance and Operations в Field Service 

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации сведений об уровне запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации уровней доступных запасов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

**Имя шаблона в интеграции данных:**
- Запасы продуктов (из Finance and Operations в Field Service)
  
**Имена задач в проекте интеграции данных:**
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
- Количество по заказу (общее зарегистрированное количество по заказу — т. е., заказы на продажу)
- Заказанное количество (общее зарегистрированное заказанное количество — т. е., заказы на покупку)

Эти сведения фиксируются по выпущенным продуктам для каждого склада и синхронизируются на основе отслеживания изменений при изменении уровня запасов.

В Field Service решение интеграции создает журналы запасов для разницы, чтобы уровни в Field Service соответствовали уровням в Finance and Operations.

Приложение Finance and Operations играет роль ведущего для уровней запасов. Поэтому важно настроить интеграцию для рабочих заказы, перемещений и корректировок из Field Service в Finance and Operations, если эта функция используется в Field Service, вместе с синхронизацией уровней запасов из Finance and Operations.

Продукты и склады, где уровни запасов поддерживаются из Finance and Operations, могут контролироваться с помощью расширенных запросов и фильтрация (Power Query).

Примечание. Можно создать несколько складов в Field Service (с настройкой "Управляется извне = Нет") и затем сопоставить их с одним складом в Finance and Operations с функцией расширенного запроса и фильтрации. Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и просто отправляло обновления в приложение Finance and Operations. В этом случае Field Service не будет получать обновления уровней запасов из Finance and Operations. См. дополнительные сведения в разделах "Синхронизация корректировок запасов из Field Service в Finance and Operations" и "Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations".

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Сущность внешних запасов продукта — это новая сущность, которая используется только для обработки интеграции на сервере. Она получает значения уровня складских запасов из Finance and Operations в интеграции, затем преобразует эти значения для журналов ручных запасов, которые затем изменяют складские продукты на складе. 

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

### <a name="in-the-data-integration-project"></a>В проекте интеграции данных
Применяйте фильтры с расширенными запросами и фильтрацией для контроля, чтобы только требуемые продукты и склады отправляли информацию об уровне запасов из Finance and Operations в Field Service.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Запасы продуктов (из Finance and Operations в Field Service): Запасы продуктов

[![Сопоставление шаблона в интеграции данных](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

