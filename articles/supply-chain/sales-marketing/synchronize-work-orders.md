---
title: Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "329858"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="a3a2c-103">Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3a2c-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3a2c-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a3a2c-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="a3a2c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="a3a2c-106">Используемый шаблон **Продукты Field Service (из Finance and Operations в Field Service)** основан на шаблоне **Продукты (из Finance and Operations в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="a3a2c-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="a3a2c-107">Дополнительные сведения см. в разделе [Продукты (из Finance and Operations в Sales) — напрямую](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="a3a2c-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="a3a2c-108">В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Finance and Operations в Field Service)** и **Продукты (из Finance and Operations в Field Service) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="a3a2c-109">Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Finance and Operations, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="a3a2c-110">Помимо этого, шаблон использует расширенные запросы и фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a3a2c-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="a3a2c-111">Templates and tasks</span></span>

<span data-ttu-id="a3a2c-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="a3a2c-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a3a2c-113">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a3a2c-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="a3a2c-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="a3a2c-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="a3a2c-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="a3a2c-115">WorkOrderHeader</span></span>
- <span data-ttu-id="a3a2c-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="a3a2c-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="a3a2c-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="a3a2c-117">WorkOrderProduct</span></span>
- <span data-ttu-id="a3a2c-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="a3a2c-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="a3a2c-119">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="a3a2c-119">Field Service CRM solution</span></span>
<span data-ttu-id="a3a2c-120">Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ".</span><span class="sxs-lookup"><span data-stu-id="a3a2c-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="a3a2c-121">Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="a3a2c-122">После изменения значения **Состояние системы** из "Открыто — В работе(690,970,000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a3a2c-123">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="a3a2c-123">Template mapping in Data integration</span></span>

<span data-ttu-id="a3a2c-124">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="a3a2c-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="a3a2c-125">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="a3a2c-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="a3a2c-126">[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="a3a2c-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="a3a2c-127">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="a3a2c-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="a3a2c-128">[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="a3a2c-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="a3a2c-129">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="a3a2c-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="a3a2c-130">[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="a3a2c-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="a3a2c-131">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="a3a2c-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="a3a2c-132">[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="a3a2c-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
