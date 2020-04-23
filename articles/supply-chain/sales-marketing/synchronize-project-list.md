---
title: Синхронизация списка проектов из Supply Chain Management в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215938"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="d2844-103">Синхронизация списка проектов из Supply Chain Management в Field Service</span><span class="sxs-lookup"><span data-stu-id="d2844-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d2844-104">В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации проектов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="d2844-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="d2844-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="d2844-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d2844-106">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="d2844-106">Templates and tasks</span></span>
<span data-ttu-id="d2844-107">Следующий шаблон и базовые задачи используются для выполнения синхронизации проектов из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="d2844-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="d2844-108">**Шаблон в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="d2844-108">**Template in Data integration**</span></span>
- <span data-ttu-id="d2844-109">Проекты (из Supply Chain Management в Field Service)</span><span class="sxs-lookup"><span data-stu-id="d2844-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="d2844-110">**Задача в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="d2844-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="d2844-111">Проекты</span><span class="sxs-lookup"><span data-stu-id="d2844-111">Projects</span></span>

<span data-ttu-id="d2844-112">Чтобы была возможна синхронизация списка проектов, требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="d2844-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="d2844-113">Счета (из Sales в Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="d2844-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="d2844-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="d2844-114">Entity set</span></span>
| <span data-ttu-id="d2844-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="d2844-115">Field Service</span></span>           | <span data-ttu-id="d2844-116">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="d2844-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="d2844-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="d2844-117">msdynce_externalprojects</span></span> | <span data-ttu-id="d2844-118">Проекты</span><span class="sxs-lookup"><span data-stu-id="d2844-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="d2844-119">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="d2844-119">Entity flow</span></span>
<span data-ttu-id="d2844-120">Проекты создаются в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d2844-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="d2844-121">Проекты, для которых в поле **Тип проекта** задано значение **Время и расходы**, а в поле **Этап проекта** задано значение **В работе**, будут синхронизироваться с объектом **Внешний проект** в Field Service, включая номер проекта, название проекта, этап проекта и сведения об организации клиента.</span><span class="sxs-lookup"><span data-stu-id="d2844-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="d2844-122">Список **Внешний проект** используется для сопоставления заказов на обслуживание в Field Service с проектами Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d2844-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d2844-123">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="d2844-123">Field Service CRM solution</span></span>
<span data-ttu-id="d2844-124">Объект **Внешний проект** получает все проекты из Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d2844-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="d2844-125">Поле **Внешний проект** было добавлено в объект **Заказ на выполнение работ**.</span><span class="sxs-lookup"><span data-stu-id="d2844-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="d2844-126">Это поле подстановки, поэтому за счет отметки проекта в вашем заказе на выполнение работ заказ на покупку будет связан с проектом в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d2844-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="d2844-127">После изменения значения **Состояние системы** из **Открыто — В работе(690,970,000)** на более высокий статус, поле **Внешний проект** будет заблокировано и вы больше не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="d2844-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d2844-128">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="d2844-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="d2844-129">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="d2844-129">Supply Chain Management</span></span>
<span data-ttu-id="d2844-130">Включение отслеживания изменений для информационного объекта проектов</span><span class="sxs-lookup"><span data-stu-id="d2844-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d2844-131">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="d2844-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="d2844-132">Проекты (из Supply Chain Management в Field Service): Проекты</span><span class="sxs-lookup"><span data-stu-id="d2844-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="d2844-133">[![Сопоставление шаблона в интеграции данных](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="d2844-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
