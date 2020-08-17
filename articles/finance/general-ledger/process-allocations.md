---
title: Обработка распределений
description: Эта статья представляет информацию о распределениях, параметры для обработки их в Microsoft Dynamics 365 Finance и как их можно использовать в бюджетном планировании. Распределения используются для распределения сумм на несколько комбинаций счетов ГК. Они помогают обеспечить, что расходы или выручка начисляются на правильные объекты учета.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 4676ea9646fa1a182103ecab93e78a69001f0b8d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "3612670"
---
# <a name="process-allocations"></a><span data-ttu-id="57e3f-105">Обработка распределений</span><span class="sxs-lookup"><span data-stu-id="57e3f-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57e3f-106">Эта статья представляет информацию о распределениях, параметры для их обработки и как их можно использовать в бюджетном планировании.</span><span class="sxs-lookup"><span data-stu-id="57e3f-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="57e3f-107">Распределения используются для распределения сумм на несколько комбинаций счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="57e3f-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="57e3f-108">Они помогают обеспечить, что расходы или выручка начисляются на правильные объекты учета.</span><span class="sxs-lookup"><span data-stu-id="57e3f-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="57e3f-109">Этот процесс поддерживают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="57e3f-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="57e3f-110">Распределение сумм проводок вручную с помощью действия "Разделить" в распределении по бухгалтерским счетам или путем применения шаблонов финансовых аналитик по умолчанию к документу.</span><span class="sxs-lookup"><span data-stu-id="57e3f-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="57e3f-111">Дополнительные сведения см. в разделе [Распределения по бухгалтерским счетам](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="57e3f-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="57e3f-112">Автоматическое распределение сумм проводок на основании условий распределения, определенных в отдельном счете ГК.</span><span class="sxs-lookup"><span data-stu-id="57e3f-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="57e3f-113">Записи счета распределения будут созданы для каждого журнала на основании процента и целевого счета ГК, когда запись учета соответствует критериям, определенным как исходный счет ГК.</span><span class="sxs-lookup"><span data-stu-id="57e3f-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="57e3f-114">Дополнительные сведения см. в разделе [Условия распределения счета ГК](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="57e3f-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="57e3f-115">Автоматическое распределение сальдо ГК или фиксированных сумм на основании правила распределения ГК.</span><span class="sxs-lookup"><span data-stu-id="57e3f-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="57e3f-116">Правила распределения ГК обрабатываются на периодической основе с помощью журналов распределения.</span><span class="sxs-lookup"><span data-stu-id="57e3f-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="57e3f-117">Дополнительные сведения см. в разделе [Правила распределения](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="57e3f-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="57e3f-118">Распределения в бюджетном планировании</span><span class="sxs-lookup"><span data-stu-id="57e3f-118">Allocations in budget planning</span></span>

<span data-ttu-id="57e3f-119">Правила распределения ГК можно использовать для бюджетных планов.</span><span class="sxs-lookup"><span data-stu-id="57e3f-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="57e3f-120">Если правила распределения главной книги используются при бюджетном планировании, правила распределения работают таким же образом, как в главной книге, но исходные данные и конечные данные поступают из бюджетного плана.</span><span class="sxs-lookup"><span data-stu-id="57e3f-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="57e3f-121">Правила распределения главной книги для использования в бюджетных планах можно выбрать вручную.</span><span class="sxs-lookup"><span data-stu-id="57e3f-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="57e3f-122">В качестве альтернативы можно использовать график распределения, выполняемый в рамках workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="57e3f-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="57e3f-123">При бюджетной планировании невозможно использовать внутрихолдинговые правила распределения главной книги.</span><span class="sxs-lookup"><span data-stu-id="57e3f-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

