---
title: Синхронизация списка проектов из Finance and Operations в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843561"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Синхронизация списка проектов Finance and Operations с Field Service

[!include[banner](../includes/banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи используются для выполнения синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

**Шаблон в интеграции данных**
- Проекты (из Fin and Ops в Field Service)

**Задача в проекте интеграции данных**
- Проекты

Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:
- Организации (из Sales в Fin and Ops) 

## <a name="entity-set"></a>Набор объектов
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Проекты                |

## <a name="entity-flow"></a>Поток объектов
Проекты создаются в Finance and Operations. Проекты, для которых в поле **Тип проекта** задано значение **Время и расходы**, а в поле **Этап проекта** задано значение **В работе**, будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента. Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами в Finance and Operations.

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Объект **Внешний проект** получает все проекты из Finance and Operations. Поле **Внешний проект** было добавлено в объект **Заказ на выполнение работ**. Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказы на покупку будут затем связаны с проектом в Finance and Operations. После изменения значения **Состояние системы** из **Открыто — В работе(690,970,000)** на более высокий статус, поле **Внешний проект** будет заблокировано и вы больше не сможете добавить, удалить или изменить значение.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления
### <a name="finance-and-operations"></a>Finance and Operations
Включение отслеживания изменений для информационного объекта проектов

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Проекты (из Fin and Ops в Field Service): Проекты

[![Сопоставление шаблона в интеграции данных](./media/FSProject1.png)](./media/FSProject1.png)
