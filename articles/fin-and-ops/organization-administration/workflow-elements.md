---
title: Элементы workflow-процесса
description: В этом разделе описываются различные элементы, которые составляют workflow-процесс.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fa9613b37fceeda1ea73c5fd5d4f7a7edc74cf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "333814"
---
# <a name="workflow-elements"></a><span data-ttu-id="a4bed-103">Элементы workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="a4bed-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4bed-104">В этом разделе описываются различные элементы, которые составляют workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="a4bed-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="a4bed-105">Бизнес-правило состоит из элементов.</span><span class="sxs-lookup"><span data-stu-id="a4bed-105">A workflow consists of elements.</span></span> <span data-ttu-id="a4bed-106">В следующих разделах описан каждый из этих типов элементов.</span><span class="sxs-lookup"><span data-stu-id="a4bed-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="a4bed-107">Задачи</span><span class="sxs-lookup"><span data-stu-id="a4bed-107">Tasks</span></span>

<span data-ttu-id="a4bed-108">*Задача* — это единица работы, которая должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="a4bed-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="a4bed-109">Есть два типа задач, которые могут быть добавлены в workflow-процесс: ручные задачи или автоматизированные задачи.</span><span class="sxs-lookup"><span data-stu-id="a4bed-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="a4bed-110">Выполняемая вручную задача</span><span class="sxs-lookup"><span data-stu-id="a4bed-110">Manual task</span></span>

<span data-ttu-id="a4bed-111">*Ручная задача* — это единица работы, которая должна быть выполнена пользователем.</span><span class="sxs-lookup"><span data-stu-id="a4bed-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="a4bed-112">Например, workflow-процесс отчета по расходам может иметь ручные задачи, которые требуют от назначенных пользователей выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="a4bed-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="a4bed-113">Просмотреть чеки, которые направляются с отчетом по расходам.</span><span class="sxs-lookup"><span data-stu-id="a4bed-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="a4bed-114">позвонить менеджеру сотрудника</span><span class="sxs-lookup"><span data-stu-id="a4bed-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="a4bed-115">Автоматизированная задача</span><span class="sxs-lookup"><span data-stu-id="a4bed-115">Automated task</span></span>

<span data-ttu-id="a4bed-116">*Автоматическая задача* — это единица работы, которая должна быть выполнена системой.</span><span class="sxs-lookup"><span data-stu-id="a4bed-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="a4bed-117">Вмешательство человека не требуется.</span><span class="sxs-lookup"><span data-stu-id="a4bed-117">No human interaction is required.</span></span> <span data-ttu-id="a4bed-118">Например, workflow-процесс заказа на продажу может иметь автоматизированные задачи, которые требуют от системы выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="a4bed-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="a4bed-119">Выполнить проверку кредита.</span><span class="sxs-lookup"><span data-stu-id="a4bed-119">Perform a credit check.</span></span>
- <span data-ttu-id="a4bed-120">Создать запись клиента для клиента, если запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a4bed-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="a4bed-121">Процессы утверждения</span><span class="sxs-lookup"><span data-stu-id="a4bed-121">Approval processes</span></span>

<span data-ttu-id="a4bed-122">*Процесс утверждения* - это процесс, состоящий из отдельных шагов.</span><span class="sxs-lookup"><span data-stu-id="a4bed-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="a4bed-123">На каждом шаге утверждения пользователь может выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a4bed-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="a4bed-124">Утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="a4bed-124">Approve the document.</span></span>
- <span data-ttu-id="a4bed-125">Отклонить документ.</span><span class="sxs-lookup"><span data-stu-id="a4bed-125">Reject the document.</span></span>
- <span data-ttu-id="a4bed-126">Запросить изменение документа.</span><span class="sxs-lookup"><span data-stu-id="a4bed-126">Request a change to the document.</span></span>
- <span data-ttu-id="a4bed-127">Назначить документ другому пользователю для утверждения.</span><span class="sxs-lookup"><span data-stu-id="a4bed-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="a4bed-128">Элементы Workflow-процесса по строке</span><span class="sxs-lookup"><span data-stu-id="a4bed-128">Line-item workflow elements</span></span>

