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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "355733"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="52434-103">Настройка workflow-процессов для расходов</span><span class="sxs-lookup"><span data-stu-id="52434-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52434-104"> Можно настроить workflow-процесс, который используется для просмотра и утверждения документов командировок и расходов.</span><span class="sxs-lookup"><span data-stu-id="52434-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="52434-105">Документы, для которых может быть определен workflow-процесс, включают в себя отчеты о расходах, заявки на командировки и запросы денежных авансов.</span><span class="sxs-lookup"><span data-stu-id="52434-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="52434-106">Бизнес-правило представляет бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="52434-106">A workflow represents a business process.</span></span> <span data-ttu-id="52434-107">Он определяет путь движения документа по системе и указывает, кто должен выполнить ту или иную задачу или утвердить тот или иной документ.</span><span class="sxs-lookup"><span data-stu-id="52434-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="52434-108">Имеется несколько преимуществ использования системы workflow-процессов в организации:</span><span class="sxs-lookup"><span data-stu-id="52434-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="52434-109">**Непротиворечивые процессы** — можно определить процесс утверждения для конкретных документов, таких как заявки на покупку и отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="52434-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="52434-110">Использование системы workflow-процессов позволяет обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="52434-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="52434-111">Видимость процессов — можно отслеживать статус, историю и метрики производительности конкретного экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="52434-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="52434-112">Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="52434-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="52434-113">Централизованный список работ — пользователи могут просматривать централизованный список работ для просмотра назначенных им задач и утверждений workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="52434-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="52434-114">**Могут быть созданы следующие типы workflow-процессов**</span><span class="sxs-lookup"><span data-stu-id="52434-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="52434-115">В следующей таблице перечислены типы workflow-процессов, которые можно создавать в модуле **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="52434-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="52434-116"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="52434-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="52434-117"><strong>Тип, который будет использоваться</strong></span><span class="sxs-lookup"><span data-stu-id="52434-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="52434-118"><strong>Отчет о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="52434-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="52434-119">Создайте workflow-процессы утверждения для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="52434-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="52434-120"><strong>Автоматическая разноска отчета о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="52434-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="52434-121">Создайте workflow-процессы автоматической разноски для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="52434-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="52434-122"><strong>Элемент строки расхода</strong></span><span class="sxs-lookup"><span data-stu-id="52434-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="52434-123">Создайте workflow-процессы утверждения для номенклатур строк в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="52434-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="52434-124"><strong>Автоматическая разноска номенклатуры строки расхода</strong></span><span class="sxs-lookup"><span data-stu-id="52434-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="52434-125">Создайте workflow-процессы автоматической разноски для номенклатур строк в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="52434-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="52434-126"><strong>Заявка на командировку</strong></span><span class="sxs-lookup"><span data-stu-id="52434-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="52434-127">Создайте workflow-процессы утверждения для заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="52434-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="52434-128"><strong>Запрос денежного аванса</strong></span><span class="sxs-lookup"><span data-stu-id="52434-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="52434-129">Создайте workflow-процессы утверждения для запросов на денежный аванс.</span><span class="sxs-lookup"><span data-stu-id="52434-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="52434-130"><strong>Возмещение НДС</strong></span><span class="sxs-lookup"><span data-stu-id="52434-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="52434-131">Создайте workflow-процессы утверждения для возмещения НДС.</span><span class="sxs-lookup"><span data-stu-id="52434-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

