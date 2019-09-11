---
title: Обзор системы бизнес-правил
description: В этой теме описывается система workflow-процессов в Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2692b9f3595ab001151f8e53a25010474bcd233
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864800"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="664d0-103">Обзор системы бизнес-правил</span><span class="sxs-lookup"><span data-stu-id="664d0-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="664d0-104">В этой теме описывается система workflow-процессов в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="664d0-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="664d0-105">Что такое Wokrflow?</span><span class="sxs-lookup"><span data-stu-id="664d0-105">What is workflow?</span></span>

<span data-ttu-id="664d0-106">Термин *workflow-процесс* можно определить 2 способами: как система и как бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="664d0-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="664d0-107">Документооборот как система</span><span class="sxs-lookup"><span data-stu-id="664d0-107">Workflow is a system</span></span>

<span data-ttu-id="664d0-108">Workflow-процесс — это система, которая устанавливается с Finance and Operations и выполняется на сервере Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="664d0-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="664d0-109">Система workflow-процессов предоставляет функции, позволяющие создавать отдельные workflow-процессы, или бизнес-процессы.</span><span class="sxs-lookup"><span data-stu-id="664d0-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="664d0-110">Документооборот как бизнес-процесс</span><span class="sxs-lookup"><span data-stu-id="664d0-110">Workflow is a business process</span></span>

<span data-ttu-id="664d0-111">workflow-процесс представляет бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="664d0-111">A workflow represents a business process.</span></span> <span data-ttu-id="664d0-112">Он определяет потоки, или перемещения, документа по системе, показывая, кто должен выполнить задачу, принять решение или утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="664d0-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="664d0-113">Например, на следующем рисунке показан workflow-процесс для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="664d0-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Workflow-процесс с элементами, назначенными пользователям](./media/workflow_user.gif)

<span data-ttu-id="664d0-115">Для прояснения этого workflow-процесса предположим, что Сэм подает отчет о расходах на сумму USD 7000.</span><span class="sxs-lookup"><span data-stu-id="664d0-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="664d0-116">В этом случае Иван должен рассмотреть приходы, направленные ему Сэмом.</span><span class="sxs-lookup"><span data-stu-id="664d0-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="664d0-117">Затем Фрэнк и Сью должны утвердить отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="664d0-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="664d0-118">Теперь предположим, что Сэм подает отчет о расходах на сумму 11 000 USD.</span><span class="sxs-lookup"><span data-stu-id="664d0-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="664d0-119">В этом случае Иван должен рассмотреть чеки, а Фрэнк, Сью и Анна должны утвердить отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="664d0-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="664d0-120">Преимущества использования системы workflow-процессов</span><span class="sxs-lookup"><span data-stu-id="664d0-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="664d0-121">Имеется несколько преимуществ использования системы workflow-процессов в организации:</span><span class="sxs-lookup"><span data-stu-id="664d0-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="664d0-122">**Непротиворечивые процессы** - можно определить как обрабатываются определенные документы, таких как заявки на покупку и отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="664d0-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="664d0-123">Использование системы workflow-процессов может обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="664d0-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="664d0-124">**Видимость процессов** - можно отслеживать статус, историю и метрики производительности экземпляров workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="664d0-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="664d0-125">Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="664d0-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="664d0-126">**Централизованный список работ** — Пользователи могут просматривать централизованный список работ, отображающий задачи workflow-процесса и утверждения, назначенные им.</span><span class="sxs-lookup"><span data-stu-id="664d0-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="664d0-127">Содержимое workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="664d0-127">Workflow content</span></span>

+ [<span data-ttu-id="664d0-128">Архитектура workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="664d0-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="664d0-129">Элементы workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="664d0-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="664d0-130">Действия workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="664d0-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="664d0-131">Создание workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="664d0-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="664d0-132">Настройка свойств workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="664d0-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="664d0-133">Настройка ручной задачи в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="664d0-134">Настройка автоматизированной задачи в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="664d0-135">Настройка процесса утверждения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="664d0-136">Настройка этапа утверждения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="664d0-137">Настройка ручного решения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="664d0-138">Настройка условного решения в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="664d0-139">Настройка параллельного действия в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="664d0-140">Настройка параллельной ветви в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="664d0-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="664d0-141">Настройка workflow-процесса по номенклатуре строки</span><span class="sxs-lookup"><span data-stu-id="664d0-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="664d0-142">Вопросы и ответы по workflow-процессу</span><span class="sxs-lookup"><span data-stu-id="664d0-142">Workflow FAQ</span></span>](workflow-FAQ.md)
