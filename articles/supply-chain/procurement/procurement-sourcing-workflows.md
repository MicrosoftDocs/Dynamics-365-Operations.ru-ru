---
title: "Workflow-процессы модуля \"Закупки и источники\""
description: "В некоторых организациях требуется, чтобы заявки на покупку и заказы на покупку утверждались пользователем, отличным от сотрудника, который ввел проводку. Чтобы настроить процесс утверждения, можно создать workflow-процесс."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3bf244786e308ebcaee27a16fae378f41086f963
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="8384d-104">Workflow-процессы модуля "Закупки и источники"</span><span class="sxs-lookup"><span data-stu-id="8384d-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8384d-105">В некоторых организациях требуется, чтобы заявки на покупку и заказы на покупку утверждались пользователем, отличным от сотрудника, который ввел проводку.</span><span class="sxs-lookup"><span data-stu-id="8384d-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="8384d-106">Чтобы настроить процесс утверждения, можно создать workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="8384d-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="8384d-107">Бизнес-правило представляет бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="8384d-107">A workflow represents a business process.</span></span> <span data-ttu-id="8384d-108">Он определяет путь движения документа по системе и указывает, кто должен выполнить ту или иную задачу или утвердить тот или иной документ.</span><span class="sxs-lookup"><span data-stu-id="8384d-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8384d-109">Имеется несколько преимуществ использования системы workflow-процессов в организации:</span><span class="sxs-lookup"><span data-stu-id="8384d-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="8384d-110">**Непротиворечивые процессы** — можно определить процесс утверждения для конкретных документов, таких как заявки на покупку и отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="8384d-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8384d-111">Использование системы workflow-процессов позволяет обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="8384d-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="8384d-112">**Видимость процессов** — можно отслеживать статус, историю и метрики производительности конкретного экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="8384d-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8384d-113">Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="8384d-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="8384d-114">**Централизованный список работ** — пользователи могут просматривать централизованный список работ для просмотра задач workflow-процесса и утверждений, в которых они участвуют.</span><span class="sxs-lookup"><span data-stu-id="8384d-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="8384d-115">Это доступно на странице "Рабочие элементы".</span><span class="sxs-lookup"><span data-stu-id="8384d-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="8384d-116">Типы бизнес-правил, которые можно создавать</span><span class="sxs-lookup"><span data-stu-id="8384d-116">The types of workflows that you can create</span></span>
<span data-ttu-id="8384d-117">Доступны следующие типы бизнес-правила для Закупок и источников.</span><span class="sxs-lookup"><span data-stu-id="8384d-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8384d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8384d-118">**Type**</span></span>                         | <span data-ttu-id="8384d-119">**Тип, который будет использоваться**</span><span class="sxs-lookup"><span data-stu-id="8384d-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="8384d-120">Обзор заявок на покупку</span><span class="sxs-lookup"><span data-stu-id="8384d-120">Purchase requisition review</span></span>      | <span data-ttu-id="8384d-121">Создание бизнес-правил проверки для заявок на закупку.</span><span class="sxs-lookup"><span data-stu-id="8384d-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="8384d-122">Рассмотрение строки заявки на покупку</span><span class="sxs-lookup"><span data-stu-id="8384d-122">Purchase requisition line review</span></span> | <span data-ttu-id="8384d-123">Создание бизнес-правил для просмотра строк заявки на закупку.</span><span class="sxs-lookup"><span data-stu-id="8384d-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="8384d-124">Workflow-процесс заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="8384d-124">Purchase order workflow</span></span>          | <span data-ttu-id="8384d-125">Проверка и утверждение бизнес-правил для заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="8384d-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="8384d-126">Workflow-процесс строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="8384d-126">Purchase order line workflow</span></span>     | <span data-ttu-id="8384d-127">Создание бизнес-правила для проверки и утверждения для строк заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="8384d-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="8384d-128">Создание workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="8384d-128">Creating a workflow</span></span>
<span data-ttu-id="8384d-129">Чтобы создать workflow-процесс, перейдите к пункту "Закупки и источники" &gt; "Настройка" &gt; "Workflow-процессы модуля "Закупки и источники" и создайте новый workflow-процесс, выбрав тип создаваемого workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="8384d-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="8384d-130">В холсте workflow-процесса можно перетаскивать элементы workflow-процесса в конструктор и связывать элементы в поток.</span><span class="sxs-lookup"><span data-stu-id="8384d-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="8384d-131">Элементы workflow-процесса должны быть настроены.</span><span class="sxs-lookup"><span data-stu-id="8384d-131">The workflow elements should be configured.</span></span> <span data-ttu-id="8384d-132">Для утверждения и элементов workflow-процесса задачи можно настроить, какой участник должен выполнять действие.</span><span class="sxs-lookup"><span data-stu-id="8384d-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="8384d-133">Типы участников</span><span class="sxs-lookup"><span data-stu-id="8384d-133">Types of participants</span></span>
----------------------

<span data-ttu-id="8384d-134">Можно назначить шаг утверждения следующим группам участников.</span><span class="sxs-lookup"><span data-stu-id="8384d-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="8384d-135">Группа пользователей</span><span class="sxs-lookup"><span data-stu-id="8384d-135">User group</span></span>    | <span data-ttu-id="8384d-136">Описание</span><span class="sxs-lookup"><span data-stu-id="8384d-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="8384d-137">Участник</span><span class="sxs-lookup"><span data-stu-id="8384d-137">Participant</span></span>   | <span data-ttu-id="8384d-138">Назначение шага утверждения членам группы или роли.</span><span class="sxs-lookup"><span data-stu-id="8384d-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="8384d-139">Иерархия</span><span class="sxs-lookup"><span data-stu-id="8384d-139">Hierarchy</span></span>     | <span data-ttu-id="8384d-140">Назначение шага утверждения пользователям в определенной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="8384d-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="8384d-141">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="8384d-141">Workflow user</span></span> | <span data-ttu-id="8384d-142">Назначение шага утверждения пользователям данного workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="8384d-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="8384d-143">Очередь</span><span class="sxs-lookup"><span data-stu-id="8384d-143">Queue</span></span>         | <span data-ttu-id="8384d-144">Назначение шага утверждения очереди задач.</span><span class="sxs-lookup"><span data-stu-id="8384d-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="8384d-145">Пользователь</span><span class="sxs-lookup"><span data-stu-id="8384d-145">User</span></span>          | <span data-ttu-id="8384d-146">Назначение шага утверждения для конкретных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8384d-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="8384d-147">См. также</span><span class="sxs-lookup"><span data-stu-id="8384d-147">See also</span></span>
--------

[<span data-ttu-id="8384d-148">Определение workflow-процессов бизнес-процессов для заявок на покупку</span><span class="sxs-lookup"><span data-stu-id="8384d-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="8384d-149">Документооборот заявок на закупку</span><span class="sxs-lookup"><span data-stu-id="8384d-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




