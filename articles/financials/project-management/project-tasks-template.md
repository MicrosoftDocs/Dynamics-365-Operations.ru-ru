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

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="9bdbf-103">Синхронизация задач проекта из Project Service Automation непосредственно мероприятия по проекту в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bdbf-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="9bdbf-104">В этой теме описывается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 for Project Service Automation в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="9bdbf-105">Dynamics 365 for Finance and Operations версии 8.0. доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="9bdbf-106">Поток данных для Project Service Automation для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bdbf-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="9bdbf-107">Решение по интеграции Project Service Automation в Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="9bdbf-108">Шаблон интеграции, доступный при использовании функции интеграции данных, включает поток данных по задачам проекта из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="9bdbf-109">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="9bdbf-110">[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="9bdbf-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="9bdbf-111">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="9bdbf-111">Template and task</span></span>

<span data-ttu-id="9bdbf-112">Для доступа к шаблону в центре администрирования Microsoft PowerApps выберите **Проекты**, а затем выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9bdbf-113">Следующий шаблон и базовые задачи используются для синхронизации задач проекта из Project Service Automation в Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="9bdbf-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="9bdbf-114">-**Имя шаблона в интеграции данных:** Задачи проекта (PSA в Fin and Ops) —**Имя задачи в проекте:** Задачи проекта</span><span class="sxs-lookup"><span data-stu-id="9bdbf-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="9bdbf-115">Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="9bdbf-116">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="9bdbf-116">Entity set</span></span>

|<span data-ttu-id="9bdbf-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9bdbf-117">Project Service Automation</span></span>               | <span data-ttu-id="9bdbf-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9bdbf-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="9bdbf-119">Задачи проекта</span><span class="sxs-lookup"><span data-stu-id="9bdbf-119">Project Tasks</span></span>                           | <span data-ttu-id="9bdbf-120">Объект интеграции для задачи проекта.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="9bdbf-121">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="9bdbf-121">Entity flow</span></span>

<span data-ttu-id="9bdbf-122">Задачи проекта управляются в Project Service Automation и синхронизируются с Finance and Operations как мероприятия по проекту.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9bdbf-123">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="9bdbf-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="9bdbf-124">Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="9bdbf-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="9bdbf-125">Power Query</span></span>

<span data-ttu-id="9bdbf-126">Необходимо использовать Microsoft Power Query для фильтрации данных при соблюдении этих условий:</span><span class="sxs-lookup"><span data-stu-id="9bdbf-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="9bdbf-127">У вас есть определенные записи ресурсов в рамках задачи проекта.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="9bdbf-128">При использовании Power Query необходимо выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="9bdbf-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="9bdbf-129">Шаблон задач проекта (PSA в Fin и Ops) имеет фильтр по умолчанию, чтобы исключить определенные записи ресурсов в рамках задачи проекта путем установки фильтра с **IsLineTask** на **False**.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="9bdbf-130">При создании собственного шаблона, необходимо добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9bdbf-131">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="9bdbf-131">Template mapping in Data integration</span></span>

<span data-ttu-id="9bdbf-132">На следующем рисунке показан пример сопоставления шаблонной задачи в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="9bdbf-133">Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9bdbf-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="9bdbf-134">[![Соответствие шаблона](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="9bdbf-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


