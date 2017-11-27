---
title: "Контракты по проектам"
description: "В этой теме приводятся примеры контрактов по проекту, которые можно создавать для различных типов проектов и источников финансирования, а также для управления контрактами и клиентами счета по проекту в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c8328bd2d93bbe763e629248edc1b7b4576005ae
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="project-contracts"></a><span data-ttu-id="6f2a4-103">Контракты по проектам</span><span class="sxs-lookup"><span data-stu-id="6f2a4-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6f2a4-104">В этой статье приводятся примеры контрактов по проекту, которые можно создавать для различных типов проектов и источников финансирования, а также для управления контрактами и клиентами счета по проекту в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="6f2a4-105">Тип проекта, создаваемый для контракта по проекту, определяет метод, используемый для выставления накладных клиентам проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="6f2a4-106">Можно изменить контракт по проекту и связанный проект, но невозможно изменить тип проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="6f2a4-107">При помощи контрактов по проекту можно выставлять накладные для нескольких проектов одновременно.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="6f2a4-108">Контракт по проекту позволяет также убедиться в том, что для каждого подпроекта в структуре проектов используется одна и та же процедура выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="6f2a4-109">Каждый проект, по которому будет выставлена накладная, связан с контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="6f2a4-110">Настройки для контракта по проекту влияют на все проекты и подпроекты, связанные с этим контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="6f2a4-111">В контракте проекта может быть указан один или несколько источников финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="6f2a4-112">Таким образом, можно разделить накладные между несколькими поставщиками, задать лимиты финансирования, чтобы источнику финансирования не выставлялись накладные, превышающие указанную сумму, и настроить правила финансирования для выставления накладных по расходам.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="6f2a4-113">Финансирование по контрактам по проектам</span><span class="sxs-lookup"><span data-stu-id="6f2a4-113">Funding for project contracts</span></span>
<span data-ttu-id="6f2a4-114">В некоторых контрактах по проектам может быть указано, что ответственность за финансирование затрат по проекту несут несколько сторон.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="6f2a4-115">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-115">Here are some examples:</span></span>

