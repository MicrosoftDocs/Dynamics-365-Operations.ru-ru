---
title: Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2019
ms.locfileid: "836450"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="f6d59-103">Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6d59-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f6d59-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6d59-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f6d59-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="f6d59-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="f6d59-106">Используемый шаблон **Заказы на выполнение работ с проектом (из Field Service в Fin and Ops)** основан на шаблоне **Заказы на выполнение работ (из Field Service в Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="f6d59-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="f6d59-107">Дополнительные сведения см. в разделе [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу в Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="f6d59-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="f6d59-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="f6d59-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="f6d59-109">**Заказы на выполнение работ с проектом (из Field Service в Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="f6d59-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="f6d59-110">**Заказы на выполнение работ (из Field Service в Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="f6d59-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="f6d59-111">Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Finance and Operations, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта.</span><span class="sxs-lookup"><span data-stu-id="f6d59-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="f6d59-112">Помимо этого, шаблон использует расширенные запросы и фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="f6d59-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f6d59-113">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="f6d59-113">Templates and tasks</span></span>

<span data-ttu-id="f6d59-114">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="f6d59-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="f6d59-115">Заказы на выполнение работ с проектом (из Field Service в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f6d59-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="f6d59-116">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="f6d59-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="f6d59-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="f6d59-117">WorkOrderHeader</span></span>
- <span data-ttu-id="f6d59-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="f6d59-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="f6d59-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="f6d59-119">WorkOrderProduct</span></span>
- <span data-ttu-id="f6d59-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="f6d59-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f6d59-121">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="f6d59-121">Field Service CRM solution</span></span>
<span data-ttu-id="f6d59-122">Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ".</span><span class="sxs-lookup"><span data-stu-id="f6d59-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="f6d59-123">Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6d59-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="f6d59-124">После изменения значения **Состояние системы** из "Открыто — В работе(690,970,000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.</span><span class="sxs-lookup"><span data-stu-id="f6d59-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f6d59-125">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="f6d59-125">Template mapping in Data integration</span></span>

<span data-ttu-id="f6d59-126">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="f6d59-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="f6d59-127">Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="f6d59-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="f6d59-128">[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="f6d59-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="f6d59-129">Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="f6d59-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="f6d59-130">[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="f6d59-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="f6d59-131">Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="f6d59-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="f6d59-132">[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="f6d59-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="f6d59-133">Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="f6d59-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="f6d59-134">[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="f6d59-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
