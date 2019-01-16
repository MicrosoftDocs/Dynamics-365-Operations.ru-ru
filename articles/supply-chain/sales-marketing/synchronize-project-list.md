---
title: "Синхронизация списка проектов из Finance and Operations в Field Service"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Синхронизация списка проектов из Finance and Operations в Field Service

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

**Имя шаблона в интеграции данных:**
- Проекты (из Finance and Operations в Field Service)

**Имена задач в проекте интеграции данных:**
- Проекты

Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:
- Организации (из Sales в Finance and Operations) 

## <a name="entity-set"></a>Набор объектов
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Проекты                |

## <a name="entity-flow"></a>Поток объектов
Проекты создаются в Finance and Operations. Проекты, для которых в поле **Тип проекта** указано "Время и расходы", а в поле **Этап проекта** указано "В работе", будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента. Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами в Finance and Operations.
Решение Field Service CRM "Внешний проект" — это новый объект, который получает все проекты из Operations.
Поле "Внешний проект" было добавлено в объект "Заказ на выполнение работ". Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Operations. После изменения состояния системы из "Открыто — В работе(690,970,000)" на более высокий статус, поле "Внешний проект" будет заблокировано и вы не сможете добавить, удалить или изменить значение.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления
### <a name="in-finance-and-operations"></a>В Finance and Operations
Включение отслеживания изменений для информационного объекта проектов

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Проекты (из Finance and Operations в Field Service): Проекты

[![Сопоставление шаблона в интеграции данных](./media/FSProject1.png)](./media/FSProject1.png)

