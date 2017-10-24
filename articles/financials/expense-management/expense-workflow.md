---
title: "Workflow-процесс для рассмотрения расходов"
description: "В этой теме рассматривается, как использовать систему workflow-процессов Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition для настройки процесса рассмотрения отчетов о расходах в модуле \"Управление расходами\"."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c2e01d4da04cd24c2df1690e6e354e1c03cb50d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="expense-workflow"></a><span data-ttu-id="93998-103">Workflow-процесс для рассмотрения расходов</span><span class="sxs-lookup"><span data-stu-id="93998-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="93998-104">Систему workflow-процессов Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition можно использовать для настройки процесса рассмотрения отчетов о расходах в модуле "Управление расходами".</span><span class="sxs-lookup"><span data-stu-id="93998-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="93998-105">Вы можете настроить workflow-процесс, в котором будут использоваться следующие критерии для определения того, кто должен утверждать отчеты о расходах:</span><span class="sxs-lookup"><span data-stu-id="93998-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="93998-106">Иерархия подотчетности сотрудников и предварительно определенные лимиты утверждения</span><span class="sxs-lookup"><span data-stu-id="93998-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="93998-107">Многоуровневое утверждение, которое поддерживает промежуточных утверждающих и окончательного утверждающего</span><span class="sxs-lookup"><span data-stu-id="93998-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="93998-108">Финансовые аналитики и ответственность за проект</span><span class="sxs-lookup"><span data-stu-id="93998-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="93998-109">Назначение определенным пользователям или группам пользователей</span><span class="sxs-lookup"><span data-stu-id="93998-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="93998-110">Утверждения в рамках workflow-процессов могут создаваться для отчетов о расходах, заявках о командировках, денежных авансов и возмещения налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="93998-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="93998-111">**Пример**</span><span class="sxs-lookup"><span data-stu-id="93998-111">**Example**</span></span>

<span data-ttu-id="93998-112">Следующий процесс является примером workflow-процесса управления расходами для отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="93998-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="93998-113">Сотрудник создает и сохраняет отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="93998-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="93998-114">Сотрудник отправляет отчет о расходах на утверждение.</span><span class="sxs-lookup"><span data-stu-id="93998-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="93998-115">Утверждающее лицо определяется на основании правил, определенных при настройке рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="93998-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="93998-116">Утверждающее лицо получает уведомление о том, что отчет о расходах готов для утверждения.</span><span class="sxs-lookup"><span data-stu-id="93998-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="93998-117">Утверждающее лицо просматривает отчет о расходах и проверяет выполнение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="93998-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="93998-118">Расходы не противоречат политикам расходов.</span><span class="sxs-lookup"><span data-stu-id="93998-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="93998-119">Если расход нарушает политику, утверждающее лицо проверяет, содержит ли отчет о расходах допустимое деловое обоснование.</span><span class="sxs-lookup"><span data-stu-id="93998-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="93998-120">К отчету о расходах присоединяются электронные квитанции.</span><span class="sxs-lookup"><span data-stu-id="93998-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="93998-121">Утверждающее лицо утверждает отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="93998-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="93998-122">Отчет о расходах назначается координатору расчетов с поставщиками для разноски.</span><span class="sxs-lookup"><span data-stu-id="93998-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="93998-123">Происходит одно из следующих действий в зависимости от того, настроена ли автоматическая разноска:</span><span class="sxs-lookup"><span data-stu-id="93998-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="93998-124">Если автоматическая разноска настроена, отчет о расходах обрабатывается для оплаты, и статус отчета о расходах обновляется.</span><span class="sxs-lookup"><span data-stu-id="93998-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="93998-125">Если автоматическая разноска не настроена, координатор расчетов с поставщиками проверяет, предоставлены ли все исходные квитанции и соответствуют ли они расходам в отчете о расходах.</span><span class="sxs-lookup"><span data-stu-id="93998-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="93998-126">Также должна быть проверена правильность всех налоговых кодов, указанных в отчете о расходах.</span><span class="sxs-lookup"><span data-stu-id="93998-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="93998-127">После проверки этих требований, отчет о расходах разносится.</span><span class="sxs-lookup"><span data-stu-id="93998-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="93998-128">После разноски отчета о расходах по отчету о расходах авторизуется платеж и сотруднику возмещаются расходы.</span><span class="sxs-lookup"><span data-stu-id="93998-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
