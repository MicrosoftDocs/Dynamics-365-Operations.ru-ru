---
title: "Настройка workflow-процессов для расходов"
description: "Можно настроить workflow-процесс, который используется для просмотра и утверждения документов командировок и расходов."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="a7c43-103">Настройка workflow-процессов для расходов</span><span class="sxs-lookup"><span data-stu-id="a7c43-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="a7c43-104"> Можно настроить workflow-процесс, который используется для просмотра и утверждения документов командировок и расходов.</span><span class="sxs-lookup"><span data-stu-id="a7c43-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="a7c43-105">Документы, для которых может быть определен workflow-процесс, включают в себя отчеты о расходах, заявки на командировки и запросы денежных авансов.</span><span class="sxs-lookup"><span data-stu-id="a7c43-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="a7c43-106">Бизнес-правило представляет бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="a7c43-106">A workflow represents a business process.</span></span> <span data-ttu-id="a7c43-107">Он определяет путь движения документа по системе и указывает, кто должен выполнить ту или иную задачу или утвердить тот или иной документ.</span><span class="sxs-lookup"><span data-stu-id="a7c43-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="a7c43-108">Имеется несколько преимуществ использования системы workflow-процессов в организации:</span><span class="sxs-lookup"><span data-stu-id="a7c43-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="a7c43-109">**Непротиворечивые процессы** — можно определить процесс утверждения для конкретных документов, таких как заявки на покупку и отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="a7c43-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="a7c43-110">Использование системы workflow-процессов позволяет обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="a7c43-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="a7c43-111">Видимость процессов — можно отслеживать статус, историю и метрики производительности конкретного экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a7c43-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="a7c43-112">Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="a7c43-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="a7c43-113">Централизованный список работ — пользователи могут просматривать централизованный список работ для просмотра назначенных им задач и утверждений workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a7c43-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="a7c43-114">**Могут быть созданы следующие типы workflow-процессов**</span><span class="sxs-lookup"><span data-stu-id="a7c43-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="a7c43-115">В следующей таблице перечислены типы workflow-процессов, которые можно создавать в модуле **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="a7c43-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="a7c43-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a7c43-116">**Type**</span></span>                           | <span data-ttu-id="a7c43-117">**Тип, который будет использоваться**</span><span class="sxs-lookup"><span data-stu-id="a7c43-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="a7c43-118">**Отчет о расходах**</span><span class="sxs-lookup"><span data-stu-id="a7c43-118">**Expense report**</span></span>                 | <span data-ttu-id="a7c43-119">Создайте workflow-процессы утверждения для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="a7c43-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="a7c43-120">**Автоматическая разноска отчета о расходах**</span><span class="sxs-lookup"><span data-stu-id="a7c43-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="a7c43-121">Создайте workflow-процессы автоматической разноски для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="a7c43-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="a7c43-122">**Элемент строки расхода**</span><span class="sxs-lookup"><span data-stu-id="a7c43-122">**Expense line item**</span></span>              | <span data-ttu-id="a7c43-123">Создайте workflow-процессы утверждения для номенклатур строк в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="a7c43-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="a7c43-124">**Автоматическая разноска номенклатуры строки расхода**</span><span class="sxs-lookup"><span data-stu-id="a7c43-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="a7c43-125">Создайте workflow-процессы автоматической разноски для номенклатур строк в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="a7c43-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="a7c43-126">**Заявка на командировку**</span><span class="sxs-lookup"><span data-stu-id="a7c43-126">**Travel requisition**</span></span>             | <span data-ttu-id="a7c43-127">Создайте workflow-процессы утверждения для заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="a7c43-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="a7c43-128">**Запрос денежного аванса**</span><span class="sxs-lookup"><span data-stu-id="a7c43-128">**Cash advance request**</span></span>           | <span data-ttu-id="a7c43-129">Создайте workflow-процессы утверждения для запросов на денежный аванс.</span><span class="sxs-lookup"><span data-stu-id="a7c43-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="a7c43-130">**Возмещение НДС**</span><span class="sxs-lookup"><span data-stu-id="a7c43-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="a7c43-131">Создайте workflow-процессы утверждения для возмещения НДС.</span><span class="sxs-lookup"><span data-stu-id="a7c43-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

