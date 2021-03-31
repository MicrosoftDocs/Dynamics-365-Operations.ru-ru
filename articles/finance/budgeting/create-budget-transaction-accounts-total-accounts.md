---
title: Создание бюджета из счетов проводки и итоговых счетов
description: Эта статья содержит обзор процесса для создания бюджетов на основе итоговых счетов. Она также описывает, как включить бюджетный контроль для итоговых счетов, если бюджетный контроль требуется.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 085bc12433616d2da2bda40a8412fb88e40db3b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210201"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="e52bb-104">Создание бюджета из счетов проводки и итоговых счетов</span><span class="sxs-lookup"><span data-stu-id="e52bb-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e52bb-105">Эта статья содержит обзор процесса для создания бюджетов на основе итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="e52bb-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="e52bb-106">Она также описывает, как включить бюджетный контроль для итоговых счетов, если бюджетный контроль требуется.</span><span class="sxs-lookup"><span data-stu-id="e52bb-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="e52bb-107">План бюджета и документы записей регистра бюджета позволяют для выполнять бюджетирование по счетам ГК, с типом счета ГК **Итого**.</span><span class="sxs-lookup"><span data-stu-id="e52bb-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="e52bb-108">Фактические показатели можно разносить только на транзакционные счета ГК.</span><span class="sxs-lookup"><span data-stu-id="e52bb-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="e52bb-109">Для периодического процесса **Создать бюджетный план на основе главной книги** на вкладке **Источник**, вы можете указать тип счета ГК **Итого** как критерий.</span><span class="sxs-lookup"><span data-stu-id="e52bb-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="e52bb-110">В этом случае каждый итоговый счет ГК будет включен в целевой бюджетный план, и сумма будет равна итоговой сумме диапазона выбранных счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="e52bb-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="e52bb-111">Вы можете активировать бюджетный контроль для счетов ГК типа **Итого**.</span><span class="sxs-lookup"><span data-stu-id="e52bb-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="e52bb-112">Эта функциональность поддерживается за счет использования бюджетных групп.</span><span class="sxs-lookup"><span data-stu-id="e52bb-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="e52bb-113">Для каждого итогового счета ГК бюджет, для которого должно реализовано управление для бюджетной группы, необходимо создать на странице **Конфигурация бюджетного контроля**.</span><span class="sxs-lookup"><span data-stu-id="e52bb-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="e52bb-114">Критерии, которые вы определяете, должны включать итоговый счет ГК и диапазон счетов.</span><span class="sxs-lookup"><span data-stu-id="e52bb-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="e52bb-115">Для того, чтобы ускорить процесс создания бюджетных групп, вы можете воспользоваться преимуществами информационного объекта групп бюджетного контроля.</span><span class="sxs-lookup"><span data-stu-id="e52bb-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="e52bb-116">При использовании бюджета в отчетности, например в финансовом отчете, сумма бюджета для итогового счета состоит из следующих сумм.</span><span class="sxs-lookup"><span data-stu-id="e52bb-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="e52bb-117">Бюджеты, созданные для каждого счета учета проводок в течение интервала итогового счета.</span><span class="sxs-lookup"><span data-stu-id="e52bb-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="e52bb-118">бюджетная сумма, непосредственно введенная в итоговом счете.</span><span class="sxs-lookup"><span data-stu-id="e52bb-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="e52bb-119">Это позволяет создавать отдельные бюджеты для самых важных счетов проводок в течение интервала итогового счета и затем добавить доступную бюджетную сумму в итоговый счет.</span><span class="sxs-lookup"><span data-stu-id="e52bb-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]