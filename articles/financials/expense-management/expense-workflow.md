---
title: Workflow-процесс для рассмотрения расходов
description: В этой теме рассматривается, как использовать систему workflow-процессов Microsoft Dynamics 365 for Finance and Operations для настройки процесса рассмотрения отчетов о расходах в модуле "Управление расходами".
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
ms.openlocfilehash: 037a6ae00b7d559f79860901f0cb2ad6ddddd7aa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "310124"
---
# <a name="expense-workflow"></a><span data-ttu-id="95403-103">Workflow-процесс для рассмотрения расходов</span><span class="sxs-lookup"><span data-stu-id="95403-103">Expense workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95403-104">Вы можете использовать систему workflow-процессов в Microsoft Dynamics 365 for Finance and Operations, чтобы настроить процесс рассмотрения для отчетов о расходах в модуле "Управление расходами".</span><span class="sxs-lookup"><span data-stu-id="95403-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="95403-105">Вы можете настроить workflow-процесс, в котором будут использоваться следующие критерии для определения того, кто должен утверждать отчеты о расходах:</span><span class="sxs-lookup"><span data-stu-id="95403-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="95403-106">Иерархия подотчетности сотрудников и предварительно определенные лимиты утверждения</span><span class="sxs-lookup"><span data-stu-id="95403-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="95403-107">Многоуровневое утверждение, которое поддерживает промежуточных утверждающих и окончательного утверждающего</span><span class="sxs-lookup"><span data-stu-id="95403-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="95403-108">Финансовые аналитики и ответственность за проект</span><span class="sxs-lookup"><span data-stu-id="95403-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="95403-109">Назначение определенным пользователям или группам пользователей</span><span class="sxs-lookup"><span data-stu-id="95403-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="95403-110">Утверждения в рамках workflow-процессов могут создаваться для отчетов о расходах, заявках о командировках, денежных авансов и возмещения налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="95403-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="95403-111">**Пример**</span><span class="sxs-lookup"><span data-stu-id="95403-111">**Example**</span></span>

<span data-ttu-id="95403-112">Следующий процесс является примером workflow-процесса управления расходами для отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="95403-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="95403-113">Сотрудник создает и сохраняет отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="95403-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="95403-114">Сотрудник отправляет отчет о расходах на утверждение.</span><span class="sxs-lookup"><span data-stu-id="95403-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="95403-115">Утверждающее лицо определяется на основании правил, определенных при настройке рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="95403-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="95403-116">Утверждающее лицо получает уведомление о том, что отчет о расходах готов для утверждения.</span><span class="sxs-lookup"><span data-stu-id="95403-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="95403-117">Утверждающее лицо просматривает отчет о расходах и проверяет выполнение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="95403-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="95403-118">Расходы не противоречат политикам расходов.</span><span class="sxs-lookup"><span data-stu-id="95403-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="95403-119">Если расход нарушает политику, утверждающее лицо проверяет, содержит ли отчет о расходах допустимое деловое обоснование.</span><span class="sxs-lookup"><span data-stu-id="95403-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="95403-120">К отчету о расходах присоединяются электронные квитанции.</span><span class="sxs-lookup"><span data-stu-id="95403-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="95403-121">Утверждающее лицо утверждает отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="95403-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="95403-122">Отчет о расходах назначается координатору расчетов с поставщиками для разноски.</span><span class="sxs-lookup"><span data-stu-id="95403-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="95403-123">Происходит одно из следующих действий в зависимости от того, настроена ли автоматическая разноска:</span><span class="sxs-lookup"><span data-stu-id="95403-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="95403-124">Если автоматическая разноска настроена, отчет о расходах обрабатывается для оплаты, и статус отчета о расходах обновляется.</span><span class="sxs-lookup"><span data-stu-id="95403-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="95403-125">Если автоматическая разноска не настроена, координатор расчетов с поставщиками проверяет, предоставлены ли все исходные квитанции и соответствуют ли они расходам в отчете о расходах.</span><span class="sxs-lookup"><span data-stu-id="95403-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="95403-126">Также должна быть проверена правильность всех налоговых кодов, указанных в отчете о расходах.</span><span class="sxs-lookup"><span data-stu-id="95403-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="95403-127">После проверки этих требований, отчет о расходах разносится.</span><span class="sxs-lookup"><span data-stu-id="95403-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="95403-128">После разноски отчета о расходах по отчету о расходах авторизуется платеж и сотруднику возмещаются расходы.</span><span class="sxs-lookup"><span data-stu-id="95403-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
