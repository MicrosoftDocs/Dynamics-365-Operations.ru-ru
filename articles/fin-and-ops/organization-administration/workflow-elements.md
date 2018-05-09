---
title: "Элементы workflow-процесса"
description: "В этом разделе описываются различные элементы, которые составляют workflow-процесс."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: abd2782ebe98fd25fc491b4b3cbcd4a6dd5c4cbd
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="workflow-elements"></a><span data-ttu-id="41f73-103">Элементы workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="41f73-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41f73-104">В этом разделе описываются различные элементы, которые составляют workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="41f73-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="41f73-105">Бизнес-правило состоит из элементов.</span><span class="sxs-lookup"><span data-stu-id="41f73-105">A workflow consists of elements.</span></span> <span data-ttu-id="41f73-106">В следующих разделах описан каждый из этих типов элементов.</span><span class="sxs-lookup"><span data-stu-id="41f73-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="41f73-107">Задачи</span><span class="sxs-lookup"><span data-stu-id="41f73-107">Tasks</span></span>
<span data-ttu-id="41f73-108">*Задача* — это единица работы, которая должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="41f73-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="41f73-109">Есть два типа задач, которые могут быть добавлены в workflow-процесс: ручные задачи или автоматизированные задачи.</span><span class="sxs-lookup"><span data-stu-id="41f73-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="41f73-110">Выполняемая вручную задача</span><span class="sxs-lookup"><span data-stu-id="41f73-110">Manual task</span></span>

<span data-ttu-id="41f73-111">*Ручная задача* — это единица работы, которая должна быть выполнена пользователем.</span><span class="sxs-lookup"><span data-stu-id="41f73-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="41f73-112">Например, workflow-процесс отчета по расходам может иметь ручные задачи, которые требуют от назначенных пользователей выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="41f73-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="41f73-113">Просмотреть чеки, которые направляются с отчетом по расходам.</span><span class="sxs-lookup"><span data-stu-id="41f73-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="41f73-114">позвонить менеджеру сотрудника</span><span class="sxs-lookup"><span data-stu-id="41f73-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="41f73-115">Автоматизированная задача</span><span class="sxs-lookup"><span data-stu-id="41f73-115">Automated task</span></span>

<span data-ttu-id="41f73-116">*Автоматическая задача* — это единица работы, которая должна быть выполнена системой.</span><span class="sxs-lookup"><span data-stu-id="41f73-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="41f73-117">Вмешательство человека не требуется.</span><span class="sxs-lookup"><span data-stu-id="41f73-117">No human interaction is required.</span></span> <span data-ttu-id="41f73-118">Например, workflow-процесс заказа на продажу может иметь автоматизированные задачи, которые требуют от системы выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="41f73-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="41f73-119">Выполнить проверку кредита.</span><span class="sxs-lookup"><span data-stu-id="41f73-119">Perform a credit check.</span></span>
-   <span data-ttu-id="41f73-120">Создать запись клиента для клиента, если запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="41f73-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="41f73-121">Процессы утверждения</span><span class="sxs-lookup"><span data-stu-id="41f73-121">Approval processes</span></span>
<span data-ttu-id="41f73-122">*Процесс утверждения* - это процесс, состоящий из отдельных шагов.</span><span class="sxs-lookup"><span data-stu-id="41f73-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="41f73-123">На каждом шаге утверждения пользователь может выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="41f73-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="41f73-124">Утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="41f73-124">Approve the document.</span></span>
-   <span data-ttu-id="41f73-125">Отклонить документ.</span><span class="sxs-lookup"><span data-stu-id="41f73-125">Reject the document.</span></span>
-   <span data-ttu-id="41f73-126">Запросить изменение документа.</span><span class="sxs-lookup"><span data-stu-id="41f73-126">Request a change to the document.</span></span>
-   <span data-ttu-id="41f73-127">Назначить документ другому пользователю для утверждения.</span><span class="sxs-lookup"><span data-stu-id="41f73-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="41f73-128">Элементы Workflow-процесса по строке</span><span class="sxs-lookup"><span data-stu-id="41f73-128">Line-item workflow elements</span></span>
<span data-ttu-id="41f73-129">Workflow-процесс может быть создан для обработки или документов, или строковых элементов в документе.</span><span class="sxs-lookup"><span data-stu-id="41f73-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="41f73-130">Например, вы создали workflow-процесс утверждения для табелей.</span><span class="sxs-lookup"><span data-stu-id="41f73-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="41f73-131">(Мы будем называть данный workflow-процесс как *workflow-процесс документов*.) Можно добавить элемент *workflow-процесс по строке* к данному workflow-процессу документов.</span><span class="sxs-lookup"><span data-stu-id="41f73-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="41f73-132">Когда выполняется элемент строкового элемента, каждый строковый элемент в документе отправляется для обработки.</span><span class="sxs-lookup"><span data-stu-id="41f73-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="41f73-133">Можно указать, что все элементы строки должны обрабатываться одним workflow-процессом по строке, а также можно указать, что каждую элемент строки должны обрабатываться отдельным workflow-процессом по строке.</span><span class="sxs-lookup"><span data-stu-id="41f73-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="41f73-134">Предположим, что сотрудник предоставил табель, похожий на следующий рисунок.</span><span class="sxs-lookup"><span data-stu-id="41f73-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Workflow-процесс с номенклатурами строк](./media/workflow_lineitemworkflow.gif) 

