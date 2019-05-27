---
title: Настройка workflow-процессов для расходов
description: Можно настроить workflow-процесс, который используется для просмотра и утверждения документов командировок и расходов.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8294aaa344e3cb6b79fa4f33f368258ca19c8205
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565144"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="0b123-103">Настройка workflow-процессов для расходов</span><span class="sxs-lookup"><span data-stu-id="0b123-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b123-104"> Можно настроить workflow-процесс, который используется для просмотра и утверждения документов командировок и расходов.</span><span class="sxs-lookup"><span data-stu-id="0b123-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="0b123-105">Документы, для которых может быть определен workflow-процесс, включают в себя отчеты о расходах, заявки на командировки и запросы денежных авансов.</span><span class="sxs-lookup"><span data-stu-id="0b123-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="0b123-106">Бизнес-правило представляет бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="0b123-106">A workflow represents a business process.</span></span> <span data-ttu-id="0b123-107">Он определяет путь движения документа по системе и указывает, кто должен выполнить ту или иную задачу или утвердить тот или иной документ.</span><span class="sxs-lookup"><span data-stu-id="0b123-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="0b123-108">Имеется несколько преимуществ использования системы workflow-процессов в организации:</span><span class="sxs-lookup"><span data-stu-id="0b123-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="0b123-109">**Непротиворечивые процессы** — можно определить процесс утверждения для конкретных документов, таких как заявки на покупку и отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="0b123-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="0b123-110">Использование системы workflow-процессов позволяет обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="0b123-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="0b123-111">Видимость процессов — можно отслеживать статус, историю и метрики производительности конкретного экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="0b123-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="0b123-112">Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="0b123-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="0b123-113">Централизованный список работ — пользователи могут просматривать централизованный список работ для просмотра назначенных им задач и утверждений workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="0b123-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="0b123-114">**Могут быть созданы следующие типы workflow-процессов**</span><span class="sxs-lookup"><span data-stu-id="0b123-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="0b123-115">В следующей таблице перечислены типы workflow-процессов, которые можно создавать в модуле **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="0b123-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="0b123-116"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="0b123-117"><strong>Тип, который будет использоваться</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="0b123-118"><strong>Отчет о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="0b123-119">Создайте workflow-процессы утверждения для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="0b123-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="0b123-120"><strong>Автоматическая разноска отчета о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="0b123-121">Создайте workflow-процессы автоматической разноски для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="0b123-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="0b123-122"><strong>Элемент строки расхода</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="0b123-123">Создайте workflow-процессы утверждения для номенклатур строк в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="0b123-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="0b123-124"><strong>Автоматическая разноска номенклатуры строки расхода</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="0b123-125">Создайте workflow-процессы автоматической разноски для номенклатур строк в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="0b123-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="0b123-126"><strong>Заявка на командировку</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="0b123-127">Создайте workflow-процессы утверждения для заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="0b123-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="0b123-128"><strong>Запрос денежного аванса</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="0b123-129">Создайте workflow-процессы утверждения для запросов на денежный аванс.</span><span class="sxs-lookup"><span data-stu-id="0b123-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="0b123-130"><strong>Возмещение НДС</strong></span><span class="sxs-lookup"><span data-stu-id="0b123-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="0b123-131">Создайте workflow-процессы утверждения для возмещения НДС.</span><span class="sxs-lookup"><span data-stu-id="0b123-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

