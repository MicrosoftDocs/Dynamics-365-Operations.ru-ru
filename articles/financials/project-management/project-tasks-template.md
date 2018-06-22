---
title: "Синхронизация задач проекта из Project Service Automation"
description: "В этой теме описывается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: ru-ru
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Синхронизация задач проекта из Project Service Automation непосредственно мероприятия по проекту в Finance and Operations

В этой теме описывается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Dynamics 365 for Finance and Operations версии 8.0. доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Поток данных для Project Service Automation для Finance and Operations

Решение по интеграции Project Service Automation в Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations. Шаблон интеграции, доступный при использовании функции интеграции данных, включает поток данных по задачам проекта из Project Service Automation в Finance and Operations.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.

[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Шаблон и задача

Для доступа к шаблону в центре администрирования Microsoft PowerApps выберите **Проекты**, а затем выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующий шаблон и базовые задачи используются для синхронизации задач проекта из Project Service Automation в Finance and Operations:

-**Имя шаблона в интеграции данных:** Задачи проекта (PSA в Fin and Ops) —**Имя задачи в проекте:** Задачи проекта

Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.

## <a name="entity-set"></a>Набор объектов

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Задачи проекта                           | Объект интеграции для задачи проекта.   |

## <a name="entity-flow"></a>Поток объектов

Задачи проекта управляются в Project Service Automation и синхронизируются с Finance and Operations как мероприятия по проекту.

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления

Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query для фильтрации данных при соблюдении этих условий:

- У вас есть определенные записи ресурсов в рамках задачи проекта.

При использовании Power Query необходимо выполните следующее:

- Шаблон задач проекта (PSA в Fin и Ops) имеет фильтр по умолчанию, чтобы исключить определенные записи ресурсов в рамках задачи проекта путем установки фильтра с **IsLineTask** на **False**. При создании собственного шаблона, необходимо добавить этот фильтр.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показан пример сопоставления шаблонной задачи в интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.

[![Соответствие шаблона](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