-   <span data-ttu-id="6f2a4-116">Крупный клиент, который имеет несколько подразделений, требует разделить финансирование проекта между подразделениями.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="6f2a4-117">Компания разделяет расходы крупного проекта с внешней организацией.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="6f2a4-118">Дорожный проект совместно финансируется двумя муниципалитетами.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="6f2a4-119">Проект по мосту финансируется за счет гранта правительства и частной корпорации.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="6f2a4-120">В Finance and Operations можно разделить выписывание накладных для одной проводки или всего проекта между несколькими клиентами, грантами или организациями.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="6f2a4-121">В проектах, финансируемых несколькими субъектами, все субъекты, которые участвуют в финансировании сложного проекта, называются источниками финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="6f2a4-122">После определения клиента, организации или гранта в качестве источника финансирования они могут быть назначены одному или нескольким правилам финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="6f2a4-123">Правила финансирования содержат критерии для распределения расходов между различными источниками финансирования проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="6f2a4-124">Поскольку учитываемые в запасах номенклатуры, например номенклатуры, которые отображаются в заявках на покупку и заказах на покупку, невозможно разделить, сумму затрат невозможно разделить между несколькими источниками финансирования во время распределения.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="6f2a4-125">Следовательно, значение источника финансирования остается на нуле до тех пор, пока не будет разнесен расход запасов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="6f2a4-126">После разноски расхода запасов сумма затрат распределяется в соответствии с правилами распределения по счетам для проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="6f2a4-127">Вот некоторые шаги, которые можно предпринять для того, чтобы упростить разделение выписывания накладных между несколькими источниками финансирования:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="6f2a4-128">Указать, что во всех вводимые по проекту проводках используется та же валюта продаж, что и в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="6f2a4-129">Настроить лимиты финансирования так, чтобы на источник финансирования не выставлялись накладные по проекту, превышающие заданную сумму.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="6f2a4-130">Настройка правил финансирования и лимитов финансирования для каждого работника, номенклатуры, категории, группы категорий и типа проводок (или для всех типов проводок).</span><span class="sxs-lookup"><span data-stu-id="6f2a4-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="6f2a4-131">Выбрать необязательные даты начала и окончания, чтобы определить период времени, в течение которого действует каждое правило финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="6f2a4-132">Ввести процент, за который несет ответственность каждый источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="6f2a4-133">Указать, какой из источников финансирования является ответственным за ошибки округления, возникающие в результате расчетов распределения финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="6f2a4-134">Настроить правила, определяющие, как затраты по проекту выставляются в виде накладных внешним клиентам и относятся на внутренние организации.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="6f2a4-135">Записать проводки на счет заблокированного финансирования до тех пор, пока не будет получено дополнительное финансирование или не будет принято решение отнести затраты на внутренние организации.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="6f2a4-136">Чтобы определить, какую налоговую группу связать с проводкой, в проекте выполняется поиск назначения налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="6f2a4-137">Если на уровне проекта нет назначения налоговых групп, выполняется поиск в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="6f2a4-138">Пример: несколько источников финансирования (простой)</span><span class="sxs-lookup"><span data-stu-id="6f2a4-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="6f2a4-139">В следующей таблице приведены сценарии управления распределением финансирования среди нескольких источников финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="6f2a4-140">Эти сценарии основаны на следующих предположениях.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="6f2a4-141">Параметры приоритета учтены при распределении финансирования до или после применения остальных критериев.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="6f2a4-142">Не указан диапазон дат действия правил финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f2a4-143"><strong>Сценарий</strong></span><span class="sxs-lookup"><span data-stu-id="6f2a4-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="6f2a4-144"><strong>Источник финансирования</strong></span><span class="sxs-lookup"><span data-stu-id="6f2a4-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="6f2a4-145"><strong>Процент распределения</strong></span><span class="sxs-lookup"><span data-stu-id="6f2a4-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="6f2a4-146"><strong>Приоритет распределения</strong></span><span class="sxs-lookup"><span data-stu-id="6f2a4-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2a4-147">Требуется распределить затраты по одному источнику финансирования, пока его фонды не будут исчерпаны, распределить затраты по второму источнику финансирования, пока его фонды не будут исчерпаны, и, наконец, распределить затраты по третьему источнику финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-148">Источник финансирования 1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="6f2a4-149">Источник финансирования 2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="6f2a4-150">Источник финансирования 3</span><span class="sxs-lookup"><span data-stu-id="6f2a4-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-151">100%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-151">100%</span></span></li>
<li><span data-ttu-id="6f2a4-152">100%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-152">100%</span></span></li>
<li><span data-ttu-id="6f2a4-153">100%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-154">1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-154">1</span></span></li>
<li><span data-ttu-id="6f2a4-155">2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-155">2</span></span></li>
<li><span data-ttu-id="6f2a4-156">3</span><span class="sxs-lookup"><span data-stu-id="6f2a4-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f2a4-157">Требуется распределить 75 процентов затрат по одному источнику финансирования и 25 процентов по второму источнику финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="6f2a4-158">Если в одном из этих источников финансирования закончатся средства, оставшуюся сумму требуется оплатить из третьего источника финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-159">Источник финансирования 1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="6f2a4-160">Источник финансирования 2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="6f2a4-161">Источник финансирования 3</span><span class="sxs-lookup"><span data-stu-id="6f2a4-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-162">75%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-162">75%</span></span></li>
<li><span data-ttu-id="6f2a4-163">25%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-163">25%</span></span></li>
<li><span data-ttu-id="6f2a4-164">100%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-165">1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-165">1</span></span></li>
<li><span data-ttu-id="6f2a4-166">1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-166">1</span></span></li>
<li><span data-ttu-id="6f2a4-167">2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2a4-168">Требуется распределить 75 процентов затрат по одному источнику финансирования и 25 процентов по второму источнику финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="6f2a4-169">Если в одном из этих источников финансирования закончатся средства, оставшуюся сумму оплаты требуется разделить между третьим и четвертым источниками финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-170">Источник финансирования 1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="6f2a4-171">Источник финансирования 2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="6f2a4-172">Источник финансирования 3</span><span class="sxs-lookup"><span data-stu-id="6f2a4-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="6f2a4-173">Источник финансирования 4</span><span class="sxs-lookup"><span data-stu-id="6f2a4-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-174">75%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-174">75%</span></span></li>
<li><span data-ttu-id="6f2a4-175">25%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-175">25%</span></span></li>
<li><span data-ttu-id="6f2a4-176">50%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-176">50%</span></span></li>
<li><span data-ttu-id="6f2a4-177">50%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-178">1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-178">1</span></span></li>
<li><span data-ttu-id="6f2a4-179">1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-179">1</span></span></li>
<li><span data-ttu-id="6f2a4-180">2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-180">2</span></span></li>
<li><span data-ttu-id="6f2a4-181">2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f2a4-182">Требуется распределить первые 25 процентов затрат по одному источнику финансирования, а остаток — по второму.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-183">Источник финансирования 1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="6f2a4-184">Источник финансирования 2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-185">25%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-185">25%</span></span></li>
<li><span data-ttu-id="6f2a4-186">100%</span><span class="sxs-lookup"><span data-stu-id="6f2a4-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6f2a4-187">1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-187">1</span></span></li>
<li><span data-ttu-id="6f2a4-188">2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="6f2a4-189">Пример: несколько источников финансирования (сложный)</span><span class="sxs-lookup"><span data-stu-id="6f2a4-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="6f2a4-190">Имеется три источника финансирования, которые требуется использовать в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="6f2a4-191">Использование источника финансирования 2 и источника финансирования 3 поровну до полного расходования средств в источнике финансирования 2.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="6f2a4-192">Дальнейшее использование источника финансирования 3 до расходования его средств.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="6f2a4-193">Использование источника финансирования 1 после расходования средств в источнике финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="6f2a4-194">Для этого необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="6f2a4-195">Настройте лимиты финансирования для источника финансирования 2 и источника финансирования 3 для их соответствующих сумм.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="6f2a4-196">Создайте следующие правила финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="6f2a4-197">Правило 1 (приоритет 1): распределять 50 процентов проводок для источника финансирования 2 и 50 процентов для источника финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="6f2a4-198">Правило 2 (приоритет 2): распределять 100 процентов проводок для источника финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="6f2a4-199">Правило 3 (приоритет 3): распределять 100 процентов проводок для источника финансирования 1.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="6f2a4-200">Такая настройка действует, поскольку проводки проверяются относительно правил и лимитов, чтобы определить, применяются ли какие-либо привила и лимиты к проводке.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="6f2a4-201">Если к проводке не применяются никакие правили или лимиты, действует правило Все проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="6f2a4-202">Правило всех проводок сопоставляет все проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="6f2a4-203">Если найдено правило, которое сопоставляется проводке, сначала применяется процент, который был распределен в этом правиле, однако это происходит только после проверки сопоставлений относительно настроенных лимитов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="6f2a4-204">Если лимит соблюден и фонды источника финансирования израсходованы, правило финансирования, которое связано с лимитом финансирования, пропускается и программа проверяет следующее применимое правило.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="6f2a4-205">В некоторых случаях в соответствии с правилом может быть распределена только часть проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="6f2a4-206">Это может произойти по достижении лимита при распределении проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="6f2a4-207">В таком случае в соответствии с правилом распределяется только определенная сумма, например 50 процентов для каждого источника финансирования.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="6f2a4-208">Это случай действия правила 1, описанного ранее в данном разделе.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="6f2a4-209">Остаток распределяется в соответствии со следующим правилом в последовательности.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="6f2a4-210">Этот сценарий более подробно представлен в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f2a4-211"><strong>Фокусирование</strong></span><span class="sxs-lookup"><span data-stu-id="6f2a4-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="6f2a4-212"><strong>Подробности</strong></span><span class="sxs-lookup"><span data-stu-id="6f2a4-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2a4-213">Правила финансирования</span><span class="sxs-lookup"><span data-stu-id="6f2a4-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-214">Правило 1 (приоритет 1): все проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="6f2a4-215">Распределить 50% из источника финансирования 2 и 50% из источника финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="6f2a4-216">Правило 2 (приоритет 2): все проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="6f2a4-217">Распределить 100% из источника финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="6f2a4-218">Правило 3 (приоритет 2): все проводки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="6f2a4-219">Распределить 100% из источника финансирования 1.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f2a4-220">Лимиты финансирования</span><span class="sxs-lookup"><span data-stu-id="6f2a4-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-221">Лимит источника финансирования 1 = 10 000</span><span class="sxs-lookup"><span data-stu-id="6f2a4-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="6f2a4-222">Лимит источника финансирования 2 = 500</span><span class="sxs-lookup"><span data-stu-id="6f2a4-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="6f2a4-223">Лимит источника финансирования 3 = 750</span><span class="sxs-lookup"><span data-stu-id="6f2a4-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2a4-224">Проводка 1</span><span class="sxs-lookup"><span data-stu-id="6f2a4-224">Transaction 1</span></span></td>
<td><span data-ttu-id="6f2a4-225"><strong>Сумма проводки:</strong> 100,00<strong>Финансирование:</strong> проводка оплачивается только согласно правилу 1, поскольку проводка оплачивается полностью только после применения правила 1.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="6f2a4-226">Проводка финансируется поровну между источником финансирования 2 и источником финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="6f2a4-227">Источник финансирования 2: 50</span><span class="sxs-lookup"><span data-stu-id="6f2a4-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="6f2a4-228">Источник финансирования 3: 50</span><span class="sxs-lookup"><span data-stu-id="6f2a4-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f2a4-229">Транзакция 2</span><span class="sxs-lookup"><span data-stu-id="6f2a4-229">Transaction 2</span></span></td>
<td><span data-ttu-id="6f2a4-230"><strong>Сумма проводки:</strong> 5000,00 <strong>Финансирование:</strong> проводка оплачивается согласно всем трем правилам.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="6f2a4-231"><strong>Правило 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="6f2a4-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="6f2a4-232">Источник финансирования 2: 450</span><span class="sxs-lookup"><span data-stu-id="6f2a4-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="6f2a4-233">Источник финансирования 3: 450</span><span class="sxs-lookup"><span data-stu-id="6f2a4-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="6f2a4-234">
<strong>Правило 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="6f2a4-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="6f2a4-235">Источник финансирования 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="6f2a4-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="6f2a4-236">
<strong>Правило 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="6f2a4-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="6f2a4-237">Источник финансирования 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="6f2a4-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2a4-238">Итоговая сумма, распределенная для каждого источника финансирования</span><span class="sxs-lookup"><span data-stu-id="6f2a4-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2a4-239">Источник финансирования 1: 3 850</span><span class="sxs-lookup"><span data-stu-id="6f2a4-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="6f2a4-240">Источник финансирования 2: 500</span><span class="sxs-lookup"><span data-stu-id="6f2a4-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="6f2a4-241">Источник финансирования 3: 750</span><span class="sxs-lookup"><span data-stu-id="6f2a4-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="6f2a4-242">Правила выставления счетов</span><span class="sxs-lookup"><span data-stu-id="6f2a4-242">Billing rules</span></span>
<span data-ttu-id="6f2a4-243">При ведении переговоров по поводу контракта по проекту с клиентом определяется способ и время выставления накладных клиенту за работу по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="6f2a4-244">После того как настроены контракт по проекту и проект, можно настроить правила выставления счетов для проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="6f2a4-245">Правила выставления счетов зависят от условий проекта, указанных в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="6f2a4-246">Создаваемые правила выставления счетов зависят от условий контракта по проекту и типа проекта, например "Время и расходы" или "Фиксированная цена", который можно связать с правилом выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="6f2a4-247">Для контракта на проект можно создать несколько правил выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="6f2a4-248">Можно также назначить правило выставления счетов нескольким проектам, связанным с одним контрактом по проекту и имеющим одинаковые условия выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="6f2a4-249">Можно настроить следующие типы правил выставления счетов:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="6f2a4-250">**Ед. изм. поставки** — накладная выставляется клиенту, когда выполнена единица поставки.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="6f2a4-251">Можно определить единицы поставки в контракте.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="6f2a4-252">**Ход выполнения** — накладная выставляется клиенту, когда выполнен указанный процент работы по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="6f2a4-253">Можно настроить правило выставления счетов так, чтобы автоматически вычислять процент завершенной работы, или автоматически вычислять процент завершенной работы и сумму, накладную на которую нужно выставить клиенту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="6f2a4-254">**Этап** — клиенту выставляется накладная на полную сумму этапа проекта, когда выполняется этап проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="6f2a4-255">**Сбор** — клиенту выставляется накладная за оказанные услуги плюс вознаграждение управляющему персоналу, обычно процент от стоимости услуг.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="6f2a4-256">**Время и расходы** — накладная выставляется клиенту на стоимость времени и расходов, используемых в проекте.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="6f2a4-257">Для всех типов правил выставления накладных можно указать процент удержания для вычета из накладных клиента до тех пор, пока не будет достигнут согласованный этап проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="6f2a4-258">Процент удержания платежей указывается в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="6f2a4-259">Сумма рассчитывается на основании итогового значения строк в накладной клиента и вычитается из него.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="6f2a4-260">Для правил выставления накладных **Время и расходы** и **Ход выполнения** можно назначить включаемые в накладную категории.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="6f2a4-261">Включаемые в накладную категории определяют проводки, которые должны быть включены в накладные клиента.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="6f2a4-262">Когда все готово для передачи накладной клиенту, сумма по накладной по проекту вычисляется на основе правил выставления счетов, и создается предложение накладной по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="6f2a4-263">В следующих разделах приведены примеры, демонстрирующие, как настраивать правила выставления накладных для проекта и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="6f2a4-264">Пример: создание правила выставления накладных на основании количества доставленных единиц</span><span class="sxs-lookup"><span data-stu-id="6f2a4-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="6f2a4-265">Организация заключает договор на проведение пяти учебных семинаров для сотрудников клиента на цене 10 000 за учебный семинар.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="6f2a4-266">Вы выставляете накладную клиенту по окончании каждого учебного семинара.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="6f2a4-267">При настройке правил выставления накладных для контракта используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="6f2a4-268">Единица доставки — один учебный семинар.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="6f2a4-269">Цена единицы продукции равна 10 000 долларов США за учебный семинар.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="6f2a4-270">Общее количество единиц продукции составляет пять учебных семинаров.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="6f2a4-271">Завершив один учебный семинар, можно создать накладную на 10 000 за первую доставленную единицу и отправить накладную клиенту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="6f2a4-272">Пример: создание правила выставления накладных на основании указанного процента выполнения проекта (расчет вручную)</span><span class="sxs-lookup"><span data-stu-id="6f2a4-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="6f2a4-273">Ваша организация — компания, консультирующая в области программного обеспечения, заключила договор с клиентом на создание части программного продукта, разрабатываемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="6f2a4-274">Ваша организация соглашается поставить программный код для продукта в течение шести месяцев.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="6f2a4-275">Клиент соглашается заплатить вашей организации за работу общую сумму 100 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="6f2a4-276">Вы создаете правило выставления накладных, чтобы выставить клиенту накладную на основании процента работы, выполненной по проекту, как указано в контракте.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="6f2a4-277">В конце первого месяца вы встречаетесь с клиентом, чтобы определить процент выполненной работы.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="6f2a4-278">После того, как клиент проверяет проект, вы решаете, что выполнено 15% проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="6f2a4-279">Вы выписываете накладную на сумму 15 000 (15% от 100 000) и отправляете ее клиенту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="6f2a4-280">Пример: создание правила выставления накладных на основании указанного процента выполнения проекта (автоматический расчет)</span><span class="sxs-lookup"><span data-stu-id="6f2a4-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="6f2a4-281">Организация, занимающаяся разработкой программного обеспечения, соглашается разработать пакет учета зарплаты для клиента стоимостью 30 000.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="6f2a4-282">Клиент соглашается платить вашей организации на основе процента выполненной работы.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="6f2a4-283">Вы оцениваете затраты по проекту в сумме 20 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="6f2a4-284">В контракте по проекту указываются категории работ, которые вы должны использовать в процессе выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="6f2a4-285">Вы настроили правила выставления счетов на автоматический расчет сумм накладных по проценту выполненных работ каждой категории.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="6f2a4-286">Для каждой категории настроен бюджет:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="6f2a4-287">**Разработка** — цена 15 000 и доход 20 000.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="6f2a4-288">**Установка** — цена 5 000 и доход 10 000.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="6f2a4-289">При создании накладной для клиента в первый раз сумма счета автоматически рассчитывается на основе следующих сведений:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="6f2a4-290">После месяца работник по проекту отправляет табель для проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="6f2a4-291">Стоимость рабочего времени консультанта составляет 5000 долларов США за разработку и 1000 долларов США за установку.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="6f2a4-292">Работа по разработке завершена на 33% (фактические затраты 5 000/бюджетные затраты 15 000), а работа по установке выполнена на 20% (фактические затраты 1 000/бюджетные затраты 5 000).</span><span class="sxs-lookup"><span data-stu-id="6f2a4-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="6f2a4-293">Сумма накладной составляет 8667 и рассчитывается автоматически (33% от 20 000 + 20% от 10 000).</span><span class="sxs-lookup"><span data-stu-id="6f2a4-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="6f2a4-294">Вы выписываете накладную на сумму 8667 и отправляете ее клиенту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="6f2a4-295">Пример: создание правила выставления накладных на основании согласованных этапов</span><span class="sxs-lookup"><span data-stu-id="6f2a4-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="6f2a4-296">Ваша организация — компания, занимающаяся управленческим консультированием, предлагает услуги по исследованию рынка по продукту клиента, который планируется клиентом для продажи.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="6f2a4-297">Клиент соглашается пользоваться вашими услугами в течение трех месяцев, начиная с марта, и соглашается заплатить вашей организации 50 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="6f2a4-298">Проект состоит из трех этапов:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-298">The project has three milestones:</span></span>

