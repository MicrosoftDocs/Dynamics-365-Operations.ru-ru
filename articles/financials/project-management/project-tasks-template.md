---
title: Синхронизация задач по проекту напрямую из Project Service Automation в Finance and Operations
description: В этой теме обсуждается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "355181"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Синхронизация задач по проекту напрямую из Project Service Automation в Finance and Operations

[!include[banner](../includes/banner.md)]

В этой теме обсуждается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - В Microsoft Dynamics 365 for Finance and Operations версии 8.0 доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.
> - При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки. Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить KB 4131710.
> - Интеграция фактических данных доступна в Microsoft Dynamics 365 for Finance and Operations версии 8.0.1 или новее.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Поток данных для Project Service Automation для Finance and Operations

Решение по интеграции Project Service Automation в Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations. Шаблон интеграции, доступный при использовании функции интеграции данных, включает поток данных по задачам проекта из Project Service Automation в Finance and Operations.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.

[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Шаблон и задача

Для доступа к шаблону в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующий шаблон и базовые задачи используются для синхронизации задач проекта из Project Service Automation в Finance and Operations:

- **Имя шаблона в интеграции данных:** задачи по проекту (PSA в Fin and Ops)
- **Имя задачи в проекте интеграции данных:** задачи по проекту

Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.

## <a name="entity-set"></a>Набор объектов

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| Задачи проекта              | Объект интеграции для задачи проекта |

## <a name="entity-flow"></a>Поток объектов

Задачи проекта управляются в Project Service Automation и синхронизируются с Finance and Operations как мероприятия по проекту.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query для Excel для фильтрации данных, если соблюдены следующие условия:

- У вас есть записи, специфичные для конкретных ресурсов, в задаче проекта.

При использовании Power Query следуйте приведенной ниже рекомендации:

- Шаблон задач проекта (PSA в Fin и Ops) имеет фильтр по умолчанию, который исключает определенные записи ресурсов из задачи проекта путем установки фильтра с **IsLineTask** на **False**. При создании собственного шаблона, необходимо добавить этот фильтр.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показан пример сопоставления шаблонной задачи в интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.

[![Соответствие шаблона](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