<span data-ttu-id="41f73-136">В этом сценарии имеет смысл создать следующие workflow-процессы по строке:</span><span class="sxs-lookup"><span data-stu-id="41f73-136">In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="41f73-137">**Workflow-процесс по строке 1** — этот workflow-процесс использоваться для обработки элементов строки, где код проекта равен 1111.</span><span class="sxs-lookup"><span data-stu-id="41f73-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="41f73-138">**Workflow-процесс по строке 2** — этот workflow-процесс использоваться для обработки элементов строки, где код проекта равен 2222.</span><span class="sxs-lookup"><span data-stu-id="41f73-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="41f73-139">**Workflow-процесс по строке 3** — этот workflow-процесс использоваться для обработки элементов строки, где код проекта равен 3333.</span><span class="sxs-lookup"><span data-stu-id="41f73-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="41f73-140">Элементы управления потоком</span><span class="sxs-lookup"><span data-stu-id="41f73-140">Flow-control elements</span></span>
<span data-ttu-id="41f73-141">Следующие элементы позволяют разрабатывать workflow-процессы, которые имеют какую-либо альтернативные ветви или ветви, которые работают одновременно.</span><span class="sxs-lookup"><span data-stu-id="41f73-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="41f73-142">Решение вручную</span><span class="sxs-lookup"><span data-stu-id="41f73-142">Manual decision</span></span>

<span data-ttu-id="41f73-143">*Ручное решение* — точка, в которой workflow-процесс делится на две ветви.</span><span class="sxs-lookup"><span data-stu-id="41f73-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="41f73-144">Пользователь должен принять решение, и это решение определяет ветвь, которая будет использоваться для обработки отправленного документа.</span><span class="sxs-lookup"><span data-stu-id="41f73-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="41f73-145">Условное решение</span><span class="sxs-lookup"><span data-stu-id="41f73-145">Conditional decision</span></span>

<span data-ttu-id="41f73-146">*Условное решение* — точка, в которой workflow-процесс делится на две ветви.</span><span class="sxs-lookup"><span data-stu-id="41f73-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="41f73-147">Однако система решает, которая ветвь используется для обработки документа, который был представлен.</span><span class="sxs-lookup"><span data-stu-id="41f73-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="41f73-148">Чтобы принять решение, система оценит документ и определит, соответствует ли он указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="41f73-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="41f73-149">Параллельное мероприятие</span><span class="sxs-lookup"><span data-stu-id="41f73-149">Parallel activity</span></span>

<span data-ttu-id="41f73-150">*Параллельное мероприятие* представляет собой элемент workflow-процесса, который включает две или несколько ветвей workflow-процесса, выполняемых одновременно</span><span class="sxs-lookup"><span data-stu-id="41f73-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="41f73-151">Вспомогательный workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="41f73-151">Subworkflow</span></span>

<span data-ttu-id="41f73-152">*Вспомогательный workflow-процесс* — это workflow-процесс, запускаемый в рамках другого workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="41f73-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