<span data-ttu-id="a4bed-129">Workflow-процесс может быть создан для обработки или документов, или строковых элементов в документе.</span><span class="sxs-lookup"><span data-stu-id="a4bed-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="a4bed-130">Например, вы создали workflow-процесс утверждения для табелей.</span><span class="sxs-lookup"><span data-stu-id="a4bed-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="a4bed-131">(Мы будем называть данный workflow-процесс как *workflow-процесс документов*.) Можно добавить элемент *workflow-процесс по строке* к данному workflow-процессу документов.</span><span class="sxs-lookup"><span data-stu-id="a4bed-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="a4bed-132">Когда выполняется элемент строкового элемента, каждый строковый элемент в документе отправляется для обработки.</span><span class="sxs-lookup"><span data-stu-id="a4bed-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="a4bed-133">Можно указать, что все элементы строки должны обрабатываться одним workflow-процессом по строке, а также можно указать, что каждую элемент строки должны обрабатываться отдельным workflow-процессом по строке.</span><span class="sxs-lookup"><span data-stu-id="a4bed-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="a4bed-134">Предположим, что сотрудник предоставил табель, похожий на следующий рисунок.</span><span class="sxs-lookup"><span data-stu-id="a4bed-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Workflow-процесс с номенклатурами строк](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="a4bed-136">В этом сценарии имеет смысл создать следующие workflow-процессы по строке:</span><span class="sxs-lookup"><span data-stu-id="a4bed-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="a4bed-137">**Workflow-процесс по строке 1** — этот workflow-процесс использоваться для обработки элементов строки, где код проекта равен 1111.</span><span class="sxs-lookup"><span data-stu-id="a4bed-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="a4bed-138">**Workflow-процесс по строке 2** — этот workflow-процесс использоваться для обработки элементов строки, где код проекта равен 2222.</span><span class="sxs-lookup"><span data-stu-id="a4bed-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="a4bed-139">**Workflow-процесс по строке 3** — этот workflow-процесс использоваться для обработки элементов строки, где код проекта равен 3333.</span><span class="sxs-lookup"><span data-stu-id="a4bed-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="a4bed-140">Элементы управления потоком</span><span class="sxs-lookup"><span data-stu-id="a4bed-140">Flow-control elements</span></span>

<span data-ttu-id="a4bed-141">Следующие элементы позволяют разрабатывать workflow-процессы, которые имеют какую-либо альтернативные ветви или ветви, которые работают одновременно.</span><span class="sxs-lookup"><span data-stu-id="a4bed-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="a4bed-142">Решение вручную</span><span class="sxs-lookup"><span data-stu-id="a4bed-142">Manual decision</span></span>

<span data-ttu-id="a4bed-143">*Ручное решение* — точка, в которой workflow-процесс делится на две ветви.</span><span class="sxs-lookup"><span data-stu-id="a4bed-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="a4bed-144">Пользователь должен принять решение, и это решение определяет ветвь, которая будет использоваться для обработки отправленного документа.</span><span class="sxs-lookup"><span data-stu-id="a4bed-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="a4bed-145">Условное решение</span><span class="sxs-lookup"><span data-stu-id="a4bed-145">Conditional decision</span></span>

<span data-ttu-id="a4bed-146">*Условное решение* — точка, в которой workflow-процесс делится на две ветви.</span><span class="sxs-lookup"><span data-stu-id="a4bed-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="a4bed-147">Однако система решает, которая ветвь используется для обработки документа, который был представлен.</span><span class="sxs-lookup"><span data-stu-id="a4bed-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="a4bed-148">Чтобы принять решение, система оценит документ и определит, соответствует ли он указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="a4bed-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="a4bed-149">Параллельное мероприятие</span><span class="sxs-lookup"><span data-stu-id="a4bed-149">Parallel activity</span></span>

<span data-ttu-id="a4bed-150">*Параллельное мероприятие* представляет собой элемент workflow-процесса, который включает две или несколько ветвей workflow-процесса, выполняемых одновременно</span><span class="sxs-lookup"><span data-stu-id="a4bed-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="a4bed-151">Вспомогательный workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="a4bed-151">Subworkflow</span></span>

<span data-ttu-id="a4bed-152">*Вспомогательный workflow-процесс* — это workflow-процесс, запускаемый в рамках другого workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a4bed-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
