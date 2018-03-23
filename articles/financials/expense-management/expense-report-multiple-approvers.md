---
title: "Отчеты о расходах и несколько утверждающих"
description: "В этом разделе представлены сведения об отчетах о расходах, которые требуют утверждения несколькими пользователями."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: ru-ru
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="b086b-103">Отчеты о расходах и несколько утверждающих</span><span class="sxs-lookup"><span data-stu-id="b086b-103">Expense reports and multiple approvers</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b086b-104">В зависимости от политик утверждения расходов вашей организации может потребоваться, чтобы несколько человек утверждали отчет о расходах, переданный сотрудником.</span><span class="sxs-lookup"><span data-stu-id="b086b-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="b086b-105">При настройке workflow-процесса для утверждения отчета о расходах можно добавить дополнительные элемента workflow-процесса, которые содержат задачи или шаги для одного или нескольких лиц, утверждающих отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="b086b-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="b086b-106">Например, можно требовать, чтобы все отчеты о расходах сначала утверждались руководителем сотрудника, передавшего отчет, а затем — координатором расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="b086b-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="b086b-107">Если вы решили использовать несколько лиц, утверждающих отчет о расходах, вы можете добавить элементы workflow-процесса следующими способами.</span><span class="sxs-lookup"><span data-stu-id="b086b-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="b086b-108">Добавьте один элемент утверждения, который имеет один шаг.</span><span class="sxs-lookup"><span data-stu-id="b086b-108">Add one approval element that has one step.</span></span> <span data-ttu-id="b086b-109">Например, шаг может требовать, чтобы отчет о расходах был назначен группе пользователей, и чтобы его утвердили 50 процентов участников этой группы.</span><span class="sxs-lookup"><span data-stu-id="b086b-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="b086b-110">Добавьте один элемент утверждения, который имеет несколько шагов.</span><span class="sxs-lookup"><span data-stu-id="b086b-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="b086b-111">Например, элемент утверждения может содержать следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="b086b-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="b086b-112">Руководитель сотрудника, создавшего отчет о расходах, утверждает его.</span><span class="sxs-lookup"><span data-stu-id="b086b-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="b086b-113">Сотрудник отдела расчетов с поставщиками проверяет получения и номенклатуры отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="b086b-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="b086b-114">Владелец бюджета утверждает отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="b086b-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="b086b-115">Добавьте несколько элементов утверждения, каждый из которых содержит один шаг.</span><span class="sxs-lookup"><span data-stu-id="b086b-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="b086b-116">Например, можно добавить отдельный элемент утверждения для каждого из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="b086b-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="b086b-117">Руководитель сотрудника утверждает отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="b086b-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="b086b-118">Владелец бюджета утверждает отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="b086b-118">The budget owner approves the expense report.</span></span>

