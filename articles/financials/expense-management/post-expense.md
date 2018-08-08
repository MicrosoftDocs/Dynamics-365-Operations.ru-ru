---
title: "Разноска отчета о расходах"
description: "В этом разделе объясняется, как разнести отчет о расходах в главную книгу."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 1252825848aedcdaf633c04edddddca7dd09d774
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="post-an-expense-report"></a><span data-ttu-id="48699-103">Разноска отчета о расходах</span><span class="sxs-lookup"><span data-stu-id="48699-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48699-104">После утверждения отчета о накладных расходах и передачи его в журнал операций отчет можно разнести в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="48699-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="48699-105">При разноске отчета о расходах определяются расходы, по которым возможен возврат налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="48699-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="48699-106">Задача проверки и восстановление платежей НДС назначена сотруднику, ответственному за проверку отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="48699-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="48699-107">Если расходы в отчете о расходах отнесены к компании, иной нежели та, в которой работает сотрудник, необходимо проверить компанию, которая понесла расходы, и компанию, которая покрыла расходы.</span><span class="sxs-lookup"><span data-stu-id="48699-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="48699-108">Например, сотрудник, который отправил отчет о расходах, работает на компанию DAT, но выставил расходы компании DIR.</span><span class="sxs-lookup"><span data-stu-id="48699-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="48699-109">В этом случае DAT является компанией, которая понесла расходы, и DIR является компанией, которая должна покрыть расходы.</span><span class="sxs-lookup"><span data-stu-id="48699-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="48699-110">После проверки этих строк журнала, можно разнести строки расходов в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="48699-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="48699-111">Для разности отчета о расходах на странице **Утвержденные отчеты по расходам** выберите отчет по расходам, затем в области действий выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="48699-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="48699-112">Можно также одновременно разнести все отчеты о расходах из списка.</span><span class="sxs-lookup"><span data-stu-id="48699-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="48699-113">Выберите все отчеты о расходах, затем выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="48699-113">Select all the expense reports, and then select **Post**.</span></span>

