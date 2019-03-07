---
title: Синхронизация списка проектов из Finance and Operations в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "312516"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="08bcb-103">Синхронизация списка проектов Finance and Operations с Field Service</span><span class="sxs-lookup"><span data-stu-id="08bcb-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="08bcb-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="08bcb-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="08bcb-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="08bcb-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="08bcb-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="08bcb-106">Templates and tasks</span></span>
<span data-ttu-id="08bcb-107">Следующий шаблон и базовые задачи используются для выполнения синхронизации проектов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="08bcb-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="08bcb-108">**Шаблон в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="08bcb-108">**Template in Data integration**</span></span>
- <span data-ttu-id="08bcb-109">Проекты (из Finance and Operations в Field Service)</span><span class="sxs-lookup"><span data-stu-id="08bcb-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="08bcb-110">**Задача в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="08bcb-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="08bcb-111">Проекты</span><span class="sxs-lookup"><span data-stu-id="08bcb-111">Projects</span></span>

<span data-ttu-id="08bcb-112">Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="08bcb-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="08bcb-113">Организации (из Sales в Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="08bcb-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="08bcb-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="08bcb-114">Entity set</span></span>
| <span data-ttu-id="08bcb-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="08bcb-115">Field Service</span></span>           | <span data-ttu-id="08bcb-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08bcb-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="08bcb-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="08bcb-117">msdynce_externalprojects</span></span> | <span data-ttu-id="08bcb-118">Проекты</span><span class="sxs-lookup"><span data-stu-id="08bcb-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="08bcb-119">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="08bcb-119">Entity flow</span></span>
<span data-ttu-id="08bcb-120">Проекты создаются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08bcb-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="08bcb-121">Проекты, для которых в поле **Тип проекта** задано значение **Время и расходы**, а в поле **Этап проекта** задано значение **В работе**, будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента.</span><span class="sxs-lookup"><span data-stu-id="08bcb-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="08bcb-122">Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08bcb-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="08bcb-123">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="08bcb-123">Field Service CRM solution</span></span>
<span data-ttu-id="08bcb-124">Объект **Внешний проект** получает все проекты из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08bcb-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="08bcb-125">Поле **Внешний проект** было добавлено в объект **Заказ на выполнение работ**.</span><span class="sxs-lookup"><span data-stu-id="08bcb-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="08bcb-126">Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказы на покупку будут затем связаны с проектом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08bcb-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="08bcb-127">После изменения значения **Состояние системы** из **Открыто — В работе(690,970,000)** на более высокий статус, поле **Внешний проект** будет заблокировано и вы больше не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="08bcb-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="08bcb-128">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="08bcb-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="08bcb-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08bcb-129">Finance and Operations</span></span>
<span data-ttu-id="08bcb-130">Включение отслеживания изменений для информационного объекта проектов</span><span class="sxs-lookup"><span data-stu-id="08bcb-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="08bcb-131">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="08bcb-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="08bcb-132">Проекты (из Finance and Operations в Field Service): Проекты</span><span class="sxs-lookup"><span data-stu-id="08bcb-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="08bcb-133">[![Сопоставление шаблона в интеграции данных](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="08bcb-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
