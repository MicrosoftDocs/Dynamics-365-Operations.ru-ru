---
title: Синхронизация списка проектов из Supply Chain Management в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
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
ms.openlocfilehash: b74a7f0445b3bdad671da4c61e561bc0d9d80cd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251600"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="02300-103">Синхронизация списка проектов из Supply Chain Management в Field Service</span><span class="sxs-lookup"><span data-stu-id="02300-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="02300-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="02300-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="02300-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="02300-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="02300-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="02300-106">Templates and tasks</span></span>
<span data-ttu-id="02300-107">Следующий шаблон и базовые задачи используются для выполнения синхронизации проектов из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="02300-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="02300-108">**Шаблон в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="02300-108">**Template in Data integration**</span></span>
- <span data-ttu-id="02300-109">Проекты (из Supply Chain Management в Field Service)</span><span class="sxs-lookup"><span data-stu-id="02300-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="02300-110">**Задача в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="02300-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="02300-111">Проекты</span><span class="sxs-lookup"><span data-stu-id="02300-111">Projects</span></span>

<span data-ttu-id="02300-112">Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="02300-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="02300-113">Счета (из Sales в Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="02300-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="02300-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="02300-114">Entity set</span></span>
| <span data-ttu-id="02300-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="02300-115">Field Service</span></span>           | <span data-ttu-id="02300-116">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="02300-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="02300-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="02300-117">msdynce_externalprojects</span></span> | <span data-ttu-id="02300-118">Проекты</span><span class="sxs-lookup"><span data-stu-id="02300-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="02300-119">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="02300-119">Entity flow</span></span>
<span data-ttu-id="02300-120">Проекты создаются в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02300-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="02300-121">Проекты, для которых в поле **Тип проекта** задано значение **Время и расходы**, а в поле **Этап проекта** задано значение **В работе**, будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента.</span><span class="sxs-lookup"><span data-stu-id="02300-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="02300-122">Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02300-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="02300-123">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="02300-123">Field Service CRM solution</span></span>
<span data-ttu-id="02300-124">Объект **Внешний проект** получает все проекты из Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02300-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="02300-125">Поле **Внешний проект** было добавлено в объект **Заказ на выполнение работ**.</span><span class="sxs-lookup"><span data-stu-id="02300-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="02300-126">Это поле подстановки, поэтому за счет отметки проекта в вашем заказе на выполнение работ заказ на покупку будет связан с проектом в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02300-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="02300-127">После изменения значения **Состояние системы** из **Открыто — В работе(690,970,000)** на более высокий статус, поле **Внешний проект** будет заблокировано и вы больше не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="02300-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="02300-128">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="02300-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="02300-129">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="02300-129">Supply Chain Management</span></span>
<span data-ttu-id="02300-130">Включение отслеживания изменений для информационного объекта проектов</span><span class="sxs-lookup"><span data-stu-id="02300-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="02300-131">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="02300-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="02300-132">Проекты (из Supply Chain Management в Field Service): Проекты</span><span class="sxs-lookup"><span data-stu-id="02300-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="02300-133">[![Сопоставление шаблона в интеграции данных](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="02300-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