-   <span data-ttu-id="6f2a4-299">Этап 1: сбор потребительских данных — 31 марта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="6f2a4-300">Этап 2: анализ потребительских данных — 30 апреля</span><span class="sxs-lookup"><span data-stu-id="6f2a4-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="6f2a4-301">Этап 3: представление предложения о жизнеспособности продукта — 31 мая</span><span class="sxs-lookup"><span data-stu-id="6f2a4-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="6f2a4-302">Клиент соглашается заплатить вашей организации 10 000 за первый этап и по 20 000 за второй и третий этапы.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="6f2a4-303">При настройке контракта по проекту вы договариваетесь выставлять клиенту накладные на основании завершенных этапов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="6f2a4-304">Настройка правила выставления счетов включает следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="6f2a4-305">Определение этапов проекта.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-305">Define the project milestones.</span></span>
-   <span data-ttu-id="6f2a4-306">Определение суммы для выставления в накладной клиенту при выполнении каждого этапа.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="6f2a4-307">Когда первый этап завершен 31 марта, отметьте данный этап как завершенный, а затем создайте накладную на сумму 10 000, чтобы отправить клиенту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="6f2a4-308">Невозможно создать накладную для этапа, пока этап не будет помечен как завершенный.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="6f2a4-309">Пример: создание правила выставления накладных на основании услуг плюс вознаграждение управляющему персоналу</span><span class="sxs-lookup"><span data-stu-id="6f2a4-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="6f2a4-310">Ваша организация — компания, занимающаяся управленческим консультированием, предлагает услуги по исследованию рынка по оценке доступности продукта, который разрабатывает клиент (розничная компания).</span><span class="sxs-lookup"><span data-stu-id="6f2a4-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="6f2a4-311">Согласно условиям договора с клиентом вы предоставляете услуги трех главных консультантов по управлению для проведения исследования на основе затрат времени и расходов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="6f2a4-312">Клиент соглашается платить 100 в час плюс 10% вознаграждения управляющему персоналу за часы консультирования, оплачиваемые по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="6f2a4-313">При настройке контракта по проекту создайте правило выставления накладных, чтобы добавить 10% вознаграждения управляющему персоналу к оплате за часы консультации по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="6f2a4-314">При создании накладной для клиента ему выставляется в счете 10 % вознаграждения управляющему персоналу плюс стоимость времени консультаций в часах.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="6f2a4-315">Например, если три консультанта работали в общей сложности 200 часов по проекту, накладная выписывается на сумму 22 000 на основе следующего расчета:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="6f2a4-316">200 часов при ставке 100 долларов США за час = 20 000 долларов США</span><span class="sxs-lookup"><span data-stu-id="6f2a4-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="6f2a4-317">управленческий сбор 10 % = 2 000</span><span class="sxs-lookup"><span data-stu-id="6f2a4-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="6f2a4-318">Итоговая сумма по счету = 22 000 долларов США</span><span class="sxs-lookup"><span data-stu-id="6f2a4-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="6f2a4-319">Если сборы облагаются налогом в отношении клиента и выбрана налоговая группа в контракте по проекту налоговая группа автоматически вводится в правило выставления счетов для сборов.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="6f2a4-320">Пример: создание правила выставления накладных по стоимости времени и расходов</span><span class="sxs-lookup"><span data-stu-id="6f2a4-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="6f2a4-321">Ваша организация — компания, консультирующая в области программного обеспечения, договорилась с клиентом предоставить пять технических консультантов для работы над проектом разработки ПО для клиента на ближайшие шесть месяцев.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="6f2a4-322">Клиент соглашается оплачивать 150 за каждый час консультаций плюс стоимость канцтоваров.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="6f2a4-323">Ваша организация отправляет счет клиенту в конце каждого месяца.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="6f2a4-324">При настройке контракта по проекту вы соглашаетесь ежемесячно выставлять клиенту накладные за затраченные время и расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="6f2a4-325">Вы создаете правило выставления счетов, включающее следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="6f2a4-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="6f2a4-326">Период времени, в течение которого действует контракт, равен шести месяцам.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-326">The contract period is six months.</span></span>
-   <span data-ttu-id="6f2a4-327">Время консультаций рассчитывается по ставке 150 за час.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="6f2a4-328">Накладная по канцтоварам выставляется по их цене, и общая стоимость проекта не должна превышать 10 000.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="6f2a4-329">Вы создаете накладную клиента в конце каждого календарного месяца на протяжении работы по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="6f2a4-330">В течение первого месяца консультантами зарегистрировано всего 800 суммарных часов консультаций по проекту.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="6f2a4-331">Стоимость канцтоваров, выставленная к оплате по проекту, равняется 2 000.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="6f2a4-332">Таким образом, в конце месяца вы создаете накладную на 122 000, рассчитанную как 800 часов по цене 150 за час плюс 2 000 за канцелярские принадлежности.</span><span class="sxs-lookup"><span data-stu-id="6f2a4-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




