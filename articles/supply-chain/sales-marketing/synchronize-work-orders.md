---
title: "Синхронизация заказов на выполнение работ Finance and Operations с Field Service"
description: "В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service с Microsoft Dynamics 365 for Finance and Operations."
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="3805f-103">Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3805f-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3805f-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service с Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3805f-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="3805f-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="3805f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="3805f-106">Используемый шаблон **Продукты Field Service (из Finance and Operations в Field Service)** основан на шаблоне **Продукты (из Finance and Operations в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="3805f-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="3805f-107">Дополнительные сведения см. в разделе [Продукты (из Finance and Operations в Sales) — напрямую](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="3805f-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="3805f-108">В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Finance and Operations в Field Service)** и **Продукты (из Finance and Operations в Field Service) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="3805f-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="3805f-109">Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Finance and Operations, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта.</span><span class="sxs-lookup"><span data-stu-id="3805f-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="3805f-110">Помимо этого, шаблон использует расширенные запросы и фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="3805f-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3805f-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="3805f-111">Templates and tasks</span></span>

<span data-ttu-id="3805f-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="3805f-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="3805f-113">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="3805f-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="3805f-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="3805f-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="3805f-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="3805f-115">WorkOrderHeader</span></span>
- <span data-ttu-id="3805f-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="3805f-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="3805f-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="3805f-117">WorkOrderProduct</span></span>
- <span data-ttu-id="3805f-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="3805f-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="3805f-119">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="3805f-119">Field Service CRM solution</span></span>
<span data-ttu-id="3805f-120">Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ".</span><span class="sxs-lookup"><span data-stu-id="3805f-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="3805f-121">Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3805f-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="3805f-122">После изменения значения **Состояние системы** из "Открыто — В работе(690,970,000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="3805f-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3805f-123">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="3805f-123">Template mapping in Data integration</span></span>

<span data-ttu-id="3805f-124">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="3805f-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="3805f-125">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="3805f-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="3805f-126">[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="3805f-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="3805f-127">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="3805f-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="3805f-128">[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="3805f-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="3805f-129">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="3805f-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="3805f-130">[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="3805f-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="3805f-131">Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="3805f-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="3805f-132">[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="3805f-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

