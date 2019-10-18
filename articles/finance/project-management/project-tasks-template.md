---
title: Синхронизация задач по проекту напрямую из Project Service Automation в Finance and Operations
description: В этой теме обсуждается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 Project Service Automation в Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 977037f0e2b313ebf05a3e1616d34567f82e82d7
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250400"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="15472-103">Синхронизация задач по проекту напрямую из Project Service Automation в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15472-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="15472-104">В этой теме обсуждается шаблон и базовая задача, которые используются для синхронизации задач проекта непосредственно из Dynamics 365 Project Service Automation в Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="15472-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="15472-105">В версии 8.0 доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.</span><span class="sxs-lookup"><span data-stu-id="15472-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="15472-106">При использовании Enterprise edition 7.3.0 после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки.</span><span class="sxs-lookup"><span data-stu-id="15472-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="15472-107">Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="15472-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="15472-108">Интеграция фактических данных доступна в версии 8.0.1 или новее.</span><span class="sxs-lookup"><span data-stu-id="15472-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="15472-109">Поток данных для Project Service Automation в Finance</span><span class="sxs-lookup"><span data-stu-id="15472-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="15472-110">Решение по интеграции Project Service Automation с Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="15472-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="15472-111">Шаблон интеграции, доступный при использовании функции интеграции данных, включает поток данных по задачам проекта из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="15472-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="15472-112">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="15472-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="15472-113">[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="15472-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="15472-114">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="15472-114">Template and task</span></span>

<span data-ttu-id="15472-115">Для доступа к шаблону в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="15472-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="15472-116">Следующий шаблон и базовая задача используются для синхронизации задач проекта из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="15472-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="15472-117">**Имя шаблона в интеграции данных:** задачи по проекту (PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="15472-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="15472-118">**Имя задачи в проекте интеграции данных:** задачи по проекту</span><span class="sxs-lookup"><span data-stu-id="15472-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="15472-119">Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.</span><span class="sxs-lookup"><span data-stu-id="15472-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="15472-120">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="15472-120">Entity set</span></span>

| <span data-ttu-id="15472-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15472-121">Project Service Automation</span></span> | <span data-ttu-id="15472-122">Финансы</span><span class="sxs-lookup"><span data-stu-id="15472-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="15472-123">Задачи проекта</span><span class="sxs-lookup"><span data-stu-id="15472-123">Project Tasks</span></span>              | <span data-ttu-id="15472-124">Объект интеграции для задачи проекта</span><span class="sxs-lookup"><span data-stu-id="15472-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="15472-125">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="15472-125">Entity flow</span></span>

<span data-ttu-id="15472-126">Задачи проекта управляются в Project Service Automation и синхронизируются с Finance как мероприятия по проекту.</span><span class="sxs-lookup"><span data-stu-id="15472-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="15472-127">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="15472-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="15472-128">Перед синхронизацией задач проекта необходимо синхронизировать контркты проекта и проекты.</span><span class="sxs-lookup"><span data-stu-id="15472-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="15472-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="15472-129">Power Query</span></span>

<span data-ttu-id="15472-130">Необходимо использовать Microsoft Power Query для Excel для фильтрации данных, если соблюдены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="15472-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="15472-131">У вас есть записи, специфичные для конкретных ресурсов, в задаче проекта.</span><span class="sxs-lookup"><span data-stu-id="15472-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="15472-132">При использовании Power Query следуйте приведенной ниже рекомендации:</span><span class="sxs-lookup"><span data-stu-id="15472-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="15472-133">Шаблон задач проекта (PSA в Fin и Ops) имеет фильтр по умолчанию, который исключает определенные записи ресурсов из задачи проекта путем установки фильтра с **IsLineTask** на **False**.</span><span class="sxs-lookup"><span data-stu-id="15472-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="15472-134">При создании собственного шаблона, необходимо добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="15472-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="15472-135">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="15472-135">Template mapping in Data integration</span></span>

<span data-ttu-id="15472-136">На следующем рисунке показан пример сопоставления шаблонной задачи в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="15472-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="15472-137">Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="15472-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="15472-138">[![Соответствие шаблона](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="15472-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
