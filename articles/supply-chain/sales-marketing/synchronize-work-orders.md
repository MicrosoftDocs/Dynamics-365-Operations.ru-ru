---
title: Синхронизация заказов на выполнение работ с проектом из Field Service в Supply Chain Management
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Dynamics 365 Field Service в Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 3678fbca8244ae6dcd050f6a91ff3b35d90e1064
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251715"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="52886-103">Синхронизация заказов на выполнение работ с проектом из Field Service в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="52886-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="52886-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Dynamics 365 Field Service в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="52886-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="52886-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="52886-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="52886-106">Используемый шаблон **Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management)** основан на шаблоне **Заказы на выполнение работ (из Field Service в Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="52886-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="52886-107">Дополнительные сведения см. в разделе [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу в Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="52886-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="52886-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="52886-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="52886-109">**Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="52886-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="52886-110">**Заказы на выполнение работ (из Field Service в Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="52886-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="52886-111">Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Supply Chain Management, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта.</span><span class="sxs-lookup"><span data-stu-id="52886-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="52886-112">Помимо этого, шаблон использует расширенные запросы и фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="52886-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="52886-113">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="52886-113">Templates and tasks</span></span>

<span data-ttu-id="52886-114">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="52886-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="52886-115">Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="52886-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="52886-116">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="52886-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="52886-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="52886-117">WorkOrderHeader</span></span>
- <span data-ttu-id="52886-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="52886-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="52886-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="52886-119">WorkOrderProduct</span></span>
- <span data-ttu-id="52886-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="52886-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="52886-121">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="52886-121">Field Service CRM solution</span></span>
<span data-ttu-id="52886-122">Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ".</span><span class="sxs-lookup"><span data-stu-id="52886-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="52886-123">Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="52886-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="52886-124">Когда значение **Состояние системы** изменяется из "Открыто — В работе(690 970 000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="52886-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="52886-125">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="52886-125">Template mapping in Data integration</span></span>

<span data-ttu-id="52886-126">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="52886-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="52886-127">Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="52886-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="52886-128">[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="52886-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="52886-129">Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="52886-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="52886-130">[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="52886-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="52886-131">Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="52886-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="52886-132">[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="52886-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="52886-133">Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="52886-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="52886-134">[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="52886-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
