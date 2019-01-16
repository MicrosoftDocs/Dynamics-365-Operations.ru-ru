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

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="79438-103">Синхронизация списка проектов из Finance and Operations в Field Service</span><span class="sxs-lookup"><span data-stu-id="79438-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="79438-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="79438-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="79438-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="79438-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="79438-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="79438-106">Templates and tasks</span></span>
<span data-ttu-id="79438-107">Следующий шаблон и базовые задачи, которые используются для выполнения синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="79438-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="79438-108">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="79438-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="79438-109">Проекты (из Finance and Operations в Field Service)</span><span class="sxs-lookup"><span data-stu-id="79438-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="79438-110">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="79438-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="79438-111">Проекты</span><span class="sxs-lookup"><span data-stu-id="79438-111">Projects</span></span>

<span data-ttu-id="79438-112">Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="79438-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="79438-113">Организации (из Sales в Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="79438-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="79438-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="79438-114">Entity set</span></span>
<span data-ttu-id="79438-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="79438-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="79438-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="79438-116">Field Service</span></span>           | <span data-ttu-id="79438-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="79438-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="79438-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="79438-118">msdynce_externalprojects</span></span> | <span data-ttu-id="79438-119">Проекты</span><span class="sxs-lookup"><span data-stu-id="79438-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="79438-120">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="79438-120">Entity flow</span></span>
<span data-ttu-id="79438-121">Проекты создаются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="79438-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="79438-122">Проекты, для которых в поле **Тип проекта** указано "Время и расходы", а в поле **Этап проекта** указано "В работе", будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента.</span><span class="sxs-lookup"><span data-stu-id="79438-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="79438-123">Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="79438-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="79438-124">Решение Field Service CRM "Внешний проект" — это новый объект, который получает все проекты из Operations.</span><span class="sxs-lookup"><span data-stu-id="79438-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="79438-125">Поле "Внешний проект" было добавлено в объект "Заказ на выполнение работ".</span><span class="sxs-lookup"><span data-stu-id="79438-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="79438-126">Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Operations.</span><span class="sxs-lookup"><span data-stu-id="79438-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="79438-127">После изменения состояния системы из "Открыто — В работе(690,970,000)" на более высокий статус, поле "Внешний проект" будет заблокировано и вы не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="79438-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="79438-128">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="79438-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="79438-129">В Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="79438-129">In Finance and Operations</span></span>
<span data-ttu-id="79438-130">Включение отслеживания изменений для информационного объекта проектов</span><span class="sxs-lookup"><span data-stu-id="79438-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="79438-131">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="79438-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="79438-132">Проекты (из Finance and Operations в Field Service): Проекты</span><span class="sxs-lookup"><span data-stu-id="79438-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="79438-133">[![Сопоставление шаблона в интеграции данных](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="79438-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

